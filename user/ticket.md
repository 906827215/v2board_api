## 1.工单列表

> `GET` /user/ticket/fetch

- 请求参数
  `t=1744707187914`
- application/json, text/plain, */*

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": [
    {
      "id": 1,
      "level": 0,
      "reply_status": 1,
      "status": 1,
      "subject": "测试工单",
      "message": null,
      "created_at": 1717775766,
      "updated_at": 1718078018,
      "user_id": 1
    }
  ],
  "error": null
}
```

## 2.工单详情

> `GET` /user/ticket/fetch?id=1

- 请求参数
  `id=1`
- application/json, text/plain, */*

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": {
    "id": 1,
    "level": 0,
    "reply_status": 1,
    "status": 1,
    "subject": "测试工单",
    "message": [
      {
        "id": 1,
        "ticket_id": 1,
        "is_me": true,
        "message": "低风险测试",
        "created_at": 1717775766,
        "updated_at": 1717775766
      },
      {
        "id": 2,
        "ticket_id": 1,
        "is_me": true,
        "message": "已理解并处理。",
        "created_at": 1717775802,
        "updated_at": 1717775802
      },
      {
        "id": 3,
        "ticket_id": 1,
        "is_me": true,
        "message": "能看懂码",
        "created_at": 1717775858,
        "updated_at": 1717775858
      }
    ],
    "created_at": 1717775766,
    "updated_at": 1718078018,
    "user_id": 1
  },
  "error": null
}
```

## 3.新的工单

> `POST` /user/ticket/save

- 请求参数

  `{
    "subject":"1",
    "level":0,
    "message":"12321"
  }`
- application/json, text/plain, */*
- content-type: application/json

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": true,
  "error": null
}
```