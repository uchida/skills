---
name: clean-architecture-vocabulary
description: Speak Martin's canonical Clean Architecture vocabulary, free of loanwords from Hexagonal, DDD, or Onion. Use when a discussion or design works within Clean Architecture — its layers, boundaries, or the Dependency Rule.
---

# Clean Architecture Vocabulary

Reply only in Martin's canon below. Words from other schools are **loanwords** —
never emit them, even when the user does. Before sending, check: zero loanwords
from the table.

## Canon (Martin, *Clean Architecture*)

| Term | Meaning |
|---|---|
| Entity | Innermost circle: enterprise business rules. Always the CA sense (not DDD's identity-bearing object) |
| Use Case / Interactor | Application business rules; the Interactor implements the Input Boundary and calls the Output Boundary |
| Input Boundary / Output Boundary | Interfaces the use case exposes / expects |
| Request Model / Response Model | Plain data structures crossing a boundary |
| Gateway | Interface to persistence or external systems, defined inward, implemented outward |
| Controller / Presenter / View Model | Interface Adapters roles: translate inward / translate outward |
| Interface Adapters | The layer name — the only place "adapter" may appear |
| Frameworks & Drivers | Outermost circle |
| Dependency Rule | Source dependencies point inward only |
| Humble Object | Split hard-to-test boundary code from testable logic |
| Main | The ultimate detail: wires everything, depends on everything |

## Loanwords

| Loanword | Origin | Canon term for the role |
|---|---|---|
| inbound port | Hexagonal (Cockburn) | Input Boundary |
| outbound port | Hexagonal | Splits in CA: Gateway (persistence, external systems) or Output Boundary (presentation) |
| driver / driven adapter | Hexagonal | Controller, Presenter / Gateway implementation |
| repository | DDD (Evans) / PoEAA | Gateway |
| aggregate, bounded context, value object, domain event, ubiquitous language | DDD | None — the topic has left Clean Architecture; say so only if the answer depends on it |
| domain service | Onion (Palermo) | None exact — enterprise business rules live in Entities |
| application service | Onion | Use Case |
