# Hugo Blox 主题自定义指南

> 快速参考：如何自定义本项目的Hugo Blox主题
> 
> 最后更新：2025年10月28日

---
官方说明： https://docs.hugoblox.com/reference/extend/

## 自定义的核心原则

### 1. 统一使用Block模式

本项目**100%采用Block模式**进行自定义：
- 新建Block：使用 `-custom` 后缀（如 `publications-custom`）
- 覆盖Block：保持原名（如 `resume-biography-3`）

### 2. CSS管理策略：Tailwind优先

```
Tailwind类（90%） > Block内嵌<style>（10%） > custom.css（全局共享）
```

**决策规则：**
- 简单样式（padding, margin, color等） → Tailwind类
- 复杂样式（伪元素、:has()、counter、动画） → Block内
- 跨Block共享 → custom.css

---

## 创建新Block（推荐方法）

### 步骤1：找到主题Block模板

**主题Block位置：**
```bash
~/Library/Caches/hugo_cache/modules/filecache/modules/pkg/mod/github.com/!hugo!blox/hugo-blox-builder/modules/blox-tailwind@v0.0.0-20250925205154-e9b31f8090c0/blox/
```

**常用模板：**
- `resume-biography-3/` - 个人简介（头像、教育、兴趣）
- `resume-experience/` - 时间线展示
- `markdown/` - 简单内容展示
- `collection/` - 列表展示（论文、项目等）

### 步骤2：复制并重命名

```bash
# 复制主题Block模板到项目
cd ~/Documents/PycharmProjects/personal-site
mkdir -p layouts/partials/hbx/blocks/your-block-custom/
cp ~/Library/Caches/.../blox/resume-biography-3/block.html \
   layouts/partials/hbx/blocks/your-block-custom/block.html
```

### 步骤3：修改Block

在 `layouts/partials/hbx/blocks/your-block-custom/block.html` 中：
1. **样式和逻辑定义** - HTML结构和Tailwind类
2. **使用Tailwind类** - 定义简单样式
3. **复杂CSS** - 仅在必要时添加`<style>`标签（文件末尾）
4. **数据来源** - 从 `.content` 等参数读取数据，**不硬编码文本内容**

**关键原则：Block = 样式容器 + 逻辑处理，文本内容在相关 `.md` 中定义**

示例对比：

❌ **错误** - 文本硬编码在 block.html：
```html
<!-- block.html 中不应该这样做 -->
<h3>Contact</h3>
<p>Email: example@example.com</p>
```

✅ **正确** - Block 接收 content 参数中的文本：
```html
<!-- block.html 中的做法 -->
<div class="section-content">
  {{ with .content.title }}
    <h3>{{ . }}</h3>
  {{ end }}
  {{ with .content.text }}
    {{ . | markdownify }}
  {{ end }}
</div>
```

```yaml
# _index.md 中的做法
- block: contact-custom
  id: contact
  content:
    title: 'Contact'
    text: |
      **Email:** example@example.com
      
      **Links:** [GitHub](https://github.com) · [ORCID](https://orcid.org)
```

---

## ChatGPT提示词模板

### 创建新Block时：

```
我需要在Hugo Blox主题中创建自定义Block。

项目信息：
- 主题：Hugo Blox Builder (Tailwind版本)
- Block位置：layouts/partials/hbx/blocks/xxx-custom/block.html

CSS规则：
1. 优先使用Tailwind类（90%）
2. 复杂样式用<style>标签（伪元素、:has()、counter、动画）
3. Block内嵌CSS写在文件末尾

请从[模板名]复制并重命名，使用Tailwind优先。
```
---

## Icon 图库说明

### 主题 Icon 库位置

所有可用的 icon 数据文件存放在：

```
~/Library/Caches/hugo_cache/modules/filecache/modules/pkg/mod/github.com/!hugo!blox/hugo-blox-builder/modules/blox-tailwind@v0.0.0-20250925205154-e9b31f8090c0/data/icons/
```

### 可用的 Icon 库（5 个）

| Icon 库 | 文件名 | 图标数量 | 说明 | 前缀示例 |
|--------|--------|---------|------|---------|
| **HeroIcons** | hero.json | 885+ | 通用设计图标库，最常用 | `hero/trophy`, `hero/academic-cap`, `hero/star` |
| **Academicons** | academicons.js | 100+ | 学术相关图标 | `academicons/google-scholar`, `academicons/orcid` |
| **Brands** | brands.yaml | 100+ | 社交媒体、品牌图标 | `brands/github`, `brands/twitter`, `brands/linkedin` |
| **DevIcon** | devicon.json | 300+ | 开发工具、编程语言图标 | 用于技能展示 |
| **Hugo Blox** | hb.yaml | 20+ | Hugo Blox 主题专属图标 | `at-symbol`, `circle-stack` |

### 使用方法

在 frontmatter 的 `icon:` 字段中使用 icon 库的图标，格式为：

```yaml
# 使用 HeroIcons（最常用）
icon: hero/trophy
icon: hero/academic-cap
icon: hero/sparkles

# 使用 Academicons
icon: academicons/google-scholar
icon: academicons/orcid

# 使用 Brands
icon: brands/github
icon: brands/twitter

# 使用 Hugo Blox 库
icon: at-symbol
icon: circle-stack
```

### 获取完整图标列表

- **HeroIcons 官方库**：https://heroicons.com
- **Academicons**：https://jpswalsh.github.io/academicons/
- **Font Awesome Brands**：https://fontawesome.com/icons?d=gallery&s=brands

---

## 原始主题Collection Block 使用说明

Collection Block 是一个功能强大的内容展示工具，用于以美观的方式组织和过滤你的内容（博客文章、论文、项目等）。

### 核心特性

- **智能过滤**：按文件夹、标签、分类、作者、发布类型等过滤
- **灵活排序**：按日期、标题或自定义字段升序或降序排序
- **多种视图**：支持卡片、紧凑、展示、引用、列表、砌体等多种布局
- **分页支持**：内置分页和项目数限制
- **自动存档链接**："查看全部" 链接到完整存档页面

### 基本配置

```yaml
- block: collection
  id: papers
  content:
    title: Publications              # Block 标题
    filters:
      folders:                        # 指定内容文件夹
        - publications
    count: 0                          # 显示的项目数（0 = 全部）
    offset: 0                         # 偏移量
    sort_by: Date                     # 排序字段（Date、Title等）
    sort_ascending: false             # 升序（true）或降序（false）
  design:
    view: citation                    # 视图类型
    columns: '1'                      # 列数
```

### 过滤选项

```yaml
filters:
  folders:                    # 按内容文件夹过滤
    - publications
  tags:                       # 按标签过滤（多个标签取并集）
    - machine-learning
    - optimization
  tag: machine-learning       # 单个标签过滤
  category: research          # 按分类过滤
  publication_type: journal   # 按发布类型过滤
  author: admin               # 按作者过滤
  featured_only: true         # 仅显示标记为特色的项目
  exclude_featured: true      # 排除特色项目
  exclude_past: true          # 排除过去的日期
  exclude_future: true        # 排除未来的日期
  kinds:                      # Hugo 页面类型
    - page
    - section
```

### 支持的视图类型

| 视图 | 说明 | 适用场景 |
|------|------|---------|
| `card` | 卡片布局，显示摘要和图片 | 博客文章、项目展示 |
| `citation` | 学术引用格式 | 论文、出版物 |
| `article-grid` | 网格布局 | 快速浏览多条内容 |
| `date-title-summary` | 日期+标题+摘要 | 新闻、事件列表 |

### 排序选项

```yaml
sort_by: Date              # 按发布日期排序
sort_by: Title             # 按标题排序
sort_by: Published         # 按发布时间排序
sort_ascending: false      # 降序（最新优先）
sort_ascending: true       # 升序（最旧优先）
```

### 使用示例

**示例1：首页展示最新论文（引用格式）**
```yaml
- block: collection
  id: papers
  content:
    title: Publications
    filters:
      folders:
        - publications
    count: 5                # 只显示最新5篇
    sort_by: Date
    sort_ascending: false
  design:
    view: citation
    columns: '1'
```

**示例2：按标签过滤的博客列表**
```yaml
- block: collection
  id: blog
  content:
    title: Machine Learning Posts
    filters:
      folders:
        - blog
      tags:
        - machine-learning
    sort_by: Date
    sort_ascending: false
  design:
    view: card
    columns: '2'
```

**示例3：特色项目展示**
```yaml
- block: collection
  id: projects
  content:
    title: Featured Projects
    filters:
      folders:
        - projects
      featured_only: true
  design:
    view: article-grid
    columns: '3'
```

### 存档页面配置

```yaml
archive:
  enable: true                        # 是否显示"查看全部"链接
  text: "See All Publications"         # 链接文本
  link: "/publications/"              # 自定义链接（可选）
```

### 自定义排序

如果需要自定义排序（如 `_index.md` 中的 `custom_sort: true`），可以在 content 中添加 `order` 字段来控制顺序。

---

## 本项目自定义Block清单

| Block | 用途 | 路径 | 数据源 |
|-------|------|------|--------|
| `resume-biography-custom` | 首页个人简介 | `layouts/partials/hbx/blocks/resume-biography-custom/block.html` | `_index.md` content |
| `education-custom` | 教育背景详情页 | `layouts/partials/hbx/blocks/education-custom/block.html` | `content/authors/admin/_index.md` |
| `publications-custom` | 论文列表 | `layouts/partials/hbx/blocks/publications-custom/block.html` | 文件夹中的 markdown 文件 |
| `projects-home` | 应用项目展示（首页） | `layouts/partials/hbx/blocks/projects-home/block.html` | `_index.md` content |
| `service-custom` | 学术服务 | `layouts/partials/hbx/blocks/service-custom/block.html` | `content/authors/admin/_index.md` |
| `awards-home` | 奖项展示（首页） | `layouts/partials/hbx/blocks/awards-home/block.html` | `content/authors/admin/_index.md` |
| `awards-detailed` | 奖项展示（详情页） | `layouts/partials/hbx/blocks/awards-detailed/block.html` | `content/authors/admin/_index.md` |
| `collection` | 内容集合展示 | 主题自带 | 文件夹中的 markdown 文件 |
| `contact-custom` | 联系信息 | `layouts/partials/hbx/blocks/contact-custom/block.html` | `_index.md` content |
| `back-to-home` | 返回首页按钮 | `layouts/partials/hbx/blocks/back-to-home/block.html` | 内置 |

**命名规则：新建Block添加 `-custom` 后缀**

**核心理念：Block 是样式容器，数据在 `_index.md` 或文件 frontmatter 中定义**

---

## 最佳实践

1. **分离关注点** - Block 定义样式和逻辑，文本内容在 `_index.md` 中定义
2. **复制模板** - 从主题Block复制，不从零开始
3. **Tailwind优先** - 90%样式用Tailwind类
4. **Block自包含** - 复杂CSS写在block.html末尾
5. **清晰命名** - 使用 `-custom` 后缀
6. **深色模式** - 始终定义 `dark:` 变体

**数据流向：**
```
_index.md (内容数据) → block.html (样式容器) → 渲染结果
```
