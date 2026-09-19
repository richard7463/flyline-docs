# 测试与验证

## 逻辑回归

```bash
node --input-type=module -e "import('./js/sim.js').then(m => console.log(m.runExperiment(1337)))"
```

重点检查：`n: 200`、real escape `100`、shuffled escape `68`、平均 lead 分别约 `0.202s` 与 `0.183s`。

## 语法检查

```bash
node --check js/sim.js
node --check js/scene-game.js
node --check js/ui.js
node --check js/scene-boot.js
```

## 浏览器流程

验证菜单、开始游戏、HUD、实验按钮、暂停、触摸控件和至少两代流程。自动化浏览器可以检查页面状态与 JavaScript 异常，但触摸阻尼、按钮位置、音效和长期节奏仍需要真实设备试玩。

## 文档检查

提交前检查 SUMMARY 中所有相对链接、公开状态标注和科学措辞。不要把内部路径、凭据或调试脚本复制到公开页面。
