# Reference Methodology for Agility

**_Original Authors_**

+ Asanka Abeysinghe, Vice President - Architecture, CTO Office | asankaa@wso2.com
+ Paul Fremantle, CTO and Co-Founder | paul@wso2.com

>This document describes a reference methodology for modern agile digital enterprises.  Our goal is to move organizations from the current maturity stage towards the integration agile stage.  The outcome of moving higher in the maturity model is to increase the productivity of employees, save costs by reallocating resources from a “center of excellence” to self-organized teams, and provide a better customer experience by being digitally aligned. The methodology for moving through these maturity stages involves people, process and technology.

## Introduction

As APIs, microservices, software as a service (SaaS), and serverless architectures evolve, integration is not fading away; instead almost every new application involves integration across an exploding set of endpoints. The microservices mantra of smart endpoints and dumb pipes fundamentally addresses a deeper problem. Integration must learn from code to become immutable, type safe, testable, continuously built and deployed  so they are more robust, resilient and above all - agile.

## A Methodology

A methodology formalizes an approach to achieve a particular goal or set of goals. Our end goal is to make an organization integration agile. The proposed methodology is an iterative process characterized by five stages. Additionally, the methodology defined in this document looks at the organizational improvements in three dimensions.

The methodology does not expect an organization to start from scratch, but rather to first conduct an assessment to understand the current state and define a path to move to the next desired level. This paper outlines a meta-process for organizations to refer and become integration agile.

## Maturity Model

A maturity model defines how an organization can measure the current stage of integration agility and defines a direction for improvement in three dimensions: people, process, and technology. There are two foundational elements for enabling the continuous improvement of an organization and move to the right in the maturity model:

+ For both people and process the foundation is the culture of an organization.

+ For technology the foundation is the architecture designed and implemented by the organization.

### Summary view

|  | Monolithic | Fast Waterfall | API-Driven | Early Agility | Integration Agile |
|---------|---------|---------|--------|--------|-------|
|**People**|Centralized|COE|API Teams|Decentralized|Self-Organised Teams|
|**Process**|Waterfall|Fast Waterfall|API Iterative|Semi-Continuous|Continuous|
|**Technology**|Silo|EAI/ESB|API-Driven|Early Agility|Continuous Agility|
|**Digital Alignment**|Separate|Ad-hoc|Early Strategic|Digital-First|Adaptive|

The maturity model defined here contains five stages, and each stage is defined in three dimensions. Let's look at each dimension in detail. 

### People

People and their ability to define solutions by understanding the current situation is the most important thing for an organization. Culture and the organizational structure control the way people operate, and it is the platform for enabling people’s productivity. Culture plays an important role in adapting to change. Habits and best practices inherited from an organization’s culture are more powerful than those merely enforced by policies.

![org structure](/media/rm-org-structure.png)

The organizational and decision-making structure affects how innovative ideas from each part of the organization are implemented and delivered to end-users. Traditional divided pyramid, hub and spoke structures create  a center-of-excellence (COE) mentality and can rapidly block the flow of innovation. As an alternative, we propose a podular organizational structure, which allows organizations to become adaptive, innovative and agile. People (organization & culture) must move from sequential waterfall and waterfall-agile approaches which include siloed “center of excellence” teams, to a fundamentally decentralized set of agile teams. In a podular structure, each of these teams then own the responsibility for building, running and managing their integration applications. One of the main characteristics of a podular organization structure is each pod act as an individual business unit [2] which allows to operate and take decisions independently as well as add the people with the required skills to the team.  

### Process

Process defines the steps an organization should take to achieve its goals. A process is connected with the people involved in its execution, as well as the technology being implemented to optimize their productivity. This document mainly focuses on defining a meta-process.

![sdp timeline](/media/rm-sdp-timeline.png)

While many software development processes have been introduced, we can put them all into two buckets: waterfall and agile. To date, there have been many attempts to become truly agile, but it has not been an easy task due to several technical and cultural constraints. As a result, many enterprises have had to fall back to waterfall-agile or fast waterfall processes. However, now we are living in an era with of DevOps improvements and extremely flexible deployment infrastructures, which create continuous processes that allow teams to operate in a truly agile manner.

### Technology

Although the reference methodology is fundamentally about people and process, it has technology requirements that must be met to enable the right processes and approach. For example, decentralized continuous integration/continuous development (CI/CD) with canary deployment requires a cloud orchestration model, such as Kubernetes. Agile development of integration applications requires integration tools that support continuous build, test and deployment. This is pushing a shift away from configuration-over-code approaches such as an enterprise service bus (ESB) towards code-over-configuration approaches that bring type validation and integrated development environment (IDE) integration and work more effectively with version control and CI/CD tooling. Integration applications must work in cloud native environments, including containers and serverless. Integration applications must be observable using distributed tracing and monitoring tools.

As we described earlier, architecture is the foundation for technology. Architecture references the maturity of the overall enterprise and integration architecture of the organization as well as the technology adoption. In the WSO2 Reference Architecture (RM) for Agility paper [1] we discussed three emerging architectural patterns; layered, segmented and cell-based, which can represent the enterprise and integration architecture implemented or planned in any organization. The desired architecture pattern has a direct impact on the technical usage and how an organization can enforce an agile approach (iterative architecture) in practice.

![evolution of architecture](/media/ra-evolution.png)

The architecture dimension represents the maturity of internal and external integration of the business, level of integration as well as how seamless.  

### Digital Alignment

Digital alignment is an outcome of the improvement of people, process and technology. Digital alignment mainly focuses on the maturity of digital transformation, both internally and externally, with employees and customers. Internally it affects how employees benefit from digital products and endpoints, such as APIs, events and streams, to increase their productivity and improve their decision-making process. Externally, it affects the experiences that customers and partners have with the digital products and endpoints focused on enabling an external transformation. In the current digital era, consumers are looking for a real-time, personalized, geo-sensitive and predictive experience from the products and the services they use.  

### Platform for Organizational Maturity

![RM platform](/media/rm-platform.png)

Together, culture and the architecture create a platform for enabling people, process, and technology to operate and improve. Culture plays the primary role in supporting people while architecture has the primary role in supporting technology. However, both of these foundations have overlapping and complementary roles in supporting all three pillars of digital alignment: people, process, and technology.

### Maturity Model: Current outlook

![maturity model](/media/rm-maturity-model.png)

## Agile Maturity Model: Matrix

|  | Monolithic | Fast Waterfall | API-Driven | Early Agility | Integration Agile |
|---------|---------|---------|--------|--------|-------|
|**People**|***Centralized***:Team is structured around a single project. |***COE***:Single or large development teams are controlled and governed by multiple centers of excellence (COE). Governance is complex.|***API Teams***:Teams are distributed; parallel projects are running, but dependencies and the execution model bring them back to waterfall.|***Decentralized***:Has distributed teams with centralized technology platforms and EA practices that create a COE.|***Self-Organised Teams***:Has decentralized teams and decision-making. Projects and systems connect by using the DevOps pipeline. Teams can rapidly and independently deliver projects.|
|**Process**|***Waterfall***:ollows a waterfall process. Executes one project at a time.|***Fast Waterfall***:Follows a waterfall or spiral method. Has lengthy project release cycles. Is highly non-agile.|***API Iterative***:End-user applications and API development follow an agile process by dividing into small teams.|***Semi-Continuous***:Continuous processes are tied to the central platform. Has one build pipeline, which creates another COE|***Continuous***:Has a pipeline-first approach for every project and individual release pipelines for each team/project. Processes are fully automated.|
|**Technology**|***Silo***:Legacy and COTS* operate as silos. There is little or no EA practice. Data is aggregated manually.|***EAI/ESB***:Relies on legacy EAI and/or ESB technologies. Is highly non-agile|***API-Driven***:API management is used within organizations to streamline governance and provide decentralized discovery.|***Early Agility***:Uses lightweight ESBs with continuous integration and test, but still centralized, with manual discovery, governance, and other processes. Early adoption to Microservice architecture is occuring.|***Continuous Agility***:Has automated decentralized integration with APIs, streams and events published and discovered in federated registries, and CI/CD. Uses a cell-based architecture.|
|**Digital Alignment**|***Separate***:Business runs individually. Edge of the business is disconnected from management.|***Ad-hoc***:The business connects with partners and has initiated digital transformation. However, only internal consumers benefit.|***Early Strategic***:Provides a basic digital experience for the customer in a batch or near real-time manner.|***Digital-First***:Is connected with the ecosystem. Provides a multi-channel digital experience to customers in real time or near real time. Each consumer has a digital identity.|***Adaptive***:Offers a comprehensive multi-channel digital experience for consumers. Adapts based on consumer feedback and demand using analytics and AI.|

(*Commercial off-the-shelf software. **Center of Excellence.)

## Maturity Model : Pragmatic view

![maturity model pv](/media/rm-maturity-model-pv.png)

The maturity model has a definite vertical separation of each stage, but most organizations might find it hard to fit into one vertical pillar. As a result, an organization may align with three different horizontal stages as depicted in the diagram. 

This approach helps an organization in planning the transformation and where to put more effort and focus. 

For example, an organization might move to a complete cloud-native infrastructure with a mature CI/CD pipeline, but the team structure might not be podular enough to have a genuinely agile enterprise.

## How to Move to the RIght in the Maturity Model: Methodology

>***“ Transformation is a journey without a destination”*** - Marilyn Ferguson

### Approach: Iterative business transformation

The overall approach of moving from one stage to another is iterative. Plan, implement, review, improve, and go back to plan. Also, start small by beginning with a small group, a single project, and one line of business instead of going for a company-wide approach. Skipping stages is dangerous because any change takes time for people to adopt and become productive. Therefore, minimizing change at each stage is an important factor in being able to continue business as usual while the transition is happening in parallel.








