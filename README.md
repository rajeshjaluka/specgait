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

### Roles and Resposibilities
| Roles | Responsibility |
| ----------- | ----------- |
| Business User | Owns the problem, scenarios and value; approves intent, design and release readiness |
| Product Manager | Shapes epics into stories and ranks the backlog |
| Developer | Reviews architecture, code and tests; gatekeeper for technical decisions |
| Tech Lead | Owns foundations: standards, security policy, autonomy levels, budgets |
| Release Owner | Approves rollout and owns production operations |
| Coding Agent | Drafts specs, designs, architecture, code, tests and evals within its autonomy level |
| Reviewer Agent | Independent agent that reviews the Coding Agent's work and has not seen how it was produced |

### Workflow Overview
| Roles | Responsibility |
| ----------- | ----------- |
| 0. Foundations | Give agents durable context, limits and Definition of Done templates |
| 1. Intent and Spec | Turn business needs into testable Behavioral Assertions |
| 2. Feasibility and Prioritization | Kill unviable ideas cheaply and rank the rest |
| 3. Experience Design | Low-fidelity to high-fidelity design, or interface contracts |
| 4. Architecture | Data contracts, threat model and decision records |
| 5. Test and Eval Design | Define done for the sprint scope before building |
| 6. Build | Skeleton, refine, bind to design, harden, independent review |
| 7. Verification | Prove the product meets the spec and is safe to ship |
| 8. Release and Operate | Roll out safely, watch, learn and feed back |


