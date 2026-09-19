# 游戏与界面边界

DOM overlay 适合菜单、长文本、HUD 和触摸控件；Phaser 适合培养皿世界、果蝇、捕食者、食物、粒子和空间反馈。

## 输入流

```text
触摸摇杆 / 鼠标 / 键盘
        → ui.js / scene input
        → GameScene
        → sim 规则
        → Phaser 世界与 HUD
```

菜单和抽卡不应直接改变 Phaser 内部对象；它们调用 scene 的公开方法。世界规则不应依赖某个 DOM 元素是否存在，这样 Node assay 和未来的不同客户端才能复用。

触摸层级必须保持：overlay 在最上层，暂停和 GF 按钮高于全屏浮动摇杆，摇杆高于画布但不遮住关键按钮。
