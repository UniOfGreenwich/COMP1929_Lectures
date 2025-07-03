---
marp: true
---

<!--
# Metadata
title: Kanban
author: Seb Blair (CompEng0001)
description: Lecture slides on Kanban
keywords: Kanban
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

# Kanban

<div align=center style="font-size:76px; padding-left:300px;padding-right:300px;" >

<!-- _footer: "[Download as a PDF](https://github.com/UniOfGreenwich/COMP1929_Lectures/raw/main/content/Kanban/kanban.pdf)" -->

```Go
module := Module{
	Code:         "COMP1929",
	Name:         "Software Engineering",
	Credits:      15,
	ModuleLeader: "Seb Blair BEng(H) PGCAP MIET MIHEEM FHEA",
}
```

---

<style scoped>
h1 {
view-transition-name: header;
display: flex;
align-items: center;
margin: 0 auto;
}
</style>


<!-- header: "_Kanban_" -->


## Introduction

- Developed by Taiichi Ohno(Industrial Engineer and Businessman) for Toyota automotive. 

<br>

- early 1940's 

<br>

- Simple planning system, the aim of which was to control and manage work and inventory at every stage of production optimally.

<br>

- David J. Anderson who was the first to apply the concept to IT, Software development and knowledge work in general in the year 2004

![bg right:40% 50% vertical drop-shadow](https://www.nimblework.com/wp-content/uploads/2022/12/Taiichi_Ohno1.webp)
![bg right:40% 50% vertical drop-shadow](https://opexlearning.com/resources/wp-content/uploads/2014/09/david-j-anderson-leankanban.png)

---

## Four Foundational Principles

<style scoped>ul { list-style: list; padding: 200; }</style>

<div style="padding-top:150px">

[1] Start with what you are doing now

<br>

[2]. Agree to pursue incremental, evolutionary change

<br>

[3] Initially, respect current roles, responsibilities and job-titles

<br>

[4] Encourage acts of leadership at all levels


</div>

<!--
Start with what you are doing now: The Kanban Method (hereafter referred to as just Kanban) strongly emphasizes not making any change to your existing setup/ process right away. Kanban must be applied directly to current workflow. 

Any changes needed can occur gradually over a period of time at a pace the team is comfortable with.

Agree to pursue incremental, evolutionary change: Kanban encourages you to make small incremental changes rather than making radical changes that might lead to resistance within the team and organization.

Initially, respect current roles, responsibilities and job-titles: Unlike other methods, Kanban does not impose any organizational changes by itself. So, it is not necessary to make changes to your existing roles and functions which may be performing well. The team will collaboratively identify and implement any changes needed. These three principles help the organizations overcome the typical emotional resistance and the fear of change that usually accompany any change initiatives in an organization.

Encourage acts of leadership at all levels: Kanban encourages continuous improvement at all the levels of the organization and it says that leadership acts don’t have to originate from senior managers only. People at all levels can provide ideas and show leadership to implement changes to continually improve the way they deliver their products and services.
-->
---

## Six Practices of the Kanban Method

<style scoped>ul { list-style: list; padding: 200; }</style>

<div style="padding-top:100px">

[1] Visualize the flow of work

<br>

[2] Limit WIP (Work in Progress)

<br>

[3] Manage Flow

<br>

[4] Make Process Policies Explicit

<br>

[5] Implement Feedback Loops

<br>

[6] Improve Collaboratively, Evolve Experimentally


<!--
2. Typically, many teams start with a WIP Limit of 1 to 1.5 times the number of people working in a specific stage. Limiting WIP and putting the WIP limits on each column of the board not only helps the team members first finish what they are doing before taking up new stuff – but also communicates to the customer and other stakeholders that there is limited capacity to do work for any team – and they need to plan carefully what work they ask the team to do.

-->

---

## Classic Kanban

In a classic Kanban board model, there are three columns, as shown in the picture right:

<div class="columns-2" style="padding-top:50px">
<div>

- “To Do”: This column lists the tasks that are not yet started. (aka “backlog”)

<br>

- “Doing”: Consists of the tasks that are in progress.

<br>
  
- “Done”: Consists of the tasks that are completed

</div>
<div>

![drop-shadow](../../figures/classicKanban.png)

</div>
</div>

---
## Kanban Diagram


![ w:1300 drop-shadow](https://kanbanize.com/wp-content/uploads/website-images/kanban-resources/Kanban_board-elements.png "centered")

<!--

Kanban Cards – This is the visual representation of tasks. Each card contains information about the task and its status, such as deadline, assignee, description, etc.

Kanban Columns – Each column on the board represents a different stage of your workflow. The cards go through the workflow until their full completion.

Work-in-Progress Limits – They restrict the maximum amount of tasks in the different stages of the workflow. Limiting WIP allows you to finish work items faster by helping your team focus only on current tasks.

Kanban Swimlanes – These are horizontal lanes you can use to separate different activities, teams, classes of service, and more.

Commitment Point – A commitment marks a point in the work process where a work item is ready to be pulled into the system.

Delivery Point – The point in the workflow where work items are considered finished.

-->
---

## Work-in-Progress (WIP) Limits

<div style="padding-top:100px">

1. Rather than timeboxing, like we do with sprints in Scrum, Kanban is a continuous flow of work,  limited by the constraint on that column of the Kanban board.

<br>

![drop-shadow](../../figures/WIP.png "centered")

<br>

2. You set your column limits to avoid bottlenecks in your development process. If there is a build up or slow movement in one stage, you can adjust the WIP limits in the columns either side to prevent a build up of stress on a single point in the system.

---

## Why/How do we limit WIP?

<div class="columns-2" style="padding-top:10px">
<div>

- Measure flow

<br>

- Where are your bottlenecks?

<br>

- How do you manage them?

<br>

- Do you throw more engineering resource at one of the stages? If you do, then what impact will that have on the following stage?

<br>

- Redeployment of resource to earlier stages or later stages may be a better way to ensure a constant flow.

</div>
<div style="padding-top:185px">

![w:900 drop-shadow](../../figures/WIP2.png "centered")

</div>
</div>

---

## Kanban Flow

<div class="columns-2" style="padding-top:60px">
<div>

- The concept of Flow is critical and by measuring Flow metrics and working to improve them. 

<br>
<br>

- You can dramatically improve the speed of your delivery processes while reducing cycle time and improving the quality of your products or services by getting faster feedback from your customers – internal or external.

</div>
<div style="padding-top:60px">

![drop-shadow](../../figures/kanbanFlow.png)

</div>
</div>

<!--

At the core of Kanban is the concept of “Flow”. This means that the cards should flow through the system as evenly as possible, without long waiting times or blockages. Everything that hinders the flow should be critically examined. Kanban has different techniques, metrics and models, and if these are consistently applied, it can lead to a culture of continuous improvement (kaizen)

-->
---

## Cumulative Flow Diagrams

<div class="columns-2" >
<div style="padding-top:300px">

- In Kanban we use cumulative flow diagrams to show how much work we are completing

</div>
<div style="padding-top:150px">

![w:700 drop-shadow](../../figures/cumulativeFlow.png)

</div>
</div>

---

## Releasing in Kanban

<div style="padding-top:50px">

- Using Kanban, **continuous deployment** is possible. 

<br>

- You can release a new iteration of your product every day.

<br>

- This has a huge advantage, even over **Scrum**, which pridws itself on releasing early and often

<br>

- Where feedback in **Scrum** can only be gathered at the end of the sprint, meaning any feature built in day one has a feedback lag of *~2 weeks*, new features can Kanban can be tested by users as soon as they are completed.

</div>

---

## Kanban for you


<div style="padding-top:50px">

- Kanban is a great approach for small projects, it helps you focus on actually finishing features.

<br>

- As an agile methodology, the idea of Kanban is to increase the likelihood that your project is going to be successful.

<br>

- Especially when working on your own, you may be tempted to work on features in an arbitrary fashion eg. half building a form, then realizing you need a database, so half building a database, then building part of the logic, while finishing nothing.

<br>

- Using Kanban, visualizing your work and limiting WIP can help prevent this.

</div>

---

## Kanban in your career

<div class="columns-2">
<div  style="padding-top:10px">

- Aside from fast moving startups or small projects you probably won’t be developing using Kanban.

<br>

- However, a working knowledge of Kanban is in demand 

<br>

- Rather than look for companies that solely use Kanban, it is important to know that Kanban is a tool that you can utilize.

<br>

- When presented with a project, consider whether Scrum, Kanban or waterfall would fit the project best.

<br>

- A lot of R&D departments will use Kanban due to the lightweight nature of the methodology and the speed at which you can deliver features.

</div>
<div  style="padding-top:150px">

![w:900 drop-shadow](../../figures/kanbanCareer.png)

</div>
</div>