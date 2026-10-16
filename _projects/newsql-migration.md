---
layout: page
title: NewSQL batch migration
description: Spark strategies for moving a sharded database into a lakehouse.
importance: 1
category: research
related_publications: true
---

My M.Sc. thesis studies how to move data out of a NewSQL system, Apache ShardingSphere with PostgreSQL, into AWS object storage stored as Delta Lake. The jobs run in Apache Spark.

I compared four batch loads: shard-by-shard and aggregated-shard, each run sequentially and concurrently. The design goal is a shorter migration, a lower cloud cost, and a lakehouse layout that reporting tools and models can use. Dr. Wendy Osborn supervised the thesis. The algorithms were presented at IEEE COMPSAC 2025.

The thesis is on [OPUS](https://hdl.handle.net/10133/6939). The conference paper is on [IEEE Xplore](https://ieeexplore.ieee.org/document/11126763).

{% cite vadlamudi2024thesis vadlamudi2025batch %}
