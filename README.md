# 栖木官网（JAM_Web）

栖木（秋招管理工具）的宣传网站。纯静态，单个 `index.html` + `assets/` 截图，无任何构建步骤和外部依赖。

在线地址：https://haoyu-zhu.github.io/JAM_Web

## 目录结构

```
栖木官网/
├── index.html          # 网站本体（样式和脚本都内联）
├── assets/
│   ├── home.png        # 首页截图（数据看板 + 代办）
│   ├── sharecard.png   # 一键生成的战绩卡
│   ├── profile.png     # 我的资料
│   ├── process.png     # 流程管理
│   └── notes.png       # 笔记
└── README.md
```

截图是用示例数据在软件里现截的（2560×1600），替换时保持同名即可。

## 部署（GitHub Pages）

- 仓库：https://github.com/haoyu-zhu/JAM_Web
- 已开启 Pages：仓库 **Settings → Pages → Deploy from a branch → `main` / `(root)`**。
- 推送到 `main` 后，GitHub 会**自动重新构建部署**，无需手动操作。

### 更新网站

```bash
git add -A
git commit -m "更新文案"
git push            # 推到 GitHub(origin)，Pages 自动重建
```

### 同步到 Gitee（可选镜像）

本仓库另设了 `gitee` 远程作为国内镜像：

```bash
git push gitee main
```

## 下载按钮指向哪里

站内「下载 Windows 版 / 下载最新版」指向 Gitee 仓库的 Releases 页
（https://gitee.com/zhy336013945/qiumu-job/releases），国内下载更快。
把 electron-builder 打出的安装包作为 Release 附件传上去，链接即生效。
