# Chapter 5: Virtual Machines Provisioning and Migration Services

## Introduction and Inspiration

- **Cloud Computing** builds on:
  - **Service-Oriented Architecture (SOA)**
  - **Grid Computing**
  - **Virtualization Technology**
  
- **Infrastructure as a Service (IaaS)**:
  - Cloud infrastructure is provided as a **public utility service**.
  - Based on **pay-as-you-use** and **on-demand** models.
  - **Provisioning cloud infrastructure** in data centers is crucial.
  - Time-consuming to set up systems and applications on physical machines.

### Key Concepts:
1. **Grid Computing**:
   - A network of computers that work together on a need basis.
   - Computers can operate independently.
   - Used internally by organizations.
   - **Grid computing** is a distributed architecture that combines computer resources from different locations to achieve a common goal.  It breaks down tasks into smaller subtasks, allowing concurrent processing.


2. **Virtual Machine (VM) Provisioning**:
   - Time-consuming tasks like installing servers, operating systems (OS), and services.
   - With **virtualization technology**, servers can be provisioned faster.
   - VM provisioning through public clouds (e.g., Amazon EC2) or private cloud setups.
   - With virtualization, **server maintenance and upgrades** are easier and faster.

---

## Virtualization Technology Overview

### Definition:
- **Virtualization** is the abstraction of four key computing resources:
  - Storage
  - Processing Power
  - Memory
  - Network or I/O

- **Emulation**: The system pretends to be another system.
- **Virtualization**: A system pretends to be multiple systems.

![[Pasted image 20241020185628.png]]

### Virtualization Architecture:
| Layer                          | Description                                                                 |
|---------------------------------|-----------------------------------------------------------------------------|
| **Virtualization Layer (VMM or Hypervisor)** | Partitions physical resources into multiple VMs. |
| **Physical Server Layer**       | The underlying hardware that VMs share.                                      |

- Virtualization improves resource utilization by **multiplexing** VMs on one physical host.
- **Server consolidation**: Scaling machines up and down on demand.
- Supports **on-demand cloning** and **live migration services**.

---

## Public Cloud and Infrastructure Services

- **Amazon Elastic Compute Cloud (EC2)**:
  - Provides **elastic compute capacity** in the cloud.
  - Offers multiple pre-built **Amazon Machine Images (AMIs)** with various OS and software.
  - Enables **quick scalable capacity** as per resource needs.
  
### EC2 Instance Types:
| Instance Type | Resources               |
|---------------|-------------------------|
| **Small, Large, Extra Large** | Based on general resources needed. |
| **High CPU Instances**        | For medium to extra-large CPU needs. |
| **High Memory Instances**     | Extra-large, double, and quadruple instances. |

---

## Private Cloud and Infrastructure Services

- **Private Clouds** allow organizations to provision services in a self-service manner, optimizing resource utilization.
- Examples:
  - **Eucalyptus**
  - **OpenNebula**

### Hybrid Cloud:
- Combines **private/internal** and **external/public** cloud resources.
- Outsources non-critical services to the public cloud while keeping critical services internal.

---

## Distributed Management of Virtualization

- Virtualization requires **powerful management** tools.
- Several products manage virtual resources:
  - **OpenNebula**
  - **IBM Virtualization Manager**
  - **VMware DRS**
  
- Initiatives like the **Reservoir Project** enable interoperability between cloud providers.

---

## High Availability

### Definition:
- Ensures **operational continuity** with minimal downtime.
  
### Key Features:
- Virtual environments provide **automatic VM restart** in case of hardware or VM failure.
- High availability reduces service interruption and downtime.

### Service-Level Agreement (SLA):
- Formalizes the **service availability objectives**.
- Determines **monthly availability** or downtime and calculates service credits accordingly.

---

## Cloud and Virtualization Standardization Efforts

- **Distributed Management Task Force (DMTF)**:
  - Provides standards for managing virtualization.
  - **Virtualization Management (VMAN)** initiative supports interoperability.
  - **Open Virtualization Format (OVF)** allows secure distribution of virtual appliances.

- **Open Cloud Computing Interface (OCCI)** by the **Open Grid Forum (OGF)**:
  - Provides a standard API for cloud IaaS.
  - Enables development of interoperable tools for deployment, scaling, and monitoring.

---

## Virtual Machine Provisioning Process

1. **Selecting a server** from a pool with the appropriate OS.
2. **Loading software** such as OS, middleware, and applications.
3. **Customizing the machine** to configure network and storage resources.

- VMs can be provisioned:
  - Using **pre-configured VM templates**.
  - By **cloning existing VMs**.
  - Using **Physical-to-Virtual (P2V)** tools to virtualize physical servers.

### Benefits of VM Provisioning:
- Reduces the time required to provision a new VM.
- Rapid VM provisioning can lead to **VM sprawl**, complicating lifecycle management.

---

## Virtual Machine Migration Services

- **Migration** moves VMs between hosts or storage locations.
- Types of migration:
  - **Hot/Live Migration**: Moving VMs while they are running, with minimal downtime.
  - **Cold Migration**: Moving VMs while they are powered off.

### Migration Techniques:
| Stage                      | Description                                               |
|-----------------------------|-----------------------------------------------------------|
| **Pre-Migration**            | VM exists on Host A.                                       |
| **Reservation**              | Resources reserved on Host B for migration.                |
| **Iterative Pre-Copy**       | Pages transferred to Host B, updating dirty pages.         |
| **Stop-and-Copy**            | VM is suspended on Host A, CPU state transferred.          |
| **Commitment**               | Host B receives the VM state and acknowledges transfer.    |
| **Activation**               | VM starts on Host B, with device drivers reattached.       |

### Example Tools:
- **VMware vMotion**
- **Citrix XenServer XenMotion**

Both allow migration of VMs with minimal downtime, enabling **zero-downtime server maintenance**.
