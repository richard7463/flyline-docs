# 贡献指南

## 先理解边界

贡献前阅读玩家指南、[技术架构](../systems/architecture.md)和[可复现实验](../biology/reproducible-experiment.md)。小改动也要知道它是否影响 seed、GF、捕食者承诺弹道和存档格式。

## 代码原则

- 保持 `sim.js` 无 DOM、无 Phaser、无 localStorage。
- 新 trait 通过 `TRAIT_INFO → recomputeStats → scene hook` 接入。
- 不在捕食者 lunge 阶段加入持续追踪。
- 不用表现层随机数改变世界规则。
- 不把规划功能写成已实现功能。
- 新增存档字段提供合理默认值。

## 提交前

1. 跑 Node 逻辑实验和语法检查。
2. 手动走一遍开始、觅食、逃逸、结算、抽卡和下一代。
3. 如果修改触摸或响应式布局，在桌面和真实移动设备上检查。
4. 更新受影响的公开文档，并标注实现状态。

当前项目许可证尚未最终确定，因此贡献代码前请确认维护者对授权方式的安排。
