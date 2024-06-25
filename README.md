# v2board-user 部分 api 整理

### passport

| URL                            | 请求 | 描述                                            |
| ------------------------------ | ---- | ----------------------------------------------- |
| /passport/comm/config          | GET  | [获取配置](/user/passport.md/#1获取配置)             |
| /passport/auth/check           | GET  | [登入校验](/user/passport.md/#2登入校验)             |
| /passport/auth/login           | POST | [登入账号](/user/passport.md/#3登入账号)             |
| /passport/comm/sendEmailVerify | POST | [发送邮箱验证码](/user/passport.md/#4发送邮箱验证码) |
| /passport/auth/register        | POST | [注册账号](/user/passport.md/#5注册账号)             |
| /passport/auth/forget          | POST | [重置密码](/user/passport.md/#6重置密码)             |

### User

| URL                  | 请求 | 描述                                   |
| -------------------- | ---- | -------------------------------------- |
| /user/logout         | GET  | [登出](/user/user.md/#1登出)                |
| /user/info           | GET  | [账号信息](/user/user.md/#2账号信息)        |
| /user/getSubscribe   | GET  | [订阅信息](/user/user.md/#3订阅信息)        |
| /user/resetSecurity  | GET  | [重置订阅链接](/user/user.md/#重置订阅链接) |
| /user/getStat        | GET  | [代办事项](/user/user.md/#5代办事项)        |
| /user/changePassword | POST | [修改密码](/user/user.md/#6修改密码)        |
| /user/update         | POST | [通知状态](/user/user.md/#7通知状态)        |
| /user/transfer       | POST | [佣金划转](/user/user.md/#8佣金划转)        |

### Plan

| URL              | 请求 | 描述                                    |
| ---------------- | ---- | --------------------------------------- |
| /user/plan/fetch | GET  | [订阅商店列表](/user/plan.md/#1订阅商店列表) |

### Order

| URL                           | 请求 | 描述                             |
| ----------------------------- | ---- | -------------------------------- |
| /user/order/fetch             | GET  | [订单列表](/user/order.md/#1订单列表) |
| /user/order/getPaymentMethod  | GET  | [支付方式](/user/order.md/#2支付方式) |
| /user/order/details?trade_no= | GET  | [订单详情](/user/order.md/#3订单详情) |
| /user/order/check?trade_no=   | GET  | [订单状态](/user/order.md/#4订单状态) |
| /user/order/save              | POST | [创建订单](/user/order.md/#5创建订单) |
| /user/order/checkout          | POST | [结算订单](/user/order.md/#6结算订单) |
| /user/order/cancel            | POST | [关闭订单](/user/order.md/#7关闭订单) |

### Invite

| URL                  | 请求 | 描述                                  |
| -------------------- | ---- | ------------------------------------- |
| /user/invite/fetch   | GET  | [邀请码管理](/user/invite.md/#1邀请码管理) |
| /user/invite/save    | GET  | [生成邀请码](/user/invite.md/#2生成邀请码) |
| /user/invite/details | GET  | [邀请明细](/user/invite.md/#3邀请明细)     |

### Notice

| URL                | 请求 | 描述                              |
| ------------------ | ---- | --------------------------------- |
| /user/notice/fetch | GET  | [公告信息](/user/notice.md/#1公告信息) |


# v2board-admin 部分 api 整理

### passport

| URL                            | 请求 | 描述                                            |
| ------------------------------ | ---- | ----------------------------------------------- |
| /passport/auth/login           | POST | [登入账号](/user/passport.md/#3登入账号)             |

### User

| URL                            | 请求 | 描述                          |
| ------------------------------ | ---- |-----------------------------|
| /passport/auth/login           | POST | [登出](/admin/user.md/#1登入账号) |