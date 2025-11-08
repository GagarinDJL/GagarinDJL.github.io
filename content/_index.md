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
        url: uploads/CV-Lynn.pdf
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
      title: Publications
      custom_sort: true  # 启用自定义排序
      filters:
        folders:
          - publications
    design:
      view: citation
      columns: '1'

  - block: projects-home
    id: projects
    content:
      title: Applied Projects
      subtitle: "Selected case studies"
      projects:
        - title: Safety Violation Analytics for Power-Grid Construction
          role: Student Project Coordinator
          institution: UCAS × State Grid Henan EPRI
          period: 2022.10–2022.12
          description: Led a 6-member student team under faculty supervision to build a taxonomy and labeled dataset (~1.5k cases), perform association and clustering analyses, and draft targeted management measures.
        
        - title: "Accident-Tree Modeling: Methods and Applications"
          role: Student Co-Lead (under faculty supervision)
          institution: Department of Emergency Management
          period: 2022.05–2023.04
          description: Developed a hazard root-tracing ("source tree") method based on fault-tree analysis; completed case studies and authored substantial sections of the final report.

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
      title: Skills & Hobbies
      username: admin
      courses_can_teach: "Data Mining & Analytics · Machine Learning · Network Science / Social Network Analysis · Optimization / Operations Research · Algorithms & Data Structures · Python for Data Science"
    
  - block: contact-custom
    id: contact
    content:
      username: admin
      title: Contact
      status:
        - icon: hero/map-pin
          text: Currently Visiting at UT Dallas
        - icon: hero/user-group
          text: Open to Collaboration


---
