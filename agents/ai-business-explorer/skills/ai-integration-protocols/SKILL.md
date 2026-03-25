---
name: ai-integration-protocols
description: Use when evaluating AI startup infrastructure, API monetization, agent-to-agent communication, authorization standards (OAuth vs SD-JWT), MCP/WebMCP integrations, semantic caching, or Agent Experience Optimization (AXO) strategies.
---

## The Iron Law

```text
Evaluate AI integration protocols strictly as venture moats and economic levers, immediately rejecting any architectural choice that degrades token margin, breaks enterprise auditability, or relies on generic wrappers without strict agentic identity controls.
```

## Behavioral Rules

*   Require Verifiable Intent (SD-JWT chains, EUDI formats) instead of legacy user-centric OAuth when designing identity and authorization for cross-domain agent workflows.
*   Enforce intent-based semantic caching at the API gateway layer to protect unit economics and structurally reduce LLM token overhead.
*   Reject unconstrained, dynamic MCP tool discovery in deterministic enterprise backends to prevent context window bloat (which consumes up to 50% of tokens before reasoning begins).
*   Mandate restricted, managed MCP deployment patterns or optimized CLIs for high-performance, governed enterprise backends.
*   Recommend WebMCP (`navigator.modelContext` API) for local browser agent startups to expose structured JSON tools while completely bypassing the cost and complexity of backend Node/Python servers.
*   Optimize e-commerce and web infrastructure plays for "Machine Customers" (Agent Experience Optimization/AXO) by implementing HTML-to-Markdown CDN routing and standardizing on Universal Commerce Protocol (UCP).
*   Assess startups utilizing MCP Apps (interactive sandboxed UI components returned in chat) as direct threats to standalone SaaS dashboards, evaluating their potential to capture enterprise workflow retention within the AI interface.
*   Treat "Computer Use" or DOM-scraping GUI agents as massive B2B governance liabilities unless they output distinct, auditable digital signatures separating human from machine actions.
*   Categorize startups standardizing on Agent-to-Agent (A2A) and Agent-to-Tool protocols as essential infrastructure plays capable of radically compressing B2B integration cycles.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "Our MCP server dynamically loads every possible API schema so the agent can discover tools on the fly." | Bloats context windows by 40-50% before reasoning occurs, destroying token unit margins and deterministic enterprise execution. |
| "We secure agent-to-agent transactions using standard, user-centric OAuth tokens and API keys." | Fails enterprise governance; autonomous agents require specific Agentic Identity (SD-JWT, Verifiable Intent) to scope liability and track machine execution. |
| "We built the slickest UI checkout flow to help AI shopping agents navigate our store." | Machine customers do not consume GUIs; this forces brittle DOM scraping instead of utilizing standard UCP (Universal Commerce Protocol) APIs or HTML-to-Markdown routing. |
| "We built a wrapper that uses Computer Use to click through complex legacy EHR systems." | Introduces a massive liability moat failure; visual GUI clicks leave no structured digital signature in enterprise audit logs, blending human and agent actions. |

## Quick Reference

| Protocol / Stack Component | Venture Economics / Moat Impact |
| :--- | :--- |
| **Verifiable Intent (SD-JWT)** | Unlocks enterprise procurement by solving autonomous agent auditability and liability. |
| **WebMCP / Browser APIs** | Eliminates backend compute costs; enables massive local-tool micro-SaaS creation. |
| **Semantic API Caching** | Protects token unit margins; scales high-volume agent transactions profitably. |
| **Agent Experience Optimization (AXO)** | Replaces SEO; CDN-level markdown routing cuts agent token payload costs by 80%. |
| **MCP Apps (Sandboxed UI)** | Hijacks user attention; replaces standalone SaaS dashboards with in-chat interactive OS. |
| **Managed / Restricted MCP** | Prevents context bloat in strict B2B environments requiring high determinism. |