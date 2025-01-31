# ADR-0005: Adopt Logging Framework

## Metadata

Title:  ADR-0005_Adopt Logging Framework
Date:   20250131
Author: [Peter Rossbach](mailto://peter.rossbach@bee42.com)
Keywords: Logging, Java
Tags: type=framework
Decision Makers: [Insert Names]

## Status

[__Drafted__ | Proposed | Accepted | Rejected | Deprecated | Superseded | Implemented]

## Context

Our current logging framework requires an update to address multiple challenges, including readability, observability, performance, security, and cross-language compatibility. The following factors drive this decision:

* __Adoption of Structured Logging__: Unstructured logs make log processing and analysis difficult. Structured logging will enhance readability and enable better log aggregation, filtering, and searchability.

* __Framework Transition__: The migration from Log4J to Logback is motivated by improved performance, a simpler configuration model, and security considerations.

* __Shift to Tracing__: A transition to distributed tracing will improve end-to-end observability, especially in microservices architectures.

* __Context Enrichment__: Enforcing standardized metadata inclusion (UUIDs, error codes, system IDs, flow IDs) will improve debugging, monitoring, and correlation across services.

__Multi-Language Support__: As applications span multiple programming languages, a unified approach to logging will ensure consistency and ease of integration across different services.

## Decision

We will:

* Adopt structured logging across all services by enforcing JSON or key-value log formats.
* Migrate from Log4J to Logback in Java-based services to improve performance, security, and configuration simplicity.
* Integrate distributed tracing by adopting OpenTelemetry for tracing propagation and correlation across microservices.
* Enforce contextual metadata standards by including trace IDs, error codes, and request identifiers in all logs.
* Standardize logging across languages by choosing logging libraries that align with OpenTelemetry and structured logging principles for polyglot environments.

## Consequences

### Positive Outcomes:

* Improved log readability and structured parsing.
* Enhanced security and performance with Logback.
* Better debugging and observability using tracing and contextual metadata.
* Consistency in logging practices across various languages and services.

### Trade-offs:

* Migration effort required to update existing logging implementations.
* Potential learning curve for teams adapting to new logging and tracing mechanisms.
* Increased log volume due to additional metadata, requiring optimized log storage and retention strategies.

## Next Steps

* Define a migration plan with clear milestones for structured logging adoption.
* Update logging libraries and configurations across services.
* Implement and test distributed tracing in staging environments before full rollout.
* Educate teams on best practices for structured logging and observability.

## Notes

* Which attribute we use as logging message formats?
* Accept all developers that we need Error/Message codes anywhere?
* Think about tracing vs logging!
* We really accept Opentelemetry standards?


