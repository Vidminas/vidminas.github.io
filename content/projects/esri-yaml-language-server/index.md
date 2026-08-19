---
title: "A VS Code language server for Esri's YAML specification"
summary: Software developer internship at Esri
tags:
  - Web development
  - TypeScript
  - Developer Tools
  - JSON Schema
date: '2019-08-01T00:00:00Z'
links:
  - type: code
    label: yaml-language-server
    url: https://github.com/redhat-developer/yaml-language-server
---

Over the summer of 2019, I interned as a software developer at Esri in Edinburgh, building a Visual Studio Code language server extension for Esri's in-house YAML specification.

Code editors get their clever functionality -- validation, auto-completion, go-to-definition, find-all-references -- from a language server plugin running behind the scenes. Esri's configuration files used a custom YAML specification with no such support, so writing them meant working without any supporting functionality.

I adapted Red Hat's open-source [yaml-language-server](https://github.com/redhat-developer/yaml-language-server) to the custom specification, and contributed the improvements that weren't Esri-specific back upstream.

The project involved C, C++, TypeScript, and Node.js, with modules in different languages binding together to produce the finished extension. It was also my first substantial use of JSON Schema, which came back round several years later on the [TUSAIL experimental measurements database](../tusail-emdb/).
