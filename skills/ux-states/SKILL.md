---
name: ux-states
description: UX state coverage for frontend changes. Use when implementing or changing UI behavior, adding error/loading handling, or fixing user-facing bugs. Not for purely visual styling or backend logic.
---

# UX States

Walk the changed UI as the user, not as the code. Enumerate every state the user can land in — loading, empty, partial, error, success — and hold each to the invariant: **no dead ends**.

Four questions per state:

1. **Reachability** — Which user actions lead here? If no real path does, don't handle it in the UI; fix the layer that produces it.
2. **Cognition** — What does the user see, and what do they conclude happened? User-triggered actions get immediate feedback.
3. **Next move** — What can the user do from here, toward their goal? Empty needs a call to action; loading needs cancel or timeout behavior; partial needs what's missing and how to complete it; success needs the next step; error needs a way back into the flow. A state with no next move is a dead end.
4. **Reversibility** — Can the user back out or undo? Risky transitions stay reversible.

Focus and screen-reader announcements must survive every transition.

Record each non-ideal state as `Trigger → User sees → Next move`.

Done only when every user-visible state of the changed surface is enumerated and answers all four questions. When transitions carry guard conditions or exceed a handful of states, map them in [`assets/state-map-template.yaml`](assets/state-map-template.yaml).
