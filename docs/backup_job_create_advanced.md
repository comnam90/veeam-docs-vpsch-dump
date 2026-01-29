---
title: "Configuring Advanced Settings"
product: "vpsch"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vpsch/userguide/backup_job_create_advanced.html"
last_updated: "10/30/2025"
product_version: ""
---

# Configuring Advanced Settings


To configure backup job advanced settings, do the following:

1. Click Advanced to open the Advanced settings window.
2. To [schedule synthetic full backups](synthetic_full_backup.md), on the Backup tab, select the Create synthetic full backups periodically check box, click Configure and choose whether you want to create synthetic full backups on specific days every week or on specific days of specific months.

|  |
| --- |
| Important |
| * Synthetic full backups cannot be scheduled if an object storage repository is selected as the target location for backups. |

1. To [schedule active full backups](active_full_backup.md), on the Backup tab, select the Create active full backups periodically check box, click Configure and choose whether you want to create active full backups on specific days every week or on specific days of specific months.

Alternatively, you can create active full backups manually when needed. For more information, see [Creating Active Full Backups](active_full_create.md).

|  |
| --- |
| Important |
| Do not schedule synthetic and active full backups to run at the same time. Due to technical limitations, Veeam Plug-in for Scale Computing HyperCore will be unable to create synthetic full backups according to the specified schedule. |

1. To instruct Veeam Plug-in for Scale Computing HyperCore to periodically [perform a health check](how_health_check_works.md) for backups created by the backup job, on the Maintenance tab, select the Perform backup files health check (detects and auto-heals corruption) check box, click Configure and specify a schedule for the health check to run.

|  |
| --- |
| Important |
| * It is recommended that the backup and health check schedules configured for the job do not overlap to avoid data access issues. * If you have selected an off-premise cloud object storage repository as the target location for backups at [step 4](backup_job_create_destination.md), it is recommended that a [helper appliance is configured in the repository settings](https://helpcenter.veeam.com/docs/vbr/userguide/compatible_mount_server.html?ver=13). Otherwise, additional data transfer costs may occur. |

1. To decreases the size of the backup, on the Storage tab, from the Compression level drop-down list, select a compression level for the backup: None, Dedupe-friendly, Optimal, High or Extreme. For more information on data compression, see [Compression and Deduplication](https://helpcenter.veeam.com/docs/vbr/userguide/compression_deduplication.html?ver=13).
2. To optimize job performance and storage usage, on the Storage tab, from the Storage optimization drop-down list, select the block size that will be used to process VMs. For more information on the data block sizes and how they affect performance, see [Storage Optimization](https://helpcenter.veeam.com/docs/vbr/userguide/compression_deduplication.html?ver=13#optimization).
3. To configure settings for automated email delivery of job results, on the Notifications tab, select the Send email notifications to the following recipients check box and specify email addresses of recipients. For more information on on mail server settings required for email notifications, see [Configuring Email Settings](email_settings.md).

[![Specify Backup Job Advanced Settings](images/backup_job_create_advanced.webp)](images/backup_job_create_advanced.webp "Specify Backup Job Advanced Settings")

