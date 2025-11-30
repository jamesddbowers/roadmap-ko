# Project Brief: RoadmapKO

**Status:** Work in Progress - Consolidation Phase
**Last Updated:** 2025-11-30

---

## Executive Summary

**Product Concept:**

RoadmapKO is an AI-native, opinionated SaaS platform designed to **master the "front-half" of the software development lifecycle**, guiding teams from a raw idea to a perfectly aligned, developer-ready backlog. Using specialized AI agents, RoadmapKO orchestrates the complete planning process—from ideation through production-ready specifications—while naturally teaching best practices through opinionated workflows.

**The Problem:**

A chronic and costly disconnect exists between high-level business strategy and the day-to-day work of software development teams. Software teams struggle to maintain comprehensive, consistent documentation across the SDLC, where:

- **Disconnected Artifacts:** Analysis artifacts (briefs, research) don't properly cascade into planning documents (PRDs, architecture), creating gaps that lead to miscommunication, scope creep, and failed projects
- **Inefficient Translation:** Business needs are poorly translated into actionable engineering tasks, leading to features that miss the mark
- **Unhealthy Backlogs:** Critical issues and tech debt are deferred indefinitely, causing ongoing quality problems
- **Inconsistent Competency:** Quality of product planning varies wildly depending on individual PM skill, leading to unpredictable outcomes
- **Lost Context:** Teams forget *why* architectural decisions were made, hampering future development

**Impact:** Wasted R&D spending, delayed time-to-market, low team morale, and failure to deliver on business objectives. Studies show 70% of software projects fail due to poor requirements (Standish Group).

**Why Existing Solutions Fall Short:**

Current tools are either too rigid (Jira, Linear—excellent for execution but assume planning is already done) or too freeform (Notion, Confluence—flexible but provide no guidance or structure). Traditional PM tools enforce rigid templates without intelligence to adapt, while AI coding assistants lack understanding of strategic context.

**Target Market:**

RoadmapKO serves a diverse range of users who all share the need for better planning:

**Primary Segments (Equal Weight):**
- **Solo Developers & Indie Hackers:** Individual developers building SaaS products (5-15 years experience) who need professional-grade project planning but lack dedicated PMs/architects
- **Modern Software Teams & Leaders:** PMs, EMs, and leads at high-velocity startups frustrated by legacy tools, who value speed and efficiency

**Secondary Segments:**
- **Digital Agencies:** 2-10 person teams managing multiple client projects requiring standardized documentation ($500K-2M annual revenue)
- **Business Stakeholders:** C-suite and VPs who need predictability and clear view of ROI from tech investments

**Tertiary & Expansion:**
- **Visual/No-Code Developers:** Using platforms like Lovable, v0, Base 44, Bolt.new
- **Developers & Engineers:** Individual contributors directly impacted by poor planning
- **ChatGPT/Claude Desktop Users:** Seeking structured workflows to replace ad-hoc prompting
- **BMAD Method Enthusiasts:** Who love the methodology but don't want DIY setup

**The Solution:**

RoadmapKO provides a **single AI agent that orchestrates specialized sub-agents** (Analysis + Planning phases) to create and maintain all upstream project documentation. The platform combines:

1. **AI Multi-Agent Orchestration:** 6-8 specialized AI agents (Analyst, PM, UX, Architect, QA, Security) working behind the scenes through one conversational interface
2. **Opinionated Workflow:** Enforces the proven Initiative → Epic → Feature → Story → Task hierarchy to prevent scope chaos
3. **Intelligent Backfilling:** If you start discussing features, the agent recognizes missing upstream artifacts and backfills them
4. **Three-Column Workspace:** Unified view with hierarchy navigation, live document preview, and agent chat
5. **Human-in-the-Loop:** AI drafts, humans review and approve—never fully autonomous

**Key Value Proposition:**

**"Never start from a blank page again"** — RoadmapKO is the **essential 'Phase Zero' for high-performance software teams**, providing:

- Project briefs, PRDs, and architecture docs in **hours, not weeks**
- **10x faster** client onboarding for agencies (generate standardized briefs at $149/mo instead of 40 billable hours)
- Complete planning in **7 days or less** (vs. 30+ days manual)
- Embedded BVSSH methodology that solves dependency and alignment issues **before** they become costly engineering problems

**Strategic Positioning:**

RoadmapKO positions as a powerful, complementary partner to execution-focused tools like Linear and Jira—we generate the planning artifacts they require. With system-of-record architecture integrating with Linear, Jira, Notion, and Azure Boards, RoadmapKO preserves full context even if users switch platforms, providing platform migration safety and multi-platform support.

**Why Now:**

- AI agent orchestration became practical in 2024
- Remote work amplifies the need for better async documentation
- Distribution channels (ChatGPT Apps SDK, Claude Desktop MCP) reach 800M+ users without building marketplace presence from scratch

---

## Problem Statement

**The Front-Half Planning Gap:**

In today's high-velocity technology landscape, a chronic and costly disconnect exists between high-level business strategy and the day-to-day work of software development teams. Most software projects fail not during implementation, but during planning—or more accurately, due to lack of proper planning. Teams jump straight into execution tools (Jira stories, Linear issues) without establishing clear strategic context or mastering the "front-half" of the SDLC.

**Critical Pain Points:**

1. **Disconnected Artifacts:** Market research exists in Notion, PRD in Google Docs, architecture in Confluence, stories in Linear—no single source of truth
2. **Inefficient Translation:** Business needs are poorly translated into actionable engineering tasks, leading to features that miss the mark
3. **Lost Context:** 6 months into development, no one remembers *why* architectural decisions were made
4. **Scope Creep:** Without clear Initiative/Epic boundaries, features get added reactively without strategic evaluation
5. **Unhealthy Backlogs:** Critical issues and tech debt are deferred indefinitely, causing ongoing quality problems and poor user experience
6. **Inconsistent Competency:** Quality of product planning varies wildly depending on the skill of the individual product manager, leading to unpredictable outcomes
7. **Onboarding Nightmare:** New team members face fragmented documentation across 5+ tools
8. **Rework Cycles:** Implementation discovers gaps in requirements, forcing costly backtracking

**Quantified Impact:**

- **70% of software projects fail** due to poor requirements (Standish Group)
- Average team **spends 8-12 hours/week** searching for context across documentation silos
- Agencies report **30-40% of billable hours lost** to rework from unclear requirements
- **Wasted R&D spending**, delayed time-to-market, low team morale, failure to deliver on business objectives

**Why Existing Solutions Fall Short:**

| Tool Type | Strength | Gap |
|-----------|----------|-----|
| **Jira/Linear** | Excellent for execution tracking | Assumes planning is already done; provides no upstream guidance for the "front-half" |
| **Notion/Confluence** | Flexible documentation | Too freeform—no structure, relationships between docs, or embedded methodology |
| **Traditional PM tools** | Enforce process | Rigid templates; no intelligence to adapt or guide; too complex (Jira) |
| **AI coding assistants** | Great at code generation | No understanding of strategic context, document relationships, or outcome-driven development |

**Why Now?**

1. **AI agent orchestration is newly viable:** Multi-agent systems with tool use only became practical in 2024
2. **Remote work amplifies the problem:** Distributed teams need better async documentation practices
3. **Distribution channels exist:** ChatGPT Apps SDK + MCP provide access to 800M+ users without building marketplace presence from scratch
4. **Market maturity:** Teams are frustrated with legacy tools and ready for opinionated, AI-native solutions

---

## Proposed Solution

**Core Concept: Your AI Planning Team**

RoadmapKO is an AI-native SaaS platform that provides a **single primary agent orchestrating 6-8 specialized sub-agents** behind the scenes to generate all planning documentation—from raw business idea to fully aligned, developer-ready backlog. It's a **complete, embedded methodology based on BVSSH principles** that masters the "front-half" of the software development lifecycle.

**"Never start from a blank page again"**—users review, refine, and approve agent-drafted documents rather than creating from scratch.

**The Three-Column Workspace:**

- **Left Column:** Hierarchy navigation (Initiative → Epic → Feature → Story → Task tree)
- **Middle Column:** Live document preview (TipTap markdown rendering)
- **Right Column:** Agent chat interface

**Multi-Agent Orchestration (Two-Phase Workflow):**

```
USER ──> RoadmapKO Primary Agent
              │
              ├─ PHASE 1: ANALYSIS
              │  ├── Analyst (brainstorming, discovery)
              │  ├── Market Research
              │  └── Competitive Analysis
              │
              └─ PHASE 2: PLANNING
                 ├── PM (PRD, requirements)
                 ├── Architect (tech stack, data models)
                 ├── UX (flows, wireframes)
                 ├── Security (threat modeling)
                 └── QA (test strategy)
```

**Key Differentiators:**

1. **Embedded Outcome-Driven Methodology:** Complete BVSSH-based system that amplifies team competency and teaches SDLC best practices through conversation
2. **Orchestrated Sub-Agents:** One conversational interface, 6-8 specialized experts working behind the scenes
3. **Intelligent Backfilling:** Jump to features? Agent recognizes missing Initiative/Brief and backfills it automatically
4. **Opinionated Workflow:** Initiative → Epic → Feature → Story → Task hierarchy prevents scope chaos and solves alignment issues *before* they become costly engineering problems
5. **Human-in-the-Loop:** Agent drafts, human reviews and approves—never fully autonomous
6. **Unified Workspace:** Hierarchy navigation, live document preview, agent chat—all in one view
7. **Integration-First with System-of-Record Architecture:**
   - Pull existing artifacts from Linear, Jira, Notion, Azure Boards
   - Create new in both systems simultaneously
   - RoadmapKO is always system of record
   - Platform migration safety

**Technical Architecture:**

- **Hybrid System:** Vercel AI SDK (lightweight interactions) + CrewAI/FastAPI (complex multi-agent orchestration)
- **Multi-Provider Access:** OpenRouter for unified LLM access across Anthropic, Google, OpenAI
- **Serverless-First:** Optimized for cost and scale
- **Modern Stack:** Next.js 14, shadcn/ui, Supabase (PostgreSQL + pgvector), Clerk auth, Stripe payments

**Phase Transitions & Status Indicators:**

- UI shows phase context explicitly (Analysis Phase 75% → Planning Phase)
- Status updates show which sub-agent is working
- Human-like interactions for longer processes ("I'm working with the Security architect to analyze...")

**Why This Will Succeed:**

- **Distribution Leverage:** ChatGPT Apps SDK (800M+ users), Claude Desktop MCP extension
- **Complementary Positioning:** Not competing with execution tools—we generate the planning artifacts they require
- **Value-Based Pricing:** $49-149/mo is accessible and offers 10x+ ROI on time savings (7 days vs 30+ days)
- **Natural Learning:** Users absorb SDLC best practices through guided conversation
- **Managed Service:** Unlike open-source BMAD/SuperClaude, we provide hosted orchestration with zero setup

**High-Level Vision:**

Establish RoadmapKO as the essential **"Phase Zero" for all high-performance software teams**, with long-term goal of evolving into a fully autonomous, end-to-end platform that eventually competes with Linear on execution.

---

## Target Users

### Primary Segment 1: Solo Developers & Indie Hackers

**Profile:**
- Individual developers building SaaS products
- 5-15 years experience, strong technical skills but limited PM/architecture training
- Often using AI coding assistants (Cursor, v0, Lovable, Bolt.new)

**Current Behaviors:**
- Jump straight into code without written requirements
- Keep context in head or scattered Notion docs
- Waste hours searching for "what was I building again?"

**Pain Points:**
- *"I should write a PRD, but it takes 8 hours I don't have"*
- Lose context on architectural decisions 6 months later
- Look unprofessional to investors/clients without proper documentation
- Backend architecture becomes an afterthought with visual dev tools

**Goals:**
- Ship faster with clear requirements
- Build planning habits without massive time investment
- Get view-by-view UX specs and component-level prompts optimized for AI coding tools

**Value Proposition:**
*"Never start from a blank page again—get project briefs, PRDs, and architecture docs in hours, not weeks"*

---

### Primary Segment 2: Modern Software Teams & Their Leaders

**Profile:**
- Small dev teams (2-10 people) at high-velocity startups or digital agencies
- PMs, EMs, and tech leads managing 3-10 concurrent projects
- $500K-2M annual revenue range (agencies)
- Frustrated by legacy tools, value speed and efficiency

**Current Behaviors:**
- Copy-paste previous project docs, struggle with consistency
- Senior devs bottlenecked creating planning docs
- Spend 2 weeks in meetings before every project kickoff

**Pain Points:**
- *"Every project starts with 2 weeks of meetings"*
- Lost revenue when senior people draft docs instead of billing clients
- Developers directly impacted by poor planning seek clarity and stability
- Onboarding nightmare for new team members (fragmented docs across 5+ tools)

**Goals:**
- Standardize planning across projects
- Free up seniors to review vs. draft
- Enable juniors to contribute to planning
- Connect developers' work to its purpose

**Value Proposition:**
*"10x faster client onboarding—generate standardized briefs at $149/mo instead of 40 billable hours"*

---

### Secondary Segment: Business Stakeholders & Orgs with Weak PM Competency

**Profile:**
- C-suite and VPs at companies without strong PM function
- Non-technical founders who need to translate vision into tech requirements
- Organizations where PM quality varies wildly by individual

**Pain Points:**
- Need predictability and clear view of ROI from tech investments
- Unpredictable outcomes due to inconsistent planning competency
- Can't evaluate if development is aligned with business objectives

**Goals:**
- Amplify team competency without expensive PM hires
- Learn SDLC best practices through guided process
- Get transparency into "what are we actually building?"

**Value Proposition:**
*"Democratize world-class PM competency—embedded methodology ensures consistent, outcome-driven planning"*

---

### Expansion Segments (Future)

- **ChatGPT/Claude Desktop Users:** Unstructured planners with 50+ conversations about one project (distribution via ChatGPT Apps SDK, MCP)
- **BMAD Method Enthusiasts:** Love the methodology but don't want DIY setup (managed service positioning)
- **Linear/Jira Users at Mid-Size Teams:** Requires integrations first (system-of-record architecture enables this)
- **Visual/No-Code Developers:** Using Lovable, v0, Base 44, Bolt.new (component-level prompts + UX specs)

---

## Goals & Success Metrics

### Business Objectives

1. **Launch MVP and acquire first 100 paying users within 3 months of launch** (aligns with Month 3 target below)
2. **Achieve $60K MRR ($720K ARR) by end of Year 1** with 500 paying customers
3. **Reach break-even by Month 9**
4. **Secure 10 enterprise customers ($499/mo tier) by Month 12**
5. **Product Hunt #1 Product of the Day** at launch
6. **Maintain <$500 Customer Acquisition Cost** (CAC)

### User Success Metrics

- **Planning Speed:** Users complete planning in **7 days or less** (vs. 30+ days manual) = **50%+ time reduction**
- **Document Quality:** **85%+ approval rate** on agent-drafted documents
- **Activation:** **70% of new users complete first project within 30 days**
- **Engagement:** Active users create **3-5 projects per month**
- **Satisfaction:** Maintain **Net Promoter Score (NPS) of 50+**
- **Trial Conversion:** **5%+ conversion rate** from free trial to paid subscription

### Key Performance Indicators (KPIs) by Phase

**MVP Success (Month 3):**
- 20 paying customers = $1.5-2K MRR
- 80%+ document approval rate
- Users complete full projects in <7 days avg time
- 100 total users acquired (20% paying = 5% conversion)

**Phase 1.0 (Month 5):**
- 50 customers = $5-8K MRR
- 500+ trials via ChatGPT Apps SDK distribution
- Maintain 5%+ trial-to-paid conversion

**Year 1 (Month 12):**
- 500 customers = $60K+ MRR
- 80%+ annual retention rate
- LTV:CAC ratio of 3:1 or better
- 10 enterprise customers ($499/mo tier)

---

## MVP Scope

### MVP Definition

**Agent-first approach:** Analysis + Planning agents with 6-8 core document types, web UI with three-column workspace, markdown export, 7-day free trial (limited to 1 Initiative with Brief + PRD only), Stripe payment integration.

### Core Features (Must Have)

1. **Three-Column Workspace UI**
   - **Left:** Hierarchy tree navigation (Initiative → Epic → Feature → Story → Task)
   - **Middle:** Live document preview (TipTap Notion-like rendering)
   - **Right:** Agent chat interface for conversational AI interaction

2. **Single Primary Agent with Two-Phase Workflow**
   - **Phase 1: Analysis** (Analyst, Market Research, Competitive Analysis)
   - **Phase 2: Planning** (PM, Architect, UX, Security, QA, PO)
   - 6-8 specialized sub-agents orchestrated behind the scenes

3. **Complete Document Generation Suite**
   - Guided planning from idea → project brief → PRD → architecture → user stories
   - BMAD-inspired workflows embedded
   - Document generation and storage

4. **Hierarchy Management**
   - Create, navigate, delete/archive artifacts
   - Initiative → Epic → Feature → Story → Task organization
   - Clear view of planning artifact relationships

5. **Workflow Navigator**
   - Phase switching (Analysis ↔ Planning)
   - Cascading edits support
   - Status indicators showing which sub-agent is active

6. **Markdown Export**
   - Per-document and bulk export capabilities

7. **Authentication & Payment**
   - Clerk (email/password, social OAuth)
   - Stripe (subscriptions + usage-based pricing)

### 7-Day Free Trial Limits

- **1 Initiative only**
- **2 documents only** (Project Brief + PRD)
- No export capabilities
- No access to advanced docs (Architecture, UX, Security, QA)

### Out of Scope for MVP (Deferred to Post-MVP)

**Phase 1.0+ (Deferred):**
- ChatGPT Apps SDK distribution
- Claude Desktop MCP extension
- Freemium tier (indefinitely free)
- Adaptive approval buttons
- Voice-to-text input

**Phase 2.0+ (Deferred):**
- Linear/Jira/Notion integrations (system-of-record architecture)
- Real-time collaboration
- Cascading change management
- Advanced UI (collapsible panels, detail cards, keyboard shortcuts, canvas visualization)

**Long-Term (Deferred):**
- Execution features (Triage Inbox, Cycles, Git Integration)
- Analytics & Collaboration (Core Analytics dashboard, Slack Integration)
- Pillar 3 (Full DevOps & Observability automation)
- Gamification (confetti, badges)

### MVP Success Criteria

- **20 paying customers** using web UI consistently
- **80%+ document approval rate**
- Users **complete full projects in <7 days** avg time
- **NPS of 40+**
- **<$500 CAC** through organic channels (Product Hunt, dev communities, ChatGPT/Claude distribution later)

---

## Post-MVP Vision

### Phase 1.0: ChatGPT Apps SDK Integration (Month 4-5)

**Goal:** Tap into 800M+ ChatGPT user base for distribution

**Features:**
- ChatGPT App exposing RoadmapKO agent as native capability
- "Start planning a new project" → immediate agent conversation
- Seamless handoff to web UI for full workspace experience

**Success Metrics:**
- 500+ trial signups via ChatGPT Apps
- 50+ paid conversions from ChatGPT
- 50 paying customers = $5-8K MRR
- Featured in ChatGPT Apps Store

---

### Phase 1.5: Claude Desktop MCP Integration (Month 6-7)

**Goal:** Secondary distribution via Claude Desktop users

**Features:**
- MCP server exposing RoadmapKO agents as Claude Desktop tools
- Local-first workflows for privacy-conscious users
- Multi-provider distribution strategy (reduces platform risk)

**Success Metrics:**
- 200+ trial signups via Claude Desktop MCP
- 100 paying customers = $10-12K MRR
- 60%+ monthly retention (Month 1 → Month 2 cohort)
- Multiple distribution channels validated

---

### Phase 2.0: Linear/Jira/Notion Integrations (Month 8-10)

**Goal:** Enable "system of record" push to execution tools

**Features:**
- **System-of-Record Architecture:**
  - Pull existing artifacts from Linear, Jira, Notion, Azure Boards
  - Create new in both systems simultaneously
  - RoadmapKO is always system of record
  - Platform migration safety
- Fully interactive 'Living Roadmap' with drill-down modals
- Advanced analytics dashboard

**Success Metrics:**
- Mid-size teams (10-50 people) adopt RoadmapKO
- 3 integrations built (Linear, Jira, Notion)
- Unlock expansion to Linear/Jira Users segment

---

### Long-Term Vision (Year 2+)

**Phase 3+: Evolve into Fully Autonomous Platform**

1. **Pillar 3: Full DevOps & Observability Automation**
   - "Performance-to-ROI Mapping" feature
   - "Intelligent Defect Prevention" system
   - Automated deployment orchestration

2. **Execution Features (Compete with Linear)**
   - Triage Inbox for issue management
   - Cycles for sprint planning
   - Git Integration for code-to-planning linkage

3. **Advanced Collaboration & Analytics**
   - Real-time collaboration
   - Cascading change management
   - Core Analytics dashboard
   - Slack Integration
   - Adaptive approval buttons

4. **Vertical-Specific Templates**
   - **SaaS startups:** Pre-built templates for common SaaS features (auth, payments, onboarding)
   - **E-commerce:** Templates for product catalogs, checkout flows, inventory management
   - **Fintech:** Compliance-aware templates with built-in security/audit requirements
   - **Healthcare:** HIPAA-compliant templates with privacy-by-design

5. **White-Label for Agencies**
   - Custom branding for digital agencies
   - Multi-tenant client management
   - Revenue sharing model

---

### Expansion Opportunities

**Market Evolution:**
- After mastering the "front-half," expand to compete directly with Linear on execution
- Position for potential strategic acquisition by Atlassian, Linear, or Notion

**Competitive Moat:**
- **Network effects:** More tools integrate → more valuable for users
- **Switching costs:** RoadmapKO contains institutional knowledge spanning years
- **Data moat:** Millions of planning documents train better agents
- **Distribution leverage:** ChatGPT Apps SDK + Claude MCP reach 800M+ users

**Revenue Expansion:**
- Vertical-specific templates (Year 2)
- White-label for agencies (Year 2)
- Enterprise tier with custom agents ($499-999/mo)

---

## Technical Considerations

### Platform Requirements

- **Primary:** Responsive web application (Chrome, Firefox, Safari, Edge)
- **Phase 1.0:** ChatGPT Apps SDK
- **Phase 1.5:** Claude Desktop MCP
- **Performance Standards:**
  - Agent response: <3s for simple queries, <30s for document generation
  - UI interaction: <100ms feedback (sub-100ms standard)

---

### Technology Stack

**Frontend:**
- Next.js 14 (App Router, TypeScript, React Server Components)
- shadcn/ui + Tailwind CSS for UI components
- TipTap for Notion-like markdown rendering
- Turborepo monorepo structure
- Vercel hosting

**Backend & AI Orchestration:**
- **Hybrid Approach:**
  - **Vercel AI SDK v5:** UI-native agents for chat, Q&A, streaming (simple interactions)
  - **CrewAI (FastAPI):** Multi-agent orchestration for complex workflows
- **Multi-Provider Access:** OpenRouter for unified LLM access across Anthropic, OpenAI, Google, Groq, Fireworks
- Vercel Serverless Functions + FastAPI (Python) on Vercel Serverless

**Database & Storage:**
- **Supabase:** PostgreSQL + pgvector (embeddings) + Realtime + Storage
- **Upstash Redis:** Serverless caching
- **Cloudflare R2:** Zero egress for document exports

**AI Models (Multi-Model Strategy):**

| Agent | Primary Model | Cost per 1M Tokens |
|-------|--------------|-------------------|
| Discovery/QA | google/gemini-2.0-flash | $0.075 input / $0.30 output |
| Requirements | anthropic/claude-3.5-sonnet | $3.00 input / $15.00 output |
| Architecture | anthropic/claude-3.5-sonnet | $3.00 input / $15.00 output |
| Quality | google/gemini-2.0-flash | $0.075 input / $0.30 output |

**Supporting Services:**
- **Auth:** Clerk (email/password, Google OAuth, GitHub OAuth)
- **Payment:** Stripe (subscriptions + usage-based pricing)
- **Email:** Resend (React Email templates)
- **Docs:** Mintlify
- **Analytics:** PostHog (product analytics + feature flags)
- **Monitoring:** Sentry (error tracking), Langfuse (LLM observability)
- **Real-time:** Pusher/Ably for streaming agent progress

---

### Architecture Pattern

```
User → Vercel (Next.js) → Decision Point
                            ├→ Simple: Vercel AI SDK → OpenRouter
                            └→ Complex: CrewAI Service → OpenRouter
                                         ├→ Anthropic (Claude)
                                         ├→ Google (Gemini)
                                         └→ OpenAI (GPT-4)
```

**Rationale:**
- **Cost optimization:** Use cheap Gemini Flash for Discovery/QA, expensive Claude Sonnet only for critical planning
- **Flexibility:** OpenRouter provides unified access to 100+ models with automatic failover
- **Scalability:** Serverless-first architecture with zero fixed infrastructure costs
- **Performance:** Hybrid approach balances simplicity (Vercel AI SDK) with power (CrewAI)

---

### Repository Structure (Turborepo Monorepo)

```
roadmap-ko/
├── apps/
│   ├── web/                 # Next.js web app (MVP)
│   ├── chatgpt-app/         # ChatGPT Apps SDK (Phase 1.0)
│   └── mcp-server/          # Claude Desktop MCP (Phase 1.5)
├── packages/
│   ├── ui/                  # Shared shadcn/ui components
│   ├── database/            # Supabase schema, migrations, types
│   ├── agents/              # Agent orchestration (CrewAI configs)
│   └── integrations/        # Linear, Jira, Notion connectors (Phase 2.0)
└── services/
    └── crewai-api/          # FastAPI service for CrewAI orchestration
```

---

### Cost Structure (MVP)

**Monthly Operating Costs:**
- Vercel: $0-20
- Supabase: $0-25
- Clerk: $0
- OpenRouter (AI models): $20-50
- Resend (email): $20
- Dev tools (PostHog, Sentry, Langfuse): $220
- **Total: ~$285-335/mo**

**Gross Margin at Scale:** 95%+ (SaaS model with minimal marginal costs)

---

### Security & Compliance

- **Encryption:** AES-256 at rest, TLS 1.3 in transit
- **Row-Level Security (RLS):** Enforced in Supabase for multi-tenant data isolation
- **GDPR Compliance:** Data export, right to deletion, 90-day grace period
- **SOC 2 Type II:** Enterprise tier requirement (Year 2)

---

## Pricing Strategy

### Pricing Philosophy

Users already pay $200-250/mo for ChatGPT/Claude/Gemini. RoadmapKO is **additive value** on top, not replacement. Pricing balances accessibility for solo devs with revenue potential from teams and enterprises.

### Pricing Tiers

**Free Trial: $0**
- 7-day trial (then pauses)
- 1 Initiative, 2 documents (Brief + PRD only)
- No export capabilities
- Community support

---

**Starter: $49/month** ($470/year - save $118)

*Target: Solo developers, indie hackers*

- 3 Initiatives per month
- All 6-8 document types (Brief, PRD, Architecture, UX, Security, QA)
- Full hierarchy navigation
- Markdown export
- 25 usage credits/month
- Email support (48-hour SLA)
- **Overage:** $5 per Initiative, $0.50 per credit

---

**Professional: $149/month** ($1,430/year - save $358)

*Target: Small dev teams, digital agencies*

- **Unlimited Initiatives**
- 100 usage credits/month
- **1 integration included** (Linear, Jira, Notion, Azure Boards)
- Priority support (24-hour SLA)
- Early access to features
- **Team collaboration** (up to 5 users)
- **Overage:** $0.40 per credit, $29/mo per additional integration

---

**Enterprise: $499/month** ($4,790/year - save $1,198)

*Target: Mid-size teams, organizations*

- **Unlimited Initiatives**
- **Unlimited credits** (fair use: <5,000/month)
- **All integrations included** (Linear, Jira, Notion, Azure Boards)
- **Dedicated Slack/Teams support**
- **SLA guarantees** (99.9% uptime)
- **SSO (SAML)** authentication
- **Custom agent training** on company-specific workflows
- **Private deployment option** (+$499/mo)
- **Unlimited team members**

---

### Usage Credits System

**1 Credit Charged For:**
- Generate new document (Brief, PRD, Architecture, UX, Security, QA)
- Major document revision
- Export to integration (Linear, Jira, Notion)

**0 Credits (Free):**
- Agent chat and Q&A
- Minor edits and refinements
- View/read documents
- Markdown export

**Credit Add-On Packs:**
- 100 credits: $8
- 400 credits: $32
- 1000 credits: $80
- 4000 credits: $320

---

### Revenue Projections (Year 1, Month 12)

| Tier | Customers | Price | MRR |
|------|-----------|-------|-----|
| Starter | 300 | $49 | $14,700 |
| Professional | 150 | $149 | $22,350 |
| Enterprise | 50 | $499 | $24,950 |
| **Base MRR** | **500** | - | **$62,000** |
| Add-ons (integrations, credits) | - | - | **$3,240** |
| **Total MRR** | **500** | - | **$65,240** |
| **ARR** | - | - | **$782,880** |

**Blended LLM Cost Margin:** 90-95% (70% Gemini Flash, 20% Claude Sonnet, 10% specialized models)

---

## Constraints & Assumptions

### Budget Constraints

- **Development Costs:** $285-335/mo (MVP), $770-1,070/mo (Month 6 at 150 customers)
- **Solo founder:** No salary first 6-12 months
- **Marketing Budget:**
  - Month 1-5: $0 (Product Hunt launch, ChatGPT Apps SDK, content marketing only)
  - Month 6+: Max $500/mo for paid acquisition
- **Break-even:** Month 9 target

### Timeline Constraints

- **Aggressive 3-month MVP deadline** (12 weeks)
- **Solo founder commitment:** 60-80 hours/week
- **AI productivity multiplier:** Expecting 3-5x with AI dev tools (Cursor, v0, Claude Code)
- **Checkpoint cadence:** Weekly milestone reviews, 2-week buffer built into timeline

### Resource Constraints

- **Solo founder** through Month 6
- **Part-time admin/support:** Month 6-9 (as needed)
- **First full-time hire:** Month 9-12 (when MRR hits $10K+)
- **Founder skills:** Strong backend, architecture, AI orchestration
- **Learning curve:** Frontend (Next.js), UI/UX polish

### Technical Constraints

- **Vercel:** 10s timeout (Hobby/Pro tiers), 300s (Enterprise tier)
- **Supabase Free Tier:** 500MB database, 2GB bandwidth; Pro tier: 8GB database, 250GB bandwidth
- **OpenRouter Rate Limits:** Model-dependent, typically 60-100 req/min
- **LLM API Quotas:** Default $1K/month, can request increases

### Key Assumptions

**Product Assumptions:**
- **BVSSH/BMAD methodology can be successfully productized** into guided AI workflows
- **AI agents can achieve 80%+ approval rate** on generated documents with proper prompt engineering
- **Users want opinionated workflow** over maximum flexibility
- **Current AI agent frameworks (CrewAI, Vercel AI SDK) are mature enough** for production use

**Market Assumptions:**
- **Solo dev market is large enough** (50K+ globally actively building SaaS)
- **Users will pay $49-149/mo** for planning automation (10x ROI on time saved)
- **Credit-based model drives higher revenue** than pure fixed tiers
- **Significant market exists for highly opinionated tool** (not everyone wants flexibility)

**Distribution Assumptions:**
- **ChatGPT Apps SDK + MCP will drive significant acquisition** (500+ trials in first 2 months)
- **Product Hunt launch generates 50-100+ trial signups**
- **Content marketing + community engagement sustains 20-30 trials/month**

**Competitive Assumptions:**
- **Linear/Jira won't build competing front-half features** for 12-18 months (focused on execution)
- **18-month runway before major competition** (time to build moat through integrations, data, network effects)

**Cost Assumptions:**
- **Blended LLM costs remain within 10-15% of credit revenue** (90-95% margin)
- **Multi-model strategy (70% Gemini Flash, 20% Claude, 10% specialized)** keeps costs low
- **OpenRouter provides stable pricing** and reliable access to models

---

## Risks & Open Questions

### 🔴 Critical Risks

**1. Agent Output Quality Below 80% Approval** (Probability: 40-45%)

- **Impact:** User churn, negative reviews, failed product-market fit
- **Mitigation:**
  - Extensive prompt engineering and A/B testing
  - Multi-model strategy (Claude Sonnet for critical planning, Gemini Flash for discovery)
  - Daily monitoring of approval rates
  - Design partner feedback loop
- **Early Warning Signals:** <70% approval by Week 8, <75% by Month 3
- **Contingency:** If <70% by Week 8, pause 2 weeks for quality improvements; If <75% Month 3, delay public launch

---

**2. Solo Founder Velocity Insufficient** (Probability: 35-40%)

- **Impact:** Delayed revenue, competitive window closes, founder burnout
- **Mitigation:**
  - Weekly milestone checkpoints with ruthless prioritization
  - AI dev tools (Cursor, v0, Claude Code) for 3-5x productivity multiplier
  - Month 2 assessment: On track or descope?
  - 2-week buffer built into 12-week timeline
- **Early Warning Signals:** Missing 2+ weekly milestones, <40 hours/week output
- **Contingency:** Descope from 7 to 3-5 agents, extend timeline 2-4 weeks, hire contractor ($3-5K/month)

---

**3. ChatGPT Apps SDK / MCP Distribution Fails** (Probability: 40-50%)

- **Impact:** Growth stalls at <50 customers, revenue targets missed, CAC unsustainable
- **Mitigation:**
  - Don't rely solely on platform distribution
  - Build organic channels: Product Hunt, content marketing, dev communities
  - Partnerships with Cursor, Lovable/v0, visual dev tools
- **Early Warning Signals:** <50 trials from ChatGPT by Month 5, <10 trials from MCP by Month 7
- **Contingency:** Pivot to paid ads ($500/mo), double down on content, influencer partnerships

---

### 🟡 Significant Risks

**4. Pricing Too High for Solo Devs** (Probability: 30-35%)

- **Impact:** Low trial-to-paid conversion (<5%), revenue targets missed
- **Mitigation:**
  - Value messaging (7 days vs 30+ days, 10x ROI on time saved)
  - A/B test pricing ($39 vs $49 Starter tier)
  - Annual discounts (20% off)
- **Early Warning Signals:** <5% conversion rate by Month 3
- **Contingency:** Drop to $39/mo Starter, add lifetime deal ($299-499), introduce freemium tier

---

**5. Linear/Jira Builds Native AI Agents** (Probability: 25-30% in 12-18 months)

- **Impact:** Market adoption of RoadmapKO threatened by incumbent with distribution advantage
- **Mitigation:**
  - Move fast to build 12-18 month lead
  - Multi-platform positioning (ChatGPT Apps, MCP, standalone)
  - Deep specialization in "front-half" with BVSSH methodology
  - System-of-record architecture enables platform migration
- **Early Warning Signals:** Linear announces AI roadmap features, Jira beta tests planning agents
- **Contingency:** Pivot to distribution-first (ChatGPT Apps primary), enterprise specialization, or position for strategic acquisition

---

**6. Customer Support Overwhelms Development** (Probability: 25-30% if >100 customers Month 4)

- **Impact:** Solo founder spends >50% time on support, development velocity drops
- **Mitigation:**
  - Self-service docs (Mintlify)
  - In-app help and contextual tooltips
  - Community support (Discord/Slack)
  - Office hours (2x/week)
  - Clear SLAs by tier (48-hour Starter, 24-hour Pro)
- **Early Warning Signals:** >15 support tickets/week, >10 hours/week on support
- **Contingency:** Hire part-time support Month 6 ($600-1,600/mo), delay Phase 1.0 by 2-4 weeks

---

**7. Market Adoption of Highly Opinionated Tool** (Probability: 25-30%)

- **Impact:** TAM smaller than expected, growth caps at <200 customers
- **Mitigation:**
  - Productize BVSSH/BMAD methodology that's proven to work
  - Target users who value speed over flexibility (solo devs, agencies)
  - Position as "embedded PM competency" not just "tool"
- **Contingency:** Add customization options, white-label for agencies, pivot to less opinionated workflow

---

**8. Legal Implications of Productizing BMAD Method** (Probability: 15-20%)

- **Impact:** IP disputes, need to rebrand methodology
- **Mitigation:**
  - Consult IP attorney before launch
  - Position as "inspired by" not "official BMAD"
  - Create distinct brand identity for methodology within RoadmapKO
- **Contingency:** Rebrand methodology, license from BMAD creators, or develop original framework

---

### Open Questions

**Strategic Direction:**
- Venture-scale or lifestyle business trajectory?
- If Linear builds competing agents by Month 9, pivot or compete head-on?
- Solo devs or agencies as primary long-term focus?

**Product Decisions:**
- Which integration to build first: Linear, Jira, or Notion?
- ChatGPT App Store or standalone web first?
- Freemium tier or trial-only?

**Go-to-Market:**
- Optimal pricing: $39, $49, or $59 for Starter tier?
- Best user acquisition channels beyond Product Hunt and ChatGPT Apps?
- Content strategy: technical deep-dives or beginner-friendly tutorials?

**Technical:**
- Vercel AI SDK + CrewAI hybrid vs. pure Vercel AI SDK?
- OpenRouter vs. direct LLM provider APIs?
- Supabase vs. Firebase for MVP?

---

## Appendices

### A. Research Summary

**Competitive Analysis:**
- **Linear:** Execution-focused, opinionated workflows, beautiful UI, lacks front-half planning features
- **Jira:** Too complex, overwhelming for small teams, strong enterprise presence
- **Azure Boards:** Enterprise-focused, Microsoft ecosystem lock-in
- **Trello:** Simple but lacks structure, no built-in methodology

**Strategic Insights:**
- Linear's playbook: Start opinionated, focus on speed/UX, expand gradually
- Gap in market: No tool masters the "front-half" (idea → backlog)
- Opportunity: Position as complementary to Linear/Jira, not competitive (initially)

**Market Research:**
- Solo dev/indie hacker segment: 50K+ globally, underserved by enterprise tools
- Digital agencies: $500K-2M revenue, frustrated by inconsistent planning
- AI coding tool users (Cursor, v0, Lovable): Growing segment, high need for structured planning

**Technical Feasibility:**
- Multi-agent frameworks (CrewAI, Vercel AI SDK) production-ready as of 2024
- OpenRouter provides unified multi-provider LLM access with automatic failover
- ChatGPT Apps SDK + MCP enable zero-cost distribution to 800M+ users

---

### B. Stakeholder Input

[Not applicable for solo founder project - no external stakeholders]

---

### C. References

**Methodology:**
- BMAD (Business, Methodology, Architecture, Development) documentation
- BVSSH (Business, Vision, Strategy, Solution, How) principles
- Outcome-driven development frameworks

**Market Data:**
- Standish Group: 70% of software projects fail due to poor requirements
- Solo developer market size estimates (GitHub, Indie Hackers, Product Hunt data)

**Competitive Intelligence:**
- Linear product strategy and growth trajectory
- Jira/Atlassian strategic positioning
- ChatGPT Apps SDK + Claude MCP adoption data

**Technical Documentation:**
- Vercel AI SDK v5 documentation
- CrewAI multi-agent orchestration guides
- OpenRouter API documentation
- Supabase architecture best practices

---

## Next Steps

### Immediate Actions (Weeks 1-2)

**Pre-Development Validation:**
1. **Design Partner Recruitment:** Recruit 10 design partners
   - 3 solo developers/indie hackers
   - 3 digital agencies (2-10 person teams)
   - 2 BMAD methodology enthusiasts
   - 2 ChatGPT/Claude power users
2. **Competitive Deep-Dive:** Analyze users of Cursor, Replit, v0, Lovable, Bolt.new
3. **Pricing Validation:** Interview 20 potential users on willingness to pay $49-149/mo
4. **Technical Stack Setup:**
   - Initialize Turborepo monorepo
   - Configure Vercel + Supabase + Clerk
   - Set up OpenRouter API access
   - Initialize CrewAI + Vercel AI SDK hybrid architecture

---

### Month 1-3: MVP Development (12 Weeks)

**Week 1-2: Foundation**
- Turborepo setup with apps/web, services/crewai-api, packages
- Supabase schema: users, initiatives, documents, agents, credits
- Clerk authentication + Stripe payment integration
- Three-column workspace UI skeleton (shadcn/ui + TipTap)

**Week 3-4: Agent Orchestration**
- CrewAI orchestration layer + OpenRouter integration
- Vercel AI SDK chat interface
- Agent status indicators and phase transitions
- Multi-model routing (Gemini Flash vs Claude Sonnet)

**Week 5-6: Analysis Phase Agents**
- Analyst agent (brainstorming, discovery)
- Market Research agent
- Competitive Analysis agent
- Document generation: Project Brief

**Week 7-8: Planning Phase Agents**
- PM agent (PRD generation)
- Architect agent (tech stack, data models)
- UX agent (flows, wireframes)

**Week 9-10: Planning Completion**
- Security agent (threat modeling)
- QA agent (test strategy)
- Hierarchy management (Initiative → Epic → Feature → Story → Task)
- Markdown export functionality

**Week 11-12: MVP Polish & Private Beta**
- Design partner onboarding (10 users)
- Approval rate monitoring (target: 80%+)
- Bug fixes and UX refinements
- Self-service docs (Mintlify)

**MVP Success Gate:** 80%+ approval rate, <7 days avg planning time, NPS 40+ before public launch

---

### Month 4-5: Phase 1.0 - ChatGPT Apps SDK

- Build ChatGPT App exposing RoadmapKO agent
- "Start planning a new project" → immediate conversation
- Seamless handoff to web UI for full workspace
- **Goal:** 500+ trial signups, 50+ paid conversions, Product Hunt launch

---

### Month 6-7: Phase 1.5 - Claude Desktop MCP

- Build MCP server exposing RoadmapKO agents as Claude Desktop tools
- Local-first workflows for privacy-conscious users
- **Goal:** 200+ trial signups, 100 paying customers, 60%+ retention

---

### Month 8-10: Phase 2.0 - Linear/Jira/Notion Integrations

- System-of-record architecture implementation
- Pull existing artifacts, create new in both systems
- RoadmapKO always system of record
- **Goal:** 3 integrations live, unlock mid-size team segment

---

### Month 12: Year 1 Target

- **500 paying customers**
- **$60K+ MRR ($720K ARR)**
- **80%+ annual retention**
- **LTV:CAC ratio of 3:1**
- **10 enterprise customers ($499/mo tier)**

---

## PM Handoff

This **consolidated Project Brief for RoadmapKO** is now complete and ready for Product Requirements Document (PRD) development.

**Brief Summary:**
RoadmapKO is an AI-native SaaS platform that masters the "front-half" of the software development lifecycle, guiding teams from raw ideas to developer-ready backlogs using a primary agent that orchestrates 6-8 specialized sub-agents (Analyst, PM, Architect, UX, Security, QA).

**Key Decisions Made During Consolidation:**
- **Product Positioning:** "Masters the front-half of SDLC" + AI multi-agent orchestration
- **Target Market:** Equal emphasis on solo developers AND modern software teams
- **Pricing:** Starter $49, Professional $149, Enterprise $499 with usage credits
- **Tech Stack:** Hybrid Vercel AI SDK + CrewAI/FastAPI → OpenRouter multi-provider
- **Distribution:** Standalone web (MVP) → ChatGPT Apps (Phase 1.0) → MCP (Phase 1.5) → Integrations (Phase 2.0)

**Next Phase:** Please start in **'PRD Generation Mode'**, review the brief thoroughly, and work with the user to create the PRD section by section as the template indicates, asking for any necessary clarification or suggesting improvements.

---

**End of Consolidated Project Brief**

*Next: Deduplication & Refinement Phase*
*Prepared by Mary (Business Analyst Agent) - 2025-11-30*
