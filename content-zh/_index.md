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
      title: 代表性研究工作
      custom_sort: true
      count: 6
      filters:
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
      title: 应用项目
      subtitle: "代表性案例与项目"
      projects:
        - title: "中国科技发展基金会“2025 国际青年伙伴计划”"
          role: 申报与执行负责人
          institution: 中国科技发展基金会 × UMass Boston
          period: 2025.12–2026.05
          description: 主导项目申报与全流程执行，组织 UMass Boston Hongmin（William）Du 博士来华开展为期 5 天的学术交流，完成学术议程设计、报告与研讨组织及项目结项；交流主题涵盖大语言模型、网络安全信息披露与数据驱动风险分析。

        - title: 电网施工安全违规数据分析：风险识别、案例标注与管理决策
          role: 学生项目负责人
          institution: 中国科学院大学 × 国网河南电力科学研究院
          period: 2022.10-2022.12
          description: 在教师指导下带领 6 人团队，构建安全违规分类体系与 1,498 条标注案例数据，开展关联分析和聚类分析，并将数据模式转化为面向施工安全治理的管理建议。

        - title: "事故树建模与风险源追溯：方法构建与案例应用"
          role: 学生联合负责人（教师指导）
          institution: 应急管理相关课题
          period: 2022.05-2023.04
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
      title: 荣誉奖励

  - block: resume-skills-custom
    id: skills
    content:
      title: 技能与教学
      username: admin
      courses_can_teach: "数据结构与算法 · Python 数据分析 · 数据挖掘与机器学习 · 运筹学与优化方法 · 管理决策建模 · 社会网络分析 · 信息系统与数据治理 · AI 可信与智能决策"

  - block: contact-custom
    id: contact
    content:
      username: admin
      title: 联系方式
      status:
        - icon: hero/map-pin
          text: 2025.01-2026.01 曾赴美国得克萨斯大学访问研究
        - icon: hero/user-group
          text: 申请教学科研岗、师资博士后、博士后及青年科研岗位
---
