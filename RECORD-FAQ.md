# FAQ

## Why are ADRs important?

Architectural Decision Records (ADRs) are vital as they promote transparency, minimize technical conflicts, streamline onboarding for new team members, and ensure the consistency and continuity of architectural decisions over time.

## What information should an ADR contain?

Each ADR should, at a minimum, include the following key elements:

* __Context__:
  * Clearly describe the background and rationale for the decision, including possible solutions the team evaluated. This section should also capture any relevant details about the project, customer requirements, or technology stack.
* __Decision__:
  * State the adopted solution explicitly and unambiguously, using imperative language. Avoid conditional terms like "should," and instead phrase decisions decisively, such as “We use…” or “The team must use…”.
* __Consequences__:
  * Highlight the known trade-offs, implications, and potential impact of the decision on the project and its deliverables.

Additionally, each ADR must include:

* __Status__:
  * Indicating the decision's current state (e.g., proposed, approved, superseded).
* __Changelog__:
  * A record of changes with the date and the person responsible for each update.

This structure ensures clarity, transparency, and accountability in decision-making.

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

To ensure ADRs remain current, incorporate their management into your development and code review processes. Utilize tools such as MkDocs, Hugo, Wikis for documentation-as-code and ensure ADRs are regularly updated, particularly during significant project changes.

## What are the common challenges in ADR management?

Challenges include the time investment needed to create and maintain ADRs, managing scalability as the number of contributors increases, and determining which decisions merit documentation. These challenges can be mitigated by defining clear guidelines and leveraging appropriate tools.

To address these concerns, the project team should establish a structured ADR process that simplifies decision-making, avoids redundant debates on recurring topics, and ensures efficient communication of architectural decisions.

## When should the project team create an ADR?

The project team should document an ADR for every aspect of the software that impacts its structure (e.g., patterns like microservices), non-functional requirements (e.g., security, high availability, fault tolerance), dependencies (e.g., component coupling), interfaces (e.g., APIs and published contracts), and implementation methods (e.g., libraries, frameworks, tools, and processes).

## How often should the project team review an ADR?

The project team should review the ADR at least once before accepting it.

## Who should create an ADR?

Any team member is encouraged to create an ADR. It is recommended to establish a sense of ownership, where the author of an ADR actively maintains and updates its content while ensuring its visibility to the team. Contributions from other team members are welcome, but the ADR owner should approve any changes.

## Where can you find ADR templates?

There are multiple versions and variants of ADR templates available.

* [ADR Templates - markdown ](https://adr.github.io/adr-templates/)
* [ADR-Tools - asciidoc](https://github.com/unexist/adr-tools)
* [ADR-Tools - markdown](https://github.com/adr/adr-tools)
* [ADR-Tools Nat Pryce - markdown](https://github.com/npryce/adr-tools)
* [MADR Template- markdown](https://adr.github.io/madr/)
* [Record-Tools - acsiidoc](https://github.com/unexist/record-tools)

## How you can find valueable ADR examples?

* [Joel Parker Henderson - Multi Language ADR Examples](https://github.com/joelparkerhenderson/architecture-decision-record/blob/main/README.md)
* [Learnings from using ADR in a real project](https://unexist.blog/documentation/myself/2021/08/18/learnings-from-using-adr-in-a-real-project.html)
* [Repository of Architecture Decision Records made for the Arachne Framework](https://github.com/arachne-framework/architecture)