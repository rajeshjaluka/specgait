# SpecGait
## The human-in-the-loop orchestration platform governing the AI software development lifecycle.

### Purpose
When developers delegate the entire lifecycle to an agent without strict process gates, three systemic failures happen immediately:
* **The Telepathic Fallacy:** Developers assume the LLM implicitly understands edge cases, security contexts, and business intent that were never written down.
* **Review Fatigue Blindness:** An agent can generate 500 lines of complex code in seconds. No human can deeply review code at that velocity. Eventually, developers just hit "Merge" and pray, abdicating their role as a gatekeeper.
* **Architecture Erosion:** Agents optimize for localized code changes to close a ticket quickly. Without macro-level structural discipline, the codebase quickly becomes unmaintainable and unsupportable.

The **SpecGait** workflow brings the discipline of traditional software engineering to AI-driven delivery: every step produces a named, versioned artifact, and a human approves at each gate. It is iterative, not sequential. Any phase can reopen an earlier one, and the re-entry rules in the cross-cutting section say what becomes stale when it does.

### Principles
* **Artifact first.** A step is done when its artifact exists, is linked to its parent, and is approved.
* **The spec is the source of truth.** Designs, tests, evals and code all derive from the Behavioral Assertions.
* **Fail fast and cheap.** Feasibility checks, low-fidelity design and skeleton prototypes come before expensive work.
* **Humans gate, agents draft.** Each step has an autonomy level: draft only, act with approval, or act within a budget.
* **Everything is traceable.** Every artifact links to its parent and children, including agent runs and production signals.
* **Close the loop.** Production signals create new epics.
