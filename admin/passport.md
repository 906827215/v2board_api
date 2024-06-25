## 1.登入账号

> `POST` /passport/auth/login

- 请求参数 `json`

```json
 {
  "email": "xxxx@xx.com",
  "password": "1234567890"
}
```

| 参数名      | 类型     | 必填  | 描述   |
|----------|--------|-----|------|
| email    | string | ✔︎  | 邮箱地址 |
| password | string | ✔︎  | 密码   |

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": {
    "token": "ede07b2e62d652a82fa620a033ef694f",
    "is_admin": 1,
    "auth_data": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6MSwic2Vzc2lvbiI6ImJkNDZmYzNiZmFmYjJhMThhM2MzMDVmMGZiNTI2ZDA1In0.OnTfbpQq_xHMuzmUIgQ5i02tGCaEwzzE41917X5OGQo"
  },
  "error": null
}
```

| 参数名       | 类型     | 描述            |
|-----------|--------|---------------|
| token     | string | 用户 token      |
| is_admin     | number | 是否管理员         |
| auth_data | string | base64(邮箱:密码) |
