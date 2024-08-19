## 1.仪表盘主数据

> `GET` /stat/getOverride

- 请求参数
  `null`

- 成功返回示例 `json`


```json
{
  "day_income": 0,
  "last_day_income": 0,
  "month_income": "2181183",
  "last_month_income": "4107289",
  "total_income": "7826558",
  "commission_month_payout": "806677",
  "commission_last_month_payout": "1526531",
  "month_register_total": 1894,
  "last_register_total": 6218,
  "ticket_pending_total": 11,
  "commission_pending_total": 9,
  "today_list": [
    {
      "channel_id": 1,
      "channel_name": "正气支付",
      "total_amount": "56206"
    },
    {
      "channel_id": 2,
      "channel_name": "你爱支付",
      "total_amount": "0"
    },
    {
      "channel_id": 3,
      "channel_name": "百佳支付",
      "total_amount": "267958"
    }
  ],
  "yesterday_list": [
    {
      "channel_id": 1,
      "channel_name": "正气支付",
      "total_amount": "0"
    },
    {
      "channel_id": 2,
      "channel_name": "你爱支付",
      "total_amount": "0"
    },
    {
      "channel_id": 3,
      "channel_name": "百佳支付",
      "total_amount": "182648"
    }
  ],
  "pay_num": 11,
  "reg_num": 49,
  "last_pay_num": 11,
  "last_reg_num": 49,
  "plan_nums": 1595,
  "plan1_nums": 1035,
  "plan1_year_nums": 28,
  "plan2_nums": 404,
  "plan2_year_nums": 14,
  "plan3_nums": 98,
  "plan3_year_nums": 7,
  "plan4_nums": 40,
  "plan4_year_nums": 6,
  "plan5_nums": 17,
  "plan5_year_nums": 6,
  "plan6_nums": 1,
  "plan6_year_nums": 1
}
```
| 参数名  | 类型     | 描述        |
|------|--------|-----------|
| day_income | number | 今日流水      |
| last_day_income | number | 昨日流水      |
| month_income | string | 本月流水      |
| last_month_income | string | 上月流水      |
| total_income | number | 总流水       |
| commission_month_payout | string | 本月佣金支出    |
| commission_last_month_payout | number | 上月佣金支出    |
| month_register_total | number | 本月注册数     |
| last_register_total | number | 上月注册数     |
| ticket_pending_total | number | 工单待处理     |
| commission_pending_total | number | 佣金待确定     |
| pay_num | number | 今日首充      |
| reg_num | number | 今日注册      |
| last_pay_num | number | 昨日首充      |
| last_reg_num | number | 昨日注册      |
| plan_nums | number | 总付费用户数    |
| plan1_nums | number | Mini 会员数  |
| plan1_year_nums | number | Mini 年会数  |
| plan2_nums | number | Lite 会员数  |
| plan2_year_nums | number | Lite 年会数  |
| plan3_nums | number | Stand 会员数 |
| plan3_year_nums | number | Stand 年会数 |
| plan4_nums | number | Pro 会员数   |
| plan4_year_nums | number | Pro 年会数   |
| plan5_nums | number | Plus 会员数  |
| plan5_year_nums | number | Plus 年会数  |
| plan6_nums | number | Moon 会员数  |
| plan6_year_nums | number | Moon 年会数  |
| today_list | obj    | 昨日支付列表    |
| yesterday_list | obj | 今日支付列表    |


| 参数名  | 类型     | 描述   |
|------|--------|------|
| channel_id | number | id   |
| channel_name | string      | 通道名称 |
| total_amount | number      | 金额   |




## 2.仪表盘订单统计

> `GET` /stat/getOrder

- 请求参数
  `null`

- 成功返回示例 `json`

```json
[
  {
    "type": "佣金笔数(已发放)",
    "date": "06-06",
    "value": 0
  },
  {
    "type": "佣金金额(已发放)",
    "date": "06-06",
    "value": 0
  },
  {
    "type": "收款笔数",
    "date": "06-06",
    "value": 0
  },
  {
    "type": "收款金额",
    "date": "06-06",
    "value": 0
  },
  {
    "type": "佣金笔数(已发放)",
    "date": "06-07",
    "value": 0
  },
  {
    "type": "佣金金额(已发放)",
    "date": "06-07",
    "value": 0
  },
  {
    "type": "收款笔数",
    "date": "06-07",
    "value": 1
  },
  {
    "type": "收款金额",
    "date": "06-07",
    "value": 1
  },
  {
    "type": "佣金笔数(已发放)",
    "date": "06-08",
    "value": 0
  },
  {
    "type": "佣金金额(已发放)",
    "date": "06-08",
    "value": 0
  },
  {
    "type": "收款笔数",
    "date": "06-08",
    "value": 1
  },
  {
    "type": "收款金额",
    "date": "06-08",
    "value": 1
  }
]
```

| 参数名  | 类型     | 描述      |
|------|--------|---------|
| type | string | 类型      |
| date | string | 日期      |
| value | number | 数值      |


## 3.仪表盘获取今日流量排行

> `GET` /stat/getServerLastRank

- 请求参数
  `null`

- 成功返回示例 `json`

```json
[
  {
    "server_id": 101,
    "server_type": "vmess",
    "u": 865469181,
    "d": 66396079807,
    "total": 62.64219897612929,
    "server_name": "香港01"
  },
  {
    "server_id": 201,
    "server_type": "vmess",
    "u": 1189712004,
    "d": 55849020166,
    "total": 53.12145889736712,
    "server_name": "台湾01"
  },
  {
    "server_id": 702,
    "server_type": "vmess",
    "u": 206585007,
    "d": 36529024061,
    "total": 34.21270201727748,
    "server_name": "美国02"
  }
]
```

| 参数名  | 类型         | 描述    |
|------|------------|-------|
| server_id | number     | 节点id  |
| server_name | string     | 节点名称  |
| server_type | string | 节点类型  |
| u | number | 上传b   |
| d | number | 下载b   |
| total | number     | 总量(G) |

## 4.仪表盘获取昨日节点流量排行

> `GET` /stat/getServerYesterdayRank

- 请求参数
  `null`

- 成功返回示例 `json`

```json
[
  {
    "server_id": 101,
    "server_type": "vmess",
    "u": 865469181,
    "d": 66396079807,
    "total": 62.64219897612929,
    "server_name": "香港01"
  },
  {
    "server_id": 201,
    "server_type": "vmess",
    "u": 1189712004,
    "d": 55849020166,
    "total": 53.12145889736712,
    "server_name": "台湾01"
  },
  {
    "server_id": 702,
    "server_type": "vmess",
    "u": 206585007,
    "d": 36529024061,
    "total": 34.21270201727748,
    "server_name": "美国02"
  }
]
```

| 参数名  | 类型         | 描述    |
|------|------------|-------|
| server_id | number     | 节点id  |
| server_name | string     | 节点名称  |
| server_type | string | 节点类型  |
| u | number | 上传b   |
| d | number | 下载b   |
| total | number     | 总量(G) |

