## 1.队列监控获取队列状态

> `GET` /system/getSystemStatus

- 请求参数
  `null`

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "\u64cd\u4f5c\u6210\u529f",
  "data": {
    "failedJobs": 388,
    "jobsPerMinute": 1,
    "pausedMasters": 0,
    "periods": {
      "failedJobs": 10080,
      "recentJobs": 60
    },
    "processes": 8,
    "queueWithMaxRuntime": "order_handle",
    "queueWithMaxThroughput": "order_handle",
    "recentJobs": 676,
    "status": true,
    "wait": {
      "redis:send_telegram": 0
    }
  },
  "error": null
}
```

| 参数名  | 类型      | 描述       |
|------|---------|----------|
| failedJobs | number  | 7日内报错数量  |
| jobsPerMinute | number  | 每分钟工作量   |
| pausedMasters | number  | 是否登出成功   |
| periods | obj     | 是否登出成功   |
| processes | number  | 当前任务数量  |
| queueWithMaxRuntime | string  | 队列最大运行时间 |
| queueWithMaxThroughput | string  | 队列最大吞吐量  |
| recentJobs | number  | 近一个小时处理量 |
| status | boolean | 运行状态     |
| wait | obj     | 是否登出成功   |

#### periods 时期

| 参数名  | 类型      | 描述         |
|------|---------|------------|
| failedJobs | number  | 失败保留时长（分钟） |
| recentJobs | number  | 成功保留时长（分钟） |

#### wait 等待时间计时器
| 参数名  | 类型      | 描述         |
|------|---------|------------|
| redis:send_telegram | number  | 发送电报消息队列数量 |


## 2.队列监控获取队列工作量

> `GET` /system/getQueueWorkload

- 请求参数
  `null`

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": [
    {
      "name": "batch_traffic_fetch",
      "length": 4,
      "wait": 0,
      "processes": 4,
      "split_queues": null
    },
    {
      "name": "default",
      "length": 0,
      "wait": 0,
      "processes": 1,
      "split_queues": null
    },
    {
      "name": "order_handle",
      "length": 0,
      "wait": 0,
      "processes": 1,
      "split_queues": null
    },
    {
      "name": "send_email",
      "length": 0,
      "wait": 0,
      "processes": 1,
      "split_queues": null
    },
    {
      "name": "send_email_mass",
      "length": 0,
      "wait": 0,
      "processes": 1,
      "split_queues": null
    },
    {
      "name": "send_telegram",
      "length": 0,
      "wait": 0,
      "processes": 1,
      "split_queues": null
    },
    {
      "name": "traffic_fetch",
      "length": 0,
      "wait": 0,
      "processes": 1,
      "split_queues": null
    }
  ],
  "error": null
}
```
| 参数名  | 类型     | 描述   |
|------|--------|------|
| batch_traffic_fetch | string | 流量消费队列(高速)	 |
| order_handle | string | 订单队列	 |
| send_email	 | string | 邮件队列	 |
| send_email_mass	 | string | 邮件群发队列		 |
| send_telegram	 | string | Telegram消息队列		 |
| traffic_fetch	 | string | 流量消费队列	 |

| 参数名  | 类型     | 描述   |
|------|--------|------|
| name | string | 队列名称 |
| length | number | 作业量  |
| wait | number | 等待数量 |
| processes | number | 任务量  |
| split_queues | number | 拆分队列 |

