# Cloudflare Pages 免费部署计划

本网站已发布在 GitHub 公共仓库 `jiachenshi999/jiachenshi999.github.io`，并于 2026-09-29 通过 Cloudflare Pages 的 Git 集成部署到 <https://jiachenshi.pages.dev/>。项目名为 `jiachenshi`，生产分支为 `main`，框架为 None，构建命令留空，输出目录为 `.`。以后更新 `main` 分支时，两个站点可同时更新。Cloudflare Pages 免费提供 `*.pages.dev` 地址，但不提供免费的独立 `.com` 或 `.cn` 域名。

当前待办：注册并验证 FreeDNS 账号，创建可用的共享 `.com` 子域名，再将它绑定到 Cloudflare Pages。

## 账号准备

1. Cloudflare 账号已注册，Cloudflare Pages 项目已部署。账号和密码由网站所有者本人保管。
2. 由网站所有者注册并验证 [FreeDNS 账号](https://freedns.afraid.org/signup/)。FreeDNS 需要验证码和邮箱验证。它可免费提供共享 `.com` 域名下的子域名，例如 `jiachenshi.mooo.com`；具体名称须以创建时的可用性为准。

## 部署到 Cloudflare Pages

1. 在 Cloudflare 控制台进入 **Workers & Pages → Create application → Pages → Connect to Git**。
2. 授权 GitHub 仓库 `jiachenshi999/jiachenshi999.github.io`，选择该仓库。
3. 生产分支选 `main`；框架选 **None**；根目录保持仓库根目录；构建命令留空；构建输出目录填 `.`（仓库根目录已有 `index.html`）。如果控制台要求构建命令，可填 `exit 0`。
4. 部署后记录 Cloudflare 实际分配的 `<project>.pages.dev` 地址，并确认首页、CSS、照片都正常显示。

不要选择拖拽上传：Git 集成可在以后每次更新仓库时自动重新部署。

## 配置免费的共享 `.com` 子域名

1. 在 FreeDNS 的 **Subdomains** 中选择管理员持有的 `mooo.com`，尝试创建含姓名的子域名。记录实际获得的完整域名。
2. 在 Cloudflare Pages 项目的 **Custom domains → Set up a domain** 中添加该完整域名。
3. 按 Cloudflare 给出的目标，在 FreeDNS 为该子域名设置 `CNAME`，指向实际的 `<project>.pages.dev`（只填主机名，不带 `https://`）。
4. 等待 Cloudflare 显示域名与 HTTPS 证书均为活动状态，然后测试首页和静态资源。
5. 暂时保留 `index.html` 的 canonical、`sitemap.xml` 和 `robots.txt` 指向 GitHub Pages。FreeDNS 的共享子域名可能受搜索引擎收录限制；先将它作为便于记忆的访问别名，确认长期可用且可收录后，再决定是否改为主域名。

共享子域名由他人拥有，不等同于自己注册的独立域名。FreeDNS 的 FAQ 说明共享子域名默认对 Google 不可见，可以联系管理员申请处理。Cloudflare Pages 免费版也不提供中国大陆境内的 Cloudflare China Network 加速；需从实际使用的大陆网络测试，保留 GitHub Pages 地址作为备用。

## 官方资料

- [Cloudflare Pages：连接 GitHub](https://developers.cloudflare.com/pages/get-started/git-integration/)
- [Cloudflare Pages：静态 HTML](https://developers.cloudflare.com/pages/framework-guides/deploy-anything/)
- [Cloudflare Pages：自定义域名](https://developers.cloudflare.com/pages/configuration/custom-domains/)
- [Cloudflare China Network：适用范围](https://developers.cloudflare.com/china-network/)
- [FreeDNS：共享域名说明](https://freedns.afraid.org/signup/moreinfo/)
- [FreeDNS：共享域名长期使用提醒](https://freedns.afraid.org/faq/)

