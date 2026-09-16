# Myna Home

Myna 的静态首页，用于介绍 AI 智能体工作空间，并将访客引导至 Huabot.com 的 Myna 控制台。

页面展示智能体任务执行示例、运行环境、使用场景、可用订阅套餐和智能服务快捷入口。

## 技术栈

- 单文件 HTML、CSS 和原生 JavaScript
- [Tailwind CSS](https://tailwindcss.com/) CDN
- [Lucide](https://lucide.dev/) 图标 CDN
- Huabot.com 公开接口提供动态套餐和快捷入口数据

本仓库不包含构建步骤、包管理清单或后端服务。

## 本地预览

项目可以直接在浏览器中打开 `index.html`。如需通过本地 HTTP 服务预览，在仓库根目录执行：

```sh
python3 -m http.server 8080
```

然后访问 [http://localhost:8080](http://localhost:8080)。

页面依赖外部 CDN 和 `https://huabot.com` 的公开 API；离线环境下，图标、样式和动态数据可能无法加载。套餐或快捷入口接口不可用时，页面会保留相应的提示信息。

## 页面能力

- 中英文切换与明暗主题，偏好保存在浏览器 `localStorage`
- 可交互的任务演示与应用场景切换
- 从公开订阅接口加载套餐、配额与购买链接
- 从公开系统配置接口加载智能服务快捷入口
- 所有控制台和外部服务链接在新标签页打开

## 目录

```text
.
├── index.html   # 页面结构、样式和交互逻辑
├── LICENSE      # MIT License
└── README.md
```

## 修改说明

页面内容、样式和客户端交互均位于 `index.html`。修改动态接口时，请同时检查其响应结构和接口不可用时的降级文案；不要在此静态站点中加入私密凭据或访问令牌。

## License

本项目采用 [MIT License](LICENSE)。
