# 技术架构

## 分层

```text
index.html + style.css + ui.js
  DOM 菜单、HUD、抽卡、触摸输入
          ↕ CustomEvent / scene methods
scene-game.js
  Phaser 世界、玩法编排、捕食者与世代
          ↓ import 纯函数
sim.js
  常量、种子 RNG、GF、实验、traits、stats
```

辅助模块包括：`scene-boot.js` 程序化贴图、`audio.js` WebAudio、`main.js` Phaser 启动和响应式画布尺寸。

## 关键边界

- `sim.js` 不依赖 DOM、Phaser 或 localStorage，可由 Node 直接运行。
- `scene-game.js` 是规则编排唯一入口，负责把纯逻辑和世界对象连接起来。
- `ui.js` 只负责展示和收集输入，不应复制游戏规则。
- 画布使用 `this.scale.gameSize`，世界坐标独立于屏幕像素。

## 事件桥

游戏通过 `flyline:log`、`flyline:genstart` 和 `flyline:genend` 通知 DOM。菜单通过 `beginRun`、`nextGen`、`setSeed` 等 scene 方法发起动作。

## 未来插入点

agent 接口、环境修饰、代中事件和更多突变应在现有层级中加入，不要让 UI 直接修改模拟状态，也不要把 Phaser 对象引入纯逻辑层。
