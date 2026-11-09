---
title: ''
date: 2025-10-29
type: landing

design:
  spacing: '1rem'

sections:
  - block: resume-biography-custom
    id: author-bio
    content:
      username: "admin"
      text: ''
      button:
        text: 下载简历
        url: /uploads/%E6%88%B4%E4%BD%B3%E4%BC%B6_CV_homepage.pdf
      headings:
        about: '关于我'
        education: '教育经历'
        interests: '研究兴趣'
    design:
      css_class: hbx-bg-gradient
      avatar:
        size: large
        shape: circle
      spacing:
        padding: ['3rem', '0', '3rem', '0']

  - block: collection-custom
    id: papers
    content:
      title: 代表性成果
      custom_sort: true
      filters:
        featured_only: true
        folders:
          - publications
      archive:
        enable: true
        text: 查看全部论文
    design:
      view: citation
      columns: '1'

  - block: page-summary-custom
    id: research-themes
    content:
      page: /research-themes
      link_text: 查看研究主题

  - block: service-custom
    id: service
    content:
      username: admin
      title: 学术服务与交流

  - block: awards-home
    id: awards
    content:
      username: admin
      title: 主要荣誉

  - block: contact-custom
    id: contact
    content:
      username: admin
      title: 联系方式
      text: 欢迎对计算建模、优化算法或智能决策感兴趣的同行与我联系，一起探讨研究问题、开展合作。
      status:
        - icon: hero/map-pin
          text: 中央财经大学
---
