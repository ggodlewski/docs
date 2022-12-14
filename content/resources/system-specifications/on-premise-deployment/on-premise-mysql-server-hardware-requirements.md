---
title: "On-Premise MySQL Server Hardware Requirements"
date: "2020-02-27T20:46:26.827Z"
url: "resources/system-specifications/on-premise-deployment/on-premise-mysql-server-hardware-requirements.html"
version: 13
id: "1sFxsuXYfKxXzBfI_aincS17dkeDC7MCmK91r3_IVezM"
source: "https://drive.google.com/open?id=1sFxsuXYfKxXzBfI_aincS17dkeDC7MCmK91r3_IVezM"
menu:
    main:
        name: "On-Premise MySQL Server Hardware Requirements"
        identifier: "1sFxsuXYfKxXzBfI_aincS17dkeDC7MCmK91r3_IVezM"
        parent: "1W32Q90BZqGacjJHvzQiKrDRBIvh47oBt5LK4gwHK5HI"
        weight: 6240
---
## Dedicated Server Minimum Requirements

Deployment of a dedicated MySQL instance for the {{% system-name %}} system requires several factors to be taken into consideration, to properly allot hardware resources needed to handle everyday usage, peak usage, and capacity planning for future usage. The following are minimal software and hardware resource recommendations for a dedicated MySQL database server.

## Software

The following required software/configuration may have other required dependencies:

* 64-bit Linux OS
    * [Red Hat® Enterprise Linux 6.7](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/6.7_Release_Notes/) or [7](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/index.html)
    * [CentOS 6.7](https://wiki.centos.org/Manuals/ReleaseNotes/CentOS6.7) or [7](https://wiki.centos.org/Manuals/ReleaseNotes/CentOS7)
* [Percona Server](https://www.percona.com/software/mysql-database/percona-server) latest version 5.5
* [Percona Toolkit](https://www.percona.com/software/mysql-tools/percona-toolkit)
* [Percona xtrabackup](https://www.percona.com/software/mysql-database/percona-xtrabackup)

## Hardware

The minimum hardware resource recommendations for a dedicated MySQL instance fall into three levels: small, medium and large. These levels directly relate to the number of concurrent {{% sys-name %}} users (i.e., the number of users accessing the {{% system-name %}} system at the same time). Memory and storage recommendations vary, and may be influenced by a number of factors that may increase requirements (e.g., large data set, the migration of legacy system data, and the expected growth of users).

Experience has shown, MySQL requires sufficient memory to provide optimal performance and depends on the quantity of information stored in the tables. By caching hot datasets, indexes, and ongoing changes, InnoDB is able to provide faster response times and utilize disk IO in a much more optimal way. From a CPU standpoint, faster processors with many cores provide better throughput with large concurrent workloads. Storage formatted as [EXT4](https://ext4.wiki.kernel.org/) and mounted with noatime, barrier=0 running the [deadline IO schedule](https://www.percona.com/blog/2009/01/30/linux-schedulers-in-tpcc-like-benchmark/) provide optimal performance.

The table below represents rough estimates of hardware requirements and are based on {{% sys-name %}} experience, [MySQL documentation](https://dev.mysql.com/doc/refman/5.5/en/linux-installation.html), and [other recommendations](http://dba.stackexchange.com/questions/15030/mysql-recommended-hardware). These are meant for illustration and may vary significantly depending on workload and storage.

<table>
  <tr>
    <td>Level</td>
    <td>Max Concurrent Users</td>
    <td>Resource Recommendation</td>
  </tr>
  <tr>
    <td>Small</td>
    <td>5 - 10</td>
    <td>
* 2-4 CPU cores
* 12Gb ECC memory
* Storage
    * 20Gb root OS installation
    * 50Gb DB storage
    </td>
  </tr>
  <tr>
    <td>Medium</td>
    <td>10 - 50</td>
    <td>
* 4-8 CPU cores
* 32-64Gb ECC memory
* Storage
    * 20Gb root, OS installation
    * 50Gb DB storage
    </td>
  </tr>
  <tr>
    <td>Large</td>
    <td>50 - 100</td>
    <td>
* 8 or more CPU cores
* 128-256Gb ECC memory
* Storage
    * 20Gb root, OS installation
    * 50Gb DB storage
    </td>
  </tr>
</table>

## Managed Services

{{% sys-name %}} offers consulting and database managed services that can help plan, deploy and manage your {{% system-name %}} system. Please contact your account manager for more information and/or see our [Database Managed Services Summary](https://docs.google.com/document/d/1YX-G0aO0wZ13vsiHUtroPGSzE3q6yjKeLdzgX3fvMrs/edit#heading=h.t72wiklw6qpf).

