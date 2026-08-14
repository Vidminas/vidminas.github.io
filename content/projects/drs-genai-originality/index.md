---
title: "Measuring originality in student work written with and without ChatGPT"
summary: Digital Research Services Ambassador project
tags:
  - AI
  - Education
  - Python
  - Data Analysis
date: '2024-05-01T00:00:00Z'
---

As a Digital Research Services Ambassador in 2024, I worked with a team in the University of Edinburgh Business School on a study of how students used ChatGPT in a coursework exercise.

Students on the Digital Business course (n=192) were asked to write business proposals for a competition in which the most original proposal would win. They first wrote proposals without generative AI, then refined them using ChatGPT. The project host wanted to know whether human-written or AI-assisted proposals were more original.

My role was to work out how to measure that. We defined the originality of a proposal as the inverse of its similarity to all the other proposals. Over the course of the project both I and the hosts learned a good deal about text similarity: we tried orthographic (character-level) similarity, sequence (string) similarity, and cosine similarity using both static and contextual embeddings. We settled on an average of several similarity measures, averaging in turn between cosine distance to all other proposals and to the ten closest proposals within the same task.

The headline result was a statistically significant but small difference in originality between the AI-assisted and human-written texts.

My calculations, code, documentation, and analysis form part of a larger project on students' use of generative AI, which is not yet published -- so this page stays at the level of the approach and that top-line finding.
