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
        text: 下载 CV
        url: /uploads/cv-lynn-zh.pdf
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
        - title: 电网建设安全违规数据分析
          role: 学生项目负责人
          institution: 中国科学院大学 × 国网河南电力科学研究院
          period: 2022.10-2022.12
          description: 在教师指导下带领 6 人团队，构建安全违规分类体系与约 1500 条标注数据，开展关联分析和聚类分析，并提出针对性管理建议。

        - title: "事故树建模：方法与应用"
          role: 学生联合负责人（教师指导）
          institution: 应急管理相关课题
          period: 2022.05-2023.04
          description: 基于故障树分析方法提出危险源追溯的“源树”建模思路，完成案例研究，并参与结题报告核心章节写作。

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
      courses_can_teach: "数据挖掘与分析 · 机器学习 · 网络科学 / 社会网络分析 · 优化 / 运筹学 · 算法与数据结构 · Python 数据科学"

  - block: contact-custom
    id: contact
    content:
      username: admin
      title: 联系方式
      status:
        - icon: hero/map-pin
          text: 2025.01-2026.01 访问 UT Dallas
        - icon: hero/user-group
          text: 寻求博士后、师资博士后、青年教师/科研岗位与合作机会
---
