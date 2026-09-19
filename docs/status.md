# 项目状态

本文把当前功能和未来设想分开，避免把设计稿误读成产品承诺。

## 已实现

- 单机培养皿生存：觅食、能量、自动产卵、捕食者和 50 秒世代。
- 捕食者的 approach → committed lunge → recover 状态机。
- GF 逃逸反射、PC 键鼠操作、移动端浮动摇杆和 GF 按钮。
- 跨代血脉、Mutation Draft 三选一、玩家与 wild type 卵数比较。
- 多个数值与行为突变、昼夜变化、音效、粒子和慢动作表现。
- 种子实验：真实连接与 shuffled connectivity 的配对比较。
- 浏览器 localStorage 存档和可直接运行的纯逻辑模拟层。

## 建设中

- 24 个突变的完整行为化重构，包括 rover、sitter、mimic、cannibal、diapause、adh、phototax、guard、clock、hopper、pheromone。
- 捕食者的佯攻与连续扑杀、代中事件、每五代环境轮换。
- 每日种子挑战、血脉树和更完整的新手引导。
- 真实设备上的手感、平衡和长时间留存评估。

## 远期方向

- 受限 observation/action schema 下的 AI agent 模式。
- 同一确定性世界中的人类与 agent 对照。
- 开放只读观测接口、跨种子评测和可复现 benchmark。
- 多人或大逃杀模式。
- 趋光、生物钟、嗅觉与信息素等更多生物学回路，前提是它们真正改变玩法。

远期方向只有在规则、接口和评测标准完成后才会升级为产品功能描述。
