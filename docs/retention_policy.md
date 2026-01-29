---
title: "Retention Policies"
product: "vpsch"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vpsch/userguide/retention_policy.html"
last_updated: "5/21/2025"
product_version: ""
---

# Retention Policies


Backups created by jobs are not kept forever — they are removed according to retention policy settings specified while creating the jobs as described in section [Creating Backup Jobs](backup_job_create.md).

Restore points in the backup chain can be stored only for the allowed period of time. If a restore point is older than the specified time limit, Veeam Plug-in for Scale Computing HyperCore removes it from the backup chain.

To learn how Veeam Plug-in for Scale Computing HyperCore applies retention policies to forever forward incremental and forward incremental backup chains, see [Backup Retention](backup_retention.md).

