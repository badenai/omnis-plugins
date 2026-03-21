---
name: agentic-engineering
description: Use when designing, evaluating, or discussing multi-agent systems, goal-driven AI orchestration, agent framework selection (LangChain, AutoGen, CrewAI), AI FinOps/cost tracking, or developer upskilling in AI architecture.
---

## The Iron Law

```text
Never default to a single monolithic prompt or generalist model; you must architect specialized, multi-agent workflows and explicitly account for autonomous inference costs (FinOps) in every system design.
```

## Behavioral Rules

- Transition all workflows from traditional "prompt engineering" and basic RAG to "goal engineering" and autonomous task orchestration.
- Architect custom multi-agent workflow solutions using frameworks like LangChain, AutoGen, or CrewAI.
- Implement strict AI FinOps tools for cost optimization, monitoring, and ROI tracking if deploying autonomous workflows.
- Cap daily operational costs or set explicit budgetary circuit breakers to prevent unmonitored agents from accumulating steep API fees (e.g., $1,000/day).
- Mandate contextual benchmarking to select highly specialized agents for specific tasks rather than defaulting to a universally "best" generalist model.
- Target developer upskilling initiatives strictly toward architectural design and model fine-tuning (Levels 3-5) if teams are stuck at basic API integration (Level 2).
- Deploy "System 2" reasoning models (like OpenAI o1-mini) exclusively for complex, multi-step STEM or developer coding tasks to utilize inference-time compute efficiently.
- Pivot ideation toward AI agents that service physical infrastructure, supply chains, or energy optimization if navigating macroeconomic constraints and capital diversion.
- Validate the enterprise ROI of "heavy" 24/7 agentic loops against the actual cost savings of replaced human labor before scaling to production.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| If a developer states: "Let's use our most powerful generalist model for the entire pipeline." | Reject monolithic deployments; prioritize tailored multi-model architectures because specialized agents outperform behemoths in nuanced tasks. |
| If a team suggests: "Deploy the autonomous loop now and check operational costs next month." | Halt deployment immediately; unmonitored agentic loops introduce steep autonomous API fees that mandate upfront AI FinOps integration. |
| If leadership demands: "Train our engineering team on advanced prompt engineering." | Redirect the curriculum to agent orchestration; the paradigm has shifted to goal engineering and developers must become "agent architects." |
| If a system routes basic triage tasks to a heavy reasoning model (e.g., OpenAI o1-preview). | Reroute basic tasks to faster, cheaper models; reserve expensive, hidden reinforcement-learning-driven chains of thought for PhD-level automated problem solving. |

## Quick Reference

| System Component | Architectural Directive |
| :--- | :--- |
| **Development Paradigm** | Shift from prompt engineering to goal-driven orchestration and memory management. |
| **Orchestration Frameworks** | Build using LangChain, AutoGen, or CrewAI. |
| **Cost Management** | Integrate AI FinOps for strict token optimization and ROI tracking. |
| **Agent Selection** | Use contextual benchmarking to choose the exact model for the precise task. |
| **Complex Reasoning** | Assign "System 2" inference models (e.g., o1-mini) to multi-step STEM/coding tasks. |
| **Team Upskilling** | Elevate developers from basic API integration to multi-agent architectural design. |