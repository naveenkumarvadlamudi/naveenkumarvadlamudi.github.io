---
layout: single
author_profile: true
title: "Cloud data management"
permalink: /
excerpt: "M.Sc., University of Lethbridge. Batch migration for sharded NewSQL systems, lakehouse storage, and the data platforms that run them."
header:
  overlay_color: "#12344d"
  overlay_filter: "0.25"
  actions:
    - label: "Publications"
      url: "/publications/"
    - label: "Thesis"
      url: "https://hdl.handle.net/10133/6939"
---

I am a computer scientist working on how large, sharded databases move into cloud analytics storage. The question I keep returning to is practical: how to make that move faster, cheaper, and ready for reporting and for model training.

I completed an M.Sc. in Computer Science at the University of Lethbridge in 2024. Dr. Wendy Osborn supervised my thesis on batch migration from a NewSQL system into a lakehouse. That work was accepted to IEEE COMPSAC 2025, and I presented it in Toronto.

## Current appointments

- **Mitacs Business Strategy Internship**, University of Lethbridge, January 2026–present. Independent research developing a product for Trueffect in partnership with the university.
- **Co-founder**, Huroca, Lethbridge, August 2025–present. The Huroca team placed first at the 2026 Launch Point Pitch Competition.
- **Database, API, and report developer**, Sofvie Inc., September 2024–present. Database releases, REST APIs, and in-app reports for a safety platform used in mining.

## Research

**NewSQL batch migration.** My thesis and the COMPSAC paper study migration out of Apache ShardingSphere with PostgreSQL into AWS object storage in Delta Lake format. I implemented the loads in Apache Spark and compared sequential and concurrent strategies, both shard by shard and after aggregating shards. Published methods for this kind of sharded migration are scarce. Shorter pipelines lower the cloud bill and put data in analysts' and models' hands sooner.

**Databases for program evaluation.** With Sidney J. Shapiro, Vivian Oystrick, and Alison Liu, I co-authored a *Canadian Journal of Program Evaluation* article on when a non-profit should leave spreadsheets for a database, and what that choice asks of a small team.

**Applied data platforms.** The same problems show up in production. At ValueMomentum I built Snowflake pipelines for an insurance carrier and cut a subject-area job from about six hours to roughly 90–150 minutes by running work in parallel. At the University of Lethbridge I replaced a facilities workflow that took two or three days by hand with an Airflow and dbt pipeline that finishes in under ten minutes.

[Read the research narrative](/research/) · [Full publication list](/publications/) · [Industry and academic CV](/experience/)

## Selected work

1. **Naveen Kumar Vadlamudi** and Wendy Osborn. 2025. Batch processing algorithms for NewSQL-based big data systems. *IEEE COMPSAC*, 301–306. [DOI](https://doi.org/10.1109/COMPSAC65507.2025.00048)
2. **Naveen Kumar Vadlamudi**. 2024. *Cost-effective batch-based migration strategies for NewSQL-based big data systems*. M.Sc. thesis, University of Lethbridge. [OPUS](https://hdl.handle.net/10133/6939)
3. Sidney J. Shapiro, Vivian Oystrick, Alison Liu, and **Naveen Kumar Vadlamudi**. 2024. From spreadsheets to scalability: Databases as a next step for non-profits. *Canadian Journal of Program Evaluation*, 39(2), 363–372. [DOI](https://doi.org/10.3138/cjpe-2023-0050)
