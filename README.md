# 24029100313.github.io

个人学术主页。纯静态，零框架，零构建步骤。

## 结构

```
index.html                  # 全部内容与样式都在这一个文件里
images/avatar.jpg           # 头像，512×512，页面裁成圆形显示
images/turning-point.jpg    # 时间轴 t=0 那一条的配图
.nojekyll                   # 告诉 GitHub Pages 不要跑 Jekyll
```

## 部署

仓库名必须是 `24029100313.github.io`，然后 Settings → Pages → Source 选 `main` 分支根目录。
几分钟后访问 https://24029100313.github.io

## 怎么改内容

直接编辑 `index.html`。文件里有中文注释标出各个区块。常见改动：

- **加一篇论文** — 复制 `<article class="pub">` 整块，改标题、作者、venue
- **加一条时间轴** — 复制 `<div class="entry">` 整块。注意 `.offset` 里的
  `t + N mo` 是相对 2025-05-02 21:05 的偏移，加新条目时要算一下
- **补 CV / Scholar 链接** — 找到 `class="soon"` 的 `<span>`，换成 `<a href="...">`
- **删掉开头那段给爬虫看的玩笑** — 整个 `<p class="egg">` 删掉即可

## 设计约定

- 配色只有五个变量，全在 `:root` 里
- **金色 `--mark` 全站只用在 t=0 那一条时间轴上**，不要复用
- 字体：Newsreader 已弃用；当前用 Source Sans 3 + IBM Plex Mono，从 Google Fonts 加载
- 邮箱做了点击才显示的处理，防爬虫；改邮箱要动页面底部的 `<script>`
