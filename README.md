# Shuo-Liang-0111.github.io

个人学术主页。纯静态，零框架，零构建步骤。

## 结构

```
index.html                  # 全部内容与样式都在这一个文件里
images/avatar.png           # 头像，页面裁成圆形显示
images/paper-ra-bench-cover.webp  # RA-Bench 论文首页缩略图
images/paper-dfpr-result.webp     # DFPR 结果图缩略图
images/experience-*               # Experience 区域的学校/实验室标识
images/experience-infrec.png       # InfRec / Cardinal AI 官网原版标识
files/Shuo_Liang_CV.pdf     # CV，页眉的 cv 链接指向这里
.nojekyll                   # 告诉 GitHub Pages 不要跑 Jekyll
```

## 部署

仓库名必须是 `Shuo-Liang-0111.github.io`，然后 Settings → Pages → Source 选 `main` 分支根目录。
几分钟后访问 https://shuo-liang-0111.github.io

## 怎么改内容

直接编辑 `index.html`，各个内容区块由对应的 `<section>` 标题区分。常见改动：

- **加一篇论文** — 复制 `<article class="paper">` 整块，改标题、作者、venue
- **加一段经历** — 复制 `<article class="xp">` 整块，补充机构标识、职责、地点与日期
- **换 CV** — 覆盖 `files/Shuo_Liang_CV.pdf` 即可，链接不用改

## 设计约定

- 配色变量集中在 `:root` 里
- 字体：系统无衬线字体优先，Inter 从 Google Fonts 加载作为回退
- 深浅色：默认跟随系统，右上角按钮切换，并在当前浏览器保存选择
- 首尾使用动态点阵背景；减少动态效果的系统设置下显示静态背景
- 青岛二中使用现有横版标志中的校徽部分，通过 CSS 容器显示，原始图片保持完整
- 邮箱使用可直接点击的 `mailto:` 链接
- **对外邮箱统一用 Gmail**：QQ 邮箱常被海外高校的邮件服务器过滤
- **发表署名统一用 Shuo Liang**，与 arXiv 一致，不要出现别的英文名

## 本次更新来源（2026-10-16）

- InfRec 实习：2026-10-14 开始，远程，算法研究与开发；日期和职责由本人提供。
- 公司官网：[Cardinal AI](https://www.cardinal-agi.com/)。经历图片直接使用官网公开的 [InfRec 标识](https://www.cardinal-agi.com/prelogin/assets/infrec-logo.png)，保存为 `images/experience-infrec.png`，未修改标识。
- RA-Bench 状态：`Submitted to ICLR 2027`，仅表示投稿。参照 [ICLR 2027 Author Guidelines](https://iclr.cc/Conferences/2027/AuthorGuidelines)：审稿期间允许 arXiv 预印本，投稿正文和补充材料仍须匿名；不要把投稿状态写成录用。

## 版式更新（2026-11-16）

- 采用本人提供并确认的页面预览：大标题、动态点阵、论文卡片、机构标志和深浅色切换。
- RA-Bench 状态简化为 `ICLR 2027 · Under review`。
- 发布文件移除本地预览的 `noindex` 标记，并设置正式标题与 canonical 地址。
