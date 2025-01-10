## Title

Document Architecture System Decisions and the Technical Depts

## Patlet

InnerSource projects that want to achieve high participation rates and make the best possible decisions for everybody involved need to find ways to create participatory format for all system components, tools and workflows. Michael Nygard announced 2011 the idea to document architecture decision with a simple markdown template and shared it with a simple git project. Today this adr tool is well proven and a many of teams around the globe use __architetecure desicion records (ADRs)__ to document there design desicions.

Another important aspect of defining architectural decisions is documenting technical debt. In Technical Debt Records, Dr. Michael Stal explores the systematic tracking and management of technical debt in software development using __Technical Debt Records (TDRs)__.__ Similar to how Architecture Design Records (ADRs) capture architectural decisions, TDRs document trade-offs in code quality made to accelerate delivery. The TDRs provides a detailed template for documenting technical debt, and Christoph Kappel  introduces a record tool to streamline the process of ADRs and TDRs.

## Problem

In an InnerSource project, where the entire organization must remain resilient to the pressures of introducing new features and keeping up with rapid technological advancements, a substantial number of architectural decisions and responses to technical debt are required. This raises critical questions: What are the consequences of a change? On what basis is the decision made between possible options?

To support an open environment for contributions and make changes easier to implement, contributors need clarity. But how can a contributor understand the rationale behind current decisions? How can we effectively discuss the risks of a radical refactor or redesign? Clear documentation and collaborative discussions are key to addressing these challenges and ensuring the project's adaptability and sustainability.

Projects may come with varying requirements, such as the desire to introduce features that conflict with one another or result in excessive complexity, causing architectural inefficiencies.

Identifying such conflicts or misunderstandings late in the development process—such as after the software is already built—can be extremely costly. These unresolved issues can frustrate all parties involved and harm the collaborative culture within the project. A common scenario where such disagreements arise is when an architectural decision remains unresolved for a long time because the idea's proponent and the project's maintainers fundamentally disagree on whether the proposed change should be implemented at all.

For an InnerSource project this situation happens more frequently when the project is maintained by multiple teams in the company i.e. shared ownership.

## Story - The Challenge of Balancing Decisions and Collaboration

Imagine a complex application composed of multiple interconnected projects, each maintained by a different team. Each team owns its domain of the system and occasionally contributes InnerSource changes to other areas. However, the real challenges begin when larger, cross-cutting changes are proposed. These require collaboration across team boundaries, involving diverse technical perspectives, competing priorities, and varying levels of technical debt in different parts of the system.

In one such scenario, the system's scalability is identified as a critical issue. Several valid options emerge:

* Refactor the existing architecture to improve performance.
* Introduce a new distributed microservices, serverless or go back to your modulith approach.
* Optimize specific bottlenecks incrementally without overhauling the system.
* Experiment with a novel framework to future-proof the application.

### Writers' Workshops for Exploration

To address these possibilities, the teams convene a series of writers' workshops. Here, architects, maintainers, and engineers document the technical debt in their respective areas and outline how each solution impacts the project. These workshops were designed to help committers produce well-documented decisions using structured templates, such as Architecture Decision Records (ADRs) and Technical Debt Records (TDRs). By utilizing these templates, the workshops supported a shared understanding of existing trade-offs and supported open, transparent discussions. The ADRs captured the rationale behind architectural choices, while the TDRs helped document the technical debt in various parts of the system. This approach not only ensured a thorough exploration of options but also created a traceable record of decisions, making it easier for all stakeholders to follow the reasoning behind each direction taken.

* [Writes Workshop Pattern](https://hillside.net/conferences/plop/235-how-to-hold-a-writers-workshop)

### Building Prototypes Before Committing

Recognizing the importance of implementation experience, the teams decide to build experimental versions of the proposed solutions. This isn't just theoretical planning—each solution is implemented in small, controlled test environments. The teams are empowered to explore how these options integrate into the larger system. Some engineers even build experimental APIs and measure their usability and performance.

### The Debate

Once the experiments are complete, teams come together to analyze the results. The workshops focus on tangible learnings:

* Does the microservices approach simplify deployment, or does it introduce new operational complexities?
* Does refactoring existing code risk destabilizing legacy systems?
* Does the incremental optimization fall short in addressing long-term needs?

Through structured discussions and debates, enriched with real implementation data, teams develop a clearer perspective on the benefits and drawbacks of each option.

### The Decision

Instead of leaving the decision solely to technical leads, the process prioritizes transparency and inclusivity. The maintainers weigh the trade-offs, ensure alignment with the system’s strategic goals, and incorporate feedback from contributors. Ultimately, the team selects a hybrid approach—refactoring the architecture's core areas while experimenting with microservices for future scalability.

### The Outcome

This iterative process not only solves the scalability issue but strengthens the project's collaboration culture. Engineers feel more empowered, as they see their contributions directly shaping the architecture. The documented technical debt and decision-making process now serve as a reference point for future changes, paving the way for an adaptive, innovative development environment.

This story underscores the value of combining technical rigor, experimentation, and collaboration to make thoughtful architectural decisions while embracing the complexity of modern software projects.

This approach leads to greater innovation, closer collaboration, and the widespread dissemination of knowledge across the organization. Achieving this requires full buy-in from all disciplines at every level, and most importantly, an environment of psychological safety where individuals feel comfortable proposing and debating ideas openly. This culture of open dialogue and shared decision-making is the foundation for creating impactful solutions.

Like any process, this requires ongoing refinement to maintain its effectiveness. Regular feedback may reveal areas for improvement, such as adjustments to the ADR and TDR templates or the decision-making process itself, ensuring that it remains inclusive, collaborative, and adaptive. By supporting an environment of continuous learning and improvement, we not only enhance the decisions we make today but also create a sustainable foundation for future growth and innovation.

## Context

* __Shared ownership by many teams and contributors of the System Architecture__:
  * The architecture is a collective responsibility, involving diverse teams that each own different parts of the system.
* __Overarching design decisions cannot always be made by a central body (e.g., a group of architects)__:
  * Due to time constraints and insufficient domain-specific knowledge, centralized decision-making is impractical in all cases.
* __Decisions need preparation__:
  * Each architectural decision requires careful preparation, considering current and future system requirements, technical constraints, and potential changes.
* __Continuous definition of technical debt__:
  * As you work on the system, you must document and track technical debt, preparing it for potential future changes or refactors.
* __Input from various types of users__: 
  * Key stakeholders such as developers, product owners, and product managers provide valuable input on the direction and decisions related to specific projects.
* __Asynchronous decision-making__:
  * Given the diverse stakeholders, decisions must be made asynchronously, avoiding the need for frequent synchronous meetings and instead encouraging discussions via writers' workshops and ongoing documentation.
* __Desire to document decisions__:
  * It’s essential to record decisions and technical deps in writing to create a clear, traceable record, ensuring that all stakeholders can refer back to the rationale behind every architectural choice made.

## Forces

* Often, the involved parties want to make decisions promptly, balancing speed with quality.
* Documenting decisions (before implementation begins) is a new skill for many of those involved in the process.
* Typically, only one option is thoroughly discussed or implemented.
* No one discusses the architectural decisions and technical deps with a broader audience.

## Sketch

??

## Solutions

We chose an ADR and TDR like process for increasing the transparency of our architectural decision making process.

Important elements of the solution are:

* __A description of when to document an ADR/TDR (and when not to)__: 
  * Clear guidelines for when architectural decisions or technical debts require formal documentation and when they can be managed informally.
* __A template for ADR/TDR documentation__:
  * Should encourage the author to examine the decision from multiple perspectives (technical, business, user, etc.).
  * Should prompt the author to provide both a high-level, easily accessible overview as well as a detailed, in-depth explanation of the rationale and implications.
* __A well-defined, lightweight process surrounding ADR/TDRs__:
  * How to publish an ADR/TDR and share it with all relevant stakeholders (e.g., via Slack, mailing lists, or project boards).
  * How to collect feedback effectively on the ADR/TDR from diverse stakeholders, ensuring a broad range of input.
  * How to incorporate the feedback and adjust the ADR/TDR as needed.
  * How to move the ADR/TDR towards a conclusion or final decision (e.g., with sign-off from relevant maintainers or decision-makers).
  * The use of appropriate tools, considering that non-technical stakeholders may not have direct access to source control or specialized software.
* __A commitment to iterating on the ADR/TDR templates and process__: 
  * Regularly refining the ADR/TDR templates and associated processes based on feedback and the evolving needs of the organization.

### Examples/Templates

* [Documenting architecture decisions - Michael Nygard](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
* [ADR-Tools - markdown](https://github.com/adr/adr-tools)
* [ADR-Tools Nat Pryce - markdown](https://github.com/npryce/adr-tools)
* [ADR-Tools - asciidoc](https://github.com/unexist/adr-tools)
* [Record-Tools - acsiidoc](https://github.com/unexist/record-tools)

## Resulting Context

Implementing an ADR/TDR-like process has proven to be valuable, as it makes architecture decision-making more transparent for everyone and ensures that all voices are heard.

Observable positive effects:

* Democratization of decision-making for architectrure that impact multiple teams (also easing the burden on team leads).
* An open, asynchronous communication method that works well across teams and geographies, improving accessibility and collaboration. Contribute to the ADR and TDR documents and discuss your ideas to invite all to a writes workshop.
* Empowering individuals and teams with your architecuture decisions to drive large-scale change within the organization.
* A record of decisions or technical deps made, providing a reliable point of reference for context and future decision-making.
* Scaling the impact of experienced engineers, allowing them to contribute asynchronously and remotely, rather than requiring their presence in synchronous meetings.
* Alignment of terminology, such as explicitly defining concepts like “system tests” to ensure common understanding.
* Alignment of processes, by clearly documenting processes like the out-of-hours support procedure, ensuring clarity across teams.
* Greater clarity of thought, as documenting architectural decisions or technical debt makes the author critically assess their rationale.

The ADR/TDR approach also carries risks that we want to acknowledge:

* __It doesn’t always work!__ Some people might still challenge a decision made through the ADR/TDR process. However, having a decision documented in writing is still valuable in these situations because it provides a clear record of when and why a decision was made.
* __Pre-documenting design proposals (architecture, protocols, etc.) can resemble waterfall-like design__, which may not fit the iterative development model preferred by many teams. We must remember the Agile principle: “Working software over comprehensive documentation.” Therefore, the ADR/TDR process should be as lightweight as possible to avoid unnecessary overhead.
* __The ADR/TDR can become too long and cumbersome__, leading to long comment threads and debates. In these cases, we might complement the process with synchronous communication, such as working groups or in-person meetings. Still, time is saved by allowing participants to review the ADR/TDR before the meeting rather than explaining everything during the discussion.

## Rationale

??

## Known Instances

??

## Status

??

## Author(s)

- Peter Rossbach
- Christoph Kappel

## Aliases

* [Michael Nygards ADRs Idea](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)
* [Learnings from using ADR in a real project](https://blog.unexist.dev/documentation/myself/2021/08/18/learnings-from-using-adr-in-a-real-project.html)
* [Technical Debt Records Idea](https://www.heise.de/blog/Technical-Debt-Records-Dokumentation-technischer-Schulden-9876115.html)
* [Requests for Comments](https://en.wikipedia.org/wiki/Request_for_Comments)
* [30-years-of-rfcs](https://www.rfc-editor.org/rfc/rfc2555.txt)
