<h1 align="center"> The Golden Path to Become an Agentic Enterprise </h1>
<h3 align="center"> A WSO2 Methodology </h3>
<p align="center">
<i>
Version: Summer-2026<br/>
<b>First Published On: Summer-2026<br/>  </b>
</i>
</p>
 
**Authors**
- Selvaratnam Uthaiyashankar | Chief Product Officer, [WSO2, Inc](https://wso2.com/) | [@xx](https://twitter.com/)
- Ruwan Linton | Chief Customer Officer, [WSO2, Inc](https://wso2.com/) | [@xx](https://twitter.com/)
- Rania Khalaf | Chief AI Officer, [WSO2, Inc](https://wso2.com/) | [@xx](https://twitter.com/)
- Mifan Careem | Chief Solutions Officer, [WSO2, Inc](https://wso2.com/) | [@xx](https://twitter.com/)
- Derric Giling | GM API Platform BU, [WSO2, Inc](https://wso2.com/) | [@xx](https://twitter.com/)
- Asanka Abeysinghe | Chief Technology Officer, [WSO2, Inc](https://wso2.com/) | [@asankama](https://twitter.com/asankama)

## Contents

- [Overview](#overview)
- [Roles used in this document](#roles-used-in-this-document)
- [How to use this](#how-to-use-this)
- [Step 1: Sanctioned access](#step-1-sanctioned-access)
- [Step 2: Safe general-purpose use](#step-2-safe-general-purpose-use)
- [Step 3: Grounded enterprise knowledge](#step-3-grounded-enterprise-knowledge)
- [Step 4: Central governance with distributed enforcement](#step-4-central-governance-with-distributed-enforcement)
- [Step 5: Governed coding agents](#step-5-governed-coding-agents)
- [Step 6: Expose your capabilities to external agents](#step-6-expose-your-capabilities-to-external-agents)
- [Step 7: Monetize your capabilities](#step-7-monetize-your-capabilities)
- [Step 8: Automate entire operational processes](#step-8-automate-entire-operational-processes)
- [Step 9: Agents as part of your workforce](#step-9-agents-as-part-of-your-workforce)
- [Step 10: Monetize your agents](#step-10-monetize-your-agents)
- [Closing thought](#closing-thought)
- [Mapping WSO2 to the golden path](#mapping-wso2-to-the-golden-path)
- [References](#references)

## Overview
 
Enterprises know they need to move on agentic AI. Most don't know where to start, or what comes after the first pilot. This document lays out ten sequential achievements that answer both questions, and maps a set of controls to each one.
 
Each achievement is binary, not scored. You either have safe, attributable AI access for your employees or you don't. You either have a governed catalog of MCP tools or you don't. There's no partial credit and no benchmarking against peers. Each achievement is also a precondition for the ones that follow it: the first four steps build the governance foundation everything else depends on. Skip that foundation and the later steps, especially external exposure and monetization, get far more expensive to retrofit than to build correctly the first time.
 
This document is vendor neutral. The ten achievements and their controls apply regardless of which vendors you use. A separate section at the end maps WSO2's platform against each step, for readers evaluating WSO2 specifically.

## Roles used in this document

Most enterprises haven't settled on where AI strategy and AI security ownership sit. Some fold it into the CIO, some run a dedicated Chief AI Officer, some split AI security out of the CISO entirely. Data protection ownership varies just as much, and the agent sponsor role in step 9 doesn't have a settled title anywhere yet. The roles below appear as functional labels instead of specific titles for that reason. Every other role referenced (Finance, Legal, HR, COO, CEO, Product Management) is stable enough across enterprises that it doesn't need translation.

- **AI Strategist**: CIO, Chief AI Officer, CTO, Head of AI, VP AI Strategy
- **Platform Lead**: CTO, VP Engineering, Head of Platform Engineering
- **AI Security & Compliance**: CISO, VP Security, Head of Information Security
- **Data Protection Officer**: DPO, Chief Privacy Officer, Privacy Counsel (many enterprises don't have this as a distinct role; it sits with Legal or gets folded into AI Security & Compliance instead)
- **Agent Sponsor**: Line manager (this one's genuinely new: it doesn't map to an existing title in most orgs yet. See step 9)

## How to use this

Enter wherever you already are. Most enterprises have already made some progress on steps 1 through 3. Few have touched steps 8 through 10. The path is roughly sequential: each step assumes the governance foundation built in the steps before it. Step 5 (coding agents) is the exception. It applies the same governance model built in steps 2 through 4 to a different population (developers instead of general employees) and can run in parallel.

Every step has the same five questions answered: what you need, why it matters, how you know it's working, who owns it, and what your AI Security & Compliance function will ask about it before signing off. That last part is not an afterthought. Every step on this path that fails does so because governance was bolted on after the fact instead of built into the achievement itself.

![gp timeline](/media/golden-path-diagram-selection.png)

Blue steps are efficiency plays: they save time and reduce risk. Green steps are growth plays: they turn the same governed foundation into revenue. Notice that growth never shows up before step 6. You cannot monetize or externalize what you have not first governed.

| Step | Description | What it gets you | Goal |
|---|---|---|---|
| 1 | Sanctioned access | One safe, attributable way for employees to use AI; everything else blocked | Efficiency |
| 2 | Safe general-purpose use | Guardrails and cost controls on general AI tools (ChatGPT, Claude, Gemini) | Efficiency |
| 3 | Grounded enterprise knowledge | AI answers grounded in your own data, with access control enforced at query time | Efficiency |
| 4 | Central governance | One policy, enforced everywhere, with a shared catalog instead of every team rebuilding | Efficiency |
| 5 | Governed coding agents | The same governance model applied to coding agents and AI-assisted development | Efficiency |
| 6 | Expose capabilities | Your capabilities published as governed MCP servers for external agents to consume | Growth |
| 7 | Monetize capabilities | Metering and billing on the capabilities you've exposed | Growth |
| 8 | Automate processes | Whole operational workflows running agent-first, not just agent-assisted | Efficiency |
| 9 | Delegate to agents | Agents acting under a user's delegated authority, not a standing service account | Efficiency |
| 10 | Monetize agents | Agents themselves packaged as products, with outcome-based pricing | Growth |

## Step 1: Sanctioned access

**Achievement**: Employees can use conversational AI without security, safety, or data leakage as an open question.

### What you need
- At least one approved conversational AI product, reached behind SSO, so every prompt is attributable to a person
- Everything else blocked at the proxy or egress layer
- A one page acceptable use position and a short AI literacy note

### Why it matters
This is the bare minimum, and it's the only thing that actually reduces shadow AI. 78% of AI users already bring their own tools to work, and 52% are reluctant to admit using AI for their most important tasks.(1) Blocking without providing an alternative just drives usage underground. It also isn't optional: the EU AI Act's Article 4 AI literacy obligation has applied since February 2, 2025, regardless of risk category.(2)

### You'll know it's working when
- Over 90% of employees have sanctioned access within a quarter
- Zero unsanctioned AI domains are still reachable from the corporate network
- A new employee gets access the same day, self-service

**Who owns it**: The AI Strategist. Every framework and auditor asks for this person first.

**Where it breaks**: Prompts and responses get retained at the model provider with no attribution to a person, so no investigation is possible if data walks out. Meanwhile employees are already using consumer AI you cannot see.

### Controls
- SSO and MFA, per-user attribution
- Egress allow-listing to the sanctioned endpoint only
- A CASB or secure web gateway for AI-app discovery, starting in monitor mode
- Acceptable use policy plus AI literacy training
- A live AI register: tool, owner, data touched, business process

## Step 2: Safe general-purpose use

**Achievement**: Employees can safely use general-purpose conversational AI (ChatGPT, Claude.ai, Gemini, and similar).

### What you need
- A model that does not train on your data, hosted locally or in your own cloud tenancy, with contractual no-training terms
- Guardrails configured before rollout, not after: PII masking, prompt-injection shields, denied topics, output limits
- A token budget per user and per department from day one
- A documented prompt and response retention period

### Why it matters
This step is about two things: data leakage and cost control. Conversational and agentic workloads consume metered capacity non-deterministically, so a small design flaw becomes a large bill and a malicious prompt becomes an economic attack. It's also the first piece of infrastructure-enforced governance: control applied outside the application, at a shared boundary, so coverage doesn't depend on every team implementing it correctly.

### You'll know it's working when
- Zero confirmed data-leakage incidents through AI tools
- Consumer AI egress is down more than 80% against the step 1 baseline
- Cost per active user is flat or falling
- Guardrail false-positive rate is under 2% (a noisy guardrail gets switched off)
- 100% of AI traffic passes through the gateway

**Who owns it**: AI Security & Compliance owns the guardrail policy set; Finance owns the budget envelope.

**Where it breaks**: The provider trains on your data. Jailbreaks produce unlawful, defamatory, or embarrassing output. Spend goes unbounded (denial-of-wallet). Data residency and cross-border transfer become a problem. Shadow endpoints bypass the gateway entirely.

### Controls
- Guardrail policy set: PII redaction, denied topics, prompt-injection shields, output length and format limits
- Token quotas and hard spend ceilings with automatic cutoff, not just alerts
- Prompt and response logging with an explicit retention schedule
- Data residency configuration and no-training contractual terms
- Network egress allow-list so the gateway cannot be bypassed; keys in a vault, never in app config

## Step 3: Grounded enterprise knowledge

**Achievement**: Employees can use conversational AI to access enterprise knowledge and take isolated, low-risk actions, not just general questions.

### What you need
- Skills, plugins, and knowledge bases made available through retrieval, RAG, and indexed search
- Curated sources, starting with non-PII content
- A context engine for storage, mastering, and retrieval
- Source-level access control enforced at query time, not only at ingest: retrieval must respect the asker's existing entitlements
- Citations on every answer, sensitive-data scanning before ingest, and recorded data lineage
- Start read-only. Earn the right to write.

### Why it matters
Grounding is the single most effective control against confabulation, a risk named explicitly in NIST AI 600-1 and OWASP's LLM Top 10.(3) It's also the first place a real data boundary has to exist: an over-permissioned index is a data breach with a chat interface. And it's the first step that produces a defensible business number instead of enthusiasm.

### You'll know it's working when
- Every governed knowledge source and tool has a named owner
- Over 95% of answers cite a retrievable source (groundedness)
- A meaningful share of "where do I find" queries get resolved without a human (deflection rate)
- Time saved per task, and tasks completed per employee per week, both move
- Zero incidents of a user seeing content they weren't entitled to

**Who owns it**: Team-level leadership and AI Security & Compliance. Each knowledge source and tool needs a named business owner, not just a technical one.

**Where it breaks**: Over-permissioned retrieval returns documents the asker should never see. Embeddings become an uncontrolled second copy of sensitive data. Poisoned or stale documents steer answers, or carry an injection payload. Tools get granted more scope than the task requires. Actions get taken on the strength of a wrong answer.

### Controls
- Document-level ACLs enforced at query time (security trimming)
- Index segregation by sensitivity tier; PII and secret scanning before ingest; encrypted embedding store
- MCP over OAuth 2.1 with PKCE S256; audience-bound tokens (RFC 8707); protected resource metadata (RFC 9728)(4)
- Indirect prompt-injection defense: retrieved content is data, never instruction
- Groundedness and citation enforcement on output; source integrity and provenance checks

## Step 4: Central governance with distributed enforcement

**Achievement**: The enterprise has central governance and control over AI use while driving standardized reuse, instead of every team building its own stack.

### What you need
- One control plane for AI: policy authored, versioned, and reviewed once (permitted models, data handling, guardrails, oversight thresholds, evidence requirements, cost limits), then distributed to enforcement points near the action
- A live register of AI apps, models, tools, and agents, each with a named owner
- A shared catalog so teams reuse rather than rebuild
- An exception register with mandatory owner and expiry
- Evidence from the data plane fed back into policy

### Why it matters
Central policy without distributed enforcement becomes a bottleneck teams route around, and shadow AI regrows. Distributed enforcement without central policy becomes fragmentation and risk accumulating in the seams. Standardized reuse is where the cost curve bends: every governed tool gets reused by the next use case, so the marginal cost of the next AI project falls. This matters because the alternative is common: 63% of organizations have no AI governance policies at all, and 97% of organizations that had an AI-related breach lacked proper AI access controls.(5)

### You'll know it's working when
- 100% of AI traffic passes a governed control point
- Reuse rate climbs: new use cases consume cataloged tools instead of building new ones
- Time from request to approved AI use case drops from weeks to days
- Control coverage: the current policy version is enforced across all domains
- Policy drift incidents per quarter hit zero, and no exceptions sit open past expiry

**Who owns it**: An AI center of excellence or steering committee, chaired by the AI Strategist or Platform Lead, with AI Security & Compliance, Legal, Data Protection, Finance, and business domain owners at the table. Domain teams keep implementation autonomy inside enterprise policy.

**Where it breaks**: You get one of two opposite failures: a central gate so slow that teams bypass it, or local freedom so wide that controls are inconsistent and unauditable. Policy drift opens up between what's written and what's actually enforced. An exception gets granted once and never revisited. There's no way to prove enterprise-wide coverage to a regulator or auditor.

### Controls
- Policy-as-code with version control, peer review, and CI validation
- Automated drift detection between authored and enforced policy
- Enforcement coverage reporting by domain and by control
- AI register and exception register, both with mandatory owner and expiry
- Control crosswalk: NIST AI RMF (Govern/Map/Measure/Manage) mapped to ISO/IEC 42001 Annex A and to the OWASP LLM and Agentic Top 10
- Separation of policy authorship from policy enforcement duties

## Step 5: Governed coding agents

**Achievement**: The same governance extends to coding agents and AI-assisted development, which is where it's most likely to be missing.

### What you need
- Sanctioned tools on private model endpoints. No proprietary source goes into consumer AI.
- Scope what a coding agent may read (which repos, which paths) and what it may do: branch and raise a PR, never push to a protected branch
- Governed tools and short-lived credentials instead of standing secrets
- AI-generated code and its dependencies scanned before merge; human review and signed commits on every merge

### Why it matters
Coding agents are the highest-adoption and highest-leverage agent class, and the one most likely to arrive ungoverned, because developers adopt them individually. They're also the highest blast radius: they read source, secrets, and infrastructure, and their output ships to production. Same governance model as conversational AI, very different consequences. Getting this right early is what makes every later step in this path cheaper to build.

### You'll know it's working when
- A high share of developers are on sanctioned coding agents
- Your DORA metrics move against baseline: PR cycle time, deployment frequency, change failure rate, MTTR
- AI-authored PRs merge with zero security or license findings
- Secrets or incompatible licenses reaching main hits zero
- Cost per merged PR, including model spend, is known and trending the right way

**Who owns it**: The Platform Lead owns adoption and productivity; AI Security & Compliance owns the control set; platform engineering owns the golden paths. Legal owns open-source license exposure.

**Where it breaks**: Proprietary source code or secrets get sent to an external model. AI-generated vulnerabilities and license contamination reach production. Agents hold write access to protected branches or CI/CD credentials. A supply-chain compromise arrives through the agent's own dependencies or a third-party MCP server. Reviewers rubber-stamp large AI-authored diffs.

### Controls
- Private or self-hosted model endpoints for code; block consumer coding tools on proprietary repositories
- Repo and path scoping per agent; branch protection; no direct push; short-lived credentials from a vault
- Secret scanning, SAST, DAST, and SCA on every AI-authored PR; SBOM generation
- Open-source license compatibility checks
- Mandatory human review, signed commits, and a diff-size threshold that forces smaller PRs
- Third-party MCP server and extension review before it touches a repo

## Step 6: Expose your capabilities to external agents

**Achievement**: External agents, including conversational AI apps you don't control, can consume your capabilities.

### What you need
- Your capabilities published as MCP servers, with agent identity and MCP auth so you can offer them securely
- Public, non-PII content first, then integrations that expose systems of record, knowledge bases, and RAG
- Publication in an agent-facing catalog with machine-readable tool descriptions, scopes, rate plans, and a named owner per tool
- Every third-party MCP server reviewed before anything is allowed to call it

### Why it matters
This is where your capabilities become reachable by the whole agent ecosystem, not just your own applications. The MCP registry and API catalog become the enterprise system of record for what any agent can discover, invoke, and expose. It's also where risk moves from language to action, so the boundary has to exist before the consumers do. This is the highest-leverage step on the whole path: build it once, and every later agent, internal or external, reuses it.

### You'll know it's working when
- External agents, partners, and AI apps are actually consuming your MCP tools
- MCP tool call volume, success rate, and p95 latency are healthy
- A new external consumer can make its first successful call in under a day, fully self-service
- Partner integrations ship with no bespoke code
- 100% of tools have a named owner and a published scope

**Who owns it**: The Platform Lead owns the platform; Product Management owns the external proposition and partner roadmap. AI Security & Compliance signs off the exposure model; Legal owns partner terms.

**Where it breaks**: Third-party agents operate with enterprise credentials. Tokens carry far more scope than the tool needs. You get a confused deputy: the tool acts with its own privilege rather than the caller's. Tool sprawl accumulates with no owner and no lifecycle. A tool definition or MCP server gets compromised in the supply chain.

### Controls
- MCP as an OAuth 2.1 resource server with PKCE S256
- RFC 9728 protected resource metadata so clients discover the right authorization server; RFC 8707 resource indicators so tokens are audience-bound to one server and can't be redirected(4)
- Per-consumer scopes, quotas, and ACLs; tool allow-lists
- Schema validation on tool inputs and outputs; parameter constraints, not just tool-name permissions
- Third-party MCP server review checklist; egress controls on outbound tool calls
- Note: the MCP authorization spec is moving fast. Track it, it has been changing with breaking implications for how RFC 9728 and RFC 8707 get applied.

## Step 7: Monetize your capabilities

**Achievement**: New revenue streams from monetizing the capabilities you've exposed as MCP servers and APIs.

### What you need
- Metered rate plans: per call, per token, per outcome, or subscription tiers, with entitlement enforced at the gateway rather than in application code
- Usage metering you can actually invoice from, reconciled to billing
- Self-service onboarding: sign-up, credentials, sandbox, documentation
- Commercial terms: acceptable use, SLA, liability, IP, and data handling

### Why it matters
This turns the governed capability layer from a cost center into a revenue line. Once tools are cataloged, metered, and authorized per consumer, monetization becomes a pricing decision rather than an engineering project, which is why it sits immediately after the catalog step rather than years later. It also changes the internal conversation: the API and AI platform stops being overhead you have to defend at budget time.

### You'll know it's working when
- There's real revenue from monetized tools and APIs
- Paying consumers, net revenue retention, and free-to-paid conversion are all moving
- ARPU per tool and gross margin per call (after model, tool, and infrastructure cost) are known
- Metering-to-invoice reconciliation variance is under 1%
- Partner-sourced pipeline is attributable to the catalog

**Who owns it**: The Platform Lead and Product Management own product and pricing; Finance owns revenue recognition and margin; Legal owns terms and liability. Don't commit pricing or contractual terms without Finance and Legal sign-off.

**Where it breaks**: Metering that can't be reconciled to invoices, or that a customer can dispute. Entitlement bypass, where a consumer exceeds a paid plan or reaches an unpaid tool. PII or regulated data crosses a commercial boundary. Contractual exposure opens up on availability, accuracy, IP indemnity, and liability. A monetized endpoint becomes an attractive attack or scraping target.

### Controls
- Entitlement and quota enforcement at the gateway, not in application code
- Tamper-evident usage metering with an immutable record, reconciled to billing
- Per-consumer data-boundary policies, redaction, and purpose limitation
- WAF, bot, and abuse protection; per-consumer rate limits and anomaly detection
- Contractual review of SLA, acceptable use, liability, IP, and data processing terms
- For customer-facing offerings: EU AI Act Article 50 transparency, in force since August 2, 2026, plus applicable consumer-protection, advertising, and anti-spam law

## Step 8: Automate entire operational processes

**Achievement**: Whole operational processes and product delivery workflows run agent-first, not merely agent-assisted.

### What you need
- Agents built and run on a managed runtime with session isolation
- Every agent has a unique identifier, a named owner, a registry entry, and a budget. Never a shared service account.
- Scoped tool bindings drawn from the catalog built in step 6
- Evals in CI and continuous evaluation in production; agents monitored and managed; traces on by default
- Parameter-level authorization before any write: which record, which field, which amount, which recipient
- Human approval tiers for high-risk, irreversible, or regulated actions

### Why it matters
This is where value moves from assistance to throughput, the first step where the business case is capacity, not convenience. It also raises the governance bar sharply: the path matters, not just the output. What authority was used, what tool was called, with what parameters, and was the action reversible. Gartner expects over 40% of agentic AI projects to be canceled by the end of 2027, naming inadequate risk controls as one of three causes.(6) The controls in this section aren't the tax on reaching production. They're the route to it.

### You'll know it's working when
- A real number of end-to-end processes are running agent-first, not just agent-assisted
- Straight-through processing rate climbs: the share of cases completed with no human touch
- Cost per transaction and cycle time beat baseline
- Eval pass rate at release is high, and production incidents per 1,000 agent actions is low
- Rework and reversal rate on agent actions stays low (this is the number that decides whether you can widen scope)
- Cost per outcome per agent is known, with a named budget owner

**Who owns it**: The COO or process owner owns the outcome and the target metric; the Platform Lead owns the platform; AI Security & Compliance owns the control set. Every agent needs a named business owner and a budget owner, reviewed whenever people change roles.

**Where it breaks**: Anonymous agents run on shared service accounts, unattributable and unrevocable. Excessive agency lets an agent do far more than the task requires. You get a permitted-but-wrong action: technically authorized, wrong for the business context. Irreversible operations happen with no compensating path. Runaway loops, excessive fan-out, and unbounded consumption occur. Indirect prompt injection arrives through a document or a tool response.

### Controls
- One identity per agent; least-privilege, scoped tool bindings; no standing privilege
- Parameter-level authorization via ABAC or ReBAC (Cedar, OPA, or equivalent): allow-listed amounts, recipients, record scopes, and query shapes
- Sandboxed code execution; per-agent network egress control; secrets in a vault
- Runtime safety: prompt-injection and jailbreak defense, output filtering, memory write validation, fan-out and retry caps
- OTEL tracing of intent, authority, tool calls, parameters, policy decisions, and approvals, replayable in audit
- Per-agent budgets and a tested kill switch; dry-run mode before enabling writes
- Red-teaming and regression evals gating every model, prompt, tool, or policy change

## Step 9: Agents as part of your workforce

**Achievement**: Agents work alongside and on behalf of your employees, acting under delegated user authority rather than a standing service identity.

### What you need
- Agents get a token from users to act, including on PII data, on the user's behalf
- The token is audience-bound, time-limited, and scoped to the task
- The delegation chain is preserved and propagated: who initiated, what authority was granted, and whether the agent stayed inside it
- Support for background and asynchronous consent, so agents can act when the user isn't present
- Every agent identity has a human sponsor; access is revocable on demand and reviewed periodically

### Why it matters
This step is about attribution. Without an explicit delegation chain, authorization becomes approximate, audit becomes incomplete, cost attribution becomes unclear, incident response slows down, and human accountability blurs. Delegation is not impersonation: both the human and the agent have to remain visible in the record. This is the step that turns "we have chatbots" into "agents can safely touch customer data." Worth stating plainly: first-class agent identity and multi-step delegation are still developing at the standards level. Design to capabilities, not to named drafts.

### You'll know it's working when
- A real number of agents operate under user delegation in production
- 100% of agent actions have a complete, replayable authority chain
- Mean time to revoke delegated authority is measured in minutes
- Approval queue median time-to-decision is fast, and the override rate isn't a rubber-stamp warning sign
- Agent-assisted tasks per employee per week climb, and employee trust in the periodic survey holds up
- Orphaned agent credentials after a joiner-mover-leaver event hit zero

**Who owns it**: AI Security & Compliance and the AI Strategist jointly own the delegation model; line managers act as agent sponsors and are accountable for their agents' access. HR and Legal weigh in on workforce and employment implications. The Data Protection Officer owns the lawful basis for PII processing by an agent.

**Where it breaks**: Impersonation gets dressed up as delegation, and the human disappears from the audit trail. Consent fatigue leads users to grant broad, long-lived scopes. Standing privilege outlives the task. Agent credentials go orphaned after someone leaves. Approvals become rubber-stamps, and the approver gets socially engineered by the agent's own framing. A delegated token gets replayed against a different resource.

### Controls
- RFC 8693 OAuth 2.0 token exchange with the act (actor) claim, which expresses delegation rather than impersonation, and nests to carry a multi-hop chain(4)
- Short-lived, audience-bound tokens (RFC 8707); scope minimization; just-in-time access
- On-demand revocation and periodic access reviews for agent identities
- A human sponsor per agent, enforced by a lifecycle workflow that reassigns on departure
- Separation of duties between requester, agent, and approver; tiered approval thresholds; out-of-band confirmation for high-value actions
- Approval evidence retained with the action trace
- Watch, don't depend on: OAuth identity chaining and the Identity Assertion Authorization Grant are still IETF drafts

### Step 10: Monetize your agents

**Achievement**: New revenue streams from packaging agents themselves as products, not just the capabilities behind them.

### What you need
- Outcome- or task-based pricing, a multi-tenant runtime with hard tenant isolation, per-tenant budgets, quotas, and SLAs
- External-facing agent identity and delegation, so your customer's own users can authorize your agent to act for them
- Per-tenant evidence: every action replayable for the customer's own auditors
- An AI management system aligned to ISO/IEC 42001, plus AI system impact assessments, because a regulated buyer's own security and compliance function will ask before signing

### Why it matters
This is the end state: agents as a revenue-generating product line, not just an internal efficiency program. It only works if the earlier steps on this path are genuinely done. A buyer's own security and compliance function will ask for the delegation chain, the evidence trail, the impact assessment, and the incident process before signing, and increasingly for a certificate. The market gap is the opportunity: only 21% of companies planning agentic AI report a mature agent governance model, while close to three-quarters plan to deploy within two years.(7) Being in that 21% is a commercial advantage, not just a compliance posture.

### You'll know it's working when
- There's real revenue from agent-as-a-product and outcome-based pricing
- Gross margin per agent task, after model, tool, and infrastructure cost, is known
- Tenant count, net revenue retention, and expansion rate are all moving
- SLA attainment and cost-per-outcome trend are healthy (these two numbers decide whether outcome pricing is safe)
- Enterprise security-review cycle time shortens as your evidence matures
- Cross-tenant data incidents stay at zero

**Who owns it**: CEO or Chief Product Officer owns the P&L; the Platform Lead owns the platform; AI Security & Compliance and Legal own assurance, contracts, and regulatory exposure. There's a named accountable executive for the AI management system, as ISO/IEC 42001 and the EU AI Act both expect.

**Where it breaks**: Cross-tenant data leakage is the incident that ends the product line. Liability accrues for an autonomous action taken on a customer's behalf. Unverifiable claims about accuracy, safety, or compliance get made in sales. Regulatory exposure spans jurisdictions; data residency and sovereignty become live questions. A denial-of-wallet attack hits a metered agent. Personal accountability falls on the named executive.

### Controls
- Hard tenant isolation: separate cells or namespaces, per-tenant keys, policies, and evidence stores
- Per-tenant budgets, rate limits, circuit breakers, and kill switches
- AI system impact assessments per ISO/IEC 42005, and an AI management system per ISO/IEC 42001 (clauses 4 through 10 plus 38 Annex A controls; certification valid three years with surveillance)(8)
- EU AI Act: Article 50 transparency for customer-facing agents, in force since August 2, 2026; Article 25 documentation and testing-access rights over upstream model providers; Annex III high-risk obligations from December 2, 2027 if in scope
- Independent penetration testing and red-teaming; AI-specific incident response with customer notification paths
- Contractual limits on liability, autonomy scope, and human oversight, reviewed by Legal, never asserted in a deck

## Closing thought

Ten achievements, not five stages. No score, no benchmark against peers, no partial credit for being "mostly there" on a dimension. Just a sequence of things that have to be genuinely true, in roughly this order, before the next one is safe to build. Skip the governance work in steps 1 through 4 and steps 6 through 10 will eventually cost you far more than the time you saved.

----------------------------------------

## Mapping WSO2 to the golden path

The path above is vendor neutral. This section is not. It maps WSO2's platform against each step for readers evaluating WSO2 specifically. If you're using a different stack, the achievements and controls above still apply; substitute your own tooling.

| Step | WSO2 capability |
|---|---|
| 1. Sanctioned access | **WSO2 AI Gateway**, single egress control point with SSO and per-user attribution and usage visibility. Models can be hosted in your own tenancy over a private endpoint. |
| 2. Safe general-purpose use | **WSO2 AI Gateway** for guardrails, PII masking and redaction, token-based rate limiting, semantic caching, and multi-provider routing and failover. **WSO2 AI Workspace** for providers, guardrails, and AI Insights in one place. |
| 3. Grounded enterprise knowledge | **WSO2 Integrator**, AI-native integration for RAG and GenAI apps with 600+ connectors to data, APIs, and MCP servers. **WSO2 AI Gateway** for guardrails and grounding checks on the response path. **WSO2 AI Workspace**. |
| 4. Central governance | **WSO2 AI Gateway**. **WSO2 AI Workspace**. **WSO2 API Portal & MCP Hub**, to expose skills and tools as governed MCP with scopes and owners. |
| 5. Governed coding agents | **WSO2 Agent Manager** (currently waitlist), enterprise control plane for AI agents. **WSO2 Agent Builder**. **WSO2 AI Gateway**. **WSO2 API Portal & MCP Hub**. **WSO2 Developer Platform / OpenChoreo** for golden paths, CI gates, and environment promotion enforced by the platform rather than by convention. |
| 6. Expose capabilities | **WSO2 Agent Manager** (waitlist). **WSO2 Agent Builder**. **WSO2 AI Gateway**. **WSO2 API Portal & MCP Hub**. **WSO2 Developer Platform / OpenChoreo**. |
| 7. Monetize capabilities | **WSO2 AI Gateway**. **WSO2 API Portal & MCP Hub**. **WSO2 Monetization**, powered by Moesif. **WSO2 Developer Platform / OpenChoreo**. |
| 8. Automate processes | **WSO2 Integrator** for building agents with low-code and pro-code parity and 600+ connectors. **WSO2 Agent ID** to register, authenticate, authorize, and audit agents. **WSO2 Agent Manager** (waitlist) to run, govern, observe, and evaluate agents across frameworks and runtimes. **WSO2 AI Gateway + API Manager** for parameter-level policy, guardrails, and approval routing at the boundary. **OpenChoreo Cells** on AKS or EKS for isolation, declared gateway topology, and scale-to-zero for idle agents. |
| 9. Delegate to agents | **WSO2 Agent ID** for agent identity, delegation, and fine-grained authorization. **WSO2 Identity Server 7.3** for token exchange, background-agent delegation via CIBA, MCP policy enforcement, and on-demand credential revocation. It federates to whichever identity authority you already run (for example Microsoft Entra Agent ID or AWS Bedrock AgentCore Identity) rather than replacing it. **WSO2 API Manager** enforces the delegated scope at the boundary where the action happens. |
| 10. Monetize agents | **WSO2 Agent Manager + WSO2 Agent ID** (waitlist) for multi-tenant agent governance, identity, and evidence. **WSO2 API Manager** monetization for rate plans, metering, and billing on agent products. **WSO2 AI Gateway** for per-tenant budgets, quotas, and cost attribution. **OpenChoreo** for per-tenant Cells and environments on AKS or EKS, with sovereign and multi-region topologies. **WSO2 Identity Server** for external customer identity and delegation. |

## References
1. 2024 Work Trend Index Annual Report, Microsoft and LinkedIn (https://www.microsoft.com/en-us/worklab/work-trend-index/ai-at-work-is-here-now-comes-the-hard-part)
2. EU AI Act, Article 4, AI literacy (https://digital-strategy.ec.europa.eu/en/policies/ai-talent-skills-and-literacy), in force since February 2, 2025
3. NIST AI 600-1, Artificial Intelligence Risk Management Framework: Generative AI Profile; OWASP Top 10 for Large Language Model Applications, owasp.org (https://owasp.org/www-project-top-10-for-large-language-model-applications/)
4. RFC 8693 (OAuth 2.0 Token Exchange), RFC 8707 (Resource Indicators for OAuth 2.0), RFC 9728 (OAuth 2.0 Protected Resource Metadata), rfc-editor.org (https://www.rfc-editor.org/)
5. IBM Cost of a Data Breach Report 2025 (https://newsroom.ibm.com/2025-07-30-ibm-report-13-of-organizations-reported-breaches-of-ai-models-or-applications,-97-of-which-reported-lacking-proper-ai-access-controls)
6. Gartner: Over 40% of agentic AI projects will be canceled by end of 2027 (https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027)
7. Deloitte, State of AI in the Enterprise 2026 (https://www.deloitte.com/us/en/insights/topics/emerging-technologies/ai-agents-scaling-faster.html), survey of 3,235 IT and business leaders
8. ISO/IEC 42001:2023, AI management system; ISO/IEC 42005:2025, AI system impact assessment (https://www.iso.org/standard/42005)
