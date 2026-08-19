---
title: "Gig workers' personal data on the decentralised web"
summary: Two research internships with the EWADA team at the University of Oxford
tags:
  - Decentralised Web
  - Personal Data
  - Participatory Research
  - AI
  - Python
date: '2023-09-01T00:00:00Z'
links:
  - type: site
    label: EWADA project
    url: https://www.oxfordmartin.ox.ac.uk/ethical-web-and-data-architectures/
  - type: code
    label: chatdocs-streamlit
    url: https://github.com/Vidminas/chatdocs-streamlit
---

Over two research internships -- August to November 2022, and July to September 2023 -- I worked with the [Human Centred Computing group](https://www.cs.ox.ac.uk/research/HCC/) in the Department of Computer Science at the University of Oxford, on the Oxford Martin School's [EWADA](https://www.oxfordmartin.ox.ac.uk/ethical-web-and-data-architectures/) (Ethical Web and Data Architectures in the Age of AI) project.

The question we worked on was how gig workers -- Uber drivers, Amazon workers, Deliveroo riders -- might take control of, and make better use of, their personal and work data in a setting shaped by platform power.

## Worker-led data sharing

The first internship was a participatory design study: user interviews and co-design exercises about gig worker-led data sharing initiatives, with workers and the organisations that support them. I conducted some of the interviews, coded them, and analysed the findings to outline potential sociotechnical models for platforms.

The resulting paper examines how researchers might empower gig workers to steer how web decentralisation gets implemented in platform work, rather than having it done to them. It was published at CHI 2023: [‘You are you and the app. There's nobody else.': Building Worker-Designed Data Institutions within Platform Hegemony](https://doi.org/10.1145/3544548.3581114).

## Decentralised generative AI

The second internship was technical: designing, building, and evaluating app prototypes using [Solid](https://solidproject.org/), the Social Linked Data protocol. Gig workers can request their data from platforms under GDPR subject access requests, but the responses arrive in incompatible schemas and unhelpful formats. The main prototype used large language models (small enough to run locally so the data never leaves the user's control) to automatically integrate datasets with mismatched schemas, and to produce map and timeline visualisations from DSAR response data. Some of that work is open source at [chatdocs-streamlit](https://github.com/Vidminas/chatdocs-streamlit).

That line of work later led to SocialGenPod, a Solid-based architecture for privacy-friendly generative AI applications: user data -- chat history, app configuration, personal documents -- stays in the user's own Pod rather than being tied to a model or application provider, with Solid's access control deciding who can read it. It was published as a demo at The Web Conference 2024: [SocialGenPod: Privacy-Friendly Generative AI Social Web Applications with Decentralised Personal Data Stores](https://doi.org/10.1145/3589335.3651251), with the prototype at [github.com/Vidminas/socialgenpod](https://github.com/Vidminas/socialgenpod).
