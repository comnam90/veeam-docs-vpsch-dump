---
title: "Before You Begin"
product: "vpsch"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vpsch/userguide/backup_job_create_prerequisites.html"
last_updated: "10/30/2025"
product_version: ""
---

# Before You Begin


Before you create a backup job, consider the following limitations:

* You can back up each VM with one backup job at a time. If a VM is already being processed by a backup job, another backup job will not start processing this VM until the currently running backup operation completes.

* You cannot back up a VM being restored. Wait for the restore process to complete, and then start the backup job.

* You cannot back up Scale Computing HyperCore objects that are not considered VMs.
* You cannot back up VMs with the same BIOS UUID.

* By default, Veeam Plug-in for Scale Computing HyperCore [enables deduplication](https://helpcenter.veeam.com/docs/vbr/userguide/compression_deduplication.html?ver=13) for backed-up data. Due to technical limitations, you cannot disable it while configuring backup jobs.

* By default, [backup encryption](https://helpcenter.veeam.com/docs/vbr/userguide/data_encryption.html?ver=13) is disabled for backed-up data. However, you can enable encryption at the repository level as described in the Veeam Backup & Replication User Guide, section [Access Permissions](https://helpcenter.veeam.com/docs/vbr/userguide/access_permissions.html?ver=13).
* [VM guest OS file indexing](https://helpcenter.veeam.com/docs/vbr/userguide/indexing.html?ver=13) is not supported for backups created with Veeam Plug-in for Scale Computing HyperCore.

* Since Veeam Backup & Replication does not allow you to assign [information about locations](https://helpcenter.veeam.com/docs/vbr/userguide/locations.html?ver=13) to the Scale Computing HyperCore cluster and workers, job statistics do not include information on the Scale Computing HyperCore VM data migration between different geographic regions.
* You cannot back up VM disks that do not allow snapshot creation.

