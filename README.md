# 24029100313.github.io

个人学术主页。纯静态，零框架，零构建步骤。

## 结构

```
index.html                  # 全部内容与样式都在这一个文件里
images/avatar.png           # 头像，页面裁成圆形显示
images/paper-ra-bench-cover.webp  # RA-Bench 论文首页缩略图
images/paper-dfpr-cover.webp      # DFPR 论文首页缩略图
files/Shuo_Liang_CV.pdf     # CV，页眉的 cv 链接指向这里
.nojekyll                   # 告诉 GitHub Pages 不要跑 Jekyll
```

## 部署

仓库名必须是 `24029100313.github.io`，然后 Settings → Pages → Source 选 `main` 分支根目录。
几分钟后访问 https://24029100313.github.io

## 怎么改内容

直接编辑 `index.html`。文件里有中文注释标出各个区块。常见改动：

- **加一篇论文** — 复制 `<article class="pub">` 整块，改标题、作者、venue
- **加一条时间轴** — 复制 `<div class="entry">` 整块，按实际日历时间倒序插入；
  `t = 0` 只用来标记 2025 年春天开始转向科研探索的阶段，不再计算分钟级偏移
- **换 CV** — 覆盖 `files/Shuo_Liang_CV.pdf` 即可，链接不用改

## 设计约定

- 配色只有五个变量，全在 `:root` 里
- **金色 `--mark` 全站只用在 t=0 那一条时间轴上**，不要复用
- 字体：Newsreader 已弃用；当前用 Source Sans 3 + IBM Plex Mono，从 Google Fonts 加载
- 邮箱做了点击才显示的处理，防爬虫；改邮箱要动页面底部的 `<script>`
- **对外邮箱统一用 Gmail**：QQ 邮箱常被海外高校的邮件服务器过滤
- **发表署名统一用 Shuo Liang**，与 arXiv 一致，不要出现别的英文名
