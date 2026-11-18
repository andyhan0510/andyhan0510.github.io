# Xuzheng (Andy) Han 个人学术网站

纯静态网站（HTML + CSS），不需要 Jekyll 或任何构建工具，可直接部署到 GitHub Pages。

## 文件结构（分页，参考 AcademicPages 的布局）
| 页面 | 文件 | 内容 |
|---|---|---|
| About（首页） | `index.html` | 个人简介、研究兴趣、Current Research、News |
| Publications | `publications.html` | 期刊论文、在写论文 |
| Talks | `talks.html` | 会议报告 |
| Projects | `projects.html` | 项目列表（按时间倒序，每项有标题、日期、一句话简介、封面图） |
| 项目详情 | `projects/*.html` | 每个项目一页：背景方法、关键发现、意义、工具、相关论文 |
| CV | `cv.html` | 教育、工作经历、研究经历、论文、会议报告、技能、PDF 下载 |

- `assets/style.css`：所有页面共用的样式
- `assets/profile.jpg`：头像照片
- `assets/figures/`：Projects 页面用的论文插图（来自博士和硕士论文）
- `assets/Xuzheng_Han_CV.pdf`：公开版简历（已去掉电话号码）
- `.nojekyll`：告诉 GitHub Pages 不要用 Jekyll 处理

## 本地预览
直接双击文件夹里的 `index.html`，用浏览器打开即可，点导航栏可以切换页面。

## 部署到 GitHub Pages（约 5 分钟）
1. 登录 GitHub，新建一个公开仓库，名字必须是 `你的用户名.github.io`（例如 `xuzhenghan.github.io`）。
2. 在仓库页面点 **Add file → Upload files**，把本文件夹里的 5 个 `.html` 文件、`projects/` 文件夹、`assets/` 文件夹、`README.md` 和 `.nojekyll`一起拖进去，点 **Commit changes**。
   （Mac 上 `.nojekyll` 是隐藏文件，在 Finder 里按 `Cmd + Shift + .` 显示。）
3. 打开 **Settings → Pages**，Source 选 **Deploy from a branch**，Branch 选 `main` / `(root)`，保存。
4. 1–2 分钟后访问 `https://你的用户名.github.io`。

## 以后怎么修改（不用装任何软件）
1. 打开你的仓库页面，点要改的页面文件，再点右上角的 ✏️（Edit this file）：
   - 加新闻 / 改简介 → `index.html`，在 `<ul class="news">` 下面复制一行 `<li>…</li>`，改日期和文字。
   - 加论文 → `publications.html`，在 `<ol class="pubs">` 里复制一个 `<li>…</li>`，改作者、题目、期刊。
   - 加会议报告 → `talks.html`；改教育/技能 → `cv.html`。
   - 加项目 → 在 `projects.html` 复制一个 `<article class="pf-item">…</article>`，再复制 `projects/` 里任意一个详情页改内容和文件名。
2. 侧边栏（照片、邮箱、Scholar、ORCID）在每个页面里都有一份，改的话 5 个文件都要改一下。
   - 论文发表后：把它从 "Manuscripts in Preparation" 移到 "Peer-Reviewed Journal Articles"。
3. 点右上角 **Commit changes…** → 再点 **Commit changes**。1–2 分钟后网站自动更新（浏览器可按 `Cmd + Shift + R` 强制刷新）。
4. 替换文件（新版 CV PDF、照片）：进入 `assets` 文件夹 → **Add file → Upload files**，上传**同名文件**会直接覆盖。

提示：每次修改 GitHub 都会保留历史版本，改坏了可以在 **History** 里找回。

## 可选补充
- 有 DOI 后，可把论文旁的 Scholar 搜索链接改为 `https://doi.org/...`。
- 有 LinkedIn / ResearchGate 时，在侧边栏注释里填入链接并取消注释。
- 照片目前是 128×128 像素，换一张更大（至少 400×400）的正方形照片会更清晰，存为 `assets/profile.jpg` 覆盖即可。
