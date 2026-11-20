# Foundry Models on Microsoft Foundry

Microsoft Foundry Models gives you one place to discover, evaluate, deploy, and operate more than 11,000 models from Microsoft, OpenAI, Anthropic, Meta, Mistral, DeepSeek, Cohere, xAI, Hugging Face, and more. The resources below walk you through choosing the right model for each task, deploying it the way your workload needs, keeping cost and quality in balance, and governing it in production.

---

# Ignite 2026 sessions

Ignite runs November 17–20, 2026, in San Francisco and online. These sessions cover models on Microsoft Foundry. After the event, check each session page for the recording.

| Session | Format | What it covers |
| --- | --- | --- |
| [BRK280: Designing an agent harness that orchestrates models](https://ignite.microsoft.com/en-US/sessions/BRK280) | Breakout | Routing tasks to different models to balance quality, latency, cost, and control |
| [BRK252: Turn your data into AI advantage with Training in Microsoft Foundry](https://ignite.microsoft.com/en-US/sessions/BRK252) | Breakout | Fine-tuning, reinforcement learning, and RL environments in Foundry, with customer stories from Docusign and Heidi Health |
| [BRK249: From traces to better agents: The Foundry improvement loop](https://ignite.microsoft.com/en-US/sessions/BRK249) | Breakout | Using traces, evaluations, and optimization in Foundry to improve agent quality and manage cost |
| [LTG1201: Optimizing AI decisions with the model router in Foundry Models](https://ignite.microsoft.com/en-US/sessions/LTG1201) | Lightning talk | The latest model router capabilities for optimizing quality, latency, and cost |

---

# Ignite 2026 announcements

## [Ignite 2026: Building the frontier ecosystem](https://blogs.microsoft.com/blog/2026/11/17/ignite-2026-building-the-frontier-ecosystem/)

In his Ignite 2026 opening keynote, Satya Nadella, Microsoft Chairman and CEO, frames models around one goal: matching the right intelligence to each task with the best economics. For Foundry, that means GPT-6.2 arriving in Foundry, Meta's latest models all coming to Foundry, and Microsoft-Decision-1.1 becoming generally available for routing, classification, and other decisions inside your software. The keynote also introduces the MAI Code 2 family of agentic coding models and MAI Cyber 2 Flash for security work.

It also announces MAI Licensed Weights, which gives trusted customers access to Microsoft AI model weights so you can customize a model with your own data and run it in your own Azure environment. Beyond models, the keynote covers Microsoft IQ, Agent 365 Business Analytics for tying AI spend to business outcomes, and the Microsoft AI Transparency Initiative. The Book of News has the full list of Ignite announcements.

**Links:** [Ignite 2026: Building the frontier ecosystem](https://blogs.microsoft.com/blog/2026/11/17/ignite-2026-building-the-frontier-ecosystem/) | [Microsoft Ignite 2026 Book of News](https://news.microsoft.com/events/ignite/2026/book-of-news/)

## [GPT-6.2 Astra and GPT-6.2 Sol now generally available in Microsoft Foundry](https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/gpt-6-2-astra-and-gpt-6-2-sol-now-generally-available-in-microsoft-foundry/4574122)

OpenAI's GPT-6.2 Astra and GPT-6.2 Sol are generally available in Foundry. GPT-6.2 Astra is the next reasoning model in the Astra family, built for the most demanding work, with improvements in reasoning, writing, coding, computer use, and creating documents, slides, and spreadsheets. In Foundry benchmark testing, it reached higher average accuracy than GPT-6 Astra with substantially fewer output tokens, so you get better results at a lower cost per task for the same per-token price.

GPT-6.2 Sol, built on GPT-6.1, is designed for production agents that run all day, with more concise technical writing, more focused coding and debugging, and better decisions about when and how to use tools. Both models support 12-hour prompt cache writes on Standard deployments, alongside the 30-minute default, so agents that go quiet overnight can still reuse cached instructions, documents, and tool definitions at discounted rates. Both run with the same layered safety protections as the rest of the GPT-6 series in Foundry.

**Link to post:** [GPT-6.2 Astra and GPT-6.2 Sol now generally available in Microsoft Foundry](https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/gpt-6-2-astra-and-gpt-6-2-sol-now-generally-available-in-microsoft-foundry/4574122)

## [New MAI models and Microsoft-Decision-1.1](https://microsoft.ai/news/microsoft-ignite-2026/)

Microsoft AI released a family of new models at Ignite, built for strong quality at a price you can run at scale. MAI Image 2.7 and MAI Image 2.7 Flash, for image editing and high-volume image generation, are available in Foundry. MAI Code 2 and MAI Code 2 Flash target everyday enterprise coding tasks and are generally available in GitHub Copilot, with MAI Code 2 Flash also in limited-access preview in Foundry. The lineup also includes MAI Cyber 2 Flash for security, MAI Realtime 1 for live speech-to-speech conversations, and MAI Licensed Weights for running a customized MAI model in your own Azure environment.

Microsoft-Decision-1.1 is generally available in Foundry. It's a decision model that chooses among the actions you allow, within the constraints you set, and returns calibrated confidence scores so your application can defer when it's uncertain. It's built for structured decisions such as routing, classification, prioritization, verification, and workflow control. Version 1.1 is more than twice as fast as the first model, adds image input, and has been used by more than 4,000 customers since its public preview.

**Links to posts:** [Seven new world-class models at scalable price-performance](https://microsoft.ai/news/microsoft-ignite-2026/) | [MAI Code 2 and Code 2 Flash](https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/) | [MAI Image 2.7](https://microsoft.ai/news/introducing-mai-image-2-7/) | [Microsoft-Decision-1.1 is now generally available](https://commandline.microsoft.com/microsoft-decision-model-ga/)

## [What's new in model router: November 2026](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/whats-new-model-router)

Model router picked up several updates in November. With Auto (preview), you set `model` to `auto` in a request and model router handles it with nothing to deploy. Model router now supports the Responses API natively and adds the Anthropic Messages API (preview), so it also works with Claude Code and the Claude Agent SDK. New per-request routing controls (preview) let you set the routing mode or limit the models for a single request, and adaptive session affinity keeps a conversation on the same model while its prompt cache is still warm.

You can now see what routing saves you. The new **Monitor** tab on a model router deployment shows requests by model, latency, cache hit rate, and estimated cost compared with single-model baselines, and you can evaluate model router against a single model in the Foundry portal. Routed requests also use your own provisioned and pay-as-you-go deployments first (preview), so traffic fills the capacity you already pay for. As of November 18, 2026, model router routes across 45 models, including new Claude 5.5 models, GPT-6.1 models, and MAI Code 2 Flash.

**Links to docs:** [What's new in model router](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/whats-new-model-router) | [Model router APIs](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/model-router-apis) | [Monitor model router](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/monitor-model-router)

---

# Presentation and documentation

## [Foundry Models: Build adaptable, reliable, and scalable AI systems](./Microsoft%20Foundry%20Models%20Pitch%20Deck.PDF)

This 34-slide deck lays out how to build AI systems on Foundry Models that keep up as new models arrive and your workloads grow. It's organized in three stages. **Start with evaluations** covers exploring the model catalog, comparing models on your own data, and setting a quality bar before you commit. **Optimize** covers Model Router, the deployment types (Standard, Priority, Provisioned, Batch, Flex, and managed compute), where your data is processed (Global, Data Zone, or Regional), and post-training options for when an off-the-shelf model isn't enough.

**Operate and learn** covers running models in production: observability with tracing and continuous evaluation, and governance with Microsoft Entra, Microsoft Defender, Microsoft Purview, and Agent 365. The deck closes with a five-step playbook for getting started and links to the Foundry portal, SDK, documentation, and learning resources.

**Download the deck:** [Foundry Models (PDF)](./Microsoft%20Foundry%20Models%20Pitch%20Deck.PDF)

## [Microsoft Foundry Models overview](https://learn.microsoft.com/en-us/azure/foundry/concepts/foundry-models-overview)

The model catalog in Foundry includes more than 10,000 models, with about 50 new models published each month. Models fall into two groups. Models sold by Azure are hosted by Azure, billed through your Azure subscription, covered by Azure SLAs, and supported by Microsoft. Models from partners and community, such as Anthropic's Claude models and Hugging Face models, are supported by their providers and billed through Azure Marketplace. You can filter the catalog by task, provider, region, deployment type, lifecycle stage, and capabilities, and compare models with the leaderboard and benchmark data.

The overview also explains your two ways to run a model. Serverless deployments give you an API and bill by token, while managed compute runs model weights on dedicated virtual machines and bills by core hour. The companion page on models sold by Azure lists every Azure OpenAI model, plus selected models from Cohere, DeepSeek, Meta, Mistral AI, and xAI, with their capabilities, context windows, and region availability by deployment type.

**Links to docs:** [Foundry Models overview](https://learn.microsoft.com/en-us/azure/foundry/concepts/foundry-models-overview) | [Foundry Models sold by Azure](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/models-sold-directly-by-azure)

## [Deploy a model and choose a deployment type](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/how-to/deploy-foundry-models)

To deploy a model, go to **Build** > **Catalog** > **Model Catalog** in the Foundry portal, pick a model, review its model card, and select **Deploy**. Partner and community models also ask you to accept Azure Marketplace terms. After deployment, you can try the model in the playground and copy sample code to call it from your app. For some supported models, instant access (preview) lets you call the model by name without creating a deployment at all.

Every deployment has a type that decides where your data is processed and how you pay. Start with Global Standard: it gets new models first, has the lowest price, and offers the broadest region coverage. Move to Data Zone (US, EU, or Asia Pacific) or a geography-based type when you have data residency requirements, to Provisioned when you need reserved, predictable throughput, or to Batch for large asynchronous jobs at a 50% discount. Each deployment uses tokens-per-minute (TPM) quota, which is assigned per subscription, region, model, and deployment type. The quota guide shows how to view your quota, allocate it across deployments, and request more.

**Links to docs:** [Deploy Foundry Models in the Foundry portal](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/how-to/deploy-foundry-models) | [Deployment types](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/deployment-types) | [Manage quota](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/quota)

## [Use Claude models in Microsoft Foundry](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/claude-models)

Claude is available in Foundry in two versions. Hosted on Azure runs end to end on Azure and is generally available. Hosted on Anthropic runs on Anthropic's infrastructure and gives you the full Claude catalog. You deploy Claude from the model catalog with an Azure Marketplace subscription, choose Global Standard or US Data Zone Standard (for supported models), and call it through the Anthropic Messages API with the Anthropic SDKs or REST. You can authenticate with Microsoft Entra ID or an API key. The concepts page lists each Claude model's context window, output limits, supported capabilities, and preview status.

If your developers use Claude Code, Anthropic's agentic coding tool, you can point it at your Foundry deployments so it runs on Azure with your role-based access control, networking, and cost management. The setup guide covers the prerequisites, environment variables, Entra ID sign-in, and using model router to route across Claude models.

**Links to docs:** [Claude models in Microsoft Foundry](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/claude-models) | [Deploy and use Claude models](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/how-to/use-foundry-models-claude) | [Configure Claude Code for Microsoft Foundry](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/how-to/configure-claude-code)

## [Route each request to the right model](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/model-router)

Model router is a model you deploy like any other, but it looks at each prompt and sends it to the most suitable underlying model, so simple requests don't pay frontier-model prices. You choose a routing mode: Balanced (the default) picks the cheapest model within a narrow quality range of the best one, Cost widens that range to save more, and Quality always picks the highest-rated model. You can also limit routing to a subset of models. The usable context window is set by the smallest model in that subset.

Two other features lower cost without changing models. Prompt caching reuses identical prompt prefixes, so keep stable content such as system instructions and tool definitions at the top of your prompt and put content that changes at the bottom. For work that doesn't need an immediate answer, global batch processes large jobs from a single file with a 24-hour target turnaround at 50% less than Global Standard pricing, and it uses its own quota so your live traffic isn't affected.

**Links to docs:** [Model router concepts](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/model-router) | [How to use model router](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/model-router) | [Prompt caching](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/prompt-caching) | [Global batch processing](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/batch)

## [Plan for pricing and capacity](https://azure.microsoft.com/en-us/pricing/details/microsoft-foundry/)

Foundry is made up of several optional Azure services, so cost planning starts with the services in your architecture. The cost management guide shows how to estimate costs, validate them with a small test workload, monitor spend by project in the Foundry portal, and reconcile it in Microsoft Cost Management. It also explains how models are billed, including token-based pricing for serverless deployments and the training, hosting, and inference charges for fine-tuned models.

When you have predictable, high-volume, latency-sensitive traffic, provisioned throughput units (PTUs) reserve dedicated model capacity for a deployment and are billed per PTU per hour. The billing guide explains how PTUs are charged, and a Microsoft Foundry Provisioned Throughput Reservation lowers the hourly rate for a one-month or one-year term. Standard pay-per-token deployments remain the better fit for development and unpredictable traffic. For a full walkthrough of AI cost management on Foundry, see [FinOps on Microsoft Foundry](../finops-on-microsoft-foundry/README.md).

**Links:** [Microsoft Foundry pricing](https://azure.microsoft.com/en-us/pricing/details/microsoft-foundry/) | [Plan and manage costs](https://learn.microsoft.com/en-us/azure/foundry/concepts/manage-costs) | [Provisioned throughput](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/provisioned-throughput) | [PTU billing](https://learn.microsoft.com/en-us/azure/foundry/openai/concepts/provisioned-throughput-billing) | [PTU reservations](https://learn.microsoft.com/en-us/azure/cost-management-billing/reservations/microsoft-foundry)

## [Govern, secure, and observe your models](https://learn.microsoft.com/en-us/azure/foundry/control-plane/overview)

Foundry governance (previously Foundry Control Plane) gives you one place to manage your AI fleet across four areas: agent identity, access policies for model deployments and tools, cost management, and safety. Its Fleet, Cost, Operations, Compliance, Quota, and Gateways views give you visibility, while enforcement comes from Azure Policy and the underlying services. It integrates with AI Gateway, Microsoft Agent 365, Microsoft Purview, and Microsoft Defender. To cap token use, you can apply the `llm-token-limit` policy in Azure API Management, which returns a 429 when a caller exceeds a tokens-per-minute rate and a 403 when a quota runs out.

Guardrails are named sets of controls that scan user input, model output, and (for agents, in preview) tool calls and tool responses for risks such as hate, violence, prompt attacks, and protected material, then annotate or block. Every model deployment gets a default guardrail, and you can create your own. Observability ties it together with built-in evaluators for quality, safety, and agent behavior, OpenTelemetry-based tracing, and Azure Monitor dashboards for token use, latency, and errors, from choosing a base model through production.

**Links to docs:** [Foundry governance overview](https://learn.microsoft.com/en-us/azure/foundry/control-plane/overview) | [Enforce token limits for models](https://learn.microsoft.com/en-us/azure/foundry/control-plane/how-to-enforce-limits-models) | [Guardrails overview](https://learn.microsoft.com/en-us/azure/foundry/guardrails/guardrails-overview) | [Observability in Foundry](https://learn.microsoft.com/en-us/azure/foundry/concepts/observability)

---

# Hands-on lab

## [AI Gateway labs](https://github.com/Azure-Samples/AI-Gateway)

This Azure-Samples repo has more than 30 labs for running models, MCP servers, and agents behind an AI gateway built on Azure API Management and Microsoft Foundry. Each lab is a Jupyter notebook with Bicep templates and API Management policies you can deploy and try. The model labs cover backend pool load balancing across endpoints, token rate limiting, semantic caching, model routing by model and version, and a FinOps framework with automated quota controls.

To run the labs, you need an Azure subscription with Contributor and Role Based Access Control Administrator roles, Python 3.12 or later, uv, VS Code with the Jupyter extension, and the Azure CLI. You can also open the repo in GitHub Codespaces.

**Link to repo:** [Azure-Samples/AI-Gateway](https://github.com/Azure-Samples/AI-Gateway)

---

# Get started

- [Microsoft Foundry portal](https://ai.azure.com): Browse the model catalog and deploy your first model.
- [Microsoft Foundry SDK](https://aka.ms/AIFoundrySDK): Build with Foundry from Python, C#, JavaScript, and Java.
- [Microsoft Foundry documentation](https://aka.ms/FoundryDocumentation): The full documentation for Foundry.
- [Create agentic AI solutions](https://aka.ms/CreateAgenticAISolutions): A Microsoft Learn plan for building agentic AI solutions with Foundry.
