# 19th July - Thesis Defense

*Good morning, my name is Francesca, and I am thrilled to present my thesis defense on the role of Oracle Cloud EPM Business Rules for Efficient Planning. 
I am deeply grateful to Prof. Matteo Francia for his guidance and support throughout this journey. 
Without further delay, let's move to the content of the project.*

## Overview

This thesis is linked to an actual implementation process for a Holding Group which is a global leader in the fashion and design industry.

- **Introduction**: We will start with a brief overview of the project, exploring its scope, objectives and requirements.
- **EPM**: We will deepen the concept of EPM, analyzing its benefits and challenges.
- **Oracle Cloud EPM**: We will explore the Oracle Cloud EPM implementation journey with all its phases.
- **Costs and Revenues in EPM**: We will then move to the core part of the project - my role in the implementation - which regards the management of revenues and costs in the EPM environment. We will see two key processes, which are:
- **Cost allocation**
- **Intercompany management**
- **Conclusions**: Finally, we will get some insights and final thoughts about the project.

## Introduction 

### Slide 1

In today's highly competitive business environment and, with the advent of **digital transformation**, companies are now offered with huge opportunities and challenges.

One of the prerequisites to stay competitive in the digital era is to be able to effectively manage **corporate performance** using performance management systems.

The goal of this project is to improve the overall financial performance of the Holding Group by improving data accuracy and gaining real-time **visibility** into financial data across all the Entities which compose the Group.

Prior to this implementation, the Holding Group faced significant **challenges** in accessing and **consolidating** financial data from across the Entities.

So, with this **EPM system**, they plan to achieve an **integrated view** of the data belonging to the different Entities, which can be used for planning, reporting, budgeting and forecasting purposes.

### Slide 2

The requirements for the project fall within the goal of designing and maintaining a **comprehensive** and **integrated** planning solution to gain visibility and control over the Group's performance. 

This implementation project is addressed to the **Management Control Department** of the Holding Group, which is responsible for assessing the financial situation and evaluating the overall performance of the Entities.

Of course, the EPM system will be used by the different **Brands**, meaning that it should be tailored to their needs.

At the same time, the system should be easy to use, flexible, customizable and **scalable**, in order to adapt to future expansion or changes in the Group structure.

## Enterprise Performance Management

### Slide 1

Enterprise Performance Management refers to the management approach which **integrates** multiple business processes to allow organizations to gain visibility into their **performance**. 
It allows them to plan, measure, analyze and optimize performance, resulting in improved **decision-making** and higher profitability.

Here, we can see the Enterprise Performance Management Framework, which is composed of three phases: Strategy, Execution and Performance.

The **strategy** phase is the foundation of the EPM cycle as it refers to the definition of the strategic goals to achieve.
Then, the **execution** phase focuses on implementing the strategies set during the previous phase, ensuring that day-to-day activities are in line with the overall goals of the organization.
Finally, the **performance** phase involves evaluating the organization's performance deriving insights in order to drive continuous improvement.

### Slide 2

As organizations strive for excellence, EPM offers them a **systematic approach** to measure and improve performance across various dimensions.
We can identify different **benefits** and **challenges** associated with its implementation.

First, it facilitates improved **performance measurement** and **reporting** capabilities.
At the same time, it enhances **transparency** and accountability, fostering trust and communication within the organization.

Another benefit regards its ability to support **strategic alignment** as, by integrating performance management with strategic objectives, organizations can ensure that day-to-day activities align with long-term goals.

On the other hand, implementing and EPM solution can pose **challenges** for organizations, like, resistance to change, resource constraints or the need for a robust **technology infrastructure**.

## Oracle Cloud EPM Implementation

### Slide 1

The Holding Group has a complex **financial structure** and was facing significant challenges in managing financial data across the Entities.
Also, its reporting processes were inefficient, relying heavily on manual data entry and lacking **visibility** across the Brands.

The first step in the creation of the EPM solution is the selection of the most **suitable tool** among the ones available.

Here, we can see the **Gartner Magic Quadrant** for financial planning software published in 2022.
As we can see, **Oracle Cloud** has been named Leader as it is recognized for its ability to provide a **comprehensive** and **customizable** EPM solution.

Oracle Cloud EPM brings together multiple capabilities into a **single suite**, ranging from financial planning to cost management and tax reporting.

For the Holding Group, Oracle Cloud EPM was the right choice due to its ability to be **customized** to meet the specific needs of the organization.

### Slide 2

To better explain the implementation process, let's start by getting a comprehensive understanding of the **elements involved** in the process.

The suite of Oracle Cloud EPM includes various **modules** that are designed to address specific business needs.
For this project, we will focus on **Planning and Budgeting**, which offers a cloud environment that allows organizations to streamline their processes in a collaborative environment with flexible modeling and real-time visibility.

One fundamental component of Oracle Cloud EPM refers to **Dimensions**.
Considering that we are working with Multidimensional Databases, dimensions provide a way to organize data, allowing users to perform complex calculations among them.

Dimensions are typically structured as **hierarchies**, with each level representing a different **level of detail**, and we usually have a dimension for each domain of the process.
Here, we can see some of the dimensions of the database, which are the Geography dimension, Channel of Distribution, Product, Brand and Entity.

### Slide 3

To load financial data into the system, we need to undertake a process of **data normalization** and **mapping**, in order to align data coming from different sources to the dimensions and members in the target system.

Of course, the different Entities have different **data collection** tools and methodologies, ranging from, for example, ERP software solutions like SAP, Excel spreadsheets or Cloud solutions.

The process of data load run **continuously** in order to keep the EPM system up-to-date with respect to the financial situation of the Holding Group.
Therefore, it is important to **update** the loading process **systematically** to allow the system to run smoothly and meet changes in business operations.

## Costs and Revenues Management

Enterprise Performance Management encompasses various processes and methodologies aimed at managing and improving the **financial performance** of an organization. 
**Revenue** and **cost** management plays crucial roles in ensuring effective financial planning and analysis.

In this regard, while working on various sections of the EPM solution, two **implementations** emerged as particularly relevant, showcasing how **Oracle Cloud EPM** can meet specific needs of customers: Cost Allocation and Intercompany Management.

### Slide 1 - Cost Allocation

Cost allocation refers to the process of assigning and **distributing costs** to various departments or divisions within the organization.

This process follows some **policies**, specific to the Holding Group, that are personalized to align with the specific needs and characteristics of the Entities.

One of the significant **challenges** faced during this implementation process regards the fact that the different Entities have different **data collection** tools, resulting in variations in the **granularity level** of the financial data.

To address this issue, the process uses specific cost drivers, set by the Holding Group, which goes around three dimensions: Brand, Geography and Channel.

### Slide 2 - Cost Allocation

We start by having costs on different **combinations** of Brand, Geography and Channel, with different levels of **details**.
These elements, can be of three types:

- They can be **specific**, meaning that the expense was incurred by a specific Brand, in a specific country and through a specific Channel of distribution.
- The member can be **unknown**, meaning that the expense should be allocated in order to identify the attributable Brand, Geography and Channel.
- It can be a **Member_ToAllocate**, meaning that the element is given but represents a lower level of detail. For example we can have a group of countries like EMEA or a group of Brands which includes some others.

The goal here is to reach the maximum level of detail through **cost drivers** and to do so, we built some **business rules**.
But what are Business Rules: they can be considered as a set of calculations, written in a specific language supported by Oracle, which can be used to perform data manipulations across the database.

The allocation process starts by assessing the **validity** of the driver based on the combination of Brand, Geography and Channel to allocate.
Then, if the driver is valid, the rule proceeds with the **cancellation** of the cost on the initial intersection and its subsequent **distribution** according to the percentage specified in the driver.

### Slide 3 - Intercompany

The second implementation regards the process of **intercompany management**, which refers to financial transactions that occur between Entities of the same parent company.

Sending goods and services among related Entities is a common practice but, it is important to note that such transactions can introduce **complexities** in financial reporting and consolidation.
That because, when intercompany transactions are not appropriately **accounted** for and **eliminated** during the consolidation process, they can distort the financial statements and create an **artificial economic value** within the Group.

### Slide 4 - Intercompany

Intercompany transactions involve a **two-way relationship** between entities: on one side, an Entity records a revenue in its local currency, while on the other side, another Entity incurs a cost in its local currency. 
This creates a **complex intersection** of financial relationships that need to be accurately
identified, matched, and eliminated during the consolidation process. 

The complexity increases further when considering the concept of **data protection**: each
Entity operates independently and cannot have **unrestricted** access to the financial data of other entities.

To overcome this issue of **restricted access**, we designed a system where data about intercompany transactions are inputted only by one Entity and the associated Entity will be **automatically retrieved** by means of specific functions.

## Conclusions

### Slide 1

Throughout the implementation process, I had the opportunity to gain valuable insights into **best practices** practices for Oracle Cloud EPM implementation.

These include:

- **Data accuracy**, as it directly impacts the quality and reliability of financial data;
- **Stakeholder engagement**, to ensure that the solution aligns with the needs and expectations of users;
- **Clear communication**, which is especially crucial when it comes to technical and functional requirements;
- **Continuous improvement**, to drive ongoing optimization within the EPM framework.

### Slide 2

These two implementations clearly illustrate the ability of **Oracle Cloud EPM** to be **customized** to meet the specific requirements of the Organization.

Through this system, we were able to **automate** critical processes such as financial consolidation, budgeting, cost allocation or intercompany management, all by leveraging Oracle Cloud **business rules**.
These rules enabled the creation of ad-hoc **calculations** and **workflows**, which allowed the Holding Group to efficiently streamline their **planning** and **reporting** processes.

## Thank you and Q&A