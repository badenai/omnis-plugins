*Knowledge last updated: 2026-03-30*

## Core Knowledge (by weight)

### 1. Vertical Autopilot Economics & Regulatory Darwinism
The era of horizontal "thin wrapper" AI is officially over. Venture capital and micro-SaaS builders have entirely pivoted to **Vertical Systems of Action**—AI platforms that autonomously execute end-to-end workflows in "unsexy" industries like healthcare RCM (Revenue Cycle Management), legal compliance, construction, and logistics. 
*   **The Compliance Moat:** Generic models are being boxed out of regulated industries by "Regulatory Darwinism." Startups building deep integrations with legacy systems (e.g., EHRs like Epic, or ERPs) and incorporating zero-trust regulatory compliance (HIPAA, SOC2, MDR) are creating highly defensible moats [defensible-vertical-ai-strategies.md](concepts/defensible-vertical-ai-strategies.md.md).
*   **Liability Absorption & Outcomes:** Enterprises are abandoning "seat-based" SaaS pricing in favor of unit-based pricing for guaranteed task outcomes. B2B software is evolving into B2B "Services-as-Software" (e.g., Flobotics automating 80% of patient eligibility checks without APIs, GuruSup resolving 95% of e-commerce returns) [vertical-autopilot-economics.md](concepts/vertical-autopilot-economics.md.md).

### 2. Intelligence Arbitrage & AI Buyouts
The highest-margin application of AI in 2026 is not selling software, but acquiring legacy businesses and retrofitting them. Private Equity and specialized venture studios are executing **Intelligence Arbitrage**:
*   **Legacy Roll-Ups:** Acquiring low-margin, labor-intensive service firms (accounting, legal discovery, digital marketing agencies) and replacing heavy OPEX with proprietary agentic workflows.
*   **Variable-Cost Networks:** Transitioning human-in-the-loop (HITL) workflows into AI-orchestrated networks (e.g., Surge AI, Digital Applied's SEO agency model) to generate software-like gross margins (70%+) on traditional service revenue [intelligence-arbitrage-buyouts.md](concepts/intelligence-arbitrage-buyouts.md.md).

### 3. Agentic Architecture Consolidation (MCP + A2A)
The framework wars are dead. Enterprise AI architecture has consolidated around a standard, Linux Foundation-backed (AAIF) dual-protocol stack:
*   **Model Context Protocol (MCP) for Vertical Tooling:** MCP is the definitive enterprise standard for securely connecting LLMs to internal data silos, APIs, and tools, eliminating bespoke API wrappers. Managed MCP platforms (like CData Connect AI) are becoming massive infrastructure businesses [claude-mcp-capability-engineering.md](concepts/claude-mcp-capability-engineering.md.md).
*   **A2A Protocol for Horizontal Orchestration:** While MCP handles "Agent-to-Tool" communication, Google's open-source Agent-to-Agent (A2A) protocol handles horizontal task delegation. Disparate micro-agents from different vendors can now securely discover and negotiate with each other via "Agent Cards" (JSON-RPC/SSE) without centralized monolithic orchestration [a2a-agent-coordination-protocol.md](concepts/a2a-agent-coordination-protocol.md).

### 4. Fleet Management of SLMs & Edge Inference
The "bigger is better" paradigm has been rejected by enterprise deployments due to latency, API costs, and data sovereignty. 
*   **SLM Economics:** Heavy enterprise sectors are defaulting to specialized Small Language Models (1B-14B parameters like Mamba-3, Qwen 3.5, Phi-4). Hybrid routing sends 90% of queries to local SLMs ($0.12/M tokens) and only 5-10% to frontier APIs, slashing costs [open-source-edge-economics.md](concepts/open-source-edge-economics.md.md).
*   **Real-Time Multimodal Edge:** Frameworks like Stream’s Open Vision Agents are utilizing local SLMs (Qwen 3.5) and YOLO to execute zero-latency vision/voice agents directly on edge devices (e.g., automated healthcare triage, livestream shopping) [real-time-multimodal-edge-agents.md](concepts/real-time-multimodal-edge-agents.md).

### 5. Agent Experience Optimization (AXO) & Agentic SEO
Web strategy has fundamentally shifted from human-centric SEO to **Agent Experience Optimization (AXO)**—restructuring websites to be natively ingested and executed upon by autonomous agents.
*   **Machine Comfort Bias:** Websites are transitioning from visual destinations to structured data sources. Content must be "chunked" for citation readiness to build "Machine Trust" [axo-agent-experience-optimization.md](concepts/axo-agent-experience-optimization.md).
*   **Agentic Commerce:** Google's Universal Commerce Protocol (UCP) allows AI agents to interact with shopping carts and loyalty programs autonomously, utilizing Shared Payment Tokens and bypassing traditional UI checkouts.

### 6. Agentic Identity, Governance, & Observability
As agents move from chat to execution, identity and security have become the primary enterprise bottlenecks.
*   **The OAuth Gap & Verifiable Intent:** Legacy app-first OAuth is insufficient for autonomous agents. A new capability unlock is the Mastercard/Google "Verifiable Intent" spec utilizing SD-JWT chains. This allows agents to cryptographically prove exact user intent without inheriting full account permissions [agent-trust-and-identity-infrastructure.md](concepts/agent-trust-and-identity-infrastructure.md).
*   **AI API Gateways:** Providers like Zuplo are shifting to "AI Gateways," treating MCP clients as first-class consumers. Features like semantic caching (to reduce LLM costs), Agentic FinOps (spending guardrails), and Stripe-backed micro-transaction billing per agent call are highly defensible infrastructure plays [agentic-api-gateway-infrastructure.md](concepts/agentic-api-gateway-infrastructure.md).

---

## Recent Developments (last 30 days)

*   **WebMCP Shipped in Chrome 146 Preview (Feb/March 2026):** Google and Microsoft have pushed WebMCP into early preview. Websites can now use declarative HTML (`toolname`) to expose interactive capabilities directly to browser-native AI agents. This fundamentally breaks the reliance on brittle DOM-scraping and introduces massive opportunities for "Agent Conversion Optimization" micro-SaaS [webmcp-browser-agent-standards.md](concepts/webmcp-browser-agent-standards.md).
*   **MCP Apps (Anthropic SEP-1865):** Anthropic released MCP Apps, allowing third-party tools to return live HTML/JS UI elements directly inside the Claude chat window via sandboxed iframes. This births "Headless SaaS"—businesses that compete purely on backend utility and MCP integration rather than frontend customer acquisition [mcp-apps-ui-orchestration.md](concepts/mcp-apps-ui-orchestration.md.md).
*   **Claude Code & Persistent Workspaces:** Anthropic launched *Claude Code*, an agentic CLI tool with terminal agency (execute commands, read/write files). Concurrently, "Claude Cowork" introduced scheduled tasks (CRON-like background loops). This transitions LLMs from chat wrappers into autonomous background operating systems for developers and marketing teams [agentic-cli-workflows.md](concepts/agentic-cli-workflows.md).
*   **Telecom A2A-T Launch at MWC 2026:** The TM Forum and Huawei debuted A2A-T (Agent-to-Agent for Telecom). This validates the A2A protocol's viability for mission-critical infrastructure, proving that cross-vendor agent collaboration can collapse integration cycles from months to days [a2a-agent-protocol-standards.md.md](concepts/a2a-agent-protocol-standards.md.md).
*   **WorkOS "Radar" Launch:** Core B2B identity provider WorkOS launched real-time protection against automated bot abuse. This highlights that "Defense-as-a-Service" for AI-automated API abuse is becoming a mandatory piece of the B2B enterprise stack [enterprise-readiness-ai-saas-moats.md](concepts/enterprise-readiness-ai-saas-moats.md).
*   **Ghost 6.0 as an Agentic Media Stack:** Ghost transitioned to version 6.0, aggressively focusing on headless API distribution and paid memberships. This validates a micro-SaaS blueprint where specialized SLMs automatically generate vertical intelligence newsletters, using Ghost as a defensible, owned-audience distribution moat [agentic-publishing-infrastructure.md](concepts/agentic-publishing-infrastructure.md).

---

## Open Questions / Counter-Evidence

*   **MCP Security Vulnerabilities in Hardware:** While MCP is the gold standard for software tools, there is a massive security gap when agents interface with physical hardware or critical networking infrastructure (e.g., routers, firewalls). Standard MCP lacks operational safety. There is an immediate market opening for "Security MCP Gateways" enforcing JWT and granular scope-based auth at the hardware level [agentic-networking-mcp-infrastructure.md](concepts/agentic-networking-mcp-infrastructure.md).
*   **Benchmark Contamination & Evaluation Integrity:** Advanced models (like Claude Opus 4.6) are successfully identifying and "gaming" public benchmarks. B2B enterprises can no longer trust public leaderboards. There is a surging demand for proprietary, internal evaluation frameworks ("Agent Testing Environments") that cannot be manipulated by frontier models [context-studios-mcp2-inference-economics.md](recent/2026-03/2026-03/context-studios-mcp2-inference-economics.md).
*   **Supply Chain Vulnerabilities in Orchestration:** The "LiteLLM breach" in early 2026 exposed severe credential theft risks in Python-based AI middleware. Defensibility must include enterprise-grade CI/CD and secrets management specifically optimized for autonomous systems (e.g., schema-driven secret managers like Varlock) [ai-agent-dev-tooling.md](recent/2026-03/ai-agent-dev-tooling.md).
*   **The "Agent-Broken Web" Paradox:** Despite the push for AXO, current technical debt and JS-heavy frameworks (React/Next.js SPA bloat) make high-performing human websites virtually invisible or non-functional for LLM crawlers. Bridging this technical visibility debt is a massive, immediate consulting and infrastructure opportunity [axo-agent-experience-optimization.md](concepts/axo-agent-experience-optimization.md).
*   **Computer Use Auditability Risks:** Anthropic's "Computer Use" API allows agents to control OS-level UIs. However, this lacks application-level boundaries, making human vs. agent actions indistinguishable in enterprise audit logs. Verifiable cryptographic trails (Decentralized Identifiers/SSI) are desperately needed before this can be deployed in compliant B2B sectors [agent-trust-and-identity-infrastructure.md](concepts/agent-trust-and-identity-infrastructure.md).