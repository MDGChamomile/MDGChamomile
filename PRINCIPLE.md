# Harness minimalism: keep context clean, procedures lean, and boundaries firm

> “Every component in a harness encodes an assumption about what the model can't do on its own, and those assumptions are worth stress testing, both because they may be incorrect, and because they can quickly go stale as models improve.”
>
> — Anthropic, [Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)

> “Find the simplest solution possible, and only increase complexity when needed.”
>
> — Anthropic, [Building effective agents](https://www.anthropic.com/research/building-effective-agents)

Complex procedures and harnesses introduced to compensate for earlier models' limitations can hinder the autonomy and efficiency of more capable models. Keeping interventions that a model no longer needs adds cost and debugging overhead.

- Keep context concise and current by removing duplication, stale information, and irrelevant material without losing necessary detail. Structure information for easy use. Keep always-loaded context to the project's purpose and core constraints; load task-specific detail only when needed. Prefer clearer tools and data over more instructions.

- Start with the goal, essential context, success criteria, and boundaries. Leave the approach to the model unless evidence warrants a prescribed procedure.

- Provide direct feedback through tests and execution results. Add procedures only to address failures that recur in representative evaluations or real work, and add no more than necessary. Adopt or retain procedures only when their benefits justify their costs against a minimal baseline with the same boundaries; remove procedures that no longer help. For provisional additions awaiting validation, define removal criteria and revisit them as evidence becomes available.

- Preserve boundaries for safety, authorization, and data protection. For high-cost or irreversible risks, justified system-level controls need not wait for repeated failures. Do not rely on prompts alone: enforce least privilege, isolation, and explicit approval at the system level. Changes to core boundaries require clear justification and the harness owner's approval.
