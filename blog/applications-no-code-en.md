---
title: "Low code / no code applications"
description: "A selection of no code applications for academic research."
author: emchateau
date: 2024-08-28
draft: false
lang: en
tags: [tools]
---

# Low code - No code applications

“Low code” or “no code” applications are software solutions that provide graphical interfaces to simplify data entry, management, and analysis. This type of solution gained prominence especially at the turn of the 2020s with the emergence of proprietary software such as [Notion](https://www.notion.so) and [Air Table](https://www.airtable.com).

Due to their versatility and user-friendliness, many researchers quickly adopted these softwares for managing their research data. However, these tools are proprietary and do not adhere to standardized formats or data models. Export capabilities are sometimes incomplete, and using such software poses significant risks to research data management. The widespread adoption of these tools risks creating a situation similar to the use of FileMaker software in historical research.

Therefor, it is crucial to identify alternative solutions that offer comparable services while ensuring better data durability.

## Open Source alternatives to Notion and AirTable

In response to the success of proprietary software, a number of free and open source alternatives have emerged. Their development has been swift, and they are increasingly providing comparable functionality. Depending on the business models implemented by their developers, these software solutions can be either self-hosted or offered as paid online services.

### AppFlowy

> Bring projects, wikis, and teams together with AI. AppFlowy is an AI collaborative workspace where you achieve more without losing control of your data. The best open source alternative to Notion.

- url: https://www.appflowy.io
- code: https://github.com/AppFlowy-IO/AppFlowy/
- Licence: AGPL v3 +
- language: Dart + Rust

### Baserow

Baserow is an application designed for creating databases and applications without coding. Although the software is open source, it is not truly free software.

>Create it. Scale it. Own it. The open platform to create scalable databases and applications—without coding.

- url: https://baserow.io
- code: https://gitlab.com/bramw/baserow
- licence: custom
- language: Python

### Espocrm

> EspoCRM is a web application that allows users to see, enter and evaluate all your company relationships regardless of the type. People, companies, projects or opportunities — all in an easy and intuitive interface.

- url: https://www.espocrm.com
- licence: https://github.com/espocrm/espocrm
- licence: GPL V3
- language: PHP

### Grist

>Simple. Flexible. Powerful. A modern, open source spreadsheet that goes beyond the grid.

- url: https://www.getgrist.com
- code: https://github.com/gristlabs/grist-core
- licence: Apache 2.0
- language: TypeScript

### NocoDB

>Build Databases As Spreadsheets : No-Coding Required. NocoDB allows building no-code database solutions with ease of spreadsheets. Bring your own database or choose ours! Millions of rows? Not a problem. Your Data. Your rules. You are in control.

- url: https://nocodb.com
- code: https://github.com/nocodb/nocodb
- licence: AGPL V3
- language: JavaScript

### Mathesar

>Quickly enter and analyze your data – in one open source interface. Mathesar is an **open source** and web-based interface that works on top of your database. You can enter and slice and filter and structure your data… **in minutes**. No technical skills required.

- url: https://mathesar.org
- code: https://github.com/mathesar-foundation/mathesar
- licence: GPL v3
- language: Python + Svelte

### Metabase

>Don’t be a bottleneck. Fast analytics with the friendly UX and integrated tooling to let your company explore data on their own.

- url: https://www.metabase.com
- code: https://github.com/metabase/metabase
- licence: AGPL v3 + divers
- language: Clojure + TypeScript

### Open data editor

> No-code application to explore and publish all kinds of data: datasets, tables, charts, maps, stories, and more. Forever free and open source project powered by open standards and generative AI.

- url: https://opendataeditor.okfn.org
- code: https://github.com/okfn/opendataeditor
- licence: MIT Licence
- language: Python + JavaScript

### Rowy

> Low-code Backend. Manage your database on a spreadsheet-UI and build powerful backend cloud functions, scalably without leaving your browser. Start like no-code, extend with code. 

- url: https://www.rowy.io
- code: https://github.com/rowyio/rowy
- licence: Apache 2.0
- language: TypeScript

## CMS specialized for historical research

### Omeka-S

Omeka-S is a content management system specialized for the heritage and cultural sectors, developed by the Center for History and New Media. Highly flexible, the software integrates various document models and features for the use of controlled vocabularies, with compatibility with [Zotero](https://www.zotero.org) and [Tropy](https://tropy.org). It allows for partial data publication through an API.

- url: https://omeka.org/s/
- code: https://github.com/omeka/omeka-s
- licence: GNU GPL v3
- language: PHP (Laminas)

### Arches

Arches is a general-purpose open source data management platform for cultural heritage developed by the Getty Conservation Institute and the World Monuments Fund.

- url: https://www.archesproject.org
- code: https://github.com/archesproject/arches
- licence: AGPL3
- language: Python + JavaScript

### Research-Space

Research-Space is a software developed in collaboration between art historians, curators, and archaeologists to create a digital research documentation system, developed by the British Museum and supported by the Andrew W. Mellon Foundation.

- url: https://www.researchspace.com
- code: https://github.com/researchspace
- licence: AGPL3
- language: TypeScript