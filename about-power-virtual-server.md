---

copyright:
  years: 2019, 2020

lastupdated: "2020-05-26"

keywords: power systems, infrastructure as a service, multiple virtual servers, hybrid cloud environment, linux, aix, ibm i

subcollection: power-iaas

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:external: target="_blank" .external}

# What is a Power Systems Virtual Server?
{: #about-virtual-server}

{{site.data.keyword.powerSysFull}} uses the existing {{site.data.keyword.cloud}} platform to create Power Systems virtual servers, also known as logical partitions (LPAR), that run on IBM Power Systems hardware with the PowerVM hypervisor.
{:shortdesc}

The Power Systems Virtual Servers are a form of infrastructure as a service (IaaS). With the {{site.data.keyword.powerSys_notm}} service, you can quickly create and deploy one or more virtual servers (that are running either the AIX or IBM i operating systems) to the public cloud. After you provision the virtual server in the cloud, it is your responsibility to make sure that your operating system is secure.

Current AIX, IBM i, and Linux clients can use the {{site.data.keyword.powerSys_notm}} service for a number of workload scenarios, including disaster recovery, development environments, and partial IT infrastructure moves. {{site.data.keyword.powerSys_notm}} clients can stay competitive with the scaling of their infrastructure and remain flexible with their workload management and capacity both on- and off-premise. And since the infrastructure layer is identical, system administrators who run on-premises AIX, IBM i, and Linux systems today can use their same tools, workflows, and enhancements in the cloud.

## Key features
{: #key-features}

The following are some of the key features for the {{site.data.keyword.powerSys_notm}} service.

### Straightforward billing
{: #straightforward-billing}

The {{site.data.keyword.powerSys_notm}} service uses a monthly billing rate that includes the licenses for the AIX and IBM i operating systems. The monthly billing rate is pro-rated by the hour based on the resources that are deployed to the {{site.data.keyword.powerSys_notm}} instance for the month. When you create the {{site.data.keyword.powerSys_notm}} instance, you can see the total cost for your configuration based on the options that you specify. You can quickly identify what configuration options provide you with the best value for your business needs. For more information, see [Pricing](/docs/power-iaas?topic=power-iaas-pricing-virtual-server#pricing-virtual-server).

The {{site.data.keyword.powerSys_notm}} service does not provide Linux stock images. You must bring your own Linux image (OVA format) and subscription. Only Red Hat and SUSE Linux OVA images are currently supported. [Learn more](/docs/power-iaas?topic=power-iaas-using-linux)
{: note}

### Hybrid cloud environment
{: #hybrid-cloud}

You can use the {{site.data.keyword.powerSys_notm}} service to run any AIX or IBM i workloads off-premise from your existing Power Systems hardware infrastructure. Running your workloads in the public cloud allows you to enjoy all of the advantages the cloud has to offer such as self-service, fast delivery, elasticity, and connectivity to other IBM Cloud services. Although your AIX, IBM i, and Linux workloads are running in the cloud, you still keep the same scalable, resilient, production-ready features that Power Systems hardware is known to provide.

### Infrastructure customization
{: #infra-customization}

You can configure and customize the following options when you create a {{site.data.keyword.powerSys_notm}}:

* Number of virtual server instances
* Number of cores
* Amount of memory
* Data volume size and type
* Network interfaces

### Bring your own image
{: #bring-own-image}

IBM provides you with stock AIX and IBM i images when you create a {{site.data.keyword.powerSys_notm}}. However, you can always [bring your own](/docs/power-iaas?topic=power-iaas-deploy-custom-image) custom AIX or IBM i image that you've tested and deployed. The {{site.data.keyword.powerSys_notm}} service does not provide Linux stock images. You must bring your own Linux image (OVA format) and subscription. Only Red Hat and SUSE Linux OVA images are currently supported.

When provisioning a {{site.data.keyword.powerSys_notm}} to support SAP NetWeaver applications, select a version of the IBM-provided AIX operating system stock image. IBM i and operating system custom images are not supported for SAP workloads at this time.
{: note}

## Hardware specifications
{: #hardware-specifications}

The following IBM Power Systems can host a {{site.data.keyword.powerSys_notm}}: IBM Power System E880 (9119-MHE), IBM Power System S922 (9009-22A), and IBM Power System E980 (9080-M9S). For more information about these systems and how they're used inside the {{site.data.keyword.powerSys_notm}} service, see their data sheets and the hardware overview table.

If you'd like to compare your current environment's performance to what's available through the {{site.data.keyword.powerSys_notm}} service, see the [IBM Power Systems performance report](https://www.ibm.com/downloads/cas/K90RQOW8){: new_window}{: external}. For a more condensed comparison, see [IBM Power Systems CPW performance data comparison](https://www.itechsol.com/wp-content/uploads/2018/07/IBM-Power-Systems-CPW-Performance-Data-Comparison-P7-vs-P8-vs-P9-rev3-July-2018.pdf){: new_window}{: external}.
{: tip}

**Data sheets**

* [IBM Power System E880 (9119-MHE)](https://www-01.ibm.com/common/ssi/ShowDoc.wss?docURL=/common/ssi/rep_sm/5/872/ENUS9119-_h05/index.html&lang=en){: new_window}{: external}
* [IBM Power System S922 (9009-22A)](https://www.ibm.com/downloads/cas/KQ4BOJ3N){: new_window}{: external}
* [IBM Power System E980 (9080-M9S) - Frankfurt only](https://www.ibm.com/downloads/cas/VX0AM0EP){: new_window}{: external}

| Compute  | Storage   | Network   |
|--------- | --------- | --------- |
|<ul><li>Power e880 (9080-MHE)</li><li>Power s922 (9009-22A)</li></ul> | <ul><li>Storwize V7000F(2076-AF6) dual controller</li><li>Storwize V7000 (2076-624) dual controller </li><li>IBM SAN64B-6 (Brocade)</li></ul> | <ul><li>Cisco Nexus9000 93180YC-EX (10G)</li><li>Cisco Nexus9000 C9348GC-FXP (1G)</li><li>Avocent ACS8048</li></ul> |
{: class="simple-tab-table"}
{: tab-group="hardware"}
{: caption="Table 1. Hardware overview (Washington, D.C.)" caption-side="top"}
{: #hw-spec-1}
{: tab-title="Washington, D.C. (WDC04)"}

| Compute  | Storage   | Network   |
|--------- | --------- | --------- |
|<ul><li>Power e880 (9080-MHE)</li><li>Power s922 (9009-22A)</li></ul> | <ul><li>Storwize V7000F(2076-AF6) dual controller</li><li>Storwize V7000 (2076-624) dual controller</li><li>Tier-1 9846-AF8 FlashSystem 9150 dual controller</li><li>Tier-3 9846-AF8 FlashSystem 9150 dual controller</li><li>IBM SAN64B-6 (Brocade)</li><li>IBM SAN256B-6 (Brocade)</li></ul> | <ul><li>Cisco Nexus9000 C9336PQ  (Spine 10G)</li><li>Cisco Nexus9000 C93180YC (10G)</li><li>Cisco Nexus9000 C93108TC-EX (1G)</li><li>Cisco UCS - APIC controller</li><li>Cisco ASR1001-HX Router</li><li>Avocent ACS8016</li></ul> |
{: class="simple-tab-table"}
{: tab-group="hardware"}
{: caption="Table 2. Hardware overview (Dallas, TX)" caption-side="top"}
{: #hw-spec-2}
{: tab-title="Dallas (DAL13)"}

| Compute  | Storage   | Network   |
|--------- | --------- | --------- |
|<ul><li>Power E980 (9080-M9S)</li><li>Power s922 (9009-22A)</li></ul> | <ul><li>Tier-1 9846-AF8 FlashSystem 9150 dual controller</li><li>Tier-3 9846-AF8 FlashSystem 9150 dual controller</li><li>IBM SAN64B-6 (Brocade)</li><li>IBM SAN256B-6 (Brocade)</li><li>IBM SAN64B-6 (Brocade)</li></ul> | <ul><li>Cisco Nexus9000 N9K-C9364C (Spine 10G)</li><li>Cisco Nexus9000 9348GC-FXP (Leaf 1G) </li><li>Cisco Nexus9000 93180YC-FX (Leaf 25G)</li><li>Cisco UCS - APIC controller</li><li>Cisco ASR1001-HX Router</li><li>Avocent ACS8032DAC-400</li></ul> |
{: class="simple-tab-table"}
{: tab-group="hardware"}
{: caption="Table 3. Hardware overview (Frankfurt, Germany, and London, United Kingdom)" caption-side="top"}
{: #hw-spec-3}
{: tab-title="Frankfurt and London (FRA04/FRA05/LON06)"}

## Public and private networks
{: #public-private-networks}

When you create a {{site.data.keyword.powerSys_notm}}, you can select a private or public network interface.

**Public network**

* Easy and quick method to connect to a {{site.data.keyword.powerSys_notm}} instance.
* IBM configures the network environment to enable a secure public network connection from the internet to the {{site.data.keyword.powerSys_notm}} instance.
* Connectivity is implemented by using an IBM Cloud Virtual Router Appliance (VRA) and a Direct Link Connect on Classic connection.
* Protected by firewall and supports the following secure network protocols:
    * SSH
    * HTTPS
    * Ping
    * IBM i 5250 terminal emulation with SSL (port 992)

**Private network**

* Allows your {{site.data.keyword.powerSys_notm}} instance to access existing {{site.data.keyword.cloud_notm}} resources, such as IBM Cloud Bare Metal Servers, Kubernetes containers, and Cloud Object Storage.
* Uses a Direct Link Connect on Classic connection to connect to your IBM Cloud account network and resources.
* Required for communication between different {{site.data.keyword.powerSys_notm}} instances.

  For more information about the different options for configuring a private network, see [Configure a private network](/docs/power-iaas?topic=power-iaas-configuring-subnet).
  {: note}

<!-- The following figure displays the basic configuration for a public and private network:

![Displays how network traffic flows for public or private connection](/images/power-iaas-network1.svg "Displays how network traffic flows for public or private connection"){: caption="Figure 1. Private and public network configuration" caption-side="bottom"} -->
