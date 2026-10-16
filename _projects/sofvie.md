---
layout: page
title: Sofvie database and reports
description: Database administration, APIs, and reports for a mining safety product.
importance: 3
category: industry
---

Since February 12, 2024 I have worked remotely on the database behind Sofvie, a safety platform for mining operations. Through September 2, 2024 I was a student database administrator. On September 3, 2024 the role became permanent and full-time: database administrator, API and report developer. The office is in Lively, Ontario.

I write reports, test APIs, run database releases, and handle production issues. That includes stored procedures, schema maintenance, query optimization, and automated data entry. Client reporting dashboards run from SQL through the UI on MariaDB. Indexing cut report load times by about 40 percent, p95 latency fell by about 35 percent, and support tickets fell by about 30 percent. The dashboards are in use by 3 or more clients. REST APIs serve 5 or more accounts.

An EC2-to-RDS migration kept releases at zero downtime and brought uptime to about 99.9 percent, with about 20 hours a month less operations work. Automated ingestion removed about 15 hours a week of manual onboarding and shortened time-to-value by about 60 percent. Feature flags and phased rollouts covered 4 or more features and cut post-release defects by about 50 percent.
