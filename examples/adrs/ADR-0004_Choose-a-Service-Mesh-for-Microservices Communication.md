# ADR-0004: Choose a Service Mesh for Microservices Communication

## Metadata

Title:  ADR-0004_Choose-a-Service-Mesh-for-Microservices Communication
Date:   20250128
Author: [Peter Rossbach](mailto://peter.rossbach@bee42.com)

## Status

[__Drafted__ | Proposed | Accepted | Rejected | Deprecated | Superseded | Implemented]

## Context

With a growing number of microservices, managing service-to-service communication, security (mTLS), and observability has become challenging.

## Decision
Adopt a service mesh (e.g., Istio, Linkerd) for microservice communication in Kubernetes.

### Rationale

* Centralized traffic management and load balancing.
* Built-in observability with tracing and metrics.
* Secure inter-service communication with encryption (mTLS).

## Consequences

* __Pros__: Easier troubleshooting, scalability, and secure traffic flows.
* __Cons__: Increased complexity and additional resource requirements.