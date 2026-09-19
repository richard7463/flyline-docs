# 部署

Flyline 是可由任意静态托管服务提供的前端项目：HTML、CSS、JavaScript、Phaser vendor 文件和文档 Markdown 都可以直接发布。

部署前确认：

- ES module 路径在 HTTPS 或正确的 HTTP server 下可加载；
- `vendor/phaser.min.js` 和所有相对路径存在；
- 生产页面没有依赖本机文件；
- 游戏回归和 `runExperiment(1337)` 通过；
- 不把本地存档、开发凭据或调试日志上传到公开目录。

当前文档方案是仓库 Markdown 与 GitBook 同步。GitBook 连接和发布应由项目维护者在外部平台配置；本仓库不声称已经自动发布了 GitBook 站点。
