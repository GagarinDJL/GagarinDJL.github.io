---
title: 'Projects'
date: 2024-05-19
type: landing

design:
  # Section spacing
  spacing: '5rem'

# Page sections
sections:
  - block: collection
    id: projects
    content:
      title: "Applied Projects"
      subtitle: "Selected case studies"
      # 抓取来源（可二选一——推荐 folders）
      # page_type: project         # 如果你的项目 content 使用 type = "project"
      filters:
        folders: ["projects"]       # 读取 content/project/ 下的内容
        featured_only: true        # 只显示你标记了 featured: true 的条目
        exclude_future: true
        exclude_past: false
      count: 2                     # 只展示 2 条
      sort_by: "Date"
      sort_ascending: false
      archive:
        enable: false              # 不显示 “See all”
    design:
      view: article-grid                      
      # card | citation | article-grid | date-title-summary
      columns: 2
---