---
# Leave the homepage title empty to use the site title
title: ''
date: 2023-11-14
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: About Me
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  # - block: skills
  #   content:
  #     title: Skills
  #     text: ''
  #     # Choose a user to display skills from (a folder name within `content/authors/`)
  #     username: admin
  #   design:
  #     columns: '1'
  # - block: experience
  #   content:
  #     title: Experience
  #     # Date format for experience
  #     #   Refer to https://docs.hugoblox.com/customization/#date-format
  #     date_format: Jan 2006
  #     # Experiences.
  #     #   Add/remove as many `experience` items below as you like.
  #     #   Required fields are `title`, `company`, and `date_start`.
  #     #   Leave `date_end` empty if it's your current employer.
  #     #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
  #     items:
  #       - title: CEO
  #         company: GenCoin
  #         company_url: ''
  #         company_logo: org-gc
  #         location: California
  #         date_start: '2021-01-01'
  #         date_end: ''
  #         description: |2-
  #             Responsibilities include:

  #             * Analysing
  #             * Modelling
  #             * Deploying
  #       - title: Professor of Semiconductor Physics
  #         company: University X
  #         company_url: ''
  #         company_logo: org-x
  #         location: California
  #         date_start: '2016-01-01'
  #         date_end: '2020-12-31'
  #         description: Taught electronic engineering and researched semiconductor physics.
  #   design:
  #     columns: '2'
  # - block: accomplishments
  #   content:
  #     # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
  #     title: 'Accomplish&shy;ments'
  #     subtitle:
  #     # Date format: https://docs.hugoblox.com/customization/#date-format
  #     date_format: Jan 2006
  #     # Accomplishments.
  #     #   Add/remove as many `item` blocks below as you like.
  #     #   `title`, `organization`, and `date_start` are the required parameters.
  #     #   Leave other parameters empty if not required.
  #     #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
  #     items:
  #       - certificate_url: https://www.coursera.org
  #         date_end: ''
  #         date_start: '2021-01-25'
  #         description: ''
  #         icon: coursera
  #         organization: Coursera
  #         organization_url: https://www.coursera.org
  #         title: Neural Networks and Deep Learning
  #         url: ''
  #       - certificate_url: https://www.edx.org
  #         date_end: ''
  #         date_start: '2021-01-01'
  #         description: Formulated informed blockchain models, hypotheses, and use cases.
  #         icon: edx
  #         organization: edX
  #         organization_url: https://www.edx.org
  #         title: Blockchain Fundamentals
  #         url: https://www.edx.org/professional-certificate/uc-berkeleyx-blockchain-fundamentals
  #       - certificate_url: https://www.datacamp.com
  #         date_end: '2020-12-21'
  #         date_start: '2020-07-01'
  #         description: ''
  #         icon: datacamp
  #         organization: DataCamp
  #         organization_url: https://www.datacamp.com
  #         title: 'Object-Oriented Programming in R'
  #         url: ''
  #   design:
  #     columns: '2'
  # - block: collection
  #   id: posts
  #   content:
  #     title: Recent Posts
  #     subtitle: ''
  #     text: ''
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 5
  #     # Filter on criteria
  #     filters:
  #       folders:
  #         - post
  #       author: ""
  #       category: ""
  #       tag: ""
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ""
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: compact
  #     columns: '2'
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      # buttons:
      #   - name: All
      #     tag: '*'
      #   - name: Deep Learning
      #     tag: Deep Learning
      #   - name: Other
      #     tag: Demo
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  # - block: markdown
  #   content:
  #     title: Gallery
  #     subtitle: ''
  #     text: |-
  #       {{< gallery album="demo" >}}
  #   design:
  #     columns: '1'
  # - block: collection
  #   id: featured
  #   content:
  #     title: Featured Publications
  #     filters:
  #       folders:
  #         - publication
  #       featured_only: true
  #   design:
  #     columns: '2'
  #     view: card
  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '1'
      view: citation
  # - block: collection
  #   id: conferences
  #   content:
  #     title: Conferences and Presentations
  #     filters:
  #       folders:
  #         - event
  #   design:
  #     columns: '2'
  #     view: compact

  # text: |
  #       Edinburgh Learning and Teaching Conference, Edinburgh, June 2023 -- talk on "resources"
  #       OER23, Inverness, March 2023 -- talk on "OER"

  - block: conferences
    id: conferences
    content:
      title: Conferences and Presentations
      # Date format for experience
      #   Refer to https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2, 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Open Education Global 2023
          company:
          company_url: 'https://conference.oeglobal.org/2023/'
          company_logo: oeg-logo.svg
          location: Edmonton, Alberta, Canada
          date_start: '2023-10-16'
          date_end: '2023-10-18'
          description: |2-
            Ran an action lab (workshop) on "Reinvent the Wheel or Find the Needle? Technology for Addressing Resource Reusability Barriers".

            [Session details](https://oeglobal2023.sched.com/event/1S7jw/reinvent-the-wheel-or-find-the-needle-technology-for-addressing-resource-reusability-barriers)

            [Reflections post on SICSA blog](https://www.sicsa.ac.uk/blog/sicsa-opening-doors-for-open-education-research/)
        - title: Edinburgh Learning and Teaching Conference 2023
          company: 
          company_url: 'https://blogs.ed.ac.uk/learning-teaching-conference-2023/'
          company_logo: uoe-ltc-banner_crop.jpeg
          location: Edinburgh, Scotland
          date_start: '2023-06-27'
          date_end: '2023-06-28'
          description: |2-
            Presented short talk on "Practical approaches to freeing university material stockpiles".
            
            [Slides and recording](https://blogs.ed.ac.uk/learning-teaching-conference-2023/oak-session-3/)
        - title: CHI 23
          company:
          company_url: 'https://chi2023.acm.org/'
          company_logo: chi_logo-192x192.webp
          location: Hamburg, Germany (attended online)
          date_start: '2023-04-23'
          date_end: '2023-04-28'
          description: |2-
            Supported presentation on new co-authored paper [‘You are you and the app. There’s nobody else.’ Building Worker-Designed Data Institutions within Platform Hegemony](https://doi.org/10.1145/3544548.3581114)

            [Easy read summary on Kudos ACM Showcase](https://www.growkudos.com/publications/10.1145%25252F3544548.3581114/reader)
        - title: Open Educational Resources 23
          company: 
          company_url: 'https://altc.alt.ac.uk/oer23/'
          company_logo: OER23-logo-4.png
          location: Inverness, Scotland
          date_start: '2023-04-03'
          date_end: '2023-04-07'
          description: |2-
            Presented work-in-progress findings on "Practical approaches to freeing university material stockpiles".

            [Recording](https://www.youtube.com/watch?v=332nDZkAN5o&list=PLxoWy14N6f8tB1sudj4Lof0bwq5Mzjwdk&index=32)

            [Reflections post on GO-GN blog](https://go-gn.net/seminar/oer23-reflections-vidminas-vizgirda/)
        - title: Open Educational Resources 22
          company:
          company_url: https://web.archive.org/web/20220314133554/https://altc.alt.ac.uk/oer22/
          company_logo: OER22_0.jpg
          location: London, England,
          date_start: '2023-04-26'
          date_end: '2023-04-28'
          description: |2-
            Presented "Learning resource hide and seek" in lightning talks round

            [Reflections post on GO-GN blog](https://go-gn.net/gogn/go-gn-workshop-and-oer22/)
    design:
      columns: '2'
      view: 'compact'
  - block: tag_cloud
    content:
      title: Popular Topics
    design:
      columns: '2'
  # - block: contact
  #   id: contact
  #   content:
  #     title: Contact
  #     subtitle:
  #     text: |-
  #       Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam mi diam, venenatis ut magna et, vehicula efficitur enim.
  #     # Contact (add or remove contact options as necessary)
  #     email: test@example.org
  #     phone: 888 888 88 88
  #     appointment_url: 'https://calendly.com'
  #     address:
  #       street: 450 Serra Mall
  #       city: Stanford
  #       region: CA
  #       postcode: '94305'
  #       country: United States
  #       country_code: US
  #     directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
  #     office_hours:
  #       - 'Monday 10:00 to 13:00'
  #       - 'Wednesday 09:00 to 10:00'
  #     # Choose a map provider in `params.yaml` to show a map from these coordinates
  #     coordinates:
  #       latitude: '37.4275'
  #       longitude: '-122.1697'  
  #     contact_links:
  #       - icon: twitter
  #         icon_pack: fab
  #         name: DM Me
  #         link: 'https://twitter.com/Twitter'
  #       - icon: skype
  #         icon_pack: fab
  #         name: Skype Me
  #         link: 'skype:echo123?call'
  #       - icon: video
  #         icon_pack: fas
  #         name: Zoom Me
  #         link: 'https://zoom.com'
  #     # Automatically link email and phone or display as text?
  #     autolink: true
  #     # Email form provider
  #     form:
  #       provider: netlify
  #       formspree:
  #         id:
  #       netlify:
  #         # Enable CAPTCHA challenge to reduce spam?
  #         captcha: false
  #   design:
  #     columns: '2'
---
