## 1.获取订阅列表

> `GET` /plan/fetch

- 请求参数
  `null`

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": [
    {
      "id": 1,
      "group_id": 1,
      "transfer_enable": 50,
      "name": "Mini 微量计划",
      "speed_limit": null,
      "show": 1,
      "sort": 1,
      "renew": 1,
      "content": "🔋流量: 50GB /每月<br>\n🌐中转线路<br>\n⌚️按月重置流量<br>\n🎞全流媒体解锁<br>\n🚀最大峰值1000Mbps<br>\n🎮ChatGPT解锁<br>\n🎈全球10个国家接入<br>\n☎️在线客服售后保障<br>\n💎IPLC专线",
      "month_price": 1590,
      "quarter_price": 4770,
      "half_year_price": 9540,
      "year_price": 19080,
      "two_year_price": 38160,
      "three_year_price": null,
      "onetime_price": null,
      "reset_price": 1590,
      "reset_traffic_method": 1,
      "capacity_limit": null,
      "created_at": 1717665923,
      "updated_at": 1718172088,
      "count": 103
    },
    {
      "id": 2,
      "group_id": 1,
      "transfer_enable": 100,
      "name": "Lite 轻量计划",
      "speed_limit": null,
      "show": 1,
      "sort": 2,
      "renew": 1,
      "content": "🔋流量: 100GB /每月<br>\n🌐中转线路<br>\n⌚️按月重置流量<br>\n🎞全流媒体解锁<br>\n🚀最大峰值1000Mbps<br>\n🎮ChatGPT解锁<br>\n🎈全球10个国家接入<br>\n☎️在线客服售后保障<br>\n💎IPLC专线",
      "month_price": 1990,
      "quarter_price": 5970,
      "half_year_price": 11940,
      "year_price": 23880,
      "two_year_price": 47760,
      "three_year_price": null,
      "onetime_price": null,
      "reset_price": 1990,
      "reset_traffic_method": 1,
      "capacity_limit": null,
      "created_at": 1717666098,
      "updated_at": 1718172099,
      "count": 33
    }
  ],
  "error": null
}
```

| 参数名  | 类型       | 描述         |
|------|----------|------------|
| id | number   | id         |
| group_id | number   | 权限组id      |
| transfer_enable | number   | 套餐流量(G为单位) |
| name | string   | 名称         |
| speed_limit | number   | 限速(单位Mbps) |
| show | number   | 销售状态       |
| sort | number   | 排序         |
| renew | number   | 可否续费       |
| content | text     | 套餐描述(富文本)  |
| month_price | number   | 月付         |
| quarter_price | number   | 季付         |
| half_year_price | number   | 半年付        |
| year_price | number   | 年付         |
| two_year_price | number   | 两年付        |
| three_year_price | number   | 三年付        |
| onetime_price | number   | 一次性价格      |
| reset_price | number   | 重置流量价格     |
| reset_traffic_method | number   | 流量重置方式     |
| capacity_limit | number   | 最大用户容量     |
| created_at | number | 创建时间       |
| updated_at | number  | 修改时间       |
| count | number   | 统计数量       |

## 2.添加订阅


> `POST` /plan/save

- 请求参数
  `

  show: 0

  name: tt2

  transfer_enable: 50

  group_id: 1

  month_price: 12300

  quarter_price: 21300

  half_year_price: 2100

  year_price: 2100

  two_year_price: 32100

  three_year_price: 2100

  onetime_price:

  reset_price: 12300

  reset_traffic_method: 1
  `

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": true,
  "error": null
}
```

## 3.修改订阅save全量版本

> '全量修改的话也可以用save，区别在于有没有id'

> `POST` /plan/save

- 请求参数
  `

  id: 8

  group_id: 1

  transfer_enable: 50

  name: tt3

  speed_limit: 10

  show: 0

  sort:

  renew: 0

  content:

  month_price: 1200

  quarter_price: 2100

  half_year_price: 2100

  year_price: 2100

  two_year_price: 32100

  three_year_price: 2100

  onetime_price:

  reset_price: 1200

  reset_traffic_method: 1

  capacity_limit: 100

  created_at: 1720965533

  updated_at: 1720965710

  count: 0
  `

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": null,
  "error": null
}
```

## 4.修改订阅

> `POST` /plan/update

只能修改 销售状态 'show'、 续费'renew' ,

- 请求参数
  `

  id: 8

  renew: 0

  `

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": null,
  "error": null
}
```


## 5.删除订阅

> `POST` /plan/drop


- 请求参数
  
  id: 8
  

- url参数后缀

  `
  id=8
  `
- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": true,
  "error": null
}
```