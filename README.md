# 栖木官网

栖木（秋招管理工具）的宣传网站。纯静态，单个 `index.html` + `assets/` 截图，无任何构建步骤和外部依赖。

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

## 部署在 Gitee Pages

仓库地址：https://gitee.com/zhy336013945/qiumu-job
上线后网址：https://zhy336013945.gitee.io/qiumu-job

### 首次部署

```bash
# 在本文件夹执行
git init
git add -A
git commit -m "栖木官网"
git remote add origin https://gitee.com/zhy336013945/qiumu-job.git
git push -u origin master
```

推送时会要求输入 Gitee 用户名 + 密码（或私人令牌）。

然后在 Gitee 仓库页面开启 Pages：
**服务 → Gitee Pages → 选择 master 分支 → 部署**。
（Gitee 要求账号完成实名认证后才能使用 Pages。）

### 之后更新

改完文件后：

```bash
git add -A
git commit -m "更新文案"
git push
```

再回 Gitee Pages 页面点一次 **更新** 即可（Gitee Pages 不会自动重新部署）。

## 下载按钮指向哪里

「下载 Windows 版 / 下载最新版」都指向仓库的 Releases 页
（https://gitee.com/zhy336013945/qiumu-job/releases）。
把 electron-builder 打出的安装包作为 Release 附件传上去，链接即生效。
