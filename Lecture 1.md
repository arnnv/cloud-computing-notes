## Syllabus Overview (DS3104)

1. **Introduction to Cloud Computing**
2. **Virtualization and Infrastructure as a Service**
3. **Hyper-Converged Infrastructure**

---

## Leading Cloud Service Providers (Q1 2024)

| Provider                  | Market Share |
| ------------------------- | ------------ |
| Amazon Web Services (AWS) | 31%          |
| Microsoft Azure           | 25%          |
| Google Cloud              | 11%          |
| Alibaba Cloud             | 4%           |
| IBM Cloud                 | 3%           |
| Oracle Cloud              | 2%           |
| Tencent Cloud             | 2%           |

---

## Introduction to Cloud Computing

**Definition:** Cloud computing is a techno-business disruptive model utilizing distributed large-scale data centers (private, public, or hybrid). It offers customers a scalable virtualized infrastructure and services, governed by **Service Level Agreements (SLAs)**, and is charged based on consumption of IT resources.

#### Google definition

Cloud computing is the on-demand availability of computing resources (such as storage and infrastructure), as services over the internet. It eliminates the need for individuals and businesses to self-manage physical resources themselves, and only pay for what they use.

---

## Cloud, Fog, and Edge Computing

In the context of cloud computing, it's essential to understand the differences between **Cloud Computing**, **Fog Computing**, and **Edge Computing**.

#### 1. **Cloud Computing**

- **Definition**: A model that enables access to a shared pool of configurable computing resources (e.g., networks, servers, storage, applications, and services) over the internet.
- **Key Characteristics**: Centralized data processing and storage, scalability, and remote access.
- **Example**: AWS, Microsoft Azure.

#### 2. **Fog Computing**

- **Definition**: A decentralized computing infrastructure where data, storage, and applications are distributed between the data source and the cloud.
- **Key Characteristics**: Acts as an intermediary between edge devices and the cloud, enabling low-latency processing closer to the edge.
- **Example**: A smart traffic light system using fog nodes to process traffic data locally before sending relevant insights to the cloud.

#### 3. **Edge Computing**

- **Definition**: A computing model that brings data processing closer to the data source (such as IoT devices) to reduce latency and bandwidth usage.
- **Key Characteristics**: Data is processed at or near the device generating it, often bypassing the need to send data to the cloud for processing.
- **Example**: Autonomous vehicles processing sensor data locally to make real-time decisions without relying on cloud connectivity.

| Feature               | Cloud                       | Fog                                | Edge                              |
|-----------------------|-----------------------------|------------------------------------|-----------------------------------|
| **Latency**            | Highest                     | Medium                             | Lowest                            |
| **Scalability**        | High, easy to scale         | Scalable within network            | Hard to scale                     |
| **Distance**           | Far from the edge           | Network close to the edge          | At the edge                       |
| **Data Analysis**      | Less time-sensitive data    | Real-time, decides locally or send to cloud | Real-time, instant decision making |
| **Computing Power**    | High                        | Limited                            | Limited                           |
| **Interoperability**   | High                        | High                               | Low                               |
![[Pasted image 20241020182128.png]]

---
# NIST Visual Model of Cloud Computing

![[Pasted image 20241020182213.png]]

---
## Essential Characteristics of Cloud Computing

Cloud computing systems exhibit five essential characteristics, which distinguish them from traditional IT infrastructure.

### 1. **On-Demand Self-Service**
- It's there when you need it
- Users can automatically provision computing resources (such as server time and network storage) as needed without requiring human intervention from the service provider.
- Example: A user can increase storage capacity via a management console without contacting support.

### 2. **Broad Network Access**
- Tons of connectivity options
- Cloud services are available over the network and can be accessed through standard mechanisms across various devices (e.g., laptops, mobile phones, tablets).
- This characteristic ensures accessibility from any geographical location, improving user experience.
  
### 3. **Resource Pooling**
- Sharing who-knows-where resources
- The cloud service provider’s computing resources are pooled to serve multiple customers using a multi-tenant model. 
- Physical and virtual resources are dynamically assigned and reassigned according to customer demand.
- Resources include storage, processing, memory, and network bandwidth.
  
### 4. **Rapid Elasticity**
- You get what you need
- Cloud computing resources can be quickly scaled up or down to meet user demand. 
- This elasticity appears to be infinite to the consumer, as they can provision any number of resources at any time.

### 5. **Measured Service**
- You get what you pay for
- Cloud systems automatically control and optimize resource use by leveraging a metering capability (e.g., for storage, processing, bandwidth).
- Resource usage can be monitored, controlled, and reported to provide transparency for both the provider and the consumer.

---

## Cloud Service Models

Cloud services are typically categorized into three broad models, each with varying levels of control, flexibility, and responsibility:

| Service Model                          | Description                                                                                                                                                                                                                                                                                                              |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Infrastructure as a Service (IaaS)** | Users are provided with virtualized computing resources over the internet. The user manages the infrastructure components such as virtual machines (VMs), storage, and networks, while the provider handles the underlying physical hardware. **Examples**: Amazon Web Services (AWS), Microsoft Azure Virtual Machines. |
| **Platform as a Service (PaaS)**       | The provider delivers hardware and software tools (like a platform) over the internet. Users focus on application development while the provider manages the underlying infrastructure, including servers, storage, and networking. **Examples**: Google App Engine, Microsoft Azure App Service.                        |
| **Software as a Service (SaaS)**       | A complete software solution provided over the internet. Users access software applications through the web, and the provider manages everything from infrastructure to application logic. **Examples**: Microsoft 365, Google Workspace, Salesforce.                                                                    |

![[Pasted image 20241020182352.png]]

### Detailed Explanation of Cloud Service Models:

1. **Infrastructure as a Service (IaaS)**:
   - IaaS provides the most flexibility and management control over IT resources. It allows users to rent computing power, storage, and networking resources on a pay-as-you-go basis.
   - Users can install their own software, including operating systems, databases, and applications.
   - IaaS is ideal for IT administrators looking to build and manage their infrastructure with minimal physical resource investment.
   
   **Advantages**:
   - Full control over the infrastructure.
   - Scalability based on needs.
   
   **Disadvantages**:
   - Requires a higher level of technical knowledge and management effort.

2. **Platform as a Service (PaaS)**:
   - PaaS is an environment for developers to build and manage applications without worrying about underlying infrastructure.
   - The provider manages everything from hardware to software, while the user can focus on deploying applications.

   **Advantages**:
   - Faster development and deployment.
   - No need to manage servers, databases, or networking.
   
   **Disadvantages**:
   - Limited customization and control over the environment.

3. **Software as a Service (SaaS)**:
   - SaaS delivers software over the internet, where users can access the application from anywhere using a web browser.
   - All underlying infrastructure, middleware, and application logic are managed by the provider.
   
   **Advantages**:
   - Simple to use, as the user doesn’t need to handle any infrastructure.
   - Quick access to applications without installation.
   
   **Disadvantages**:
   - Less control over data and software configurations.

### Pizza as a Service Analogy:

| Model        | You Manage                           | Vendor Manages               |
|--------------|--------------------------------------|------------------------------|
| **On-Premises** | Everything (oven, fire, toppings)     | Nothing                       |
| **IaaS**      | Toppings, Pizza Dough                | Oven, Fire                    |
| **PaaS**      | Toppings                            | Dough, Oven, Fire             |
| **SaaS**      | None (Enjoy pizza)                  | Everything (Oven, toppings)   |

---

## Cloud Deployment Models

The cloud can be deployed in various ways depending on the organizational needs and the level of control required.

| Model               | Description                                                                                                                                                                                                                                                                                                                                                           |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Public Cloud**    | Infrastructure is owned and operated by a third-party cloud service provider. All resources are shared, and it is available to the general public over the internet. Examples include AWS, Microsoft Azure, and Google Cloud.                                                                                                                                         |
| **Private Cloud**   | Infrastructure is exclusively used by a single organization. It can be physically located on-site or hosted by a third-party service provider, but all resources are dedicated to that organization. This offers greater control and security but at a higher cost.                                                                                                   |
| **Community Cloud** | Infrastructure is shared among multiple organizations that have similar requirements, such as security policies, regulatory concerns, or compliance needs. Examples include government institutions or healthcare organizations.                                                                                                                                      |
| **Hybrid Cloud**    | A combination of two or more cloud models (public, private, or community). Hybrid clouds allow for data and application sharing between environments, providing greater flexibility and optimized infrastructure use. This model is often used when organizations need to keep sensitive data private while using public cloud resources for less critical workloads. |

### Detailed Explanation of Cloud Deployment Models:

1. **Public Cloud**:
   - Owned and managed by third-party cloud providers. 
   - It offers services over the internet, and resources are shared among multiple users.
   - **Advantages**: Cost-effective, easily scalable, no maintenance required by the user.
   - **Disadvantages**: Less control over data, security concerns due to shared resources.

2. **Private Cloud**:
   - Designed for exclusive use by a single organization.
   - It can be managed internally or by a third-party provider but ensures that all resources are dedicated solely to the organization.
   - **Advantages**: Enhanced security, full control over the infrastructure.
   - **Disadvantages**: Expensive to set up and maintain, less scalable compared to the public cloud.

3. **Community Cloud**:
   - Shared by multiple organizations that have common concerns (e.g., regulatory, security, compliance needs).
   - It can be managed internally or by a third-party provider.
   - **Advantages**: Tailored to specific industry needs, shared cost and responsibility.
   - **Disadvantages**: Shared resources might limit customization, potential security risks if managed externally.

4. **Hybrid Cloud**:
   - Combines public and private clouds to offer greater flexibility.
   - This model is ideal for businesses that need to keep critical workloads private while benefiting from the scalability of the public cloud.
   - **Advantages**: Optimized resource usage, enhanced security for sensitive data, flexibility.
   - **Disadvantages**: Complex to manage, requires ensuring compatibility between different cloud environments.

![[Pasted image 20241020182456.png]]

---

## Why Adopt Cloud Computing?

### Benefits:

| Feature                       | Description                                                                                             |
| ----------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Scalability**                | Easily scalable to meet demand.                                                                         |
| **Elasticity**                 | Resources can be allocated and deallocated based on needs.                                              |
| **Lower Infrastructure Cost**  | No need for physical resources. Pay-per-use model reduces upfront costs.                                |
| **Availability**               | Access from anywhere in the world.                                                                      |
| **Collaboration**              | Enables seamless collaboration on common data.                                                          |
| **Risk Reduction**             | Test new ideas with minimal investments.                                                                |
| **Reliability**                | Higher reliability due to redundancy and SLAs.                                                          |

---

## Barriers to Cloud Adoption

| Barrier                           | Description                                                                            |
| --------------------------------- | -------------------------------------------------------------------------------------- |
| **Security**                      | Lack of control and knowledge over data storage locations.                             |
| **Interoperability**              | Lack of universal standards for cloud services, leading to vendor lock-in.             |
| **Resource Control**              | Varying degrees of control over the cloud environment.                                 |
| **Latency**                       | Internet-based access introduces latency in communication.                             |
| **Platform/Language Constraints** | Limited support for specific platforms or languages.                                   |
| **Legal Issues**                  | Concerns around data jurisdiction, protection, and compliance with international laws. |

---

## Virtualization

**Definition:** Virtualization separates the operating system (OS) from the underlying hardware. It allows running multiple OS instances on a single physical machine through virtualization software.

### Types of Virtualization:

- **Client Installed Virtualization:** Installed on endpoints like laptops, enabling virtual application execution.

![[Pasted image 20241020182518.png]]

- **Hypervisor:** A powerful, server-installed software managing virtual machines (VMs). Provides higher reliability and fault tolerance.

![[Pasted image 20241020182545.png]]

|Virtualization|Description|
|---|---|
|**Client-Installed**|Software enabling virtual applications on endpoints.|
|**Hypervisor**|Installed on physical servers, it allows creating and managing VMs efficiently.|

---

## Hyper-Converged Infrastructure (HCI)

**Definition:** HCI combines storage, computing, and networking into a single system, reducing complexity and increasing scalability. It relies on virtualization technologies and intelligent software for seamless operation.

### Benefits of Hyper-Converged Infrastructure:

|Feature|Description|
|---|---|
|**Simplicity**|Reduces data center complexity by consolidating all components into one system.|
|**Scalability**|Easily scalable by adding nodes to the pool of resources.|
|**Cost Efficiency**|Reduces costs in terms of power, space, and infrastructure maintenance.|
|**High Availability**|Provides high availability through built-in redundancy and failover mechanisms.|
|**Data Protection**|Data is protected through replication and wide-striping mechanisms.|

### Comparison: Traditional vs Hyper-Converged Infrastructure

|Feature|Traditional Infrastructure|Hyper-Converged Infrastructure|
|---|---|---|
|**Complexity**|Higher, requires managing separate components|Lower, as all components are unified|
|**Cost**|Higher due to dedicated resources for each component|Lower due to efficient resource usage and management|
|**Performance**|Moderate|High, with optimized use of hardware and resources|
|**Scaling**|Complex and expensive|Simple and cost-efficient|
### Disadvantages of Hyper-Converged Infrastructure (HCI):

1. **Initial High Cost**: The upfront investment in hyper-converged infrastructure is often expensive. Since HCI integrates compute, storage, and networking into a single system, the initial setup cost can be higher compared to traditional infrastructure where components can be purchased separately.
    
2. **High Cost for Scaling**: Expanding resources in HCI can also be costly. As compute, storage, and networking are bundled together, scaling often requires adding new nodes, leading to higher expenses compared to traditional systems where individual components can be scaled separately.
    
3. **Vendor Lock-In**: HCI solutions are typically provided by specific vendors as a complete package. This can limit flexibility and tie organizations to a single vendor for all infrastructure needs (networking, compute, and storage), making it harder to switch to other solutions.

---

## Conclusion

Cloud computing is a transformative technology enabling organizations to scale efficiently, reduce costs, and improve agility. It offers various service models (IaaS, PaaS, SaaS) and deployment models (Public, Private, Hybrid) tailored to different needs. Virtualization and Hyper-Converged Infrastructure further enhance cloud solutions by offering flexibility, efficiency, and cost benefits.
