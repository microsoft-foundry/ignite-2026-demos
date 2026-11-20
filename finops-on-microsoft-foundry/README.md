# FinOps on Microsoft Foundry

> [!TIP]
> **Interactive version:** Explore [FinOps on Microsoft Foundry](https://aka.ms/finops-for-foundry-ignite-2026) for a guided tour of everything below, with filterable sessions and interactive examples.

## FinOps in Microsoft Foundry: full demo

https://github.com/user-attachments/assets/625d8161-95ae-4c08-a046-cfc07f91d943

In this 7-minute demo, Kosti Vasilakakis from Microsoft Foundry follows a fictional bank, Woodgrove, whose fraud desk uses an AI agent to prepare suspicious-activity cases for analysts. After version 2 of the agent ships, its cost per run climbs sharply even though analysts see no difference. The demo traces the problem the way a FinOps team would: the Fleet overview and Cost view show which project, agent, and model are driving spend. The agent's traces then reveal that every step runs on the largest model and that a date stamp at the top of each prompt prevents prompt caching. Insights scans the traces automatically and flags the policy text that gets resent on every call.

To fix the cost, an evaluation over closed cases shows Model Router in cost mode matching the largest model's quality at about a tenth of the price. Agent Optimizer then tests combinations of models and instructions and recommends a smaller model with shorter instructions. Version 3 brings cost per run back down with no change in review quality. The demo ends with cost controls, which set dollar or token budgets on a resource, project, model, agent, or single conversation. It creates a per-conversation token budget with an alert at 80% and a block at 100%, then shows a conversation stopped by an error that names the control that blocked it.

**Download the video:** [FinOps in Microsoft Foundry Full Demo (MP4, 4K, 341 MB)](https://github.com/microsoft-foundry/ignite-2026-demos/raw/main/finops-on-microsoft-foundry/FinOps%20in%20Microsoft%20Foundry%20Full%20Demo.mp4)

## [FinOps in Microsoft Foundry: see your token spend, hit your quality bar for less, and set limits](https://aka.ms/Ignite26/foundryfinops)

In this Microsoft Foundry Blog post, Kosti Vasilakakis, Avinav Jami, and Bhuwan Sahni walk through FinOps for AI end to end with the same fictional Woodgrove Bank fraud-review agent shown in the demo video above. When version 2 of the agent quadruples the cost per case, from about 10 cents to about 40, the team uses Fleet, Operations, and Cost (preview) to find the project, agent, and model behind the spend. A trace then shows every step running on the frontier model and a timestamp at the top of the prompt that stops prompt caching from ever getting a hit. Insights (preview) flags the full fraud policy being resent at every step. The post also explains why Foundry's cost figures come from Azure Cost Management, so engineering and finance see the same numbers, and why cost shows up hours after usage.

To fix the cost, the team first sets a quality bar with an evaluation over 50 closed cases. Model router in Cost mode matches the frontier model's score for about a tenth of the cost. The post then works through four levers: the right model for each step, prompt caching, sending fewer tokens, and the right deployment type (Batch, Flex, or provisioned throughput). Agent Optimizer (preview) tunes the system prompt along the way, and version 3 halves the cost per case to about 20 cents at the same quality. It ends with cost controls (preview), which are dollar or token budgets on a project, deployment, agent, or hosted agent session that alert at a threshold or block new requests. It also covers customer results from Docusign and Enhans, and what's next: caller attribution (private preview) and bringing Foundry cost data into Agent 365.

**Link to blog:** [FinOps in Microsoft Foundry](https://aka.ms/Ignite26/foundryfinops)

---

# Ignite 2026 sessions

Ignite runs November 17–20, 2026, in San Francisco and online. These sessions cover cost on Microsoft Foundry. After the event, check each session page for the recording.

| Session | Format | What it covers |
| --- | --- | --- |
| [BRK308: How Microsoft IQ shapes the cost of enterprise AI](https://ignite.microsoft.com/en-US/sessions/BRK308) | Breakout | How Work IQ, Foundry IQ, Fabric IQ, and Web IQ create different cost patterns, with a live cost-estimation demo |
| [BRK280: Designing an agent harness that orchestrates models](https://ignite.microsoft.com/en-US/sessions/BRK280) | Breakout | Routing tasks to different models to balance quality, latency, cost, and control |
| [BRK249: From traces to better agents: The Foundry improvement loop](https://ignite.microsoft.com/en-US/sessions/BRK249) | Breakout | Using traces, evaluations, and optimization in Foundry to improve agent quality and manage cost |
| [BRK482: FinOps for AI: Partner Playbook for Building AI Solutions and Services](https://ignite.microsoft.com/en-US/sessions/BRK482) | Breakout | A FinOps approach for partners to anticipate costs, optimize token use, and build profitable AI services |
| [LTG1201: Optimizing AI decisions with the model router in Foundry Models](https://ignite.microsoft.com/en-US/sessions/LTG1201) | Lightning talk | Using model router to choose models per request |
| [LTG1206: Agent FinOps: Designing agents that scale responsibly](https://ignite.microsoft.com/en-US/sessions/LTG1206) | Lightning talk | Designing agents with cost in mind |

For every FinOps session at Ignite, including Copilot and GitHub sessions, see [Your guide to FinOps for AI at Microsoft Ignite 2026](https://techcommunity.microsoft.com/blog/finopsblog/your-guide-to-finops-for-ai-at-microsoft-ignite-2026/4569117).

---

# Presentation and documentation

## [FinOps for AI: Plan, manage, and optimize AI value with Microsoft Azure and GitHub](./FinOps%20for%20AI%20Azure%20and%20GitHub.PDF)

This 27-slide deck covers FinOps for AI across Microsoft Azure and GitHub, organized around three disciplines: planning, spend management, and optimization. It opens with the questions customers ask most, from "what are we actually spending on tokens?" to "how do we measure ROI?", and maps Microsoft products to each layer of the problem: Microsoft IQ for context, API Management, Agent 365, Azure Cost Management, and Foundry for cost control, and provisioned throughput and prepurchase plans for procurement.

The planning slides cover estimating business value, pricing the full solution (tokens, supporting infrastructure, and human oversight) with the Azure pricing calculator, and projecting a baseline ROI. The spend management slides cover token visibility in GitHub Enterprise and API Management, token caps and chargeback, Azure Cost Management, and comparing actual ROI against the baseline. The optimization slides cover four runtime levers (right model, right context, caching, and right execution) using Model Router, Microsoft IQ, prompt, semantic, and tool-result caching, and Agent Optimizer (preview) in Foundry, plus multi-model routing in GitHub Copilot.

**Download the deck:** [FinOps for AI Azure and GitHub (PDF)](./FinOps%20for%20AI%20Azure%20and%20GitHub.PDF)

## [Plan and manage costs for Microsoft Foundry](https://learn.microsoft.com/en-us/azure/foundry/concepts/manage-costs)

Foundry is made up of several optional Azure services, so there's no single line item in the Azure pricing calculator. This guide shows how to estimate costs for the services in your architecture, validate those estimates with a small test workload, and reconcile them against actual meter-level charges in Microsoft Cost Management before rolling out to production. It also explains how Foundry is billed, including pay-as-you-go, commitment tiers, token-based pricing for models, and the training, hosting, and inference charges for fine-tuned models.

Once you're running, the guide walks through monitoring spend in the Foundry portal, where you can see estimated costs for agents and model deployments by project and date range. For financial reconciliation, it covers using Cost Management in the Azure portal to break down costs by resource and meter, allocate shared spend back to teams with project-level chargeback (preview), set up budgets and alerts, and export cost data for analysis in tools like Excel or Power BI.

**Link to doc:** [Plan and manage costs for Microsoft Foundry](https://learn.microsoft.com/en-us/azure/foundry/concepts/manage-costs)

## [Attribute and cap model spend](https://ai.gateway.azure.com/docs/finops)

Azure AI Gateway turns token usage into estimated USD cost and emits it as OpenTelemetry metrics you can send to Application Insights or your own dashboards. By giving each application its own API key, or adding validated Microsoft Entra claims as metric dimensions, you can see exactly which applications, callers, and cost centers are driving model spend.

Once you know where the spend is going, cost-limit policies let you cap it. Each API key or Entra identity gets its own estimated USD allowance that renews on a set period, such as weekly or monthly, with overrides to raise or lower the limit for specific callers. Keep in mind these are estimates based on a Microsoft-maintained pricing catalog, not billing records, so the docs also cover how costs are calculated and how to spot models with missing prices.

**Link to doc:** [Attribute and cap model spend](https://ai.gateway.azure.com/docs/finops)

## [Lower the cost of each request](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/model-router)

Model router is a model you deploy like any other, but it looks at each prompt and sends it to the most suitable underlying model, so simple requests don't pay frontier-model prices. You choose a routing mode: Balanced (the default) picks the cheapest model within a narrow quality range of the best one, Cost widens that range to save more, and Quality always picks the highest-rated model. The usable context window is limited by the smallest underlying model, so use a model subset if you need longer contexts, and compare the router against your current setup before switching.

Two other features cut cost without changing models. Prompt caching reuses identical prompt prefixes, so keep stable content such as system instructions and tool definitions at the top and put content that changes at the bottom. Cache reads are discounted on standard deployments, but GPT-5.6 and later models can also charge for cache writes, so a prefix that keeps changing costs more. For work that doesn't need an immediate answer, global batch processes large jobs from a single file with a 24-hour target turnaround at 50% less than global standard pricing, and it uses its own quota so live traffic isn't affected.

**Links to docs:** [Model router concepts](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/model-router) | [How to use model router](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/model-router) | [Prompt caching](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/prompt-caching) | [Global batch processing](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/batch)

## [Commit to capacity with PTUs, reservations, and prepurchase](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/provisioned-throughput)

Provisioned throughput units (PTUs) reserve dedicated model capacity for a deployment and are billed per PTU per hour whether or not you send traffic. That pays off for predictable, high-volume, latency-sensitive workloads, while standard pay-per-token deployments remain the better fit for development and unpredictable traffic. PTU quota is granted per subscription, region, and deployment type rather than per model. The sizing and billing guides help you work out how many PTUs a workload needs, and spillover can send requests that overflow a busy provisioned deployment to a matching standard deployment.

To lower the hourly PTU rate, buy a Foundry Provisioned Throughput Reservation for a one-month or one-year term. You buy reservations separately for Global, Data Zone, and Regional deployments, and they don't guarantee capacity, so create your deployments first. Deleting a deployment doesn't cancel its reservation. For a broader commitment, the Microsoft Agent Prepurchase Plan sells discounted Agent commit units for a one-year term that pay down eligible usage across Foundry, Copilot Studio, Fabric, and GitHub. Its discount doesn't combine with other discounts you already have.

**Links to docs:** [Provisioned throughput overview](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/provisioned-throughput) | [PTU billing](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/provisioned-throughput-billing) | [PTU sizing](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/provisioned-throughput-sizing) | [Spillover](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/spillover-traffic-management) | [PTU reservations](https://learn.microsoft.com/en-us/azure/cost-management-billing/reservations/microsoft-foundry) | [Agent Prepurchase Plan](https://learn.microsoft.com/en-us/azure/cost-management-billing/reservations/agent-pre-purchase)

---

# Blog series

## [The Economics of Agent Optimization](https://azure.microsoft.com/en-us/blog/tag/the-economics-of-agent-optimization/)

In this four-part Azure Blog series, Foundry product leaders argue that keeping agent costs under control takes ongoing management, not just a cheaper model. Part 1 explains why costs climb: models resend the full context on every turn, and an agent can make many model calls to finish one task. It then frames the series around three decisions: optimize each request, improve each agent over time, and govern spend. Part 2 covers the runtime levers: choosing the model and deployment type (model router, standard, priority, provisioned, batch, or fine-tuning), prompt and semantic caching, prompt and agent optimizers, and observability.

Part 3 is about context engineering, which means controlling what goes into the context window on each turn. It covers Foundry IQ for retrieval, Toolbox and tool search so agents don't send every tool definition, centrally managed skills, and agent memory. Part 4 covers governance: seeing spend through Foundry cost views, project-level attribution, and gateway token metrics; capping it with Foundry Control Plane token quotas, the API Management `llm-token-limit` policy, and Cost Management budgets; and measuring business value to decide which agents to scale or retire.

**Links to posts:**

1. [From pilots to measurable returns](https://azure.microsoft.com/en-us/blog/the-economics-of-agent-optimization-from-pilots-to-measurable-returns/)
2. [Four ways to lower the cost](https://azure.microsoft.com/en-us/blog/the-economics-of-agent-optimization-four-ways-to-lower-the-cost/)
3. [Context engineering for enterprise AI agents](https://azure.microsoft.com/en-us/blog/the-economics-of-agent-optimization-context-engineering-for-enterprise-ai-agents/)
4. [How AI agent governance controls cost and proves ROI](https://azure.microsoft.com/en-us/blog/the-economics-of-agent-optimization-how-ai-agent-governance-controls-cost-and-proves-roi/)

---

# Videos

## [Tokenomics | The new AI currency & your options explained](https://www.youtube.com/watch?v=mB0IyELzjRg)

[![Tokenomics | The new AI currency & your options explained](https://img.youtube.com/vi/mB0IyELzjRg/maxresdefault.jpg)](https://www.youtube.com/watch?v=mB0IyELzjRg)

April Gittens, Microsoft Principal Cloud Advocate, joins Jeremy Chapman, Microsoft 365 Director, to break down how token pricing really works and why AI costs spike as adoption scales. Because models are stateless, every turn resends the system prompt, conversation history, tool definitions, and retrieved documents as input tokens. They cover the design fixes that keep this in check: trimming system prompts, summarizing conversation history, capping output tokens with matching instructions, and caching static prefixes at roughly 10% of normal input cost.

Model choice is the biggest lever, and the video shows how Microsoft Foundry helps you make it. You can compare models side by side on quality, cost, and throughput, or let Model Router pick a model for each prompt. Toolbox sends only the tools a request needs, cutting one agent run from about 4,700 input tokens to 467, and Agent Optimizer tests prompt, model, and tool configurations together to find the best combination.

**Link to video:** [Tokenomics | The new AI currency & your options explained](https://www.youtube.com/watch?v=mB0IyELzjRg)

For more about managing AI costs, visit [aka.ms/FoundryTokenomics](https://aka.ms/FoundryTokenomics).

---

# Hands-on lab

## [AI-Gateway FinOps framework lab](https://github.com/Azure-Samples/AI-Gateway/tree/main/labs/finops-framework)

This lab from the Azure-Samples AI-Gateway repo applies the FinOps Framework to models served through the AI gateway in Azure API Management. That's a separate route from the Azure AI Gateway cost limits described above. A Jupyter notebook deploys the environment with Bicep and applies a token-limit policy to each API Management product, so every team or customer gets its own allowance. It also includes a dashboard template and Azure Monitor workbooks for tracking spend.

When a subscription goes over its cost quota, an Azure Monitor alert triggers a Logic App that automatically disables that API Management subscription. To run it, you need an Azure subscription where you have Contributor plus Role Based Access Control Administrator (or Owner), Python 3.12 or later, VS Code with the Jupyter extension, uv, and the Azure CLI. A separate notebook removes the resources when you're done.

**Link to lab:** [AI-Gateway FinOps framework lab](https://github.com/Azure-Samples/AI-Gateway/tree/main/labs/finops-framework)

---

# Further reading

This resource applies to FinOps across the Microsoft Cloud rather than to Foundry specifically.

- [FinOps toolkit](https://github.com/microsoft/finops-toolkit): Microsoft's open-source tools for adopting FinOps on the Microsoft Cloud. It's useful as a reporting layer on top of Foundry cost data.
