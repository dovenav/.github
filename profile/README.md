# dove

一个用 Rust 生成静态网页的简洁导航站点生成器，输出可直接部署到 GitHub Pages / Cloudflare Pages / Cloudflare Workers。支持主题目录与模板引擎（Tera），可自定义 HTML/CSS/JS；支持内/外网两套页面；内置搜索引擎切换与两种布局（default/ntp）。

示例/模板配置仓库（可直接参考部署方式）：

- [dove-private](https://github.com/dovenav/dove-private)：仅包含配置与 CI 的模板仓库（Pages/Workers 均支持）

环境要求：已安装 Rust 稳定版工具链（stable）。若在 CI 中构建，请在工作流中显式安装 Rust（推荐 `dtolnay/rust-toolchain@stable`）。

## 功能特性

- 配置拆分 include：主配置支持 `include/includes`，本地支持通配（glob），远程 URL（需 `remote` 特性）。
- 分类显示模式：每组可独立设置 `display: standard|compact|list|text`（支持中文别名）。
- 主题与模板：Tera 模板、多主题目录，静态资源可覆盖。
- 内/外网两套页面、跳转中间页（倒计时、UTM、风险等级）。
- 站点地图与 SEO：`sitemap.xml`、`robots.txt`、OG、canonical、基于 `base_url`。
- 离线支持：内置 Service Worker，首次访问后可离线使用。

 
## 许可

MIT
 

