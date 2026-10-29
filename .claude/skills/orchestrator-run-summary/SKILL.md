---
name: orchestrator-run-summary
description: orchestrator-run-summary
disable-model-invocation: true
---
# Prompt Template: Orchestrator Run Summary

When invoked after an orchestrator workflow run, generate a concise, self-contained Markdown report summarizing the run's events and outcomes. The report should be understandable to someone who did not observe the run. The report must be created under the `artifacts/` folder with the name `orchestrator-run-summary.md`. Include:

A concise, self-contained Markdown report explaining what happened during this orchestrator workflow run.

Base the report on the available run history, conversation, tool outputs, and repository changes. Write for someone who did not observe the run. Cover:

- The run's objective and starting context.
- The major actions and decisions in chronological order, including any handoffs.
- Relevant files or artifacts inspected, created, or changed, and what changed.
- Checks or tests performed and their outcomes.
- Errors, retries, blockers, and unresolved issues, including how they were handled.
- The final result and any follow-up work still needed.

Be brief but cover all material events. Group routine details rather than listing every tool call. Distinguish confirmed facts from inference; do not invent missing information, and clearly note when details are unavailable. Exclude secrets and unnecessary raw logs. Return only the finished Markdown report, with a descriptive title and clear headings.