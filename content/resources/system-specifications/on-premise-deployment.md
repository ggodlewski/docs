---
title: "On-Premise Deployment"
date: "2020-02-27T21:26:18.802Z"
url: "resources/system-specifications/on-premise-deployment.html"
author: aquandt
version: 23
id: "1W32Q90BZqGacjJHvzQiKrDRBIvh47oBt5LK4gwHK5HI"
source: "https://drive.google.com/open?id=1W32Q90BZqGacjJHvzQiKrDRBIvh47oBt5LK4gwHK5HI"
menu:
    main:
        name: "On-Premise Deployment"
        identifier: "1W32Q90BZqGacjJHvzQiKrDRBIvh47oBt5LK4gwHK5HI"
        parent: "1NH8Qsk7DTsUoBvIVdUktgWvOu8yxrDOuOxmy9SsOCwU"
        weight: 6220
---
## Change Log

<table>
  <tr>
    <td>**VERSION**</td>
    <td>**DATE**</td>
    <td>**AUTHOR**</td>
    <td>**CHANGE**</td>
  </tr>
  <tr>
    <td>1.0</td>
    <td>06/20/2017</td>
    <td>DWJ</td>
    <td>Initial Version</td>
  </tr>
  <tr>
    <td>1.1</td>
    <td>09/05/2017</td>
    <td>DWJ</td>
    <td>Changed RHEL/CentOS 6 to 7</td>
  </tr>
  <tr>
    <td>1.2</td>
    <td>09/05/2017</td>
    <td>DWJ</td>
    <td>Remove Render Server - this is now done by the application</td>
  </tr>
  <tr>
    <td>1.3</td>
    <td>09/06/2017</td>
    <td>DWJ</td>
    <td>Changed MariaDB 5.5 to MariaDB 10.2.8</td>
  </tr>
</table>

## Objective

This document outlines the minimum recommended hardware configuration for deployment of {{% system-name %}}  either on dedicated hardware or within a virtualized environment.

## Confidentiality

All information supplied in this document by {{% system-name %}}  is to be considered company confidential. This document (whether in electronic or print format) should only be distributed to the minimum number of individuals possible, and is subject to the restrictions imposed by the executed Non-Disclosure Agreement (NDA) and or contract agreement.

## Assumptions

The following critical infrastructure items are assumed to be reliable, redundant and well managed by the hosting organization when considering self-hosting.

* Power
* Cooling
* Networking
* Security, physical and cyber

This document also assumes the hosting organization has the technical resources to maintain and support the services that will be deployed within the self-hosting environment.

## Prerequisites

During the installation and configuration period, all instances **must** have access to the internet for package management and installation. If this install is not an OVA install, then {{% sys-name %}} engineers **must** have root level access to the instance during installation and configuration. This elevated security is only during the installation and configuration period.

## Services

{{% system-name %}}  deploys its applications using Enterprise-level open source software. Minimally required services in the hosting environment are as follows:

* Linux, [Red Hat® Enterprise Linux 7](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/7.0_Release_Notes/index.html) or [CentOS 7](https://www.centos.org/)
* Web Services
    * [Apache 2.4](https://httpd.apache.org/docs/2.4/)
* {{% system-name %}}  System
    * Local File System
    * [MariaDB 10.2.8](https://downloads.mariadb.org/mariadb/10.2.8/) or higher
    * [memcached 1.4.4](http://memcached.org/) or higher

### State Diagram of Services

![](on-premise-deployment.images/image1.png)

## Environments

Typical standalone deployments include three environments to support a Deployment Life Cycle (DLC) for application patches, upgrades and configuration changes:

* Development
* QA
* Production

### Multi-tenant

{{% system-name %}}  has the ability to run multiple, logically isolated instances of the {{% system-name %}}  System on a single server or cluster. A [URL](https://en.wikipedia.org/wiki/Uniform_Resource_Locator) for each instance (aka handle) uniquely identifies each instance and provides direct and secure access. This type of deployment is useful for Development and QA environments.

## Infrastructure

The {{% system-name %}}  application requires an x86_64 architecture and can be deployed on bare metal hardware or within a virtualized shared or dedicated environment. The balance of this document will focus on deployment within a virtualized environment and includes minimal hardware requirements.

## Deployment Methodologies

There are three typical deployment footprints:

* All-in-one
* Dedicated DB
* High Availability / Horizontal Scalability

### All-in-one

All the required services run within a single server. This approach is best utilized in small (~50 concurrent users) deployments or for sandbox development use-cases. The "all-in-one" strategy for production is best when a virtualized environment is available for scaling and redundancy underneath the {{% system-name %}}  System. A VM image that contains all necessary services for the {{% system-name %}}  System to operate can be provided. This approach can also be used for Development and QA lifecycles. The All-in-one footprint enables quick and easy deployment and can serve as a stepping stone to larger deployments with dedicated services.

![](on-premise-deployment.images/image3.png)

### Dedicated DB

The Dedicated DB is the first useful step to scaling up to handle more load. The database I/O patterns tend to compete with other I/O so it is useful to split the database to another server with dedicated resources.

![](on-premise-deployment.images/image2.png)

### High Availability / Horizontal Scalability

The High Availability (HA) and Horizontal Scalability (HS) environment distributes low-level services across multiple systems to provide redundancy and high availability. The {{% system-name %}}  System is optimized to distribute the components across multiple servers and automatically failover to balanced redundant hardware. Managing a cluster requires expert skills in load balancing, routing, networking and monitoring.

![](on-premise-deployment.images/image4.png)

## Minimum Hardware Requirement

Hardware requirements vary greatly based on a variety of factors including the number of concurrent users, user activities and data storage requirements. For example, disk requirements will be greater when converting volumes of paper charts to digital images. We typically work with our clients to review current usage requirements and forecast anticipated growth in order to ensure Development, QA and Production environments are provisioned correctly. Minimum requirements are as follows:

<table>
  <tr>
    <td colspan="3">**ALL-IN-ONE**</td>
  </tr>
  <tr>
    <td>**Service Name**</td>
    <td>**Services**</td>
    <td>**Hardware**</td>
  </tr>
  <tr>
    <td>
* Web Services
* Database
* Data Storage
* Interface
    </td>
    <td>
* Apache
* memcached
* MariaDB
* File System
    </td>
    <td>
* 4 CPU cores
* 32G Memory
* 500G Storage
    </td>
  </tr>
</table>



<table>
  <tr>
    <td colspan="3">**DEDICATED**</td>
  </tr>
  <tr>
    <td>**Service Name**</td>
    <td>**Services**</td>
    <td>**Hardware**</td>
  </tr>
  <tr>
    <td>Web Services</td>
    <td>
* Apache
* Nginx
* node.js
* memcached
    </td>
    <td>
* 4 CPU cores
* 8G Memory
* 100G Storage
    </td>
  </tr>
  <tr>
    <td>Database</td>
    <td>* MariaDB</td>
    <td>* See [On-Premise MariaDB Database](on-premise-deployment/on-premise-mysql-server-hardware-requirements.html)</td>
  </tr>
  <tr>
    <td>Data Storage</td>
    <td>* File System</td>
    <td>
* 4 CPU cores
* 8G Memory
* 500G Storage
    </td>
  </tr>
</table>

{{% note %}}

**High Availability/Horizontal Scalability requirements are far more variable, and as such are not depicted here. Please contact your Account Manager for more discussion on this option.**

{{% /note %}}


### File Servers

* 3 x (1 as primary, 2 as replication partners)
    * 1 x Quad-core Intel E5 series or better CPUs
    * 64G RAM
    * 5T of storage (RAID6 based array)
* OS: RHEL / CentOS 7.x

### Web Servers

* 2 x Quad-core Intel E5 series or better CPUs:
    * 12G RAM minimum
    * 500G RAID1
* OS: RHEL / CentOS 7.x

### Fax Server

* If using our Dialogic based FAX server, the fax and interface box can be one in the same:
    * One server provides fax functionality, interfaces, and runs a virtual machine for the print functions:
        * 2 x Quad-core Intel E5 series or better CPUs
            * 64G RAM
            * 4 x 600G 15K SAS drives in a RAID10 volume
            * 1 x Dialogic DIVAServer E1 306-304 PCIe fax card for currently developed MIE faxing solution
        * OS: RHEL / CentOS 7.x
        * VM: Windows 7 32bit, running latest copy of Microsoft Word (for print conversions)
* If using a separate FAX server, the following specs are for a separate interface server and separate print server:
    * Print server:
        * 1 x Quad-core Intel E5 series or better CPUs
            * 2G RAM minimum
            * 20G RAID1
        * OS: Windows 7 32bit, running Word 2013

### Batch Server

* 1 x Quad-core Intel E5 series or better CPUs
    * 4G RAM minimum
    * 60G RAID1
    * OS: RHEL / CentOS 7.x

## Supportive Servers and Services

The following servers and services are not covered in detail in this document, but are typically included as part of a on-premise environment.

* Fax Server
    * Dedicated bare metal hardware
    * Dialogic DIVA 306-304 PCIe T1/PRI FAX card
* Interface
    * EDI
    * sFTP/FTPs
    * Socket based

## Deployment Guide

Below are the requirements, technical details and steps on how to install, configure and access the {{% system-name %}} system as an All-in-one VM.

### Getting Started

The All-in-One  {{% sys-name %}} VM deployment is designed to be quick and easy allow for  {{% system-name %}} environments to be launch within just a few hours.

#### Downloading All-in-One {{% sys-name %}} VM

* Using the link provided by your deployment specials, download the {{% sys-name %}} All-in-One VM Box Image. If you do not have a link contact your deployment specialist and one will provided to you.
* Deploy the VM within your Virtualized Environment
* Assign IPv4 address to VM Network and System
* Hostname
* DNS
* [VPN to MIE](https://docs.google.com/spreadsheets/d/15Ajp6KpMh34ijSyZxvwmSvsH8jJiPTsy7WOwvFFYnhc/edit#gid=1385212531)
* Firewall rules
    * tcp/443 (HTTPS) to MIE and Application Users
    * tcp/22 (SSH) to MIE
    * tcp/389 and tcp/636 LDAP to MIE
    * tcp/10050 and tcp/10051 - Zabbix
    * tcp/1514 OSSec
    * tcp/514 and udp/514 - syslog
    * tcp/4505 and tcp/4506 - Salt
* Mail Services
    * Allow mail to be sent from instance
* Monitoring of systems
* Audit Logging
* Backup

#### Web Services Configuring

* Purchase SSL certificate for selected domain name
* Configure [Apache 2.2.15](https://httpd.apache.org/docs/2.2/) with SSL certificates

## On-Premise Golive Checklist

Successful Go-Live of an On-Premise {{% system-name %}}  System requires planning, coordination and orchestration throughout the many facets of the customer's organization, including divisions and departments to bring everything pieces together. These include, but are not limited to, data migration, IT operations, staff training, support and notification to stakeholders. This document is to help you prepare and plan for such a monumental task.

### Checklist

*This checklist is to help the customer plan and give insight to what is needed for a successful go-live and is by no means is comprehensive.*

* Determine {{% system-name %}} endpoint example: ([https://ehs.mycompany.com](https://ehs.mycompany.com/))
* Purchase SSL certificates for domain ([ehs.mycompany.com](http://ehs.mycompany.com))
* Server / Application Configuration:
    * install and configuration of services
    * Install and configuration of {{% sys-name %}}
    * Logging
    * Monitoring
    * Backup configuration
    * Outbound email Configuration to {{% sys-name %}} support
* Production functionality testing
    * Access to Application
    * View / uploading data
* Failover testing (if applicable)

### Hosted vs On-Premise

<table>
  <tr>
    <td>**SERVICE**</td>
    <td colspan="2">**HOSTED** | **CUSTOMER ON-PREMISE**</td>
  </tr>
  <tr>
    <td>Infrastructure</td>
    <td>
* SOC2 type II certified Data Center
* Dedicated Services
* Highly Available
* Multi-Region Redundancy
* Tuned for best performance
* 99.95% uptime SLA
* Tuned IDS and IPS
* Auto applied security patches
* 24/7 Monitoring of infrastructure
* Backup and rotations
* Optional data-at-rest encryption
    </td>
    <td>
* Provisioning of hardware
* purchase of domain name and SSL certificates
* Configuration of load balancers
* Configuration of Linux CentOS 7, Apache, MariaDB, MIEFS, failover, logging, monitoring and other software to support the application.
* Self configured IDS and IPS
* Support Contract
* VPN Connectivity
* Access to servers
    </td>
  </tr>
  <tr>
    <td>Deployment</td>
    <td>* Easy deployment - 8 to 24 hours, and your {{% system-name %}} system is up and running ready for production</td>
    <td>
* Long deployment cycle
* Requires provisioning of hardware
* Software installation and configuration
    </td>
  </tr>
  <tr>
    <td>IT Operations</td>
    <td>
* Dedicated Operations team specializing in SaaS and experts in full stack deployment
* Continuous capacity planning, we scale as you grow
    </td>
    <td>
* Infrastructure may not support {{% sys-name %}} requirements
* May require additional resources to support {{% system-name %}} system
* Capacity planning may require the provisioning of additional costly hardware or reconfiguration
    </td>
  </tr>
  <tr>
    <td>Software Deployment</td>
    <td>* We plan and deploy hotfixes and upgrades seamlessly</td>
    <td>
* Requires patch files to be sent
* Depending on deployed infrastructure, software updates may require extended downtime to implement.
    </td>
  </tr>
</table>

## Managed Services

{{% sys-name %}} offers managed services for the following:

* [Application Managed Service Summary](on-premise-deployment/application-managed-service-summary.html)
* [Database Managed Services](https://docs.google.com/document/d/1YX-G0aO0wZ13vsiHUtroPGSzE3q6yjKeLdzgX3fvMrs/edit)