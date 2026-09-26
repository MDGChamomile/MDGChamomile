# Harness minimalism: keep procedures lean and boundaries firm

> “Every component in a harness encodes an assumption about what the model can't do on its own, and those assumptions are worth stress testing, both because they may be incorrect, and because they can quickly go stale as models improve.”
>
> — Anthropic, [Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)

> “Find the simplest solution possible, and only increase complexity when needed.”
>
> — Anthropic, [Building effective agents](https://www.anthropic.com/research/building-effective-agents)

- Complex procedures and harnesses introduced to compensate for earlier models' limitations can hinder the autonomy and efficiency of more capable models. Keeping interventions that a model no longer needs adds cost and debugging overhead.

- Start from a minimal baseline that states the goal, essential context, success criteria, and boundaries for safety, authorization, and data protection. Add other procedures only when they address failures that recur in representative evaluations or real work, and add no more than necessary. However, use justified system-level controls to prevent high-cost or irreversible risks without waiting for repeated incidents.

- Do not make unvalidated solution procedures the default. Within the minimal baseline, leave the specific approach to the model's judgment and supply task-specific context only when needed.

- Limit context injected into every session to the project's purpose and core constraints. Rather than adding instructions and examples indiscriminately, first improve the structure of tools and data; load one-off information and logs only when needed.

- Provide feedback loops that let the model check its own work directly, such as tests and execution results. For high-cost or irreversible actions, do not rely on prompts alone: enforce least privilege, isolation, and explicit approval at the system level.

- If a temporary procedure is needed before it can be measured, record the hypothesis, scope, expected benefits and costs, review date, and removal criteria. Do not present the decision as a validated conclusion.

- Compare each harness procedure or mechanism against a minimal baseline that preserves the same core boundaries, and adopt or retain it only when the overall benefits justify the costs. Revisit temporary procedures at the designated time against the stated criteria. Routine operating procedures can be adjusted flexibly, but changes to core boundaries require clear justification and the harness owner's approval.
