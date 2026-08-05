# POE2 Endgame Value Filter V1.3 — Change Log

基线版本：V1.2  
状态：V1.3 最终规则定稿

## 新引入的想法

- NeverSink 的底材评级只用于评估首饰，不引入普通武器和护甲的底材 Tier。
- 装备仅保留高价值首饰底材、卓越装备和瓦尔额外打孔装备；其他普通装备继续隐藏。
- 卓越装备与瓦尔额外打孔装备统一定为 B3。
- 高价值白底首饰加入未腐化限制，并按 NeverSink 评级调整。
- 新增 P0 评级，用于标记无法仅凭底材确定价值的未知传奇装备。

## Filter 规则变化

| Filter 规则 | V1.2 评级 | V1.3 评级 |
| --- | --- | --- |
| 卓越装备：`Quality >= 21` | G2 | **B3** |
| 大型瓦尔额外打孔装备：`Sockets >= 3` | G2 | **B3** |
| 小型瓦尔额外打孔装备：`Sockets >= 2` | G2 | **B3** |
| `Heavy Belt`、`Utility Belt`：`Rarity Normal` | G2 | 删除 |
| `Heavy Belt`、`Utility Belt`：`Rarity Normal`、`Corrupted False` | -- | 新增（**B3**） |
| `Gold Amulet`、`Gold Ring`：`ItemLevel >= 81`、`Rarity Normal` | G2 | 删除 |
| `Gold Amulet`、`Gold Ring`：`ItemLevel >= 82`、`Rarity Normal`、`Corrupted False` | -- | 新增（**R5**） |
| `Solar Amulet`：`ItemLevel >= 82`、`Rarity Normal` | G2 | 删除 |
| `Solar Amulet`：`ItemLevel >= 82`、`Rarity Normal`、`Corrupted False` | -- | 新增（**R5**） |
| 未知传奇装备回退规则：`Rarity Unique` | W1 | **P0** |
