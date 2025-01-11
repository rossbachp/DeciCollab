# FAQ

## Why are ADRs important?

Architectural Decision Records (ADRs) are vital as they promote transparency, minimize technical conflicts, streamline onboarding for new team members, and ensure the consistency and continuity of architectural decisions over time.

## How do you start writing ADRs?

Start by identifying architectural decisions that significantly impact the project. Use a standardized template to document each decision, capturing the context, available options, chosen solution, and anticipated consequences. Involve all relevant stakeholders to validate and provide feedback on the ADR.

## What tools can be used to manage ADR?

Popular tools for writing and managing ADRs include ADR Tools and Record Tools. These tools simplify the documentation process, support asynchronous discussions, and ensure decision records stay up-to-date while seamlessly integrating into development workflows and CI/CD pipelines. Additionally, they can be used to generate and publish content to your wiki, website, or CMS.

## What's the difference between an ADR and an RFC?

An RFC (Request for Comments) is a proposal document designed to discuss and evaluate significant changes before reaching a final decision. Once an RFC is approved and a decision is made, the outcome is recorded in an ADR. In essence, an RFC serves to propose and deliberate, while an ADR formalizes and documents the final decision.

## When to write an ADR and when to write an RFC?

Create an RFC when proposing a solution to an identified problem where no consensus exists on the best approach. The RFC serves as a platform for discussion, option evaluation, and gathering feedback. Once the RFC process results in a clear decision, document the outcome in an ADR. The ADR should include the context, the options considered, the chosen solution, and the rationale behind the decision.

## When should you write a technical debt record?

You should write a technical debt record when you identify a suboptimal decision or shortcut in the code, architecture, or process that may create future challenges, such as decreased maintainability, performance issues, or potential risks. This helps to document the known issues and plan for addressing them in the future.

## How long does it take to write an Architectural Decision Record?

The time needed to draft an ADR depends on the complexity of the decision. However, with a clear template and consistent practice, most ADRs can typically be written within one to two hours.

## Who is the audience for discussing and deciding on Decision Records?

The audience for discussing and deciding on Decision Records includes developers, architects, DevOps leads, and product owners.

## What types of decisions must be documented?

Decisions that significantly affect system architecture, performance, security, or maintainability should be documented in an ADR. Minor or operational changes, however, may not necessitate an ADR.

## How do you ensure your Architecture Decision Records remain current?

To ensure ADRs remain current, incorporate their management into your development and code review processes. Utilize tools such as MkDocs for documentation-as-code and ensure ADRs are regularly updated, particularly during significant project changes.

## What are the common challenges in ADR management?

Challenges include the time required to write and update ADRs, scalability as the number of participants grows, and identifying which decisions warrant an ADR. These issues can be addressed by establishing clear processes and utilizing the right tools.

