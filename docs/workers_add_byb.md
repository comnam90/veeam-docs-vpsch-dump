---
title: "Before You Begin"
product: "vpsch"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vpsch/userguide/workers_add_byb.html"
last_updated: "2/12/2025"
product_version: ""
---

# Before You Begin


Before you add a worker to the backup infrastructure, consider the following:

* It is recommended that workers are deployed on each node registered with a Scale Computing HyperCore cluster. If no worker is deployed on the node, performance of backup and restore operations will be affected as Veeam Plug-in for Scale Computing HyperCore will use a worker deployed on another node.

* Each worker must be provided with sufficient compute resources to handle backup and restore tasks in parallel. The maximum number of concurrent tasks is configured in worker settings — if this number is exceeded, the worker will not start a new task until one of the current tasks finishes.
* You can change the maximum number of concurrent tasks (the best practice is to allocate 1 vCPU and 1 GB RAM for each additional task) while deploying a new worker or editing settings of an existing one.

