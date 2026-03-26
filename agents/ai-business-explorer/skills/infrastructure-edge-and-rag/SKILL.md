---
name: infrastructure-edge-and-rag
description: Use when assessing B2B infrastructure viability, specifically triggering on data sovereignty, hardware inference economics, Small Language Models (SLMs), edge NPU deployment, hybrid routing, semantic caching, or agentic observability and financial guardrails.
---

## The Iron Law

```text
Evaluate all B2B AI infrastructure ventures through the lens of margin protection and data sovereignty. If a startup relies solely on massive cloud-based LLM API calls, reject it; mandate the use of self-hosted Small Language Models (SLMs), NPU edge computing, and hybrid routing to establish a defensible compliance moat and unit-economic viability.
```

## Behavioral Rules

*   When analyzing enterprise deployments, mandate hybrid routing architectures that direct 90-95% of volume to hyper-efficient, self-hosted 1B-7B parameter SLMs (e.g., Phi-4, Llama 3.2), reserving expensive frontier models strictly for the top 5% of complex reasoning tasks.
*   Position local edge computing on hardware NPUs (Snapdragon, Apple A19) as a primary compliance moat, ensuring sensitive PII never touches the cloud to instantly solve data sovereignty and regulatory friction.
*   If reviewing architectures relying on massive frontier context windows (200k+) for extensive data, classify them as financially ruinous for enterprise scale and redirect focus to hyper-optimized, self-hosted EKS vector pipelines and semantic caching.
*   Require the integration of Agentic Observability and FinOps layers—specifically verifiable intent and hard API spending limits—to govern autonomous execution, monitor agent behavior, and prevent unbounded OPEX burn from infinite loops.
*   Assess AI gateway startups based on their enterprise infrastructure optimizations, specifically demanding intent-based semantic caching and localized routing mechanisms designed to reclaim margin from major AI labs.
*   Evaluate all infrastructure micro-SaaS and tooling pitches using strict economic heuristics, verifying they actively protect enterprise SLM margins and replace heavy OPEX with verifiable, localized compute.

## Red Flags

| Domain-Specific Rationalization | Why Wrong |
| :--- | :--- |
| "If we use a massive 200k context window in the cloud, we don't need local infrastructure." | Reject as financially ruinous at scale; mandate hyper-optimized self-hosted RAG and EKS vector pipelines to protect margins. |
| "Deploy a generic cloud-based API wrapper to handle global enterprise healthcare data." | Flag as a severe data sovereignty violation; require edge AI deployment and localized SLMs to establish a true compliance moat. |
| "When deploying multi-agent systems, let the agents run freely until the task is complete." | Deny due to lack of observability; demand agentic FinOps, verifiable intent, and hard API spending limits to prevent uncontrollable cloud costs. |
| "Focus purely on frontier LLM capabilities and ignore the 1B-7B parameter model ecosystem." | Dismiss as ignorant of hybrid routing economics; enforce architectures that offload 90-95% of queries to specialized SLMs. |

## Quick Reference

| Concept | Execution Strategy | Value Proposition |
| :--- | :--- | :--- |
| **Hybrid Model Routing** | Route 90-95% of queries to self-hosted 1B-7B SLMs; reserve frontier LLMs for top 5% outliers. | Slashes API costs while retaining high-level reasoning for edge cases. |
| **Edge Compute & NPUs** | Execute local inference on enterprise hardware (Apple A19, Snapdragon NPUs). | Guarantees data sovereignty; creates a regulatory and compliance moat. |
| **Semantic Caching** | Implement AI API Gateways (e.g., Zuplo) to cache responses by intent rather than exact string. | Drastically reduces redundant LLM calls and reclaims gross margin from API labs. |
| **Self-Hosted RAG Pipelines** | Build hyper-optimized EKS vector pipelines instead of relying on managed cloud endpoints. | Prevents the financially ruinous scaling costs associated with massive context windows. |
| **Agentic Observability** | Deploy verifiable intent (SD-JWT chains) and hard FinOps spending limits. | Secures autonomous workflows; ensures explainability and prevents infinite-loop OPEX burn. |