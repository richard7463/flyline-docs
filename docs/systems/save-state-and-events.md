# 存档与事件

## 本地存档

当前存档 key 为 `flyline_v1`，包含 generation、玩家与 wild type 突变、world seed、connectivity mode、lineage eggs、best eggs 和历史记录。

这是浏览器本地存储，不是账号云同步。清档只影响当前浏览器站点数据，不会向外部服务发送游戏内容。

## DOM 事件

- `flyline:genstart`：新一代开始。
- `flyline:genend`：本代结束并携带结算和抽卡信息。
- `flyline:log`：HUD 日志。

Phaser 场景拥有规则状态，DOM overlay 负责显示；两者通过事件和明确的 scene 方法沟通。

## 未来

云存档、排行榜、开放 observation API 和多人状态服务都属于远期设计，当前版本没有这些外部账户或网络功能。
