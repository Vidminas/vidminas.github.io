---
title: "Enterprise search at Microsoft"
summary: Two UX developer internships with the SAGE team, Microsoft Norway
tags:
  - Web development
  - Search
  - Accessibility
  - TypeScript
date: '2021-09-01T00:00:00Z'
---

Over two summer internships -- July to September 2020, and June to September 2021 -- I worked as a user experience developer with the Search And Graph Experiences (SAGE) team, part of the FAST division of the Microsoft Development Center Norway in Oslo. I had to work remotely both times due to Covid lockdowns.

## Improving enterprise search

The first internship focused on search as it appears across Microsoft's online services: SharePoint, Outlook Web Apps, Delve, and OneDrive for Business. I built front-end components in React and TypeScript, and set up unit and visual regression testing with Storybook.js, Enzyme, Selenium, and Jest.

I worked on extending inline hero answers in the search box, when there is a high confidence result available for a search query as it is being typed.


## Returning to the team

The second internship extended the work into SharePoint, Office, and Bing Enterprise. I implemented front-end components shared across those sites, extended client-side support for new features, and built collection and analysis of usage metrics on Microsoft's telemetry framework. This round added Fluent UI and C# to the stack, working under the mentorship of senior software engineers.

The main feature I worked on was People Also Ask for enterprise search results, branded "Employees May Ask". The interface looks simple, but most of the work was under the hood:

* implementing the user interface components;
* refining accessibility features, including screen reader support and keyboard navigation;
* integrating the components into several different host applications, each with its own conventions;
* devising a solution for client-side ranking and placement of search results;
* and working around the constraints of instrumentation -- logging user interactions across those host apps.

It was rolled out to inner testing circles by the end of the internship, and has since been deployed in some enterprise Microsoft tenancies.

This internship involved collaboration with teams in China, India, Germany, the UK, and the US, and I verified my work in team bug bashes and by monitoring telemetry during gradual rollout.

