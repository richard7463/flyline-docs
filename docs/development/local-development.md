# 本地开发

Flyline 是静态页面，没有打包步骤。Phaser 已放在 `vendor/phaser.min.js`，入口页面通过 ES module 加载 `js/main.js`。

```bash
cd /path/to/flyline
python3 -m http.server 8124
```

然后打开 `http://127.0.0.1:8124/`。不要直接用 `file://` 打开，因为浏览器会限制 module 加载。

## 目录重点

- `index.html`：游戏 DOM 结构。
- `style.css`：页面和 HUD 样式。
- `js/sim.js`：纯模拟与实验。
- `js/scene-game.js`：Phaser 玩法编排。
- `js/ui.js`：菜单、HUD、抽卡和触摸输入。
- `js/scene-boot.js`：程序化纹理。
- `js/audio.js`：WebAudio 音效。

本地开发不需要账号、数据库或外部 API。
