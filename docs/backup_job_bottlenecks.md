---
title: "Analyzing Performance Bottlenecks"
product: "vpsch"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vpsch/userguide/backup_job_bottlenecks.html"
last_updated: "10/30/2025"
product_version: ""
---

# Analyzing Performance Bottlenecks


As any backup application handles a great amount of data, it is important to make sure the data flow is efficient and all resources engaged in the backup process are optimally used. For backup jobs, Veeam provides advanced statistics about the data flow efficiency and lets you identify bottlenecks at the following stages of the data transmission process:

1. Reading VM data blocks from the source.
2. Processing VM data on a worker.
3. Transporting data over the network.
4. Writing data to the target.

[![Bottleneck Diagram](images/bottlenecks_scheme.webp)](images/bottlenecks_scheme.webp "Bottleneck Diagram")

While evaluating the data transmission process, Veeam Plug-in for Scale Computing HyperCore leverages the Veeam Backup & Replication functionality to analyze performance of all the data flow components:

* Source — the source disk reader component responsible for retrieving data from the source node.
* Proxy — the worker component responsible for processing VM data.
* Network — the network queue writer component responsible for getting processed VM data from the worker and sending it over the network to the Target (directly or through the Gateway Server).
* Target — the gateway server component responsible for processing VM data, or the target disk writer component responsible for storing data in the backup repository.

To see the bottleneck statistics for a job or a specific VM processed by the job, do the following:

1. Open the Home view.
2. In the inventory pane, select Jobs.
3. In the working area, select the backup job for which you want to see the bottleneck statistics and click Statistics on the ribbon.

Alternatively, right-click the job and select Statistics.

1. In the job session details window, check the Bottleneck field in the SUMMARY column.

|  |
| --- |
| Tip |
| To see the bottleneck statistics for a specific VM, click Show Details, select the VM name in the Name column and check the Load record in the Action column. To learn how to analyze the statistics, see Veeam Backup & Replication User Guide, section [Performance Bottlenecks](https://helpcenter.veeam.com/docs/vbr/userguide/detecting_bottlenecks.html?ver=13). |

[![Analyzing Performance Bottlenecks](images/bottlenecks.webp)](images/bottlenecks.webp "Analyzing Performance Bottlenecks")

