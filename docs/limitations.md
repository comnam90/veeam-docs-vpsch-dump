---
title: "Considerations and Limitations"
product: "vpsch"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vpsch/userguide/limitations.html"
last_updated: "11/11/2025"
product_version: ""
---

# Considerations and Limitations


When you plan to deploy and configure Veeam Plug-in for Scale Computing HyperCore, keep in mind the following limitations and considerations.

Configuration

When configuring Veeam Plug-in for Scale Computing HyperCore, consider the following:

* Veeam Plug-in for Scale Computing HyperCore does not support user accounts with OpenID Connect authentication to access the Scale Computing HyperCore cluster.
* The Scale Computing HyperCore cluster must be able to establish a direct IP connection to the backup server. Connections through NAT gateways are not supported.

* After you make changes to your Scale Computing HyperCore environment (for example, you migrate a VM between cluster nodes), these changes may not appear in Veeam Backup & Replication immediately — the data synchronization process between the backup server and the Scale Computing HyperCore cluster may take up to 15 minutes to complete. You can speed up the data synchronization process by [rescanning the Scale Computing HyperCore cluster](server_rescan.md).

Backup Repositories

When managing backup repositories, consider the following:

* Veeam Plug-in for Scale Computing HyperCore does not support storing backups in Veeam Cloud Connect and [HPE Cloud Bank Storage](https://helpcenter.veeam.com/docs/vbr/userguide/storeonce_supported_features.html?ver=13#cloud-bank-storage) repositories. However, you can use them for [storing copies of backups](backups_copy.md) created with Veeam Plug-in for Scale Computing HyperCore.
* If a repository storing Scale Computing HyperCore backups becomes an extent of a scale-out backup repository, the jobs targeting that repository will fail. You can edit the job to target a scale-out backup repository to fix the problem.

Workers

When configuring workers, consider the following:

* The maximum number of parallel tasks is 25. Each task requires 1 VIRTIO drive while 1 drive is used by the worker system.
* Worker must be able to handle at least 2 parallel tasks, so the maximum number of parallel tasks cannot be less than 2.
* In case of multiple tasks being processed, workers are started one by one. A new worker is not started until a previous one is ready.

Backup

When protecting Scale Computing HyperCore resources, consider the following:

* Veeam Plug-in for Scale Computing HyperCore does not support backup of replicated VMs. These VMs are not included in the list of VMs on Veeam Backup & Replication side.

* If snapshot creation is disabled for the disks that are included in a backup job, those disks will be skipped during a job session.
* If at least one of the cluster nodes included in the connected Scale Computing HyperCore cluster becomes inaccessible, backup processing of the whole cluster will be interrupted.
* You cannot assign locations to Scale Computing HyperCore clusters in Veeam Backup & Replication. For that reason, job statistics do not include information on Scale Computing HyperCore VM data migration between different geographic regions.
* Backup move is not supported for the Scale Computing HyperCore backups.
* Retention of VeeamZIP backups is not supported.
* Application-aware processing is not supported.

Restore

When restoring Scale Computing HyperCore resources, consider the following:

* Disk size over 16TB is not supported.
* If you restore the VM from a backup stored in the archive tier of the scale-out backup repository, you must first retrieve backup data as described in the Veeam Backup & Replication User Guide, section [Retrieving Backup Files](https://helpcenter.veeam.com/docs/vbr/userguide/retrieval_job_launch.html?ver=13). Note that you cannot perform Entire VM restore from backups stored in the archive tier that consists of the Amazon S3 Glacier Instant Retrieval extent. For those backups, you can perform Instant Recovery.
* If you restore the VM from a backup of a VMware, Hyper-V, oVirt KVM or Proxmox VE VM or from a backup created by Veeam Agent, a restored VM may have network connection problems. To resolve the issue, install Scale Guest Tools on the restored VM.
* You cannot restore VMs from backups stored in external repositories, Veeam Cloud Connect repositories, and on tapes.
* You can use Veeam Backup Enterprise Manager to file-level restore guest OS files of Scale Computing HyperCore VMs and manage Scale Computing HyperCore VM backup copy jobs. All other operations are not supported.
* [SureBackup](https://helpcenter.veeam.com/docs/vbr/userguide/surebackup_recovery_verification_hv.html?ver=13) for backups created by Veeam Plug-in for Scale Computing HyperCore is supported in the Backup verification and content scan only verification mode.

