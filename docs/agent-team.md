# Agent team

For Mona's Project Pulse dashboard, I am using a custom four-agent team orchestrated through GitHub Copilot CLI in a Codespace.

- Planner — Model: Claude Opus 4.7 (copilot). Responsibility: research the repository, identify dependencies and edge cases, and create a practical implementation plan with ordered steps, file assignments, and validation expectations. Definition: .github/agents/planner.agent.md.
- Orchestrator — Model: Claude Opus 4.7 (copilot). Responsibility: break the work into phases, delegate tasks to specialist agents, and coordinate sequencing so the team can work efficiently without overlapping scopes. Definition: .github/agents/orchestrator.agent.md.
- Designer — Model: Gemini 3.1 Pro (copilot). Responsibility: shape the dashboard experience with UX, accessibility, layout, interaction flow, and polished visual design decisions for the Project Pulse frontend. Definition: .github/agents/designer.agent.md.
- Coder — Model: GPT-5.5 (copilot). Responsibility: implement the code, wire up the dashboard data and UI logic, create supporting config such as .vscode/launch.json when needed, and validate the resulting behavior. Definition: .github/agents/coder.agent.md.

This team is coordinated from the GitHub Copilot CLI inside the Codespace, with the Orchestrator delegating work to the Planner, Designer, and Coder as the dashboard is built.
