# Shuo-Liang-0111.github.io

个人学术主页。纯静态单文件架构，零框架，零构建步骤。

## 结构

```
index.html                          # 全部结构、样式、交互与 JSON-LD 元数据
robots.txt                          # 搜索引擎抓取规则
sitemap.xml                         # 站点地图
*.woff2                             # Shippori Mincho 与 Figtree 本地字体子集
*-OFL.txt                           # 字体许可证
images/avatar.webp                  # 压缩优化后的 320×320 头像（保留 avatar.png 兜底）
images/evening-coast*.webp          # 桌面与移动端暮色海岸插画
images/coast-whale-mask.svg         # 鲸鱼微动效遮罩
images/paper-ra-bench-teaser.webp   # RA-Bench Figure 1 裁切主图
images/paper-dfpr-result.webp       # DFPR 核心结果图
images/experience-*                 # Experience 区域的机构与学校标识
files/Shuo_Liang_CV.pdf             # 英文简历，页眉 CV 按钮指向这里
.nojekyll                           # 禁用 GitHub Pages 默认 Jekyll 构建
```

## 部署

仓库名为 `Shuo-Liang-0111.github.io`，在 Settings → Pages → Source 选择 `main` 分支根目录即可自动发布至 <https://shuo-liang-0111.github.io/>。

## 维护说明

直接编辑 `index.html` 中对应的语义区块即可：

- **新增论文** — 复制 `<article class="paper">` 并在脚本顶部 `BIBTEX` 对象中追加条目
- **新增经历** — 复制 `<article class="xp">`，时间轴连线会自动按首尾机构图标中心对齐
- **更新简历** — 覆盖 `files/Shuo_Liang_CV.pdf` 并同步更新 `sitemap.xml` 中的日期

## 设计与工程约定

- **视觉母题**：保留「日落前 / 日落后」双主题 WebGL 暮色流云与海岸鲸鱼微视差；正文采用暖羊皮纸 / 暖深咖质感，暗色模式下配图与机构标识使用柔和暖米白衬底。
- **排版与文案**：标题使用 `Shippori Mincho`，正文使用 `Figtree`；文案按学术审稿标准去冗余，拆分 `Papers`（科学问题、规模、核心发现与指标）与 `Experience`（角色分工、工程实现与合作关系）的职责。
- **交互细节**：顶部滑动胶囊导航 + 阅读进度细线、移动端毛玻璃目录抽屉、论文配图弹性 Lightbox 放大查看、`BibTeX` 与邮箱一键复制（带悬浮 Toast 反馈）、外链新标签页打开与轻量箭头位移，并完整兼容 `prefers-reduced-motion`。
- **检索与性能**：内嵌 `JSON-LD`（`Person` + `ScholarlyArticle`）及 Open Graph / Twitter Card 元数据；头像以 `avatar.webp`（约 11 KB）替代近 2 MB 原图，首屏更轻快。
- **署名与联络**：对外邮箱统一使用 Gmail（`liangshuo0111@gmail.com`），发表署名统一使用 `Shuo Liang`；`RA-Bench` 审稿期间标注为 `Submitted to ICLR 2027`。
