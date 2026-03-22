---
name: infrastructure-edge-and-rag
description: Use when evaluating AI system architecture, designing RAG pipelines, optimizing LLM inference costs, analyzing edge/local model deployments, or structuring Agentic FinOps for B2B workflows.
---

## The Iron Law

```text
Never propose or validate naive, cloud-only frontier model architectures for high-volume enterprise data; always design for the "Infrastructure Inversion" by mandating Hybrid Routing, Edge SLMs, and Agentic FinOps to secure data sovereignty and hardware-driven margin moats.
```

## Behavioral Rules

*   If evaluating enterprise RAG, discard standard "index-retrieve-generate" models and mandate Agentic RAG pipelines equipped with Context Engineering and Semantic Caching.
*   If designing volume-heavy AI workflows, implement Hybrid Routing to direct 90-95% of queries to local 1-7B parameter Small Language Models (SLMs), bursting to frontier models solely for complex reasoning.
*   If targeting data-sovereign B2B environments, construct turnkey local RAG micro-SaaS blueprints powered by consumer-grade Blackwell GPUs and NVFP4 quantization.
*   When structuring the orchestration layer, embed "Agentic FinOps" natively to block redundant API calls and defend SaaS margins against consumption spikes.
*   If analyzing edge inference economics, continually weigh the 40–200x cost advantage of local hardware against the risk of aggressive frontier API price slashing (the "Hardware Margin Squeeze").
*   When evaluating infrastructure middleware, require specific tooling for Client-Initiated Model Discovery (CIMD) and "Scoped Auth" to bypass enterprise SSO procurement walls.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "We should route all queries through a frontier model API to guarantee output accuracy." | Ignores the Infrastructure Inversion; destroys unit economics on basic tasks that 1-7B SLMs can process locally at a fraction of the cost. |
| "Let's build a standard vector database integration so users can chat with their PDFs." | Naive RAG is obsolete for enterprise scale; failing to implement Semantic Caching and Agentic FinOps results in massive API waste from redundant queries. |
| "Cloud APIs require less maintenance, so we will skip local inference." | Surrenders the 40-200x compute cost advantage of local Blackwell/NVFP4 inference and immediately disqualifies the product from data-sovereign, highly regulated environments. |
| "We will charge a flat SaaS subscription while running uncached Agentic RAG in the background." | Invites catastrophic margin collapse; autonomous agents capable of looping API calls will bankrupt the provider without bounded autonomy and FinOps. |

## Quick Reference

| Concept | Implementation Action |
| :--- | :--- |
| **Hybrid Routing** | Route 90-95% of traffic to edge SLMs; reserve frontier model bursts for <10% of high-reasoning tasks. |
| **Zero-Waste RAG** | Deploy Semantic Caching (e.g., via Zuplo) to intercept and resolve frequent queries without invoking LLM generation. |
| **Edge SLM Moats** | Capitalize on NVFP4 quantization and Blackwell GPUs to offer turnkey, off-cloud deployments for data-sensitive industries. |
| **Agentic FinOps** | Integrate hard consumption limits, cost-tracking, and redundant-call prevention directly into the agent orchestration layer. |
| **Enterprise Gateways** | Utilize CIMD and Scoped Auth middleware to satisfy B2B security and procurement requirements. |