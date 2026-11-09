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

  - block: projects-home
    id: projects
    content:
      title: 学术交流
      projects:
        - title: "中国科技发展基金会“2025 国际青年伙伴计划”"
          show_on_site: true
          show_on_homepage: true
          role: 项目申报与执行负责人
          institution: 中国科技发展基金会
          period: 2025.12–2026.05
          description: 在项目资助下，组织马萨诸塞大学波士顿分校 Hongmin（William）Du 博士访问中国科学院大学五天，围绕大语言模型、网络安全信息披露及数据驱动的风险分析开展学术报告与研讨。

        - title: 电网施工安全违规数据分析：风险识别、案例标注与管理决策
          show_on_site: false
          show_on_homepage: false
          role: 学生项目负责人
          institution: 中国科学院大学 × 国网河南电力科学研究院
          period: 2022.10–2022.12
          description: 在教师指导下带领 6 人团队，构建安全违规分类体系与 1,498 条标注案例数据，开展关联分析和聚类分析，并将数据模式转化为面向施工安全治理的管理建议。

        - title: "事故树建模与风险源追溯：方法构建与案例应用"
          show_on_site: false
          show_on_homepage: false
          role: 学生联合负责人（教师指导）
          institution: 应急管理相关课题
          period: 2022.05–2023.04
          description: 基于故障树分析方法提出危险源追溯的“源树”建模思路，完成多案例研究，并参与结题报告核心章节写作。

  - block: service-custom
    id: service
    content:
      username: admin
      title: 学术服务

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
      status:
        - icon: hero/map-pin
          text: 中央财经大学
---
