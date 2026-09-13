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
- Asanka Abeysinghe | CTO, [WSO2, Inc](https://wso2.com/) | [@asankama](https://twitter.com/asankama)

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
