# ADR-0006: Transition to Go as Primary Programming Language

## Metadata

Title:  ADR-0006_Transition-to-Go-as-Primary-Programming-Language
Date:   20250131
Author: [Peter Rossbach](mailto://peter.rossbach@bee42.com)
Keywords: Golang
Tags: type=programming
Decision Makers: [Insert Names]

## Status

[__Drafted__ | Proposed | Accepted | Rejected | Deprecated | Superseded | Implemented]

## Context

To enhance our development efficiency, scalability, and maintainability, we have decided to transition to Go as our primary programming language. This decision aligns with our goals of prioritizing framework reuse, improving UI development efficiency, leveraging specialized languages for performance-critical tasks, and improving developer productivity for API development.

## Decision

We will adopt Go as the primary language for application development while allowing Rust for embedded systems and kernel-level optimizations. The decision is driven by the following considerations:

Enhanced Reuse of Existing Frameworks:

* Go has a mature ecosystem with many reusable frameworks and libraries.
  * Prioritizes "buy over build" to reduce redundant development efforts.
* Efficient UI Development:
  * Go enables backend and API stability, allowing seamless UI integrations.
  * Facilitates microservices development, which simplifies UI interactions.
* Specialization Considerations:
  * Rust will be used for performance-intensive tasks such as embedded systems and kernel drivers.
  * Go will be the default choice for web applications, cloud-native services, and API development.
* Improved Developer Productivity for RESTful APIs:
  * Go’s concurrency model allows high-performance API development.
  * The simplicity and efficiency of Go enhance developer onboarding and productivity.

## Consequences

### Positive Outcomes:

* Increased Developer Productivity: Go’s simplicity and efficiency reduce development time and learning curves.
* Better API Performance: Native support for concurrency improves scalability.
* Stronger Ecosystem Integration: Adoption of well-supported frameworks ensures reliability and maintainability.

### Challenges:

* Team Composition & Training:
  * Some developers may resist or leave due to the language transition.
  * Upskilling programs and hiring initiatives will be needed to onboard Go-experienced engineers.
* Scalability Considerations:
  * Transitioning requires careful planning to avoid bottlenecks.
  * Phased migration ensures minimal disruptions to ongoing projects.
* Cost Analysis:
  * Migration incurs costs in developer training, refactoring existing applications, and potential downtime.
  * Investment in tooling and infrastructure updates may be required.

## Next Steps

* Establish a phased migration plan for transitioning services to Go.
* Provide training sessions and documentation for developers new to Go.
* Identify and prioritize services that benefit most from Go’s capabilities.
* Monitor performance and developer productivity during the transition.

## Notes

If you're considering Golang as the main programming language for implementing CLI and REST APIs, you should evaluate the following key questions:

* Suitability for CLI Development
  * Does Golang provide robust support for building CLI tools efficiently?
  * How does it compare to established CLI-focused languages like Java, C, Zig, Golang, Python, or Rust?
  * Are there well-maintained libraries for argument parsing, I/O handling, and logging?
* REST API Development Feasibility
  * Does Golang offer frameworks or libraries that simplify REST API development?
  * How well does it handle concurrent requests and scalability?
  * What is the ecosystem like for building web services and integrating with databases?
* Developer Productivity and Learning Curve
  * Is Golang widely adopted, and does it have sufficient documentation and community support?
  * How steep is the learning curve for new developers?
  * Does it enhance or hinder developer productivity in large projects?
* Performance Considerations
  * How does Golang's execution speed compare to Go or Rust in API-heavy applications?
  * Does it support efficient concurrency and parallel execution?
  * Are there optimizations for memory management and garbage collection?
* Ecosystem and Maintainability
  * Are there robust third-party libraries available for common development needs (authentication, database access, logging)?
  * Is the tooling (debuggers, linters, formatters) mature enough for long-term maintainability?
  * How difficult will it be to onboard new developers to a Golang-based codebase?
* Community and Long-Term Viability
  * Is Golang actively maintained and evolving?
    * **Peter Rossbach**
      * Yes, Go is actively maintained and continuously improved by the Go team at Google and the open-source community.
  * Are there large-scale projects or companies successfully using it?
    * **Peter Rossbach**
      * Golang is widely adopted and promoted by Google and the Cloud Native Computing Foundation (CNCF).
      * Major projects like Kubernetes, Docker, and many cloud-native platforms rely on Go for their core components.
  * What are the risks of adopting a mainstream language for critical infrastructure?
    * **Peter Rossbach**
      * Requires hiring and retaining skilled Go developers to maintain and scale projects effectively.
      * Frequent updates to external dependencies may introduce maintenance overhead.
      * Publicly available libraries can be analyzed for vulnerabilities, increasing the need for proactive security measures.