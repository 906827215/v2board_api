## 1.获取Themes

> `GET` /theme/getThemes

- 请求参数
  `null`

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": {
    "themes": {
      "Xboard": {
        "name": "Xboard",
        "description": "Xboard",
        "version": "1.0.0",
        "images": "",
        "configs": [
          {
            "label": "主题色",
            "placeholder": "请选择主题颜色",
            "field_name": "theme_color",
            "field_type": "select",
            "select_options": {
              "default": "默认(绿色)",
              "blue": "蓝色",
              "black": "黑色",
              "darkblue": "暗蓝色"
            },
            "default_value": "default"
          },
          {
            "label": "背景",
            "placeholder": "请输入背景图片URL",
            "field_name": "background_url",
            "field_type": "input"
          },
          {
            "label": "自定义页脚HTML",
            "placeholder": "可以实现客服JS代码的加入等",
            "field_name": "custom_html",
            "field_type": "textarea"
          }
        ]
      },
      "v2board": {
        "name": "v2board",
        "description": "v2board",
        "version": "1.7.2",
        "images": "https://images.unsplash.com/photo-1515405295579-ba7b45403062?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2160&q=80",
        "configs": [
          {
            "label": "主题色",
            "placeholder": "请选择主题颜色",
            "field_name": "theme_color",
            "field_type": "select",
            "select_options": {
              "default": "默认(蓝色)",
              "green": "奶绿色",
              "black": "黑色",
              "darkblue": "暗蓝色"
            },
            "default_value": "default"
          },
          {
            "label": "背景",
            "placeholder": "请输入背景图片URL",
            "field_name": "background_url",
            "field_type": "input"
          },
          {
            "label": "边栏风格",
            "placeholder": "请选择边栏风格",
            "field_name": "theme_sidebar",
            "field_type": "select",
            "select_options": {
              "light": "亮",
              "dark": "暗"
            },
            "default_value": "light"
          },
          {
            "label": "顶部风格",
            "placeholder": "请选择顶部风格",
            "field_name": "theme_header",
            "field_type": "select",
            "select_options": {
              "light": "亮",
              "dark": "暗"
            },
            "default_value": "dark"
          },
          {
            "label": "自定义页脚HTML",
            "placeholder": "可以实现客服JS代码的加入等",
            "field_name": "custom_html",
            "field_type": "textarea"
          }
        ]
      }
    },
    "active": "v2board"
  },
  "error": null
}

```

| 参数名  | 类型      | 描述        |
|------|---------|-----------|
| themes | obj     | 主题配置,固定写法 |
| active | boolean | 激活的主题     |


## 2.激活主题
> `POST` /config/save

- 请求参数
  `frontend_theme=v2board`

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": true,
  "error": null
}
```

| 参数名  | 类型      | 描述        |
|------|---------|-----------|
| themes | obj     | 主题配置,固定写法 |
| active | boolean | 激活的主题     |


## 3.获取主题配置
> `POST` /theme/getThemeConfig

- 请求参数
  `name=v2board`

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": {
    "theme_color": "default",
    "background_url": "",
    "theme_sidebar": "light",
    "theme_header": "dark",
    "custom_html": ""
  },
  "error": null
}
```

| 参数名  | 类型      | 描述   |
|------|---------|------|
| theme_color | string  | 主题颜色 |
| background_url | string | 背景图片url |
| theme_sidebar | string | 边栏风格 |
| theme_header | string | 主题顶部风格(配合用户端统一使用) |
| custom_html | string | 自定义页脚HTML |


## 4.主题配置保存
> `POST` /theme/saveThemeConfig

- 请求参数
- 参数经过 base64_encode
- 
  `config=eyJ0aGVtZV9jb2xvciI6ImRlZmF1bHQiLCJiYWNrZ3JvdW5kX3VybCI6IiIsInRoZW1lX3NpZGViYXIiOiJsaWdodCIsInRoZW1lX2hlYWRlciI6ImRhcmsiLCJjdXN0b21faHRtbCI6IiJ9&name=v2board`

- 成功返回示例 `json`

```json
{
  "status": "success",
  "message": "操作成功",
  "data": {
    "theme_color": "default",
    "background_url": "",
    "theme_sidebar": "light",
    "theme_header": "dark",
    "custom_html": ""
  },
  "error": null
}
```

