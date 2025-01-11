# ADR Template

## Title

A good format for the title is `ADR-nnnn` or `yyyy-mm-dd` description. The `nnnn` component represents an increasing number beginning from 1. 

For example, `ADR-0002` or `2025-01-10`.

## Status

The status of an Architecture Decision Record (ADR) is typically represented as an enumeration (enum) to indicate the current state of the decision within the project lifecycle. Common statuses include:

* __Proposed__:
  * The decision is under consideration and open for discussion. No final agreement has been reached.
* __Accepted__:
  * The decision has been reviewed and agreed upon by stakeholders. It is now part of the system architecture.
* __Rejected__:
  * The decision has been considered but was ultimately not approved or implemented.
* __Deprecated__:
  * The decision is no longer valid due to changes in requirements, technologies, or system priorities. It has been replaced or is planned for removal.
* __Superseded__:
  * The decision has been replaced by another ADR that reflects a more up-to-date solution.
* __Implemented__:
  * The decision has been fully integrated into the system and is currently in use.
* __Revisited__:
  * The decision is being reviewed to assess its relevance or effectiveness, usually triggered by new information or changing conditions.

Each status helps track the evolution of architectural decisions and ensures that all stakeholders understand their current standing and applicability in the project.

## Context

The context of an Architecture Decision Record (ADR) provides the background and rationale for the decision. It describes the situation or problem that led to the decision, including relevant technical, business, or environmental factors. This may include project requirements, constraints, existing systems, team preferences, or stakeholder needs. The goal is to clearly outline the "why" behind the decision, giving future readers an understanding of the circumstances and challenges at the time the decision was made.ne particular route to be more challenging.

## Decision

The Decision section of an Architecture Decision Record (ADR) clearly outlines the specific choice made to address the context or problem described. It answers the question: What was decided? This section should be concise yet detailed enough to eliminate ambiguity and serve as the definitive statement of action.

Key characteristics of the Decision section:

* __Clarity__:
  * Clearly state the selected option or approach. Avoid vague or overly technical language that might confuse readers.
* __Specificity__:
  * Include concrete details about what will be done. For example, specify the tools, patterns, or technologies involved.
* __Justification__:
  * Although the reasoning is elaborated in other sections (like Consequences), briefly touch on why this decision is appropriate.
* __Scope__:
  Define the boundaries or extent of the decision, specifying any particular areas or components it affects.

### Example:

__Decision__:

We will adopt containerd as the primary Kubernetes Container Runtime Interface (CRI) for the project. This decision is based on Containerd’s robust support for a wide range of low-level container runtimes, its modular architecture, and its proven extensibility, which align well with our project's goals for flexibility and scalability.

Containerd is a lightweight and high-performance container runtime that integrates seamlessly with Kubernetes, providing key features such as image management, container lifecycle operations, and runtime abstraction. Its design allows for a strong separation of concerns between runtime operations and orchestration, enhancing maintainability and compatibility.

Additionally, Containerd benefits from exceptional community support as a CNCF-graduated project, with extensive documentation, active development, and widespread adoption across major Kubernetes platforms and distributions, such as GKE, EKS, and AKS. Leveraging Containerd aligns our project with these cloud-native standards, improving ecosystem compatibility and long-term viability.

Given that the majority of Kubernetes-based clouds and distributions already use Containerd, adopting it will reduce the complexity of integration efforts and increase alignment with future upstream developments in Kubernetes. This decision ensures we adopt a well-supported, future-proof solution for container runtime management.

## Alternatives: Options considered, with reasons for rejection.

The Alternatives section of an Architecture Decision Record (ADR) describes the other options considered during the decision-making process. It provides insight into the reasoning behind the chosen approach by showcasing what was evaluated and why these alternatives were not selected. This section demonstrates thorough analysis, supports future reassessments, and documents lessons learned.

Structure of the Alternatives Section:

* __Option Name and Description__:
  * Briefly describe the alternative, including its key features and potential relevance to the problem.
* __Pros__:
  * Highlight the advantages or benefits of the alternative.
* __Cons__:
  * Note the drawbacks, risks, or limitations associated with the alternative.
* __Reasons for Rejection__:
  * Summarize why the alternative was ultimately not chosen, considering factors like feasibility, cost, alignment with goals, or compatibility with existing systems.

### Example:

___Alternatives Considered:__

* __Alternative A__: Docker as the Kubernetes Container Runtime Interface (CRI)
  * __Pros__: Widely adopted, mature tooling, and strong familiarity among developers.
  * __Cons__: Docker's CRI is deprecated in Kubernetes, leading to limited long-term support.
  * __Reason for Rejection__: Dependency on deprecated technology posed a significant risk to project sustainability.
* __Alternative B__: CRI-O
  * __Pros__: Lightweight and optimized for Kubernetes. Direct support for OCI standards.
  * __Cons__: Smaller community and fewer plugins compared to Containerd.
  * __Reason for Rejection__: Lack of ecosystem integration and extensibility compared to Containerd.

By thoroughly documenting these alternatives, the ADR provides a comprehensive view of the decision-making process, ensuring that future stakeholders understand the context and rationale behind the chosen solution.

## Consequences

In this section, we outline the outcomes of the decision, considering both its positive and negative impacts. Key components include:

* __Effects__:
  * The consequences or implications of the decision, detailing its impact on the system or processes.
* __Outputs__:
  * The deliverables resulting from this decision, which may include new artifacts, changes, or even additional ADRs. Addressing one decision often leads to identifying new questions to explore.
* __Follow-Ups__:
  * Any subsequent actions, tasks, or considerations required to fully implement the decision.
* __ADR Reviews__:
  *A plan to revisit and evaluate the decision and its effectiveness after the implementation, possibly scheduling a review date to assess the outcome.

To ensure accountability and clarity, all outcomes should have corresponding tickets created to track the related tasks and progress effectively.

## References

* [A Definition of Done for Architectural Decision Making](https://www.ozimmer.ch/practices/2020/05/22/ADDefinitionOfDone.html).
* [Documenting architecture decisions](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)