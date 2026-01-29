---
title: "Publishing Disks"
product: "vpsch"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vpsch/userguide/disk_publish.html"
last_updated: "11/11/2025"
product_version: ""
---

# Publishing Disks


Veeam Backup & Replication allows you to mount specific disks of backed-up VMs to any server and to instantly access data in the read-only mode. This can be helpful when you want to copy files and folders as of a point-in-time state to the target server, and perform an antivirus scan of the backed-up data. For more information, see the Veeam Backup & Replication User Guide, section [Disk Publishing (Data Integration API)](https://helpcenter.veeam.com/docs/vbr/userguide/data_integration_api.html?ver=13).

To publish disks of an Scale Computing HyperCore VM, do the following:

1. Open the Home view.
2. In the inventory pane, select Backups.
3. In the working area, expand the necessary backup job, right-click the VM that contains disks you want to mount and select Publish disks.

Alternatively, you can expand the necessary backup job, select the VM and click Publish Disks on the ribbon.

1. Complete the Publish Disk wizard as described in the Veeam Backup & Replication User Guide, section [Publishing Disks](https://helpcenter.veeam.com/docs/vbr/userguide/publishing_disks.html?ver=13).

[![Publishing disks](images/disk_publish.webp)](images/disk_publish.webp "Publishing disks")

