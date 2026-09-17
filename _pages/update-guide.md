---
layout: single
title: "如何更新网站内容"
permalink: /update-guide/
author_profile: false
description: "个人网站的内容维护说明：文字修改、作品添加、图片替换与发布检查。"
---

<style>
.page__content { font-size:16px; line-height:1.85; }
.page__content h2 { margin-top:2.2em; }
.update-intro { padding:1.3rem 1.5rem; background:#edf5ef; border-left:4px solid #5f9e86; border-radius:8px; margin:1.5rem 0; }
.page__content table { display:block; overflow-x:auto; font-size:14px; }
.page__content pre { overflow-x:auto; }
</style>

<div class="update-intro">
<strong>网站内容维护说明</strong><br>
本页记录这个个人网站的更新方法，便于后续持续补充个人经历、课程作业与作品。网站基于 Jekyll 与 AcademicPages 模板搭建，通过 HTML、CSS 和 Markdown 编辑内容，使用 GitHub 管理源文件，并由 GitHub Pages 发布。
</div>

## 一、在哪里修改内容

网站源代码保存在 [Lemcous.github.io 仓库](https://github.com/Lemcous/Lemcous.github.io)。目前网站有三个导航入口：“关于我”（首页）、“个人作品集”和“更新说明”。不同内容对应不同文件：

| 要更新的内容 | 对应文件或文件夹 |
| --- | --- |
| 关于我首页：个人介绍、教育、项目、实践与技能 | `index.md` |
| 个人作品集 | `_pages/works.md` |
| 网站名称、侧栏简介、邮箱和头像设置 | `_config.yml` |
| 全站顶部导航 | `_data/navigation.yml` |
| 图片素材 | `images/` |
| PDF、作品文档等附件 | `files/` |
| 本说明页面 | `_pages/update-guide.md` |

**“关于我”首页应修改根目录的 `index.md`。** 首页集中展示个人介绍、教育经历、研究与项目、实践经历和方法与技能。原“个人简历”已合并为“关于我”，旧的 `/cv/` 地址只用于跳转；不要再在 `_pages/cv.md` 中更新经历。旧的 `_pages/about.md` 已停用。联系方式修改时应检查首页与侧栏是否一致。

## 二、修改文字并发布

1. 登录拥有该仓库编辑权限的 GitHub 账号，进入仓库，确认当前分支为 `master`。
2. 打开需要修改的文件，点击编辑按钮（铅笔图标）。
3. 搜索页面中已有的文字，只替换目标内容，保留周围的 HTML 标签、样式类名及文件顶部的配置。
4. 检查修改差异，确认没有误删其他段落，点击 **Commit changes**，填写简短说明，例如“更新教育经历”并提交到发布分支。
5. 等待 GitHub Pages 完成构建与部署，再打开网站检查。保存源文件后，线上页面不会立即同步。

例如，修改首页简介时，找到对应段落：

```html
<p class="cv-hero__meta">南京大学新闻传播学院 · 数字营销传播方向</p>
```

只修改 `<p>` 与 `</p>` 之间的文字，就能保留原有排版。调整行间距可修改对应 CSS 的 `line-height`，调整区块间距可修改 `margin` 或 `padding`。

## 三、更新“关于我”与“个人作品集”

**更新“关于我”：** 打开 `index.md`，找到“教育经历”“研究与项目”、“实践经历”或“方法与技能”等对应区域，修改学校、时间、职责和成果。新增经历时，可复制同一区域已有的完整条目，再替换文字，保留成对的标签。

**更新“个人作品集”：** 先把 PDF 或图片上传到 `files/` 或 `images/`，再编辑 `_pages/works.md`。当前作品集有“作品整理中”的占位区域，可将该区域替换为实际作品。每件作品建议说明名称、时间、背景、个人职责和成果，并附上可访问的链接。

下面是可放入作品集内容区域的示例；文件名、文字和日期需要替换为实际信息：

```html
<section class="cv-section">
  <h2 class="cv-section__title">作品名称</h2>
  <p>完成时间：填写实际年月</p>
  <p>项目背景：介绍任务、受众与目标。</p>
  <p>我的职责：说明本人承担的工作。</p>
  <p>作品成果：概括产出、发现或收获。</p>
  <a href="/files/project-report.pdf">查看作品 PDF</a>
</section>
```

如果也希望在首页介绍该项目，可以在 `index.md` 的“研究与项目”区域添加对应经历。

## 四、上传和替换图片

1. 在仓库中进入 `images/`，使用 **Add file → Upload files** 上传图片并提交。
2. 文件名尽量简短清楚，例如 `campus-photo.jpg`，注意大小写和扩展名保持一致。
3. 在页面对应位置使用图片路径，并写明图片描述：

```html
<img src="/images/campus-photo.jpg"
     alt="校园活动摄影作品"
     style="max-width:100%;height:auto;">
```

替换图片时，可以上传新文件并修改页面引用路径。“关于我”和“个人作品集”的侧栏头像由 `_config.yml` 中的 `author.avatar` 设置，填写 `images/` 文件夹内的图片文件名；“更新说明”页面不显示侧栏。作品正文中的图片需在对应页面文件中单独检查和替换。

上传前适当压缩大图片，避免页面加载过慢；图片应使用本人作品或已获授权的素材。

## 五、新增一个页面

在 `_pages/` 中创建 Markdown 文件，例如 `new-project.md`，在文件最上方写入以下配置，再添加正文：

```markdown
---
layout: single
title: "新项目"
permalink: /new-project/
author_profile: false
---

## 项目介绍

在这里填写项目内容。
```

其中，`title` 是页面标题，`permalink` 是页面网址路径。每个新页面应使用独立路径，不要重复使用首页的 `/`、作品集的 `/works/` 或说明页的 `/update-guide/`。

如需把新页面放进顶部导航，在 `_data/navigation.yml` 的 `main:` 下添加条目，并保持与已有条目相同的缩进：

```yaml
  - title: "新项目"
    url: /new-project/
```

首页、作品集与更新说明使用同一份导航配置，更新后会同步生效。

## 六、发布后如何检查

每次更新后，检查以下事项：

- **文字：** 姓名、学校、日期、联系方式准确，删除不再需要的占位文字。
- **图片和附件：** 图片正常显示，作品与 PDF 链接可以打开。
- **排版：** 在电脑和手机宽度下检查换行、行间距、导航与图片比例。
- **页面入口：** “关于我”“个人作品集”“更新说明”及新增页面之间能正常跳转，旧的 `/cv/` 链接能返回“关于我”。
- **发布状态：** 在仓库的 Actions 中查看 Pages 构建与部署记录；必要时在 Settings → Pages 检查发布来源。

如果线上页面仍显示旧内容，先确认提交已保存、部署已完成，再尝试强制刷新或使用无痕窗口检查。若出现构建失败，应打开失败记录查看具体文件和错误位置，优先检查文件顶部配置、YAML 缩进及未闭合标签。

## 七、如何恢复误改内容

GitHub 会保留每次提交记录。发现误改时，可以打开文件的 **History**，查看修改前的版本，将需要恢复的内容复制到当前文件后重新提交。这样既能恢复页面，也能保留更新过程。

日常维护可遵循“修改一项 → 检查差异 → 提交说明 → 查看部署 → 检查网页”的顺序。完成新的课程作业、项目或实践后，及时补充作品和经历，让个人网站持续保持更新。

---

[关于我](/) · [个人作品集](/works/)
