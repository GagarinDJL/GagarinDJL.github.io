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
        interests: 'Interests'
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
      title: Selected Research Work
      custom_sort: true  # 启用自定义排序
      count: 6
      filters:
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
      title: Applied Projects
      subtitle: "Selected case studies"
      projects:
        - title: Risk and Safety Analytics for Power-Grid Construction
          role: Project Lead
          institution: UCAS × State Grid Henan EPRI
          period: 2022.10–2022.12
          description: Led a 6-member team to build a safety-violation taxonomy and 1,498-case labeled dataset, conduct association and clustering analyses, and translate data patterns into targeted management recommendations.
        
        - title: "Hazard-Source Tracing with Fault-Tree Modeling"
          role: Research Co-Lead
          institution: Department of Emergency Management
          period: 2022.05–2023.04
          description: Developed a hazard-source tracing method based on fault-tree analysis, completed multi-case studies, and contributed major sections to the final report.

  - block: service-custom
    id: service
    content:
      username: admin
      title: Service
        
  - block: awards-home
    id: awards
    content:
      username: admin
      title: Awards & Honors

  - block: resume-skills-custom
    id: skills
    content:
      title: Skills & Teaching
      username: admin
      courses_can_teach: "Data Structures & Algorithms · Data Mining & Machine Learning · Computational Modeling · Optimization / Operations Research · Decision Modeling for Management · Python for Data Science"
    
  - block: contact-custom
    id: contact
    content:
      username: admin
      title: Contact
      status:
        - icon: hero/map-pin
          text: Former visiting researcher at UT Dallas, Jan. 2025-Jan. 2026
        - icon: hero/user-group
          text: Seeking postdoctoral and research fellow opportunities


---
