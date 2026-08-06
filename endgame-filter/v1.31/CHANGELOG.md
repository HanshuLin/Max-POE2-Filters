# POE2 Endgame Value Filter V1.31 — Change Log

发布日期：2026-08-06

基线版本：V1.3

## 新引入的想法

- 特殊 Boss 门票与终局钥匙不再按市场价格分级，统一固定为 B3 蓝色。
- `Pinnacle Keys` 使用类别规则，后续新增的同类别钥匙会自动获得 B3 样式。
- 归入 `Map Fragments` 的 Boss 门票使用明确的 BaseType 名单；普通进度碎片不受影响。

## Filter 规则变化

| 规则 | 上版本品级 | 当前版本品级 |
| --- | --- | --- |
| `Class == "Pinnacle Keys"` | W1 安全回退或市场评级 | **B3** |
| 已知 `Map Fragments` Boss 门票 BaseType | H / G2 / B3 / P4 | **B3** |
| `An Audience with the King`（谒王之约）低价值隐藏 | H | 删除 |
| `Call of the Shadows`（暗影呼唤）低价值隐藏 | H | 删除 |
