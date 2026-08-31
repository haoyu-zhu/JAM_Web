# 栖木官网（JAM_Web）

栖木（秋招管理工具）的宣传网站。纯静态，`index.html` + `assets/` 截图，无构建步骤、无外部依赖。

- 在线地址：https://haoyu-zhu.github.io/JAM_Web
- 软件源码：https://github.com/haoyu-zhu/JAM

## 目录结构

```
JAM_Web/
├── index.html          # 网站本体（样式和脚本都内联）
├── .nojekyll           # 关闭 Jekyll，让 GitHub 原样托管所有文件
├── assets/             # 截图（home / sharecard / profile / process / notes）
└── README.md
```

## 部署（GitHub Pages）

- 已开启：仓库 **Settings → Pages → Deploy from a branch → `main` / `(root)`**。
- 推送到 `main` 后 GitHub 自动重新构建部署，无需手动操作。

### 更新网站

```bash
git add -A
git commit -m "更新文案"
git push
```

## 下载按钮指向哪里

两个「下载 Windows 版」按钮都直连 JAM 源码仓库的**最新发行版附件**，点击即开始下载：

```
https://github.com/haoyu-zhu/JAM/releases/latest/download/JobTracker-Setup.exe
```

`releases/latest/download/` 会自动指向最新发行版，安装包文件名固定为 `JobTracker-Setup.exe`（不带版本号）。
**发新版本时：Release 里的安装包务必仍命名为 `JobTracker-Setup.exe`**，这样这个链接永远指向最新版，`index.html` 无需再改。
