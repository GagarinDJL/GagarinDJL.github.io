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

  - block: page-summary-custom
    id: research-themes
    content:
      page: /research-themes
      link_text: Explore research themes

  - block: service-custom
    id: service
    content:
      username: admin
      title: Academic Service and Exchange
        
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
