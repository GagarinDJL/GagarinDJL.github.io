---
# Leave the homepage title empty to use the site title
title: ''
date: 2025-10-29
type: landing

design:
  # Default section spacing
  spacing: '1rem'

sections:
# Display the author biography/skills from `content/authors/admin/_index.md` on the homepage
  - block: resume-biography-custom
    id: author-bio
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: "admin"
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: /uploads/CV-Jialing-Dai-English_homepage.pdf
      headings:
        about: 'About Me'
        education: 'Education'
        interests: 'Research Interests'
    design:
      # Apply a gradient background
      css_class: hbx-bg-gradient
      # Avatar customization
      avatar:
        size: large # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
      spacing:
        padding: ['3rem', '0', '3rem', '0']
   
  - block: collection-custom  # 使用自定义版本
    id: papers
    content:
      title: Selected Publications
      custom_sort: true  # 启用自定义排序
      filters:
        featured_only: true
        folders:
          - publications
      archive:
        enable: true
        text: View all publications
    design:
      view: citation
      columns: '1'

  - block: projects-home
    id: projects
    content:
      title: Academic Exchange
      projects:
        - title: "2025 International Young Partners Program"
          show_on_site: true
          show_on_homepage: true
          role: Proposal and project lead
          institution: Foundation for the Development of Science and Technology in China
          period: 2025.12–2026.05
          description: Led a funded exchange with the University of Massachusetts Boston. Dr. Hongmin (William) Du visited the University of Chinese Academy of Sciences for five days for seminars and discussions on large language models, cybersecurity information disclosure, and data-driven risk analysis.

        - title: Risk and Safety Analytics for Power-Grid Construction
          show_on_site: false
          show_on_homepage: false
          role: Student Team Lead
          institution: UCAS × State Grid Henan EPRI
          period: 2022.10–2022.12
          description: Led a 6-member student team, under faculty supervision, to build a safety-violation taxonomy and 1,498-case labeled dataset, conduct association and clustering analyses, and translate data patterns into targeted management recommendations.
        
        - title: "Hazard-Source Tracing with Fault-Tree Modeling"
          show_on_site: false
          show_on_homepage: false
          role: Student Research Team Co-Lead
          institution: Department of Emergency Management
          period: 2022.05–2023.04
          description: Co-led the student research team under faculty supervision, developed a hazard-source tracing method based on fault-tree analysis, completed multi-case studies, and contributed major sections to the final report.

  - block: service-custom
    id: service
    content:
      username: admin
      title: Academic Service
        
  - block: awards-home
    id: awards
    content:
      username: admin
      title: Selected Honors

  - block: contact-custom
    id: contact
    content:
      username: admin
      title: Contact
      status:
        - icon: hero/map-pin
          text: Central University of Finance and Economics


---
