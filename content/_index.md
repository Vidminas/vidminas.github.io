---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3
    id: about
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ''
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      # Use the new Gradient Mesh which automatically adapts to the selected theme colors
      background:
        gradient_mesh:
          enable: false

      spacing:
        padding: [0, 0, 0, 0]

      # Name heading sizing to accommodate long or short names
      name:
        size: sm # Options: xs, sm, md, lg (default), xl

      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded

      biography:
        style: "max-width: 100%;"
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - projects
    design:
      columns: 2
      animations: false
      spacing:
        padding: [0, 0, 0, 0]
  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: |-
        > [!NOTE]
        > Quickly discover relevant content by [filtering publications](./publications/).
      filters:
        folders:
          - publications
        exclude_featured: true
    design:
      columns: '1'
      view: citation
      spacing:
        padding: [0, 0, 0, 0]
  - block: collection
    id: conferences
    content:
      title: Conference Presentations
      filters:
        folders:
          - events
    design:
      columns: '1'
      view: event-row
      spacing:
        padding: [0, 0, 0, 0]
  - block: markdown
    id: topics
    content:
      title: Popular Topics
      text: |-
        Browse all posts by topic on the [tags page](./tags/).
    design:
      columns: '1'
      spacing:
        padding: [0, 0, 0, 0]
---
