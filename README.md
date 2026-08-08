# Max POE2 Filters

Path of Exile 2 终局速刷物品过滤器，提供 Value 与 Rarity 两种过滤风格。

当前版本：**v1.4**

## 下载

- [下载最新 Release](https://github.com/HanshuLin/Max-POE2-Filters/releases/latest)
- [直接下载 v1.4 ZIP](https://github.com/HanshuLin/Max-POE2-Filters/releases/download/v1.4/Max-POE2-Filters-v1.4.zip)
- [查看所有历史版本](https://github.com/HanshuLin/Max-POE2-Filters/releases)

## 选择 Filter

### Value Filter

`endgame-filter/endgame_filter.filter`

按市场价值和物品类别分级，适合重视交易价值的终局速刷。

### Rarity Filter

`rarity-filter/endgame_rarity_filter_v1.4.filter`

按稀有度、底材档位、物品等级和 UIT 分级，适合偏好底材与稀有度逻辑的玩家。

## 当前文件

```text
endgame-filter/
├── endgame_filter.filter
└── list.html
rarity-filter/
├── endgame_rarity_filter_v1.4.filter
└── endgame_rarity_filter_v1.4_review.html
CHANGELOG.md
README.md
```

两个 Review HTML 均可直接在浏览器中打开，用于查看评级、搜索物品和核对视觉规则。

## 安装

1. 下载最新 Release ZIP 并解压。
2. 从 Value Filter 或 Rarity Filter 中选择需要的 `.filter` 文件，放入 POE2 Filter 目录。
3. Value Filter 使用 `blue.mp3`、`purple.mp3` 和 `red.mp3` 自定义音效；如需声音，请将音频放在游戏可识别的 Filter 音效路径中。
4. 在游戏设置中选择并重新加载 Filter。

## 版本维护

1. 从 `main` 创建版本分支。
2. 修改 Filter、Review HTML 和 `CHANGELOG.md`。
3. 通过 Pull Request 合并到 `main`。
4. 创建版本 tag 和 GitHub Release，并附加用户下载 ZIP。

历史版本不重复保存在 `main`。请通过 Git tags 或 GitHub Releases 查看和下载。
