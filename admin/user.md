## 1.登出

> `GET` /user/logout

- 请求参数
  `null`

- 成功返回示例 `json`

```json
{
  "data": true
}
```

| 参数名  | 类型      | 描述     |
|------|---------|--------|
| data | boolean | 是否登出成功 |

## 2.账号信息

> `GET` /user/info

- 请求参数
  `null`

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": {
    "email": "admin@3fan.com",
    "transfer_enable": 1073741824000,
    "last_login_at": null,
    "created_at": 1717649420,
    "banned": 0,
    "remind_expire": 1,
    "remind_traffic": 1,
    "expired_at": 1723018490,
    "balance": 0,
    "commission_balance": 0,
    "plan_id": 5,
    "discount": null,
    "commission_rate": null,
    "telegram_id": null,
    "uuid": "3973a663-02b6-47b5-ad65-f61a205a73ba",
    "avatar_url": "https://cdn.v2ex.com/gravatar/3dccd9d6cbebe0eb1a02e738f907e8b1?s=64&d=identicon"
  },
  "error": null
}
```

| 参数名                | 类型                     | 描述      |
|--------------------|------------------------|---------|
| email              | string                 | 邮箱地址    |
| transfer_enable    | number                 | 总可用流量   |
| last_login_at      | timestamp              | 最后登入时间  |
| created_at         | timestamp              | 创建时间    |
| banned             | number                 | 是否封禁使用  |
| remind_expire      | number                 | 到期邮件提醒  |
| remind_traffic     | number                 | 流量邮件提醒  |
| expired_at         | timestamp              | 过期时间    |
| balance            | number                 | 用户余额    |
| commission_balance | number                 | 佣金余额    |
| plan_id            | number - object(&plan) | 当前订阅id  |
| discount           | number                 | 消费折扣    |
| commission_rate    | number                 | 佣金率     |
| telegram_id        | number                 | 绑定TG id |
| uuid               | string                 | 唯一UUID  |
| avatar_url         | string                 | 头像地址    |

