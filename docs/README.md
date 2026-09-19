# Flyline

## 看见危险。判断方向。活过下一秒。

Flyline 是一款把果蝇逃逸回路变成可玩的单机血脉 roguelite。你不是控制一只拥有无限生命的角色，而是在有限能量、有限感知和捕食压力中，替一条血脉争取下一代。

> 觅食，产卵，观察逼近的危险，在 Giant Fiber（GF）反射亮起时做出决定。

## 三分钟了解项目

1. **进入培养皿**：移动果蝇，寻找糖、酵母和腐物。
2. **管理能量**：高能量会自动转化为卵；食物收益越高，通常风险也越高。
3. **读懂扑杀**：捕食者会接近，然后承诺一条弹道。GF READY 时按 Space 或触摸 GF 按钮逃逸。
4. **跨代选择**：一代结束后与 wild type 比较卵数，从 Mutation Draft 三选一；死亡只结束当前一代，血脉会继续。
5. **理解模型**：运动视觉信号在简化模型中经过 LC4/LPLC2，影响 GF 逃逸阈值。

## 当前状态

当前版本已经可以完整游玩单机生存循环、跨代突变、野生型比较、移动端操作和 connectome-inspired 对照实验。文档中的每个功能都标注为**已实现**、**建设中**或**远期**；规划中的多人、AI 同场和开放 benchmark 不是当前线上功能。

## 从哪里开始？

- 想马上玩：阅读[如何游玩](play/how-to-play.md)。
- 想理解科学边界：阅读[生物学边界](biology/biology-boundaries.md)和[逃逸回路](biology/escape-circuit.md)。
- 想复现实验：阅读[可复现实验](biology/reproducible-experiment.md)。
- 想贡献代码：阅读[技术架构](systems/architecture.md)和[贡献指南](development/contributing.md)。

## 一个重要的诚实声明

Flyline 使用真实研究中的回路名称与突触计数作为设计锚点，但当前实现是 **connectome-inspired 的可玩化简化模型**。它不是完整果蝇大脑、完整 FlyWire 连接组或完整行为仿真。游戏的价值在于把一个可检查的生物学问题变成玩家可以亲手体验、重跑和讨论的规则系统。
