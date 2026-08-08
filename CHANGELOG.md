# Max POE2 Filters v1.4 — Change Log

发布日期：2026-08-08

基线版本：v1.31

## 新增 Rarity Filter

- 新增 `rarity-filter/endgame_rarity_filter_v1.4.filter`，作为 Value Filter 之外的第二种过滤风格。
- Rarity Filter 依据物品稀有度、底材档位、物品等级和 UIT 进行评级；UIT 只会提升评级，不会降低评级。
- 新增 `rarity-filter/endgame_rarity_filter_v1.4_review.html`，可离线查看首饰底材分级、规则逻辑和视觉结果。
- Rarity Filter 已统一升级为 v1.4，并纳入同一个 `Max-POE2-Filters` 仓库和 Release。

## Value Filter

- 保留现有 `endgame-filter/endgame_filter.filter` 及 `endgame-filter/list.html`。
- Value Filter 的规则沿用 v1.31，本次发布不修改其过滤逻辑。

## 下载内容

v1.4 Release ZIP 同时包含：

- `endgame-filter/`：按市场价值分级的 Value Filter。
- `rarity-filter/`：按稀有度、底材和物品等级分级的 Rarity Filter。
- `README.md` 与 `CHANGELOG.md`。
