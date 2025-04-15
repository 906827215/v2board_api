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


### Notice

| URL                    | 请求 | 描述                             |
|------------------------| ---- |--------------------------------|
| /user/ticket/fetch     | GET  | [公告信息](/user/ticket.md/#1工单列表) |
| /user/ticket/fetch?id=1 | GET  | [公告信息](/user/ticket.md/#2工单详情) |
| /user/ticket/save      | GET  | [公告信息](/user/ticket.md/#3新的工单) |


# v2board-admin 部分 api 整理

### 仪表盘
[ticket.md](admin%2Fticket.md)
| URL           | 请求 | 描述                                           |
|---------------| ---- |----------------------------------------------|
| /stat/getOverride | GET | [仪表盘主数据](/admin/state.md/#1仪表盘主数据)           |
| /stat/getOrder | GET | [仪表盘订单统计](/admin/state.md/#2仪表盘订单统计)         |
| /stat/getServerLastRank | GET | [仪表盘获取今日流量排行](/admin/state.md/#3仪表盘获取今日流量排行) |
| /stat/getServerYesterdayRank | GET | [仪表盘获取昨日节点流量排行](/admin/state.md/#4仪表盘获取昨日节点流量排行)          |

### passport

| URL                            | 请求 | 描述                                |
| ------------------------------ | ---- |-----------------------------------|
| /passport/auth/login           | POST | [登入账号](/admin/passport.md/#1登入账号) |

### User

| URL                         | 请求 | 描述                            |
| --------------------------- | ---- |-------------------------------|
| /user/logout         | POST | [登出](/admin/user.md/#1登出)     |
| /user/info          | POST | [账号信息](/admin/user.md/#2账号信息) |

### Config

| URL           | 请求 | 描述                              |
|---------------| ---- |---------------------------------|
| /config/fetch | POST | [系统配置](/admin/config.md/#1系统配置) |
| /config/save  | POST | [配置保存](/admin/config.md/#2配置保存)   |

### Payment

| URL           | 请求 | 描述                                            |
|---------------| ---- |-----------------------------------------------|
| /payment/fetch | GET | [获取支付配置列表](/admin/payment.md/#1支付配置列表)        |
| /payment/getPaymentMethods | GET | [获取配置支付方式](/admin/payment.md/#2获取支付方式)        |
| /payment/getPaymentForm | GET | [获取配置方式form](/admin/payment.md/#3获取支付类form配置) |
| /payment/save  | POST | [支付配置新增和编辑](/admin/payment.md/#4支付方式新增和修改)    |
| /payment/drop  | POST | [支付配置删除](/admin/payment.md/#5支付方式删除)          |


### Theme

| URL           | 请求 | 描述                                           |
|---------------| ---- |----------------------------------------------|
| /theme/getThemes | GET | [获取Themes](/admin/theme.md/#1获取Themes)       |
| /config/save | POST | [激活主题](/admin/theme.md/#2激活主题)           |
| /theme/getThemeConfig | GET | [获取主题配置](/admin/theme.md/#3获取主题配置) |
| /theme/saveThemeConfig  | POST | [主题配置保存](/admin/theme.md/#4主题配置保存)   |


### plan订阅管理

| URL           | 请求 | 描述                                        |
|---------------| ---- |-------------------------------------------|
| /plan/fetch | GET | [获取订阅列表](/admin/plan.md/#1获取订阅列表)         |
| /plan/save | POST | [添加订阅](/admin/plan.md/#2添加订阅)             |
| /plan/save | POST | [全量修改save](/admin/plan.md/#3修改订阅save全量版本) |
| /plan/update  | POST | [修改销售状态和是否可续费](/admin/plan.md/#4修改订阅)     |
| /plan/drop  | POST | [删除订阅](/admin/plan.md/#5删除订阅)             |



### 队列监控

| URL           | 请求 | 描述                                  |
|---------------| ---- |-------------------------------------|
| /system/getSystemStatus | GET | [获取队列状态](/admin/system.md/#1队列监控获取队列状态) |
| /system/getQueueWorkload | GET | [获取队列工作量](/admin/system.md/#2队列监控获取队列工作量)    |


