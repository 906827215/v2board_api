## 1.支付配置列表

> `GET` /payment/fetch

- 请求参数

  pageSize=10&current=0

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": [
    {
      "id": 1,
      "uuid": "IdXl3L8e",
      "payment": "EPay",
      "name": "正气支付",
      "icon": null,
      "config": {
        "url": "https://1.hk.fgdfg-pay.top/",
        "pid": "1",
        "key": "3Z57CPxMAjOPX545X5nmm0oML4J7Mpap"
      },
      "notify_domain": null,
      "handling_fee_fixed": null,
      "handling_fee_percent": null,
      "enable": 1,
      "sort": null,
      "created_at": 1717747601,
      "updated_at": 1718725158,
      "notify_url": "https://jf16.co/api/v1/guest/payment/notify/EPay/IdXl3L8e"
    },
    {
      "id": 2,
      "uuid": "7nUQIYJJ",
      "payment": "EPay",
      "name": "你爱支付",
      "icon": null,
      "config": {
        "private_key": "11364",
        "key": "23",
        "url": "https://vipmapi.1241s.com/",
        "pid": "11364"
      },
      "notify_domain": null,
      "handling_fee_fixed": null,
      "handling_fee_percent": null,
      "enable": 0,
      "sort": null,
      "created_at": 1717829492,
      "updated_at": 1718725158,
      "notify_url": "https://jf16.co/api/v1/guest/payment/notify/EPay/7nUQIYJJ"
    }
  ],
  "error": null
}
```

| 参数名       | 类型     | 描述 |
|-----------|--------|---|
| id     | string | id |
| uuid     | number | uuid |
| payment | string | 支付方式（Epay、AlipayF2F）对应后台支付类名 |
| name | string | 名称 |
| icon | string | 图标 |
| notify_domain | string | 回调域名 |
| handling_fee_fixed | string | 固定手续费（具体数值） |
| handling_fee_percent | string | 百分比手续费 |
| enable | number | 是否启用 |
| sort | number | 排序|
| created_at | string | 创建时间 |
| updated_at | string | 更新时间 |
| notify_url | string | 回调地址（根据回调域名自动生成）|

### 2.获取支付方式

> `GET` /payment/getPaymentMethods

- 请求参数 
  `null`

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": [
    "AlipayF2F",
    "BTCPay",
    "CoinPayments",
    "Coinbase",
    "EPay",
    "MGate"
  ],
  "error": null
}
```

| 参数名  | 类型   | 描述     |
|------|------|--------|
| data | list | 支付方式类名 |


### 3.获取支付类form配置

> `GET` /payment/getPaymentForm

- 请求参数
  `payment=EPay`
  `可选参数 id=3 ； 用于编辑时` 

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": {
    "url": {
      "label": "URL",
      "description": "",
      "type": "input",
      "value": "23"
    },
    "pid": {
      "label": "PID",
      "description": "",
      "type": "input",
      "value": "2"
    },
    "key": {
      "label": "KEY",
      "description": "",
      "type": "input",
      "value": "23"
    }
  },
  "error": null
}
```

```json
{
  "status": "success",
  "message": "操作成功",
  "data": {
    "app_id": {
      "label": "支付宝APPID",
      "description": "",
      "type": "input"
    },
    "private_key": {
      "label": "支付宝私钥",
      "description": "",
      "type": "input",
      "value": "11364"
    },
    "public_key": {
      "label": "支付宝公钥",
      "description": "",
      "type": "input"
    },
    "product_name": {
      "label": "自定义商品名称",
      "description": "将会体现在支付宝账单中",
      "type": "input"
    }
  },
  "error": null
}
```
- 根据payment 的类型 不同 显示的内容不同 根据返回data格式画页面表单

| 参数名  | 类型  | 描述    |
|------|-----|-------|
| data | obj | 支付类表单 |

### 4.支付方式新增和修改

> `POST` /payment/save

- 请求参数 `form data`
#### 新增参数
```
name: test
handling_fee_percent: 6
payment: EPay
config[pid]: 1001
config[key]: sfsdfsdfsdsgdghsdg
config[url]: 2132132132132131231
```

#### 编辑参数
```
id: 4
uuid: uceowiX5
payment: EPay
name: test
icon: 
config[pid]: 1001
config[key]: sfsdfsdfsdsgdghsdg
config[url]: 2132132132132131231
notify_domain: 
handling_fee_fixed: 
handling_fee_percent: 6.00
enable: 0
sort: 
created_at: 1719716246
updated_at: 1719716246
notify_url: https://jf16.co/api/v1/guest/payment/notify/EPay/uceowiX5
```


- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": true,
  "error": null
}
```


### 5.支付方式删除

> `POST` /payment/drop

- 请求参数 `form data`
```
id: 3

/payment/drop?id=3
```

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": true,
  "error": null
}
```
