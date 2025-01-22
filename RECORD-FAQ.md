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

The audience for discussing and deciding on Decision Records includes developers, architects, DevOps leads, and product owners. The record owner and committer coordination the documentation, collobration meetings, decision, implementation, mentoring and acceptance of the consequences. 

## What types of decisions must be documented?

Decisions that significantly affect system architecture, performance, security, or maintainability should be documented in an ADR. Minor or operational changes, however, may not necessitate an ADR.

## How do you ensure your Architecture Decision Records remain current?

To ensure ADRs remain current, incorporate their management into your development and code review processes. Utilize tools such as MkDocs, Hugo, CMS, Wikis for documentation-as-code and ensure ADRs are regularly updated, particularly during significant project changes.

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
* [e-adr](https://github.com/adr/e-adr)
* [MADR Template- markdown](https://adr.github.io/madr/)
* [Record-Tools - acsiidoc](https://github.com/unexist/record-tools)

## How you can find valueable ADR examples?

* [Joel Parker Henderson - Multi Language ADR Examples](https://github.com/joelparkerhenderson/architecture-decision-record/blob/main/README.md)
* [Learnings from using ADR in a real project](https://unexist.blog/documentation/myself/2021/08/18/learnings-from-using-adr-in-a-real-project.html)
* [Repository of Architecture Decision Records made for the Arachne Framework](https://github.com/arachne-framework/architecture)

## How to be discuss an ADR?

To hold a workshop for Architecture Decision Records (ADRs):

* __Set the Objective__: 
  * Define the purpose, such as teaching ADR best practices or addressing real-world architectural decisions.
* __Prepare Materials__:
  * Create templates, examples of ADRs, and an agenda covering decision context, trade-offs, and rationale.
* __Define a Scenario__:
  * Use a realistic project scenario where participants can identify, discuss, and document architectural decisions.
* __Guide Hands-On Exercises__:
  * Walk through writing an ADR collaboratively, explaining each section and the importance of concise, clear documentation.
* __Review and Discuss__:
  * Encourage peer reviews and discussions to reinforce learning and improve the quality of ADRs.
* __Provide Resources__:
  * Share tools and repositories for ongoing ADR documentation.

End with a Q&A session to clarify doubts and solidify understanding.

* [Writers Workshop](https://hillside.net/conferences/plop/235-how-to-hold-a-writers-workshop)

## How do you define good criteria for deciding whether to grant approval?

To define good criteria for decision-making or signing approvals, you should focus on clearly structured, relevant, and measurable factors that align with the objectives of the decision. Using tools like the Pugh matrix is helpful because it provides a systematic way to evaluate options against chosen criteria.

### Define the Purpose of the Decision

* What are you trying to achieve?
* Is this decision operational, strategic, or tactical?
* Align criteria with short- and long-term goals.

### Identify and Validate Key Criteria

Good criteria are:

* Relevant: Linked directly to the goals and context of the decision.
* Measurable: Quantifiable or with clear qualitative standards.
* Comprehensive: Cover all significant aspects, like cost, quality, scalability, risk, time, etc.
* Non-redundant: Avoid overlapping or unnecessary complexity.
Examples:
* For product selection: Functionality, cost, vendor support, compatibility.
* For budget approvals: ROI, resource allocation, alignment with business strategy, risk mitigation.

### Weight the Criteria

Some factors are more critical than others. Assign weights based on priority (e.g., importance to stakeholders, potential impact).

### Generate and Assess Options

List out all potential options (projects, vendors, strategies, etc.). Then, evaluate them against the criteria using methods like the Pugh matrix:

* Assign scores to each option per criterion (e.g., -1, 0, +1).
* Use a baseline for comparison, if applicable.
* Sum the weighted scores to determine which option performs best.

### Validate Results

Consult with stakeholders to ensure alignment and buy-in.
Validate that the chosen option passes legal, compliance, or organizational thresholds.
Consider external factors that might change the decision.

### Monitor and Iterate

Post-approval, track the performance and outcomes. Use feedback to refine the decision-making process and criteria for the future.

* [Pugh matrix](https://www.decision-making-confidence.com/pugh-matrix.html)

## How Does Voting Work?

Reasons for votes:

People often shy away from addressing conflicts directly and instead seek alternatives, such as relying on authority figures, strict rules, rigid processes, or settling into stagnation. However, these substitutes rarely prove as effective as putting in the effort to resolve the conflict constructively.

Rules:

- The ADR must be discussed publicly and fully documented.
- A minimum of three committers must sign the decision record (ADR).
- The voting date must be announced in a public channel in advance.
- A minimun of three positive votes must be exists.
- For an approval, there must be more "+1" votes than "-1" votes.
- Voting periods should generally run for at least 72 hours to provide an opportunity for all concerned persons to participate, regardless of their geographic location.

Voting Guidelines:

- **+1**: Indicates **YES**, accepting the decision and its documented consequences.
- **0**: Indicates a neutral stance **(YES/NO)**.
- **-1**: Indicates **NO** and requires a rationale, which must be clearly documented.

* [APACHE Foundation Voting Process](https://www.apache.org/foundation/voting.html)

## History of ADRs

Architectural Decision Records (ADRs) have evolved as a practical method to document and communicate key architectural choices. The concept gained traction with industry thought leaders:

* 2011: [Documenting architecture decisions](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
  *  Michael Nygard popularized ADRs through Documenting Architecture Decisions, a blog post that highlighted their simplicity and value in maintaining team alignment.
  * [ADR-tools](https://github.com/npryce/adr-tools)
* 2024: [Timing Architectural Decisions](https://ozimmer.ch/assets/presos/ZIO-ITARCKeynoteTADv101p.pdf)
  * Olaf Zimmermann introduced the idea of Timing Architectural Decisions, emphasizing the importance of making and capturing decisions when they matter most.
  * [Blog Posts Olaf Zimmermann](https://ozimmer.ch/tags/#architectural-decisions)

ADRs continue to be a cornerstone for structured decision-making in software architecture.
