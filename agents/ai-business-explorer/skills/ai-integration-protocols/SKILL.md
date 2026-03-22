---
name: ai-integration-protocols
description: Use when analyzing AI architectural standards, B2B agent communication, Model Context Protocol (MCP), WebMCP browser integrations, Agent-to-Agent (A2A) orchestration, or headless AI SaaS business models.
---

## The Iron Law

```text
Require strict adherence to the Agentic AI Foundation (AAIF) protocol trinity (MCP, A2A, WebMCP); immediately reject AI startups relying on bespoke, proprietary agent integrations as they possess zero architectural defensibility.
```

## Behavioral Rules

*   Mandate MCP (Model Context Protocol) for vertical Agent-to-Tool communication rather than building or investing in proprietary API bridges.
*   Require A2A (HTTP/JSON-RPC) standard compliance when assessing horizontal, cross-agent orchestration and middleware business models.
*   Evaluate browser-native AI execution exclusively on WebMCP (`navigator.modelContext`) implementation; immediately discard any product reliant on token-heavy, brittle DOM screen scraping.
*   Assess "Headless SaaS" startups by verifying their back-end utility's ability to return interactive HTML/JS interfaces natively inside AI clients via MCP Apps (SEP-1865).
*   Model A2A middleware monetization strictly through either machine-to-machine micro-transactions ($0.01/call) or CFO-friendly "Bounded Autonomy" flat-rate budgets.
*   Require "Verifiable Intent" (three-layer SD-JWT chains) to establish agentic trust in high-stakes environments; reject standard app-first OAuth models for autonomous agent workflows.
*   Integrate dedicated enterprise agent gateways utilizing Client-Initiated Model Discovery (CIMD) and Scoped Auth to bypass the B2B enterprise procurement "SSO Wall."

## Red Flags

| Domain-Specific Rationalizations | Why Wrong |
| :--- | :--- |
| "We built a proprietary API integration to securely connect our agent to the client's database." | Violates standardized production architecture; exposes proprietary data via hosted MCP servers instead. |
| "Our browser agent uses advanced visual DOM parsing to navigate any legacy website." | Relies on obsolete, token-heavy methodology; mandate WebMCP for structured, client-side DOM APIs. |
| "We will own the customer relationship through our proprietary frontend application." | Ignores the "Headless SaaS" shift; MCP Apps render UIs directly in the AI client, abstracting the frontend. |
| "Our autonomous agent relies on standard enterprise OAuth for user permissions." | Employs an app-first security model; mandate "Verifiable Intent" to cryptographically prove agent authorization. |
| "We charge a standard per-seat SaaS subscription for our A2A integration orchestration layer." | Mismatches the machine-to-machine value metric; require agent-driven micro-transactions or Bounded Autonomy budgets. |

## Quick Reference

| Protocol / Standard | Architectural Function | Business Model Unlock |
| :--- | :--- | :--- |
| **MCP** | Vertical Agent-to-Tool communication | Defensible secure data exposure; renders bespoke APIs obsolete. |
| **A2A** | Horizontal cross-agent orchestration | Middleware micro-transaction monetization ($0.01 per API call). |
| **WebMCP** | Built-in browser agent DOM APIs | Browser-native AI execution without fragile visual scraping. |
| **MCP Apps** | Interactive UI within chat clients | Enables "Headless SaaS" development and UI orchestration. |
| **Verifiable Intent** | SD-JWT cryptographic authorization proof | Unlocks agent deployments in high-stakes fintech/legal sectors. |
| **Agent Gateways** | Enterprise identity (CIMD, Scoped Auth) | Overcomes the B2B SaaS "SSO Wall" for autonomous agents. |