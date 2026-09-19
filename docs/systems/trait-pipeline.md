# 突变管线

## 数据流

```text
TRAIT_INFO
  → recomputeStats(fly)
  → stats 数值字段与行为开关
  → scene-game.js 的消费点
```

行为 trait 应通过 `fly.stats` 判断，而不是在场景代码中到处查找 `fly.traits.includes(...)`。这样一张卡的规则入口清晰，也更容易在 Node 中测试。

## 消费点

- `getSteer`：趋光、醉跑惯性和自动行为。
- `updateFly`：代谢、进食、产卵和同类互动。
- `updatePredator`：拟态、护卵、滞育和目标选择。
- `tryDash`：主动跳跃、距离、能量与冷却。
- `updateGF`：保持当前 GF 核心与实验基线稳定。

## 新增 trait 的验收

每张卡必须有收益和代价或强情境性，必须改变玩家决策，并且不能破坏 `runExperiment(1337)` 基线。UI 文案、状态统计和保存数据应与 sim 层使用同一 key。
