# POE2 Endgame Value Filter V1.2 — Change Log

发布日期：2026-08-04  
基线版本：V1.1  
适用场景：POE2 0.5，软核交易服赛季末，终局 T15 异界速刷

## 本次变更

### 1. 修复低价值通货进入白色安全网

新增显式隐藏规则：

- `Scroll of Wisdom`
- `Transmutation Shard`
- `Regal Shard`
- `Artificer's Shard`
- `Chance Shard`
- `Alchemy Shard`
- `Orb of Transmutation`
- `Orb of Augmentation`

该规则位于 `Stackable Currency` 白色安全网之前。已知低价值物品不再以 W1 白色显示。

### 2. 调整高品级标签字号

| 品级 | V1.1 | V1.2 |
| --- | ---: | ---: |
| B3 蓝 | 32 | 36 |
| P4 紫 | 32 | 36 |
| R5 红 | 32 | 40 |
| G2 绿 | 32 | 32（不变） |
| W1 白 | 32 | 32（不变） |
| Gold | 24 | 24（不变） |

### 3. 同步 V7 柔化配色

- B3 蓝：`51 153 238 255`
- P4 紫：`163 53 238 255`
- R5 红：`255 32 32 255`
- G2 绿：`88 211 79 255`
- W1 白：`255 255 255 255`
- 通货暗金：`170 158 130 255`
- 镶嵌物边框：`190 145 225 255`
- 门票/消耗品边框：`220 220 220 255`
- 标签背景：`0 0 0 220`

金币继续使用客户端默认通货外观。三种维金改用通货暗金色，不再使用 V1.1 的任务物品棕色。

### 4. 蓝、紫、红品级统一使用自定义音效

所有 B3、P4、R5 `Show` 规则按最终品级分别指向：

- B3：`CustomAlertSound "blue.mp3"`
- P4：`CustomAlertSound "purple.mp3"`
- R5：`CustomAlertSound "red.mp3"`

对应规则中的旧 `PlayAlertSound` / `PlayAlertSoundPositional` 已移除，避免重复或覆盖。音频文件不包含在本次交付中，需由用户自行放入游戏可识别的位置。

白色、绿色、金币和维金不使用这三种自定义音效；维金继续完全静音。

### 5. 修复维金光柱 OR 逻辑

规则拆分为三层并按顺序匹配：

1. `Exceptional Verisium`：无论数量，永久棕色光柱。
2. `Verisium` 或 `Liquid Verisium` 且 `StackSize > 500`：永久棕色光柱。
3. 其余维金：显示但无光柱。

这避免了 V1.1 将“卓越维金”与“数量大于 500”错误组合成 AND 条件的问题。

### 6. 新增瓦尔传奇保护规则

- `IsVaalUnique True` 且 `Rarity Unique`：R5 红色、字号 40、红色永久光柱、红色 Star、`red.mp3`。
- `HasVaalUniqueMod True` 且 `Rarity Unique`：P4 紫色、字号 36、紫色永久光柱、紫色 Star、`purple.mp3`。
- 未加入 `TwiceCorrupted True` 装备掉落规则，因为双重腐化传奇不会作为普通掉落出现。
- 两条规则均位于传奇底材定级与低价值传奇隐藏规则之前。

## 未变更内容

- 经济快照仍为 `2026-08-03 18:00:00 Asia/Shanghai`。
- 换算仍为 `1C = 213E`、`1D = 970E`。
- 价格阈值、市场定级名单和 NeverSink 传奇代理数据未重算。
- 神圣石音效问题已确认为误报，不作为 V1.2 修复项。
- V1.1 文件未被覆盖。

## 验证结果

- B3、P4、R5 的每一个显示规则均具有正确字号和唯一对应的自定义音效。
- Filter 中不再存在 V1.1 的深蓝 `0 112 221` 或荧光绿 `30 255 0` 文本色。
- 低阶通货隐藏规则位于 `Stackable Currency` 白色安全网之前。
- 瓦尔传奇规则位于所有低价值传奇隐藏规则之前。
- 不包含 `TwiceCorrupted` 条件。
- Review HTML 的内嵌 JavaScript 已通过语法解析。
- Filter：745 行，38,895 bytes，SHA-256 `17137f082e3e06fdd21c4e90eaab5b6088b32b4612147ac21fe60fa2254ad378`。
- Review HTML：466,753 bytes，SHA-256 `86b2d8e2edf0fdc4c9cbd0295d3d604b04e5026709b7ca8427acde2eff83397c`。

## 客户端使用前检查

1. 将 `blue.mp3`、`purple.mp3`、`red.mp3` 放入客户端可识别的 Filter 音效路径。
2. 加载 `poe2_endgame_value_filter_v1_2.filter`，确认客户端无语法错误。
3. 实测低阶碎片隐藏、三档字号、自定义音效、卓越维金光柱及 `>500` 维金光柱。
