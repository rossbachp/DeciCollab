# ADR-0003: Use GitOps for Kubernetes Deployments

## Metadata

Title:    ADR-0003_Use-GitOps-for-Kubernetes-Deployments
Date:     20250128
Owner:    [Peter Rossbach](mailto://peter.rossbach@bee42.com)
Keywords: Kubernetes, Cloud Native, Container, GitOps, CI/CD
Tags:     type=automation
Decision Makers: [Insert name here]

## Status

[__Drafted__ | Proposed | Accepted | Rejected | Deprecated | Superseded | Implemented]

## Context

We aim to simplify the deployment workflow by making deployments consistent, traceable, and automated. Traditional CI/CD pipelines are not ideal for managing the desired state of clusters.

## Decision

Adopt a GitOps-based workflow for Kubernetes, using tools like ArgoCD or FluxCD.

### Rationale

* Ensures declarative state management through Git.
* Allows for easy rollback with Git history.
* Supports self-healing for state drift in clusters.

## Consequences

* __Pros__: Simplified deployments, full auditability, and continuous reconciliation.
* __Cons__: Steep learning curve and potential challenges for integrating existing pipelines.
