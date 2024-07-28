## 1.仪表盘主数据

> `GET` /stat/getOverride

- 请求参数
  `null`

- 成功返回示例 `json`

```json
{
  "data": {
    "month_income": "3828989",
    "month_register_total": 5881,
    "ticket_pending_total": 33,
    "commission_pending_total": 116,
    "day_income": "24260",
    "last_month_income": "1538086",
    "commission_month_payout": "1411394",
    "commission_last_month_payout": "451072"
  }
}
```

| 参数名  | 类型         | 描述      |
|------|------------|---------|
| month_income | string     | 本月收入    |
| commission_month_payout | string | 本月佣金支出  |
| last_month_income | string | 上月收入    |
| commission_last_month_payout | string | 上月佣金支出  |
| month_register_total | number     | 本月新增用户  |
| day_income | string     | 今日收入    |
| ticket_pending_total | number     |  待发放佣金数量|
| commission_pending_total | number     | 代发放佣金总额 |


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
