---
marp: true
math: true
---

<!--
# Metadata
title: Software Development Life Cycle (SDLC)
author: Seb Blair (CompEng0001)
description: Lecture slides on Software Development Life Cycle (SDLC).
keywords: Software Development Life Cycle (SDLC)
lang: en

# Slide styling
theme: uog-theme
_class: lead title
paginate: true
_paginate: false
transition: fade 250ms

style: |
  header em { font-style: normal; view-transition-name: header; }
  header strong { font-weight: inherit; view-transition-name: header2; }
  header:not:has(em) { view-transition-name: header; }

  -->

<style scoped>
h1 {
view-transition-name: header;
display: flex;
align-items: center;
margin: 0 auto;
}
</style>

# Software Development Life Cycle (SDLC)

<div align=center style="font-size:76px;padding-left:300px;padding-right:300px;" >

```ts
const module: Module = {
  code: "COMP1929",
  name: "Software Engineering",
  credits: 15,
  moduleLeader: "Seb Blair BEng(H) PGCAP MIET MIHEEM FHEA"
};
```

</div>

<!-- _footer: "[Download as a PDF](https://github.com/UniOfGreenwich/COMP1929_Lectures/raw/main/content/SDLC/SDLC.pdf)" -->

----

<style scoped>
h1 {
view-transition-name: header;
display: flex;
align-items: center;
margin: 0 auto;
}
</style>


<!-- header: "_SDLC_" -->

## What is SDLC


The Software Development Lifecycle (SDLC) is a structured approach to software development that ensures the creation of high-quality software, delivered on time and within budget. 

<div class="columns-2" style="padding-top:50px;padding-left:250px;padding-right:150px" >
<div>

[1] Software Process Models
<br>
[2] Planning
<br>
[3] Requirements Engineering
<br>
[4] System Modelling
<br>

</div>
<div>

[5] Implementation
<br>
[6] Testing
<br>
[7] Deployment
<br>
[8] Maintenance

</div>
</div>

---

<!--class: lead-->

# Software Process Models

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<!-- header: "_SDLC_ > **Software Process Models**" -->

<div>

- **Waterfall**
  - A sequential software development model where each phase—requirements, design, implementation, testing, deployment, and maintenance—must be completed before moving to the next, making it ideal for well-defined projects with minimal expected changes.
<br>
- **Agile/Incremental Development**
  - A flexible, iterative approach emphasizing collaboration, customer feedback, and adaptive planning to deliver smaller, functional increments of software rapidly and efficiently.
<br>
- **DevOps**
  - A culture and set of practices combining development (Dev) and operations (Ops) teams to automate processes, improve collaboration, and ensure continuous integration and delivery (CI/CD) for faster and more reliable software delivery.

</div>


---

## Waterfall Model

![h:500 center](../../figures/waterfall.png)

---

## Waterfall Model - Appropriateness

<details>
<Summary> Question: What are the benefits of using this model? What kind of systems is this model good to be used for? </summary>

- **Embedded systems** – because the inflexibility of hardware the requirements need to be clear before any implementation is carried out

- **Critical systems** – there is a need for extensive safety and security analysis of the software specification and design.  They must be complete so that this analysis is possible. 

- **Large software systems**

</details>

---

## Agile/Incremental Development Model

![center](../../figures/incremental.png)

---

## Agile/Incremental Development 

- Based on the idea of developing an initial implementation, getting feedback from users, and evolving the software through several versions until the required system has been developed

- Specification, development, and validation activities are interleaved rather than separate, with rapid feedback across activities
- This is the most common approach for application systems and software product development

---

<!-- header: "SDLC > Software Process Models" -->

## Agile/Integration and Configuration

- Based on software reuse where systems are integrated from existing components or application systems (sometimes called COTS -Commercial-off-the-shelf) systems).

- Reused elements may be configured to adapt their behaviour and functionality to a user’s requirements

- Reuse is now the standard approach for building many types of business systems


---

<!-- header: "SDLC" -->


<!-- class: lead-->

# Planning

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<!-- header: "_SDLC_ > **Planning**" -->

<div style="padding-bottom:200px">

## Software Costs

</div>

<div style="padding-bottom:200px">

- Software costs often dominate computer system costs. The costs of software on a PC are often greater than the hardware cost

<br>

- Software costs more to maintain than it does to develop. For systems with a long life, maintenance costs may be several times development costs

<br>

- Software engineering is concerned with cost-effective software development

</div>

---

<div style="padding-bottom:50px">

## COCOMO (Constructive Cost Model)

</div>

<div style="padding-bottom:200px">

COCOMO is a software cost estimation model developed by Barry Boehm in 1981. It estimates the effort, cost, and time required to develop a software system based on project size.

- Three COCOMO Models:

  1. **Basic COCOMO**: Rough estimation based on project size.
  <br>
  2. **Intermediate COCOMO**: Considers cost drivers like hardware constraints, team experience.
  <br>
  3. **Detailed COCOMO (COCOMO II)**: Adds more precision with lifecycle phases.

</div>

---

<div style="padding-bottom:50px">

## Key Components of COCOMO

</div>

<div style="padding-bottom:20px">

1. **Size Estimation** (in KLOC - thousand lines of code)
   - Example: A project with 25,000 lines of code is 25 KLOC.
   
2. **Effort Equation Estimation**: 
   - Effort (in person-months*) = $a * (KLOC)^b$
   - Constants **a** and **b** differ for project types.

- Project Types in COCOMO

  1. **Organic**: Simple projects, small teams, well-understood problems (e.g., payroll systems).
  2. **Semi-detached**: Moderately complex, mixed teams (e.g., medium business systems).
  3. **Embedded**: Complex, real-time systems with stringent requirements.

*refers to the number of months a single person would take to complete a specific task or project, assuming full-time work.

</div>

---

<div>

## Effort Estimation Example

<div style="font-size:28px">

For a 25 KLOC organic project:
- Constants for organic project: **a = 2.4**, **b = 1.05**

<br>

$$ Effort\ =\ 2.4 \cdot (25)^{1.05}\ ≈\ 61.56\ person-months $$

<br>
<br>

## Development Time Estimation

Development time (TDEV)*:
$$TDEV\ =\ c\ \cdot (Effort)^d$$
- Constants: **c = 2.5**, **d = 0.38**

<br>

$$Time\ =\ 2.5 \cdot (61.56)^{0.38}\ ≈\ 13.36\ months$$

*actual calendar time required to complete the project.

</div>

---
<!-- header: "SDLC > Planning" -->

<div>

## COCOMO Advantages

- Objective estimates from historical data.
- Adaptable to different project types.
- Accounts for various development factors (personnel, tools, etc.).

## COCOMO Limitations

- Relies on accurate size estimation.
- Historical data may not suit modern practices.
- Assumes equal contribution of all code to effort.

</div>

--- 

<!-- header: "SDLC" -->


<!-- class: lead-->

# Requirments Engineering

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<!-- header: "_SDLC_ > **Requirments Engineering**" -->

<div> 

Developers and stakeholders work together to gather and define the software’s functional and non-functional requirements. This is followed by documenting the requirements in a formal specification to guide the development process 

<br>
<br>

- **Functional**
  - describes the specific behaviors, actions, or functionalities that a system must support
<br>
- **Non-functional**
  - specifies the quality attributes or constraints of a system, such as performance, security, scalability, and usability

<br>

*Covered in detail in week 3.*

</div>

--- 

<!-- header: "SDLC" -->


<!-- class: lead-->

# Design

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<!-- header: "_SDLC_ > **Design**" -->

<div>

System design is divided into high-level design (HLD) and low-level design (LLD). HLD defines the system architecture, while LLD focuses on specifics like data structures and algorithms

<br>

- **UML diagrams**
  - **Activity diagrams**, which show the activities involved in a process or in data processing .

  - **Use case diagrams**, which show the interactions between a system and its environment. 

  - **Sequence diagrams**, which show interactions between actors and the system and between system components.

  - **Class diagrams**, which show the object classes in the system and the associations between these classes.

  - **State diagrams**, which show how the system reacts to internal and external events. 
  
  <br>
  
  *Covered in week 4.

</div>

--- 

<!-- header: "SDLC" -->


<!-- class: lead-->

# Implementation (Coding)

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<!-- header: "_SDLC_ > **Implementation (Coding)**" -->


<div>

Developers begin writing the actual code based on the design documents. Version control systems are typically used, and the code is reviewed regularly to maintain quality

<br>

- **Reuse** Most modern software is constructed by reusing existing components or systems. When you are developing software, you should make as much use as possible of existing code.
<br>
- **Configuration management** During the development process, you have to keep track of the many different versions of each software component in a configuration management system.
<br>
- **Host-target development** Production software does not usually execute on the same computer as the software development environment. Rather, you develop it on one computer (the host system) and execute it on a separate computer (the target system).

<br>

*Covered in week 6*

</div>

---

<!-- header: "SDLC" -->


<!-- class: lead-->

# Testing

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<!-- header: "_SDLC_ > **Testing**" -->

<div>

The software undergoes rigorous testing, including unit, integration, and system testing, to identify and fix bugs. User Acceptance Testing (UAT) ensures the software meets the user's needs​.

<br>

- Feature Tests 

- Functional Testing

- Performace and Load Testing

- Security Testing

- Test Driven Development

- Unit Testing
  
- User Testing

<br>

*Covered in week 8*

</div>

---

<!-- header: "SDLC" -->


<!-- class: lead-->

# CI/CD (Deployment & Maintenance)

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<!-- header: "_SDLC_ > **CI/CD (Deployment & Maintenance)**" -->

<div>

- Once testing is completed, the software is deployed in the production environment. The deployment could be done in phases or all at once, depending on the project's scale​

- After deployment, the software enters the maintenance phase, where it is regularly updated, bugs are fixed, and improvements are made based on user feedback

![w:1300 invert](../../figures/cicdPipelines.png "centered")

*Covered throughout, but specifically week 11*

---

<!-- header: "SDLC" -->


<!-- class: lead-->

# Legal and Ethical 

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<!-- header: "_SDLC_ > **Legal and Ethical**" -->

<div>

## Software Engineering Ethics

- Software engineering involves wider responsibilities than simply the application of technical skills.

<br>

- Software engineers must behave in an honest and ethically responsible way if they are to be respected as professionals.

<br>

- Ethical behaviour is more than simply upholding the law but involves following a set of principles that are morally correct

<br>
<br>

**Question:** What are the key characteristics of ethical behaviour?

</div>

---

<div>

## Issues of professional responsibility

</div>

<br>

<div>

- **Confidentiality**
  - Engineers should normally respect the confidentiality of their employers or clients irrespective of whether or not a formal confidentiality agreement has been signed.

<br>

- **Competence**
  - Engineers should not misrepresent their level of competence. They should not knowingly accept work which is out with their competence.

</div>
</div>

---

<div>

## Issues of professional responsibility

</div>
<div>

- **Intellectual property rights**
  - Engineers should be aware of local laws governing the use of intellectual property such as patents, copyright, etc. They should be careful to ensure that the intellectual property of employers and clients is protected.

<br>

- **Computer misuse** - [CMA 1990](https://www.legislation.gov.uk/ukpga/1990/18/contents)
  - Software engineers should not use their technical skills to misuse other people’s computers. Computer misuse ranges from relatively trivial (game playing on an employer’s machine, say) to extremely serious (dissemination of viruses). 

</div>
</div>

---

<div>

## Computer Misuse Act 1990 


- Unauthorised access to computer material.
<br>
- Unauthorised access with intent to commit or facilitate commission of further offences.
<br>
- Unauthorised acts with intent to impair, or with recklessness as to impairing, operation of computer, etc.
<br>
- Unauthorised acts causing, or creating risk of, serious damage
<br>
- Making, supplying or obtaining articles for use in offence under section 1,3 or 3za

</div>

<!-- _footer: ![](../../figures/Legislation.png)-->

---

## ISO

![bg right:10% 90%](../../figures/iso_logo.png)

- **ISO/IEC/IEEE 12207:2017**
  - Systems and software engineering — Software life cycle processes

- **ISO/IEC/IEEE 15288:2023**
  - Systems and software engineering — System life cycle processes

- **ISO/IEC 25010:2023**
  - Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — Product quality model

- **ISO/IEC/IEEE 29119-1:2022**
  - Software and systems engineering — Software testing