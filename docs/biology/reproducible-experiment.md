# 可复现实验

## 实验问题

在相同的捕食者接近场景中，保留 LC4/LPLC2 的真实权重关系，与打乱连接权重相比，GF 是否更可能在承诺扑杀前触发足够早的逃逸？

## 固定条件

- seed：`1337`
- 配对 trial：`200`
- 每个 trial：一次捕食者 committed lunge
- 唯一变量：real connectivity 与 shuffled connectivity
- 指标：GF 触发到承诺扑杀命中之间的 lead time，以及该 trial 是否成功逃脱

这里的 lead time 不是跳跃次数、存活总时间或产卵数；它只表示单次承诺扑杀中，逃逸是否提前达到所需窗口。

## 当前基线结果

运行 `runExperiment(1337)` 得到：

| 配置 | 逃脱率 | 平均 trigger lead |
| --- | ---: | ---: |
| Real connectivity | 100% | 0.202 s |
| Shuffled connectivity | 68% | 0.183 s |

这些结果说明，在**当前简化模型、当前指标、当前 seed 和当前 200 次配对试验**下，真实连接配置的逃逸表现更可靠。

## 如何重跑

在项目根目录运行：

```bash
node --input-type=module -e "import('./js/sim.js').then(m => console.log(m.runExperiment(1337)))"
```

实验代码位于 `js/sim.js`，不依赖 DOM 或 Phaser，因此可以在 Node 中直接执行，也可以由游戏菜单调用。

## 如何解释结果

结果不是对真实动物行为的普遍证明，也不是说“真实连接永远优于任何打乱方式”。它是一个可复现的模型比较：在定义好的 assay 中，连接权重排列改变了 GF 逃逸结果。

任何修改 GF、捕食者承诺弹道或 assay 指标的代码，都必须重新记录 seed、样本数、指标定义和结果，不能只更新宣传数字。
