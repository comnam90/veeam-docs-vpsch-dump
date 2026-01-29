---
title: "Performing Backup"
product: "vpsch"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vpsch/userguide/data_protection.html"
last_updated: "7/23/2025"
product_version: ""
---

# Performing Backup


To produce VM backups, Veeam Plug-in for Scale Computing HyperCore runs backup jobs. A backup job is a collection of settings that define the way backup operations are performed: what data to back up, where to store backups, when to start the backup process, and so on.

One backup job can be used to process multiple VMs, but you can back up each VM with one backup job at a time. If a VM is added to more than one backup job, it will be processed only by the backup job that started earlier.

|  |
| --- |
| Tip |
| Since Veeam Plug-in for Scale Computing HyperCore chooses workers to process backup workload depending on the source data location and then launches these workers one by one in a random order, it is recommended that you create separate jobs for VMs that belong to different locations — this may help you reduce the time required to perform backup operations and optimize the backup performance. |

In This Section

* [Creating Backup Jobs](backup_job_create.md)
* [Editing Backup Job Settings](backup_job_edit.md)
* [Starting and Stopping Backup Jobs](backup_job_start.md)
* [Analyzing Performance Bottlenecks](backup_job_bottlenecks.md)
* [Cloning Backup Jobs](backup_job_clone.md)
* [Enabling and Disabling Backup Jobs](backup_job_disable.md)
* [Deleting Backup Jobs](backup_job_delete.md)
* [Creating Active Full Backups](active_full_create.md)
* [Creating VeeamZIP Backups](veeamzip_create.md)
* [Adding VMs to Backup Job](backup_job_add_vm.md)

