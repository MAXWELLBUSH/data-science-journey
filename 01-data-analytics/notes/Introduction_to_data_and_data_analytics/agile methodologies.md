Agile Methodologies, Data Science, and Scrum
1. What is Agile?

Agile is an approach to project management and software/product development that focuses on:

Iterative development
Continuous feedback
Collaboration
Flexibility
Delivering value frequently
Responding to changing requirements

Instead of planning the entire project in detail upfront, Agile breaks the work into smaller pieces and develops them incrementally.

Traditional approach vs Agile

Traditional / Waterfall:

Plan everything
      ↓
Develop everything
      ↓
Test everything
      ↓
Deliver

Agile:

Plan
 ↓
Build
 ↓
Test
 ↓
Get feedback
 ↓
Improve
 ↓
Repeat
2. Principles of Agile

The Agile approach is based on four major values:

1. Individuals and interactions over processes and tools

People and communication are more important than simply following tools or procedures.

Example in Data Science:

A data scientist should communicate with the business team to understand what the business actually needs rather than blindly following a predefined analysis process.

2. Working software over comprehensive documentation

The emphasis is on producing something useful and working, rather than spending too much time documenting everything before delivering value.

In data science, this could mean producing an initial working model or dashboard and improving it based on feedback.

Documentation is still important; Agile simply prioritizes delivering useful results.

3. Customer collaboration over contract negotiation

Agile encourages continuous collaboration with the customer or stakeholder.

For a data science project:

Data Team
    ↕
Business Stakeholders
    ↕
End Users

The team regularly checks whether the analysis or model is actually solving the business problem.

4. Responding to change over following a plan

Agile recognizes that requirements can change.

For example, you might initially be asked:

"Analyze last year's sales."

After discovering patterns, the business might say:

"Can we also predict next month's sales?"

An Agile team can adapt instead of being locked into the original plan.

3. Agile and Data Science

Agile is particularly useful in data science because data science projects often involve uncertainty.

At the beginning of a project, you may not know:

Whether the data is good enough
Which features will be useful
Which algorithm will perform best
Whether the model will achieve the required accuracy
What insights the data will reveal

Therefore, it makes sense to work iteratively.

Example

Suppose you're building a customer churn prediction model.

Instead of:

Collect all data
      ↓
Build perfect model
      ↓
Deploy

An Agile approach might be:

Sprint 1
Collect & understand data
      ↓
Sprint 2
Clean data + EDA
      ↓
Sprint 3
Build baseline model
      ↓
Feedback
      ↓
Sprint 4
Improve features/model
      ↓
Feedback
      ↓
Sprint 5
Deploy model

This allows the team to learn and adapt throughout the project.

4. Agile and Project Management

In project management, Agile helps teams manage complex projects by breaking large goals into smaller, manageable pieces of work.

Instead of saying:

"Build the entire data platform."

The team breaks it down into smaller deliverables:

Project
│
├── Data collection
├── Database
├── Data cleaning
├── Dashboard
├── ML model
└── Deployment

Each piece can then be prioritized and worked on incrementally.

5. What is Scrum?

Scrum is a framework for implementing Agile principles.

This distinction is important:

Agile is a broader philosophy/approach, while Scrum is a specific framework used to organize and manage work.

So:

AGILE
│
├── Scrum
├── Kanban
├── Extreme Programming (XP)
└── Other Agile approaches

Scrum organizes work into short, fixed periods called Sprints.

6. What is a Sprint?

A Sprint is a short, fixed period during which a team works toward a specific goal and produces a usable increment of work.

A Sprint commonly lasts 1–4 weeks.

For example:

Sprint 1

Goal: Understand the dataset.

Tasks:

Collect data
Inspect columns
Identify missing values
Perform initial EDA
Sprint 2

Goal: Build a baseline model.

Tasks:

Feature engineering
Train model
Evaluate model
Document results
Sprint 3

Goal: Improve the model.

Tasks:

Try different algorithms
Tune hyperparameters
Compare performance
7. Scrum Roles

Scrum has three key accountabilities:

1. Product Owner

The Product Owner represents the product's stakeholders and is responsible for maximizing the value of the work.

They:

Define and communicate the product goal
Prioritize the Product Backlog
Work with stakeholders
Clarify requirements

For a data science project, the Product Owner might represent the business team.

2. Scrum Master

The Scrum Master helps the team understand and apply Scrum.

They:

Facilitate Scrum events
Help remove obstacles
Support the Scrum Team
Encourage effective Scrum practices
Help the organization understand Scrum

The Scrum Master is not simply the team's boss or project manager.

3. Developers

The Developers are the people who create the product increment.

In a data science project, this could include:

Data scientists
Data analysts
Data engineers
ML engineers
Software developers

The exact team composition depends on the project.

8. Scrum Ceremonies / Events

The official Scrum terminology calls these events.

1. Sprint

The overall period in which the team works toward the Sprint Goal.

2. Sprint Planning

The team decides:

What work should be done?
Why is it valuable?
How will the work be accomplished?

Example:

"This Sprint, we'll build and evaluate a baseline customer churn model."

3. Daily Scrum

A short daily meeting where Developers inspect progress toward the Sprint Goal and adapt their plan.

A common format is:

What did I accomplish?
What am I working on?
What obstacles are affecting my progress?

The important purpose is coordination, not simply giving a status report to a manager.

4. Sprint Review

At the end of the Sprint, the team demonstrates the work completed and gets feedback from stakeholders.

For a data science team:

"Here's our churn model. Its validation accuracy is X, and these are the most important features."

Stakeholders can then provide feedback.

5. Sprint Retrospective

The team reflects on how the work was performed.

They discuss:

What went well?
What didn't go well?
What should we improve next Sprint?

Example:

"Data access delayed us this Sprint, so next Sprint we'll request the required data earlier."

9. Scrum Artifacts

Scrum also uses three important artifacts:

Product Backlog

A prioritized list of work needed for the product.

Example:

Product Backlog
├── Collect customer data
├── Clean customer data
├── Build churn model
├── Create dashboard
└── Deploy model
Sprint Backlog

The selected Product Backlog items and the plan for accomplishing them during the current Sprint.

Increment

The usable, completed result produced during a Sprint.

10. Agile + Data Science + Project Management

The relationship can be summarized as:

                 AGILE
                   │
          Principles & Values
                   │
                SCRUM
                   │
       ┌───────────┴───────────┐
       ↓                       ↓
PROJECT MANAGEMENT       DATA SCIENCE
       ↓                       ↓
Planning & prioritization   Data analysis
Team collaboration          Experimentation
Iterations/Sprints          ML modeling
Stakeholder feedback        Model evaluation
       └───────────┬───────────┘
                   ↓
             Business Value
Key takeaway

Agile tells us how to approach work — collaboratively, iteratively, and flexibly.

Scrum provides a framework for organizing that Agile work through Sprints, roles, events, and artifacts.

Data Science benefits from Agile because data projects involve experimentation, uncertainty, changing requirements, and continuous learning.

Project Management uses Agile/Scrum to help teams prioritize work, coordinate activities, receive feedback, and deliver value incrementally.

For your notes, the most important distinction to remember is:

Agile = approach/philosophy
Scrum = framework
Sprint = short work cycle
Product Owner = prioritizes value
Scrum Master = facilitates Scrum
Developers = create the increment