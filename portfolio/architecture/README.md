# Architecture notes

These are **conceptual diagrams** attached to [recent product case studies](../README.md). They explain responsibilities and boundaries at a level suitable for a public engineering portfolio.

They are **not** production network maps, security diagrams, or disclosures of private repository structure.

## Customer-facing product and operations

```mermaid
flowchart TB
  User["Customer"] --> Web["Next.js + TypeScript web interface"]
  Operator["Operations user"] --> Admin["React + TypeScript dashboard"]
  Web --> UX["Data fetching and validation"]
  Admin --> DX["Dashboard data fetching"]
  UX --> Services["Service boundary"]
  DX --> Services
```

**Engineering focus:** Different user journeys, shared conceptual contract boundaries, typed data, asynchronous state, and error handling.

[Read the case study](../case-studies/modern-product-platform.md)

## Editorial publishing platform

```mermaid
flowchart LR
  Editor["Authorized editor"] --> Workspace["Protected editorial workflow"]
  Workspace --> Application["Server-side application logic"]
  Application --> Persistence["Persistent application data"]
  Visitor["Visitor"] --> Public["Public content pages"]
  Persistence --> Public
```

**Engineering focus:** Application code versus editable content, publication states, data ownership, and release checks.

[Read the case study](../case-studies/technology-studio.md)

## Commerce discovery journey

```mermaid
flowchart LR
  Social["Social content"] --> Discovery["Featured-product discovery"]
  Discovery --> Product["Product details"]
  Product --> Checkout["Existing purchase journey"]
```

**Product focus:** Stable campaign destinations, mobile usability, consistent listings, and clear calls to action.

[Read the case study](../case-studies/retail-discovery.md)

## Responsible public documentation

No secret values, internal service addresses, credentials, database schemas, access controls, unreleased features, or client records are included. The diagrams are deliberately simplified for communication, not operational reconstruction.
