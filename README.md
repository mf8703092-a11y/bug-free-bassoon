# 营造万象 · 古建中国

中国古建文明数字品牌与全媒体传播项目。完整源码和素材均可持续维护。

当前默认部署方案为 **Render 免费静态站点**，保留互动展馆、木构实验室、展板缩放、人物/IP 切换、文创筛选、纹样共创、视频和六地调研档案。此方案通过源码更新内容，暂不启用在线上传后台。

## Render 免费部署

新建 **Static Site**，关联本仓库。不要选择显示月费的 Web Service。

| 配置 | 值 |
| --- | --- |
| Branch | `main` |
| Root Directory | 留空 |
| Build Command | `node build-static.mjs` |
| Publish Directory | `dist` |

`render.yaml` 已提供同样的静态部署配置，不包含付费实例、数据库或磁盘。平台仍有免费流量与构建额度；不要为此项目开通付费套餐。

## 更新内容

文字和栏目保存在 `public/content.json`，图片在 `public/assets/images/`，视频在 `public/assets/videos/`。修改素材路径时保留大小写一致。免费部署会自动由 JSON 重建 `content.js`，无需手动维护两份内容。

每次提交后 Render 会重新发布。GitHub 保留修改历史，后续可以继续调整设计、交互和内容，也可以恢复旧版。

## 本地运行与未来后台

运行 `npm start`，用 Node.js 22+ 启动。完整服务器端编辑后台仍保留在源码中；只有配置维护口令和会话密钥才会启用。未来启用在线上传之前，需要落实可靠的持久存储，不能把新增材料只存于免费临时服务器。

完整操作和资料说明见 [使用说明.md](使用说明.md)。可编辑展板在 `exhibit-boards/`。
