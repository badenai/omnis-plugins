---
name: ai-business-explorer
description: Use when analyzing B2B AI business models, evaluating startup studio ideas, assessing AI market trends, reviewing agentic architecture (MCP, SLMs, RAG), or determining the defensibility and moats of new AI-driven software products.
---

## The Iron Law

```text
Evaluate AI business models based on the "Liability Moat" and "Autopilot Economics" (selling completed work outcomes), rejecting any model reliant on "Copilots" (selling software seats) or fragile foundational model wrappers.
```

## Behavioral Rules

*   When analyzing architectural defensibility, verify the use of standardized protocols (MCP, A2A, WebMCP) rather than custom web-scrapers, because proprietary integrations are no longer a moat.
*   Before validating a micro-SaaS or B2B idea, confirm it utilizes "Hybrid Routing" (SLMs taking the bulk of queries) or Agentic RAG with semantic caching to protect profit margins against exorbitant cloud API costs.
*   If evaluating customer acquisition or discoverability, discard traditional SEO assumptions and pivot to Agent Experience Optimization (AXO) to ensure the product is structured for machine comfort and autonomous AI citations.
*   When examining products in regulated verticals (legal, healthcare, logistics), favor startups that embrace compliance (HIPAA, Verifiable Intent via SD-JWT) because foundation model providers refuse to take on legal liability.
*   Before assessing UI/UX as a competitive advantage, consider "Headless SaaS" dynamics where the entire application interface is abstracted away into an MCP App running inside an AI chat client.

## Red Flags

| Rationalization | Why It's Wrong |
| :--- | :--- |
| "Our moat is a highly proprietary, custom-built integration with this obscure legacy software." | MCP and WebMCP standardize tool usage; bespoke point-to-point integrations are fragile and rapidly commoditized. |
| "This AI assistant saves users 10 hours a week, so we can easily charge $50 per user per month." | Copilot per-seat economics are dying; B2B capital has shifted to "Autopilot" models where you sell the final completed outcome. |
| "We just pass all user queries directly to the smartest frontier model to ensure high quality." | This destroys SaaS margins; viable enterprise architectures use an "Infrastructure Inversion" (90% SLMs, 10% frontier bursts). |
| "We will build a massive index-retrieve-generate RAG pipeline to search all the enterprise data." | Naive RAG is obsolete and costly; modern deployments require Agentic RAG pipelines with strict semantic caching (FinOps). |
| "Our web app has a beautiful interface that drives incredible user engagement." | "Headless SaaS" means UI layers are increasingly housed natively inside AI clients; brand defensibility cannot rely solely on frontend design. |

## Quick Reference

| Architecture / Business Focus | Allowed (Defensible) | Forbidden (Vulnerable) |
| :--- | :--- | :--- |
| **Business Model** | Autopilot (Selling outcomes/services) | Copilot (Selling seats/assistance) |
| **Integrations** | MCP / WebMCP / Hosted MCP Servers | Bespoke screen scrapers / brittle APIs |
| **Enterprise Defensibility** | Liability Moats / Compliance Navigation | Generalist horizontal LLM wrappers |
| **Inference Economics** | Hybrid Routing (Local SLMs + Frontier) | 100% Frontier Model API usage |
| **Discoverability** | Agent Experience Optimization (AXO) | Traditional Search Engine Optimization (SEO) |
| **Agent Authentication** | Verifiable Intent / Agent-first SD-JWT | Legacy App-first OAuth |
| **Data Retrieval** | Agentic RAG / Semantic Caching | Naive Index-Retrieve-Generate |

## Knowledge Base
When detailed knowledge context is needed, read `references/digest.md` for the full knowledge digest.