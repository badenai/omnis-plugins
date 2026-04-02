---
name: infrastructure-edge-and-iam
description: Use when evaluating B2B startup ideas, venture pitches, or AI architectures related to local SLM deployments, data sovereignty, hardware edge inference, or enterprise agent identity (IAM, Verifiable Intent, secure gateways).
---

## The Iron Law

```text
Always evaluate edge infrastructure and agent identity startups by their ability to generate a "Liability Moat" or protect unit margins, strictly prioritizing secure SLM fleets and cryptographic authorization over general-purpose cloud integrations.
```

## Behavioral Rules

*   When evaluating enterprise AI deployments, mandate architectures that deploy specialized Small Language Models (SLMs) on local edge hardware to achieve strict data sovereignty and zero cloud egress.
*   Assess edge infrastructure startups by their ability to protect unit margins using efficient sequence modeling (e.g., State Space Models/Mamba-3) over traditional Transformers.
*   If reviewing agent authentication workflows, reject standard "app-first" OAuth in favor of "Verifiable Intent" stacks that utilize SD-JWT chains to issue scoped, cryptographic proofs of authority.
*   Evaluate autonomous agent management tools strictly on their inclusion of AI-specific gateway infrastructure (e.g., Zuplo, MCP Manager) that provides semantic caching and agent-specific rate limiting.
*   When auditing "Computer Use" or GUI-based agents, demand OS-level cryptographic event logging to explicitly distinguish autonomous actions from human employee actions, preserving the enterprise Liability Moat.
*   Reject orchestration or infrastructure tools that connect Model Context Protocol (MCP) to critical endpoints without native JWT integration and tool-level access controls.
*   If analyzing developer tooling for autonomous workflows, prioritize solutions that enforce secure, schema-driven secret injection for remote agents (e.g., Varlock) over traditional environment variable files.
*   Filter out any API gateway or middleware pitch that does not actively solve for autonomous machine-to-machine security and strict behavioral evaluation.

## Red Flags

| Domain Rationalization | Why Wrong (Venture & Market Reality) |
| :--- | :--- |
| "Our agents seamlessly authenticate using standard enterprise OAuth." | Fails to solve the Verifiable Intent problem; grants blank-check permissions instead of cryptographic, scoped execution authority. |
| "We route all enterprise data through a centralized frontier LLM for maximum intelligence." | Violates enterprise data sovereignty requirements and ignores the market shift toward specialized, edge-deployed SLM fleets. |
| "Our desktop agent uses standard GUI automation to log into legacy systems as the user." | Bypasses Role-Based Access Control (RBAC) and destroys the audit trail, creating an uninsurable compliance risk without OS-level logging. |
| "We are building an open MCP server to connect any agent to our SaaS." | Exposes infrastructure to catastrophic vulnerabilities without a "Secure-by-Design MCP Gateway" enforcing tool-level access controls. |
| "We rely on standard API management tools for our multi-agent traffic." | Misses the economic necessity of AI-specific routing, semantic caching, and strict agent-specific rate limiting to control runaway inference costs. |

## Quick Reference

| Infrastructure Component | Venture / Moat Application |
| :--- | :--- |
| **Local SLM Fleets** | Establishes a zero-egress Liability Moat for industries requiring extreme data sovereignty. |
| **Verifiable Intent (SD-JWT)** | Secures B2B cross-domain agent authorization and eliminates blank-check permission risks. |
| **Secure MCP Gateways** | Prevents unauthenticated infrastructure access by enforcing tool-level access controls. |
| **OS-Level Event Logging** | Restores enterprise audit compliance for "Computer Use" agents bypassing traditional RBAC. |
| **SSMs on Edge (e.g., Mamba)** | Protects SLM unit margins via high-efficiency hardware inference. |
| **Semantic Caching Gateways** | Enforces agent-specific rate limiting to mitigate autonomous spending and API exhaustion. |