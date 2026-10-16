---
title: "Research"
permalink: /research/
excerpt: "Batch migration for sharded NewSQL systems, lakehouse storage, and data infrastructure for evaluation and operations."
---

I study cloud data management algorithms: how data leaves a sharded operational database, how it lands in analytics storage, and what that costs in time and money.

The thread running through the thesis, the COMPSAC paper, and my industry work is the same. Large organizations already hold data in systems that were built to serve transactions. Reports, dashboards, and models need that data somewhere else, usually in object storage, and they need it while the cloud bill is still defensible.

## Batch migration for NewSQL systems

Modern applications pushed databases toward NewSQL designs that keep relational operations and spread data across shards. Moving that data is a different problem from dumping a single PostgreSQL instance. Each shard has its own slice of the tables, and a migration plan has to decide whether to read those slices one at a time, read them together, or merge them before the write.

My M.Sc. thesis, *[Cost-effective batch-based migration strategies for NewSQL-based big data systems](https://hdl.handle.net/10133/6939)* (University of Lethbridge, 2024), takes Apache ShardingSphere with PostgreSQL as the source and AWS object storage as the destination. The stored form is Delta Lake, so the result sits in a lakehouse layout that downstream tools can use for business intelligence and for machine learning. The migration jobs themselves run in Apache Spark.

I compared four families of batch load:

- shard-by-shard, sequential
- shard-by-shard, concurrent
- aggregated shards, sequential
- aggregated shards, concurrent

The evaluation looks at efficiency and performance. The design goal is a shorter migration, a lower cloud cost, and data that is available sooner. Dr. Wendy Osborn supervised the thesis. I later presented the algorithms at the 49th IEEE Computers, Software, and Applications Conference (COMPSAC 2025) in Toronto, in the Data Science and Data Engineering track. The paper is [Batch Processing Algorithms for NewSQL-based Big Data Systems](https://doi.org/10.1109/COMPSAC65507.2025.00048), pages 301–306.

I shared the findings with the ISEDAM lab at Lethbridge. Jacqueline Rice, Sidney Shapiro, and John Anvik gave me that forum.

## Databases beyond the spreadsheet

A second line of work asks a smaller version of the same question: when is a database the right next system?

With Sidney J. Shapiro, Vivian Oystrick, and Alison Liu, I co-authored [From Spreadsheets to Scalability: Databases as a Next Step for Non-Profits](https://doi.org/10.3138/cjpe-2023-0050) in the *Canadian Journal of Program Evaluation* (2024). The article is about program-evaluation data. Spreadsheets are the right tool for many non-profits. They stop being the right tool when the data outgrows one computer, when several people need it at once, or when the organization is stitching together files that no longer describe one operation.

The paper walks through SQL, NoSQL, and desktop options such as Microsoft Access, and through the constraints that actually decide the choice: thin infrastructure, little or no full-time IT staff, and the need to train the people who will live with the system. Case studies in the article draw out a few practices that hold up: fit the database to the organization, keep training going, and work with someone who knows the technology. I came to that paper from the data-engineering side, including a Mitacs data-management project at Lethbridge in early 2024.

## Earlier cryptanalysis

As an undergraduate at Geethanjali College of Engineering and Technology, I published a cryptanalysis paper with Dr. N. Ravi Shankar. [Cryptanalysis of a New Cryptosystem of Color Image Using a Dynamic-Chaos Hill Cipher Algorithm](https://doi.org/10.1007/978-981-15-2414-1_47) (ICCAN 2019; Springer, 2020) gives a chosen-ciphertext attack on a published color-image cipher. The scheme uses a chaotic map to build key material, and the attack shows that the construction collapses to an affine Hill cipher whose keys can be recovered.

## Where the research meets industry

The migration work is easier to trust if you have operated the pipelines it talks about.

At ValueMomentum in Hyderabad I worked on a Snowflake platform for an insurance carrier: historic and incremental loads from on-premises systems through Amazon S3 into landing and curated layers, SCD Type 2 audit jobs in Matillion, and Snowsight reports for daily runs. Parallel execution brought one subject-area job from about six hours down to roughly 90–150 minutes, and brought Snowflake credit consumption to about 60 percent of the previous level, a saving on the order of $5,000–$6,000 a month.

At Kastech, while I was in the master's program, I built proofs of concept on an open-source stack: Airbyte, dbt, Apache Airflow, Docker, Snowflake, PostgreSQL, and OpenMetadata, including change-data-capture from PostgreSQL and MySQL. In summer 2023, as a technical specialist for University of Lethbridge Facilities, I designed an Airflow ingestion path into SQL Server, transformed the data with dbt and stored procedures, packaged the deployment in Docker, and cut a manual workflow from two or three days to under ten minutes.

Since 2024 I have been at Sofvie, working on the database behind a mining safety product: stored procedures, production promotions and backups, REST APIs, and the reports the application shows to operators and managers.

## Current direction

From January 2026 I have been a Mitacs Business Strategy Intern at the University of Lethbridge, developing a product for Trueffect in partnership with the university. I am also a co-founder of Huroca, an automation company in Lethbridge. The team placed first at the 2026 Launch Point Pitch Competition.

Alongside the systems work, I am reading and building in two related areas: query processing across cloud databases, and a more careful use of AI inside data management. A course report from CPSC 5990, [Query Processing in Multi-Cloud Systems](https://github.com/VadlamudiNaveen/Query-Processing-in-Multi-Cloud-Systems), collects the literature I started from. Notes on cloud-native data engineering, warehouses, and lakehouse architecture are on [my research notebook](https://naveenvadlamudi.hashnode.dev/).
