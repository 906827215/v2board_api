## 1.系统配置

> `GET` /config/fetch

- 请求参数
  `null`

- 成功返回示例 `json`

```json
{
  "invite": {
    "invite_force": 0,
    "invite_commission": "15",
    "invite_gen_limit": "5",
    "invite_never_expire": "1",
    "commission_first_time_enable": "0",
    "commission_auto_check_enable": "1",
    "commission_withdraw_limit": "200",
    "commission_withdraw_method": [
      "USDT"
    ],
    "withdraw_close_enable": "0",
    "commission_distribution_enable": "0",
    "commission_distribution_l1": null,
    "commission_distribution_l2": null,
    "commission_distribution_l3": null
  },
  "site": {
    "logo": null,
    "force_https": 1,
    "stop_register": 0,
    "app_name": "三番云测试",
    "app_description": "专业全球网络加速服务",
    "app_url": "https://jf16.co/",
    "subscribe_url": "https://s.3faninfo.net",
    "try_out_plan_id": 0,
    "try_out_hour": 1,
    "tos_url": null,
    "currency": "CNY",
    "currency_symbol": "¥"
  },
  "subscribe": {
    "plan_change_enable": 1,
    "reset_traffic_method": 1,
    "surplus_enable": 1,
    "new_order_event_id": 1,
    "renew_order_event_id": 0,
    "change_order_event_id": 1,
    "show_info_to_server_enable": 0,
    "show_protocol_to_server_enable": 0,
    "default_remind_expire": 1,
    "default_remind_traffic": 1
  },
  "frontend": {
    "frontend_theme": "Xboard",
    "frontend_theme_sidebar": "light",
    "frontend_theme_header": "light",
    "frontend_theme_color": "default",
    "frontend_background_url": ""
  },
  "server": {
    "server_token": "jjcZFyq3WVtbvqvLT",
    "server_pull_interval": "60",
    "server_push_interval": "60"
  },
  "email": {
    "email_template": "default",
    "email_host": null,
    "email_port": null,
    "email_username": null,
    "email_password": null,
    "email_encryption": null,
    "email_from_address": null
  },
  "telegram": {
    "telegram_bot_enable": 0,
    "telegram_bot_token": null,
    "telegram_discuss_link": null
  },
  "app": {
    "windows_version": null,
    "windows_download_url": null,
    "macos_version": null,
    "macos_download_url": null,
    "android_version": null,
    "android_download_url": null
  },
  "safe": {
    "email_verify": 0,
    "safe_mode_enable": 0,
    "secure_path": "supadmin",
    "email_whitelist_enable": 0,
    "email_whitelist_suffix": [
      "gmail.com",
      "qq.com",
      "163.com",
      "yahoo.com",
      "sina.com",
      "126.com",
      "outlook.com",
      "yeah.net",
      "foxmail.com"
    ],
    "email_gmail_limit_enable": "0",
    "recaptcha_enable": 0,
    "recaptcha_key": "",
    "recaptcha_site_key": "",
    "register_limit_by_ip_enable": 0,
    "register_limit_count": "3",
    "register_limit_expire": "60",
    "password_limit_enable": 1,
    "password_limit_count": "5",
    "password_limit_expire": "60"
  }
}
```
### 站点site

| 参数名       | 类型     | 描述   |
|-----------|--------|------|
| logo     | string | logo url |
| force_https     | number | 强制https |
| stop_register | number | 停止新用户注册 |
| app_name | string | 站点名称 |
| app_description | string | 站点描述 |
| app_url | string | 站点网址 |
| subscribe_url | string | 订阅网址 |
| try_out_plan_id | number | 注册试用订阅 |
| try_out_hour | number | 注册试用订阅时长 |
| tos_url | string | 用户条款(TOS)URL |
| currency | string | 货币   |
| currency_symbol | string | 货币符号 |

### 安全safe

| 参数名       | 类型     | 描述                    |
|-----------|--------|-----------------------|
| email_verify     | number | 是否邮箱验证                |
| safe_mode_enable     | number | 是否安全模式                |
| secure_path | string | 后台路径                  |
| email_whitelist_enable | string | 是否开启邮箱后缀白名单           |
| email_whitelist_suffix | list   | 邮箱后缀白名单列表             |
| email_gmail_limit_enable | string | 禁止使用Gmail多别名          |
| recaptcha_enable | number | 是否启用防机器人              |
| recaptcha_key | string | 防机器人key               |
| recaptcha_site_key | string | 防机器人site key          |
| register_limit_by_ip_enable | number | IP注册限制                |
| register_limit_count | string | 注册失败次数(string 数字 例如3) |
| register_limit_expire | string | 注册失败惩罚时长(string 数字 例如60)  |
| password_limit_enable | number | 密码错误限制                |
| password_limit_count | string | 密码错误次数(string 数字 例如3) |
| password_limit_expire | string | 密码错误惩罚时长(string 数字 例如60)  

### 订阅subscribe

| 参数名       | 类型     | 描述     |
|-----------|--------|--------|
| plan_change_enable     | number | 允许用户更新订阅 |
| reset_traffic_method     | number | 月流量重置方式|
| surplus_enable     | number | 开启折抵方案|
| new_order_event_id     | number | 当订阅新购时触发事件|
| renew_order_event_id     | number | 当订阅续费时触发事件|
| change_order_event_id     | number | 当订阅变更时触发事件|
| show_info_to_server_enable     | number | 在订阅中展示订阅信息|
| show_protocol_to_server_enable     | number | 在订阅中线路名称中显示协议名称|
| default_remind_expire     | number | 用户订阅到期提醒的默认设置|
| default_remind_traffic     | number | 用户流量告急提醒的默认设置|

### 邀请invite

| 参数名       | 类型     | 描述         |
|-----------|--------|------------|
| invite_force     | number | 开启强制邀请     |
| invite_commission     | string | 邀请佣金百分比    |
| invite_gen_limit     | string | 用户可创建邀请码上限 |
| invite_never_expire     | string | 邀请码永不失效    |
| commission_first_time_enable     | string | 佣金仅首次发放    |
| commission_auto_check_enable     | string | 佣金自动确认     |
| commission_withdraw_limit     | string | 提现单申请门槛(元) |
| commission_withdraw_method     | list   | 提现方式       |
| withdraw_close_enable     | string | 关闭提现       |
| commission_distribution_enable     | string | 三级分销       |
| commission_distribution_l1     | string | 佣金分配比例1    |
| commission_distribution_l2     | string | 佣金分配比例2    |
| commission_distribution_l3     | string | 佣金分配比例3    |


### 个性化 frontend

| 参数名       | 类型     | 描述     |
|-----------|--------|--------|
| frontend_theme     | string | 主题名称   |
| frontend_theme_sidebar     | string | 边栏风格   |
| frontend_theme_header     | string | 头部风格   |
| frontend_theme_color     | string | 主题色    |
| frontend_background_url     | string | 背景图url |

### 节点 server

| 参数名       | 类型     | 描述    |
|-----------|--------|-------|
| server_token     | string | 通讯密钥|
| server_pull_interval     | string | 节点拉取动作轮询间隔|
| server_push_interval     | string | 节点推送动作轮询间隔|

### 邮件 email

| 参数名       | 类型     | 描述   |
|-----------|--------|------|
| email_template     | string | 邮件模板 |
| email_host     | string | SMTP服务器地址|
| email_port     | string | SMTP服务端口|
| email_username     | string | SMTP加密方式|
| email_password     | string | SMTP账号|
| email_encryption     | string | SMTP密码|
| email_from_address     | string | 发件地址|

需要添加测试邮件功能,发送目标是当前用户邮箱

### Ttelegram telegram

| 参数名       | 类型     | 描述  |
|-----------|--------|-----|
| telegram_bot_enable     | string | 开启机器人通知|
| telegram_bot_token     | string | 机器人Token|
| telegram_discuss_link     | string | 群组地址|


### App app

| 参数名       | 类型     | 描述          |
|-----------|--------|-------------|
| windows_version     | string | Windows版本号  |
| windows_download_url     | string | Windows下载地址 |
| macos_version     | string | MacOs版本号    |
| macos_download_url     | string | MacOs下载地址   |
| android_version     | string | Android版本号  |
| android_download_url     | string | Android下载地址 |


## 2.配置保存

> `POST` /config/save

- 请求参数 `form`

```
windows_version=&windows_download_url=&macos_version=&macos_download_url=&android_version=1.11&android_download_url=
```
具体说明就是上面返回内容按照块来传递,也可以单独字段来传递，比如：
windows_version=1.0.1 即可  

| 参数名      | 类型     | 必填  | 描述   |
|----------|--------|-----|------|
| email    | string | ✔︎  | 邮箱地址 |
| password | string | ✔︎  | 密码   |

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": true,
  "error": null
}
```

- 成功返回示例 `json`