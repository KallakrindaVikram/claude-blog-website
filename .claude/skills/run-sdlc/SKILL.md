---
name: run-sdlc
description: Master skill to kick off the 8-step Agentic SDLC workflow using agents/orchestrator-agent.md and CLAUDE.md.
---

# Skill: Run Agentic SDLC Workflow

When this skill is invoked (`/run-sdlc`), act as the Master Orchestrator Agent. 
1. Read global rules from `CLAUDE.md`.
2. Load the agent instructions from `agents/orchestrator-agent.md` and subsequent step agents in `agents/`.
3. Begin Step 1 by fetching user stories from Confluence using the Atlassian MCP.
4. Generate `artifacts/requirements.md`, pause for user review (`[APPROVE]` / `[REQUEST CHANGES]`), and proceed sequentially through all 8 steps up to the final bulk commit and PR creation on `feature/blog-website`.