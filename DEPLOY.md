# Cron Builder · 部署说明（资产线热身工具 v1）

## 是什么

单文件静态网页（`index.html`，零依赖、纯前端）：cron 表达式可视化生成 + 人类语言解释 + 未来 5 次执行时间 + 12 个预设 + SEO 文案（cheat sheet + 常见坑）。已浏览器实测通过。

## 部署（飞哥一次性动作，约 10 分钟）

1. **域名**：注册一个（推荐 Namecheap/Cloudflare，约 $10/年；或先用免费子域验证流量再买）。
2. **托管**：Cloudflare Pages（免费、全球 CDN）：dash.cloudflare.com → Pages → Upload assets → 把本目录的 `index.html` 拖进去 → 得到 `xxx.pages.dev` 地址 → 绑定域名。
3. **统计**：页面里加 Cloudflare Web Analytics（免费、无 cookie）或 Umami 自托管。
4. **收录**：Google Search Console 提交（1–2 周开始出词）。

## 上线后夜班自动化能做什么

- 每晚生成 1–2 篇长尾 SEO 文章页（"cron every 30 minutes"、"crontab every monday" 等 query 向内容，模板化产出）追加到站点
- 监控 Search Console 数据（有 API 的话接入晨报）
- 第二个工具（图片表格转 Excel）复用同一套部署管线

## 后续版本 ideas

- v1.1：中文界面切换（国内流量测试）
- v1.2：6 字段（含秒）支持 + Quartz/Jenkins 方言切换
- v1.3：分享链接（把表达式编码进 URL query，便于传播）
