# Max POE2 Filters

Path of Exile 2 终局速刷物品过滤器。

当前版本：**v1.31**

## 下载

- [下载最新 Release](https://github.com/HanshuLin/Max-POE2-Filters/releases/latest)
- [直接下载 v1.31 ZIP](https://github.com/HanshuLin/Max-POE2-Filters/releases/download/v1.31/POE2-Endgame-Value-Filter-v1.31.zip)
- [查看所有历史版本](https://github.com/HanshuLin/Max-POE2-Filters/releases)

## 当前文件

```text
endgame-filter/
├── endgame_filter.filter  # 当前正式 Filter
└── list.html              # 离线规则与市场评级 Review
CHANGELOG.md               # 当前版本变更说明
```

历史版本不重复保存在 `main`。请通过 Git tags 或 GitHub Releases 查看和下载。

## 安装

1. 下载最新 Release ZIP 并解压。
2. 将解压后的 `.filter` 文件放入 POE2 Filter 目录。
3. Filter 使用 `blue.mp3`、`purple.mp3` 和 `red.mp3` 自定义音效；请将这些音频放在游戏可识别的 Filter 音效路径中。
4. 在游戏设置中选择并重新加载 Filter。

`list.html` 可以直接在浏览器中打开，用于查看评级、搜索物品和核对视觉规则。

## 版本维护

1. 从 `main` 创建版本分支。
2. 修改当前 Filter、Review HTML 和 `CHANGELOG.md`。
3. 通过 Pull Request 合并到 `main`。
4. 创建版本 tag 和 GitHub Release，并附加用户下载 ZIP。
