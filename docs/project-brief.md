# Project Brief: RoadmapKO

**Status:** Final - Ready for PRD Development
**Last Updated:** 2025-11-30
**Version:** 2.0 (Refined by Business Analyst Agent)

---

## Executive Summary

**Product Concept:**

RoadmapKO is an AI-native, opinionated SaaS platform designed to **master the "front-half" of the software development lifecycle**, guiding teams from a raw idea to a perfectly aligned, developer-ready backlog. Using specialized AI agents, RoadmapKO orchestrates the complete planning process—from ideation through production-ready specifications—while naturally teaching best practices through opinionated workflows.

**The Problem:**

A chronic and costly disconnect exists between high-level business strategy and the day-to-day work of software development teams. 70% of software projects fail due to poor requirements, with teams struggling to maintain comprehensive documentation, translate business needs into engineering tasks, and prevent scope creep.

**Target Market:**

- **Primary Segments (Equal Weight):**
  - Solo Developers & Indie Hackers (5-15 years experience building SaaS)
  - Modern Software Teams & Leaders (PMs, EMs, SMs, POs at high-velocity startups and agencies)
- **Secondary:** Digital Agencies (2-10 person teams, $500K-2M revenue), Business Stakeholders & Executives
- **Tertiary:** Visual/No-Code Developers, ChatGPT/Claude Desktop Users, BMAD Method Enthusiasts

**TAM:** ~750,000 potential users globally; ~300,000 addressable in Year 1

**The Solution:**

RoadmapKO provides **7 specialized AI agents** working through a unified conversational interface to manage the complete **Project → Initiative → Epic → Feature → Story → Task** workflow. The system combines:

1. **AI Multi-Agent Team:** Discovery, Requirements, Design, Architecture, Quality, Validation, and Planning agents—each with specialized expertise
2. **Opinionated Workflow:** Enforces the proven hierarchy to prevent scope chaos
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

RoadmapKO positions as a **complementary partner to execution-focused tools like Linear and Jira**—we generate the planning artifacts they require. With system-of-record architecture integrating with Linear, Jira, Notion, and Azure Boards, RoadmapKO preserves full context even if users switch platforms, providing platform migration safety and multi-platform support.

**Why Now:**

- AI agent orchestration became practical in 2024
- Remote work amplifies the need for better async documentation
- Distribution channels (ChatGPT Apps SDK, Claude Desktop MCP) reach 800M+ users without building marketplace presence from scratch

---

## Problem Statement

**The Front-Half Planning Gap:**

In today's high-velocity technology landscape, a chronic and costly disconnect exists between high-level business strategy and the day-to-day work of software development teams. Most software projects fail not during implementation, but during planning—or more accurately, due to lack of proper planning. Teams jump straight into execution tools (Jira stories, Linear issues) without establishing clear strategic context or mastering the "front-half" of the SDLC.

---

### User Scenarios: The Pain in Practice

**Scenario 1: Sarah - Solo Developer / Indie Hacker**

*Sarah is 8 years into her career, building a SaaS invoicing platform. She's deep into coding when she realizes she's built the wrong payment flow—her mental model didn't match actual user needs. She has no PRD, no architecture doc, just 50 scattered Notion pages and a head full of ideas. When her co-founder asks "why did we choose PostgreSQL over MongoDB?" six months later, Sarah can't remember. She spends 3 days reverse-engineering her own decisions.*

**Pain Points:** Lost context, no structured planning, rework cycles, inefficient translation of ideas to code

---

**Scenario 2: Marcus - Product Manager at a High-Velocity Startup**

*Marcus manages 3 products with 2 engineers each. Every sprint planning meeting devolves into "wait, what were we trying to accomplish with this epic again?" He has PRDs in Google Docs, competitive analysis in Notion, user stories in Linear, and architecture sketches in Figma. When stakeholders ask for a project status update, it takes him 4 hours to synthesize information across 6 tools. New engineers joining the team spend their first week just finding documentation.*

**Pain Points:** Disconnected artifacts, onboarding nightmare, inconsistent competency, lost context

---

**Scenario 3: Jennifer - Scrum Master at a Digital Agency**

*Jennifer's agency manages 5 client projects. Each project kickoff takes 2 full weeks of discovery meetings, document drafting, and revision cycles. Her team bills $150/hour, but 30-40% of that time is rework because requirements were unclear. She copy-pastes the previous project's brief, does find-and-replace on client names, and hopes she didn't miss anything. The quality of planning depends entirely on which PM is assigned—and two of her PMs are junior.*

**Pain Points:** Inconsistent competency, inefficient translation, rework cycles, disconnected artifacts

---

**Scenario 4: David - Engineering Manager**

*David's team ships features that technically work but miss the business goal. When he asks "what problem does this solve?", developers point to a Jira ticket that says "Add export button." The original business context—why users need CSV exports for tax compliance—was lost three handoffs ago. His team has 47 unresolved tech debt items because there's no systematic way to track the "why" behind decisions.*

**Pain Points:** Lost context, inefficient translation, unhealthy backlogs, scope creep

---

**Scenario 5: Priya - Product Owner**

*Priya spends sprint planning answering "what did we mean by this requirement?" She wrote the original PRD 4 months ago, but the team interpreted "user dashboard" three different ways. Now she's in damage control, clarifying scope that should have been crystal clear from day one. When the CEO asks "are we on track for Q2 launch?", she honestly doesn't know—the project boundaries keep shifting.*

**Pain Points:** Scope creep, inefficient translation, rework cycles, disconnected artifacts

---

**Scenario 6: Alex - Business Stakeholder (VP of Product)**

*Alex approved a $500K budget for a mobile app rebuild. Six months in, the CTO says they need to "re-architect the backend" because requirements changed. Alex has no idea what changed, why, or if this was preventable. He attends weekly status meetings but still can't answer the board's question: "What are we actually building and why?" The planning artifacts exist somewhere, but they're fragmented, inconsistent, and already outdated.*

**Pain Points:** Disconnected artifacts, lost context, scope creep, wasted R&D spending

---

**Scenario 7: Chris - Visual/No-Code Developer**

*Chris uses Lovable and v0 to rapidly build UIs, but he keeps hitting the same wall: "What should this actually do?" He can generate beautiful components in minutes, but without clear UX specs and backend requirements, he builds features that don't integrate properly. He spends more time fixing integration issues than building new features. The AI tools are incredibly powerful, but garbage in = garbage out.*

**Pain Points:** Inefficient translation, rework cycles, lost context, no structured planning

---

### Critical Pain Points (Cross-Cutting Issues)

1. **Disconnected Artifacts:** Market research exists in Notion, PRD in Google Docs, architecture in Confluence, stories in Linear—no single source of truth
2. **Inefficient Translation:** Business needs are poorly translated into actionable engineering tasks, leading to features that miss the mark
3. **Lost Context:** 6 months into development, no one remembers *why* architectural decisions were made
4. **Scope Creep:** Without clear Project → Initiative → Epic boundaries enforced by opinionated hierarchy, features get added reactively without strategic evaluation
5. **Unhealthy Backlogs:** Critical issues and tech debt are deferred indefinitely, causing ongoing quality problems and poor user experience
6. **Inconsistent Competency:** Quality of product planning varies wildly depending on the skill of the individual product manager, leading to unpredictable outcomes
7. **Onboarding Nightmare:** New team members face fragmented documentation across 5+ tools
8. **Rework Cycles:** Implementation discovers gaps in requirements, forcing costly backtracking

---

### Quantified Impact

- **70% of software projects fail** due to poor requirements (Standish Group)
- Average team **spends 8-12 hours/week** searching for context across documentation silos
- Agencies report **30-40% of billable hours lost** to rework from unclear requirements
- **Wasted R&D spending**, delayed time-to-market, low team morale, failure to deliver on business objectives

---

### Why Existing Solutions Fall Short

| Tool Type | Strength | Gap | How RoadmapKO's 7 Agents Solve It |
|-----------|----------|-----|-----------------------------------|
| **Jira/Linear** | Excellent for execution tracking | Assumes planning is already done; provides no upstream guidance for the "front-half" | **Discovery, Requirements, Design, Architecture, Quality, Validation, Planning agents** create all upstream artifacts before execution begins |
| **Notion/Confluence** | Flexible documentation | Too freeform—no structure, relationships between docs, or embedded methodology | **Opinionated Project → Initiative → Epic → Feature → Story → Task hierarchy** enforces structure; **Validation agent** maintains artifact relationships |
| **Traditional PM tools** | Enforce process | Rigid templates; no intelligence to adapt or guide; too complex (Jira) | **Requirements agent** adapts elicitation based on user responses; **Discovery agent** guides brainstorming intelligently |
| **AI coding assistants** | Great at code generation | No understanding of strategic context, document relationships, or outcome-driven development | **Architecture + Design agents** provide context-aware specs optimized for AI coding tools; **Validation agent** ensures stories align with PRD |

---

## Proposed Solution

**Core Concept: Your AI Planning Team**

RoadmapKO is an AI-native SaaS platform that provides **7 specialized AI agents** working through a unified conversational interface to generate all planning documentation—from raw business idea to fully aligned, developer-ready backlog. It's a **complete, embedded methodology based on BVSSH principles** that masters the "front-half" of the software development lifecycle.

**"Never start from a blank page again"**—users review, refine, and approve agent-drafted documents rather than creating from scratch.

---

### The Three-Column Workspace

RoadmapKO's interface features a sophisticated three-column layout designed for seamless workflow navigation:

**Left Column: Initiative Workflow Navigator**
- **Top:** Project selector dropdown (e.g., "E-Commerce Platform MVP")
- **Initiative Workflow:** Collapsible workflow stages showing progress
  - Discovery & Research (COMPLETE)
  - Product Definition (IN PROGRESS)
  - Design & Architecture (LOCKED)
  - Validation & Handoff (LOCKED)
- **Section Details:** Expandable sections showing document hierarchy and approval status
  - Project Brief (✓ Executive Summary v1.2 approved, ✓ Problem Statement v3 final, ✓ Target Users defined)
  - PRD Header & Context (✓ Complete)
  - Functional Requirements (⏳ Awaiting elicitation choice...)
  - Non-Functional Requirements (○ Not Started)
  - Epics & Stories (○ Not Started)
  - Acceptance Criteria (○ Not Started)

**Middle Column: Live Document Preview**
- **Header:** Document title, version, status (e.g., "PRD: E-Commerce Platform v0.4 (Draft)")
- **Status Bar:** Real-time progress indicators (⚠️ 3 sections pending approval • 2 sections in progress)
- **Document Content:** Notion-like markdown rendering (TipTap) with approval badges
  - Sections show approval status (✓ Approved, ⏳ Awaiting Elicitation, ○ Not Started)
  - Rich formatting with collapsible sections
- **Actions:** Edit, History, Export buttons

**Right Column: Agent Chat Interface**
- **Active Agent Display:** Shows current agent avatar and activity (e.g., "PM - Product Manager Agent" working on "PRD → Functional Requirements")
- **Navigation:** "Previous Agents" and "View All Chats" buttons
- **Conversational AI:** Chat-style interaction with agent messages and user responses
- **Agent Messages:** Context-aware updates from active agent
  - "Based on the approved Project Brief, I'll now help you create the Product Requirements Document..."
  - Draft content presented in message bubbles
  - User response options (numbered 1-9 for elicitation or free-form input)
- **Input Field:** "Type your response..." with Send button

**Key UI Features:**
- **Mode Indicator:** Top-right shows "INTERACTIVE" with #yolo toggle option
- **Progress Tracking:** Real-time workflow completion percentages (e.g., "Planning: 35%" with time estimates)
- **Status Indicators:** Visual badges for Complete, In Progress, Locked, Awaiting Elicitation
- **Dark Theme:** Professional dark UI with purple accent colors for agents

---

### The 7-Agent Team Architecture

RoadmapKO employs a **two-phase workflow** with specialized agents for each aspect of planning:

**PHASE 1: ANALYSIS & DISCOVERY**

**1. Discovery Agent (Business Analyst)**
- *Persona:* Analytical, curious, enthusiastic researcher
- *Abilities:*
  - Brainstorming sessions and ideation
  - Market research analysis
  - Competitor analysis
  - Project brief creation

**PHASE 2: PLANNING & EXECUTION READINESS**

**2. Requirements Agent (Product Manager)**
- *Persona:* Structured, pragmatic, collaborative PM
- *Abilities:*
  - Create PRD from Brief (Fast Track mode)
  - Interactive PRD Creation (detailed elicitation)

**3. Design Agent (UX Expert)**
- *Persona:* Creative, empathetic, user-focused UX designer
- *Abilities:*
  - Create front-end specifications
  - Generate UI prompts optimized for Lovable/v0/Cursor
  - Design component-level requirements

**4. Architecture Agent (Architect)**
- *Persona:* Systematic, detail-oriented, scalability-focused architect
- *Abilities:*
  - Create architecture from PRD + UX Spec
  - Design data models and tech stack recommendations

**5. Quality Agent (Quality Assurance)**
- *Persona:* Meticulous, proactive, quality-obsessed QA lead
- *Abilities:*
  - Early test architecture input on high-risk areas
  - Risk assessment on draft stories
  - Test strategy and risk profile creation

**6. Validation Agent (Product Owner)**
- *Persona:* Strategic, decisive, business-focused PO
- *Abilities:*
  - Run master checklist (PRD and User Story)
  - Update epics and stories with validation feedback
  - Shard documents (PRD and Architecture) for team consumption
  - Validate story drafts against PRD and architecture artifacts

**7. Planning Agent (Scrum Master)**
- *Persona:* Organized, practical, delivery-focused Scrum Master
- *Abilities:*
  - Review previous story dev/QA notes
  - Draft next story from sharded epic + architecture
  - Maintain workflow continuity across sprints

---

### Workflow Hierarchy

**Project-Level Navigation:**
- **Project:** Top-level container with Project Brief (e.g., "E-Commerce Platform MVP")
  - **Initiative:** Major body of work with complete workflow phases
    - **Epic:** Large feature set or capability
      - **Feature:** Specific user-facing functionality
        - **Story:** Atomic unit of user value
          - **Task:** Technical implementation step

**MVP Scope:** Project (with Brief) → Initiative (structure only)
**Post-MVP:** Full hierarchy unlocked progressively through Phase 1.0 and 2.0

---

### Key Differentiators

1. **Embedded Outcome-Driven Methodology:** Complete BVSSH-based system that amplifies team competency and teaches SDLC best practices through conversation

2. **7 Specialized Agents, One Interface:** Single conversational experience orchestrating expert agents behind the scenes

3. **Intelligent Backfilling:** Jump to features? Agent recognizes missing Project/Initiative/Brief and backfills it automatically

4. **Opinionated Workflow:** **Project → Initiative → Epic → Feature → Story → Task hierarchy** prevents scope chaos and solves alignment issues *before* they become costly engineering problems

5. **Human-in-the-Loop:** Agents draft, humans review and approve—never fully autonomous

6. **Unified Three-Column Workspace:** Workflow navigator, live document preview, agent chat—all in one view

7. **RoadmapKO as System of Record (MVP Core):**
   - All planning artifacts stored and versioned in RoadmapKO
   - Single source of truth for project context and history
   - Export capabilities for integration with external tools
   - **Post-MVP:** Bi-directional sync with Linear, Jira, Notion, Azure Boards

---

### Technical Architecture

**Frontend:**
- **Next.js 14** (App Router, TypeScript, React Server Components)
- **Untitled UI** component library for professional, consistent design system
- **TipTap** for Notion-like markdown rendering in document preview
- **Turborepo** monorepo structure
- **Vercel** hosting for frontend

**Backend & AI Orchestration:**
- **CrewAI + FastAPI:** Multi-agent orchestration for all 7 specialized agents
- **Modal:** Serverless hosting for Python backend (CrewAI/FastAPI services)
- **Multi-Provider Access:** OpenRouter for unified LLM access across Anthropic, Google, OpenAI

**Database & Storage:**
- **Supabase:** PostgreSQL + pgvector (embeddings) + Realtime + Storage
- **Upstash Redis:** Serverless caching for performance optimization

**Memory & Knowledge Graph (Post-MVP Foundation):**
- **Under Evaluation:** Neo4j, Weaviate, or Cognee for:
  - Long-term agent memory across sessions
  - Knowledge graph relationships between artifacts
  - Business goal tracking and reporting (front-end)
  - Development, deployment, observability integration (tail-end)
- **Strategic Note:** Foundational infrastructure decisions made during MVP to support post-MVP evolution

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
- **Real-time:** Pusher/Ably for streaming agent progress updates

---

### Architecture Pattern

```
User → Vercel (Next.js Frontend)
         ↓
      Modal (CrewAI + FastAPI)
         ↓
      OpenRouter
         ├→ Anthropic (Claude Sonnet)
         ├→ Google (Gemini Flash)
         └→ OpenAI (GPT-4)
         ↓
      Supabase (PostgreSQL + pgvector)
      [Future: Neo4j/Weaviate/Cognee for memory & knowledge graph]
```

**Phase Transitions & Status Indicators:**
- UI shows phase context explicitly (Analysis Phase 75% → Planning Phase)
- Status updates show which agent is working ("PM - Product Manager Agent" working on "PRD → Functional Requirements")
- Human-like interactions for longer processes ("Based on the approved Project Brief, I'll now help you create the Product Requirements Document...")

---

### Why Now?

Four converging trends make RoadmapKO's approach possible and necessary:

**1. AI Agent Orchestration is Newly Viable**
- Multi-agent systems with tool use only became practical in 2024
- CrewAI and production-ready frameworks now mature
- LLM capabilities reached threshold for reliable document generation

**2. Remote Work Amplifies the Planning Gap**
- Distributed teams need better async documentation practices
- Ad-hoc hallway conversations no longer suffice
- Context preservation is critical when teams span timezones

**3. Distribution Channels Reach 800M+ Users**
- ChatGPT Apps SDK + Claude Desktop MCP provide zero-cost distribution
- No need to build marketplace presence from scratch
- Users already paying $200-250/mo for AI tools—RoadmapKO is additive value

**4. Market Maturity for Opinionated Tools**
- Teams are frustrated with legacy tools (Jira complexity, Notion chaos)
- Linear demonstrated success with opinionated, beautiful workflows
- Developers now comfortable with AI-assisted workflows (Cursor, Copilot adoption)

---

### Why This Will Succeed

- **Distribution Leverage:** ChatGPT Apps SDK (800M+ users), Claude Desktop MCP extension (post-MVP)
- **Complementary Positioning:** Not competing with execution tools—we generate the planning artifacts Linear/Jira require
- **Value-Based Pricing:** $49-149/mo is accessible and offers 10x+ ROI on time savings (7 days vs 30+ days)
- **Natural Learning:** Users absorb SDLC best practices through guided conversation
- **Managed Service:** Unlike open-source BMAD/SuperClaude, we provide hosted orchestration with zero setup
- **System of Record Architecture:** RoadmapKO maintains full project context, enabling future integrations without vendor lock-in

---

### High-Level Vision

Establish RoadmapKO as the essential **"Phase Zero" for all high-performance software teams**, with long-term goal of evolving into a fully autonomous, end-to-end platform that spans from business goal setting through deployment and observability.

---

## Target Users

### Market Overview & Total Addressable Market (TAM)

**Global Software Development Market:**
- **50,000+ solo developers/indie hackers** actively building SaaS products (GitHub, Indie Hackers, Product Hunt data)
- **200,000+ small dev teams** (2-10 people) at startups and agencies globally
- **500,000+ individual practitioners** (PMs, SMs, POs, EMs) at companies of all sizes
- **TAM Estimate:** ~750,000 potential users across all segments
- **Initial Focus:** Solo devs + small teams + individual practitioners = ~300,000 addressable in Year 1

---

### Primary Segment 1: Solo Developers & Indie Hackers

**Profile:**
- Individual developers building SaaS products
- 5-15 years experience, strong technical skills but limited PM/architecture training
- Often using AI coding assistants (Cursor, v0, Lovable, Bolt.new)
- **Representative User:** Sarah (from Problem Statement scenarios)

**Current Behaviors:**
- Jump straight into code without written requirements
- Keep context in head or scattered Notion docs
- Waste hours searching for "what was I building again?"

**Pain Points:**
- *"I should write a PRD, but it takes 8 hours I don't have"*
- Lose context on architectural decisions 6 months later
- Look unprofessional to investors/clients without proper documentation
- Backend architecture becomes an afterthought with visual dev tools

**Behavioral Triggers (When They Seek RoadmapKO):**
- Starting a new SaaS product from scratch
- Pivoting an existing product and need to re-plan
- Preparing for investor pitch and need professional documentation
- Onboarding a co-founder or first hire
- Switching from visual dev tools (Lovable, v0) to production-ready architecture

**Goals:**
- Ship faster with clear requirements
- Build planning habits without massive time investment
- Get view-by-view UX specs and component-level prompts optimized for AI coding tools

**Value Proposition:**
*"Never start from a blank page again—get project briefs, PRDs, and architecture docs in hours, not weeks"*

---

### Primary Segment 2A: Product Managers

**Profile:**
- PMs at startups, scale-ups, or agencies managing 2-5 products
- Responsible for translating business vision into product requirements
- Often working with limited resources and tight timelines
- **Representative User:** Marcus (from Problem Statement scenarios)

**Current Behaviors:**
- Manually draft PRDs from scratch in Google Docs or Notion
- Copy-paste previous project docs, struggle with consistency
- Spend 40-60% of time on documentation vs. strategic work
- Jump between 6+ tools to synthesize project context

**Pain Points:**
- *"I spend more time formatting docs than thinking strategically"*
- Inconsistent PRD quality across projects
- Lost context when switching between multiple products
- Difficulty maintaining single source of truth across tools

**Behavioral Triggers (When They Seek RoadmapKO):**
- New product kickoff or major feature initiative
- Executive team requests comprehensive project brief
- Onboarding new engineers who need clear requirements
- Mid-project when scope creep becomes unmanageable
- Quarterly planning cycles requiring multiple PRDs

**Goals:**
- Standardize planning process across all products
- Free up time for strategic product thinking
- Improve alignment between business and engineering
- Create documentation that developers actually use

**Value Proposition:**
*"Go from blank page to complete PRD in 2 hours instead of 2 days—with 7 AI agents handling the heavy lifting"*

---

### Primary Segment 2B: Scrum Masters

**Profile:**
- Scrum Masters at agile teams or digital agencies managing 3-10 projects
- Responsible for team velocity, process efficiency, and removing blockers
- Often inherit poorly-defined backlogs and fragmented documentation
- **Representative User:** Jennifer (from Problem Statement scenarios)

**Current Behaviors:**
- Spend 2 weeks in discovery meetings before every project kickoff
- Manually create user stories from vague requirements
- Constantly clarify scope during sprint planning
- Chase down documentation across multiple tools and people

**Pain Points:**
- *"Every project starts with 2 weeks of meetings just to understand scope"*
- Team velocity suffers due to unclear requirements
- 30-40% of sprint capacity lost to rework from poor planning
- Junior team members can't contribute to planning without extensive mentoring

**Behavioral Triggers (When They Seek RoadmapKO):**
- New client project kickoff (agencies)
- Inheriting a project with poor documentation
- Team complains about unclear stories during sprint planning
- Executive team demands faster project delivery
- Agency scaling beyond 3-5 concurrent projects

**Goals:**
- Reduce project kickoff time from weeks to days
- Standardize story creation across all projects
- Enable junior team members to draft stories independently
- Connect every story back to business context

**Value Proposition:**
*"10x faster client onboarding—generate standardized project briefs and story backlogs at $149/mo instead of 40 billable hours"*

---

### Primary Segment 2C: Product Owners

**Profile:**
- Product Owners responsible for backlog prioritization and business value
- Bridge between business stakeholders and development teams
- Often struggle with scope management and requirement clarity
- **Representative User:** Priya (from Problem Statement scenarios)

**Current Behaviors:**
- Write acceptance criteria that get misinterpreted by developers
- Re-explain requirements during sprint planning and reviews
- Manually track dependencies between epics and stories
- Answer "what did we mean by this?" questions constantly

**Pain Points:**
- *"I wrote it clearly, but everyone interpreted it differently"*
- Scope creep from unclear epic/story boundaries
- Lost traceability between business goals and implemented features
- Difficulty validating if development aligns with business objectives

**Behavioral Triggers (When They Seek RoadmapKO):**
- Major release planning requiring dozens of aligned stories
- Stakeholders question if development is on-track
- Team velocity drops due to constant requirement clarification
- Need to validate stories against PRD and architecture
- Quarterly OKR planning requiring project briefs

**Goals:**
- Ensure stories perfectly align with PRD and architecture
- Reduce requirement ambiguity to near-zero
- Maintain clear traceability from business goals to tasks
- Validate story drafts before sprint planning

**Value Proposition:**
*"Validation Agent ensures every story aligns with PRD and architecture—no more mid-sprint 'wait, what were we building?' moments"*

---

### Primary Segment 2D: Engineering Managers

**Profile:**
- Engineering Managers leading 5-15 person development teams
- Responsible for technical delivery, team capacity, and quality
- Frustrated by features that work technically but miss business goals
- **Representative User:** David (from Problem Statement scenarios)

**Current Behaviors:**
- Discover missing context after implementation begins
- Manage 47+ tech debt items with no systematic tracking
- Ask "what problem does this solve?" and get blank stares
- Balance feature velocity with technical quality

**Pain Points:**
- *"We ship features that work but don't solve the actual problem"*
- Lost context on "why" behind architectural decisions
- Tech debt accumulates because rationale isn't documented
- Onboarding new engineers takes 2-3 weeks due to fragmented docs

**Behavioral Triggers (When They Seek RoadmapKO):**
- New engineers joining team and needing comprehensive onboarding
- Major refactoring project requiring architecture documentation
- Executive team questions technical decisions made 6 months ago
- Planning capacity across multiple concurrent initiatives
- Tech debt review requiring understanding of original context

**Goals:**
- Preserve architectural decision records (ADRs) automatically
- Connect every technical decision to business context
- Enable engineers to understand "why" behind every story
- Reduce onboarding time from weeks to days

**Value Proposition:**
*"Architecture Agent documents every technical decision with business context—6 months later, your team still knows 'why'"*

---

### Secondary Segment: Business Stakeholders & Executives

**Profile:**
- C-suite and VPs at companies without strong PM function
- Non-technical founders who need to translate vision into tech requirements
- Organizations where PM quality varies wildly by individual
- **Representative User:** Alex (from Problem Statement scenarios)

**Current Behaviors:**
- Approve large budgets without clear understanding of scope
- Attend weekly status meetings but can't answer "what are we building?"
- Discover scope changes after significant budget is spent
- Struggle to evaluate ROI on technology investments

**Pain Points:**
- *"I approved $500K but don't know if we're on track"*
- Need predictability and clear view of ROI from tech investments
- Unpredictable outcomes due to inconsistent planning competency
- Can't evaluate if development is aligned with business objectives

**Behavioral Triggers (When They Seek RoadmapKO):**
- Board meeting requiring project status and ROI justification
- Major budget approval requiring comprehensive project brief
- Technology investment underperforming expectations
- New product initiative requiring cross-functional alignment
- Scaling company beyond "founder knows everything" phase

**Goals:**
- Amplify team competency without expensive PM hires
- Learn SDLC best practices through guided process
- Get transparency into "what are we actually building?"
- Ensure technology investments align with business strategy

**Value Proposition:**
*"Democratize world-class PM competency—embedded methodology ensures consistent, outcome-driven planning across all projects"*

---

### Tertiary Segment: Visual/No-Code Developers

**Profile:**
- Developers using Lovable, v0, Base 44, Bolt.new for rapid UI development
- Strong front-end skills but need structured backend planning
- Build beautiful interfaces that lack proper integration planning
- **Representative User:** Chris (from Problem Statement scenarios)

**Current Behaviors:**
- Generate beautiful components in minutes with AI tools
- Hit integration wall when connecting to backend
- Spend more time fixing integration issues than building features
- Lack clear UX specs and backend requirements

**Pain Points:**
- *"I can build it fast, but what should it actually do?"*
- Garbage in = garbage out with AI coding tools
- Backend architecture becomes afterthought
- No structured handoff between UX and implementation

**Behavioral Triggers (When They Seek RoadmapKO):**
- Starting new project with visual dev tools
- Integration issues pile up due to unclear backend requirements
- Client requests comprehensive documentation for handoff
- Scaling beyond prototype to production-ready application

**Goals:**
- Get component-level prompts optimized for Lovable/v0
- Clear UX specs that map to backend architecture
- Structured workflow that prevents integration issues

**Value Proposition:**
*"Design Agent generates component-level prompts optimized for Lovable/v0—perfect UX specs that integrate seamlessly with backend architecture"*

---

### Expansion Segments (Post-MVP)

**ChatGPT/Claude Desktop Users**
- Unstructured planners with 50+ conversations about one project
- Distribution via ChatGPT Apps SDK, Claude Desktop MCP
- **Trigger:** Frustrated by scattered planning conversations, need structure

**BMAD Method Enthusiasts**
- Love the methodology but don't want DIY setup
- Managed service positioning
- **Trigger:** Seeking production-ready BMAD implementation

**Linear/Jira Users at Mid-Size Teams**
- Requires integrations first (system-of-record architecture enables this)
- Teams of 10-50 people seeking better front-half planning
- **Trigger:** Execution tool has great stories but unclear upstream context

---

## Goals & Success Metrics

### Business Objectives

1. **Launch MVP and acquire first 20 paying customers within 3 months of launch**
2. **Achieve $60K MRR ($720K ARR) by end of Year 1** with 500 paying customers
3. **Reach break-even by Month 9**
4. **Secure 10 enterprise customers ($499/mo tier) by Month 12**
5. **Product Hunt #1 Product of the Day** at launch
6. **Maintain <$500 Customer Acquisition Cost** (CAC)

### User Success Metrics

- **Planning Speed:** Users complete planning in **7 days or less** (vs. 30+ days manual) = **50%+ time reduction**
- **Document Quality:** **80%+ approval rate** on agent-drafted documents
- **Activation:** **70% of new users complete first project within 30 days**
- **Engagement:** Active users create **3-5 projects per month**
- **Satisfaction:** Maintain **Net Promoter Score (NPS) of 50+**
- **Trial Conversion:** **5%+ conversion rate** from free trial to paid subscription

### Key Performance Indicators (KPIs) by Phase

**MVP Success (Month 3):**
- **20 paying customers** = $1.5-2K MRR
- **400 total trial signups** (5% conversion rate = 20 paying)
- **80%+ document approval rate**
- Users complete full projects in **<7 days avg time**
- **NPS of 40+** from early users

**Phase 1.0 - ChatGPT Apps SDK Distribution (Month 5):**
- **50 paying customers** = $5-8K MRR (cumulative from MVP + Phase 1.0)
- **1,000+ total trials** (500+ from ChatGPT Apps SDK)
- Maintain **5%+ trial-to-paid conversion**
- **60%+ monthly retention** (Month 1 → Month 2 cohort)

**Phase 1.5 - Claude Desktop MCP Integration (Month 7):**
- **100 paying customers** = $10-12K MRR (cumulative)
- **2,000+ total trials** (200+ from Claude Desktop MCP)
- **60%+ monthly retention** maintained
- Multiple distribution channels validated

**Year 1 Target (Month 12):**
- **500 paying customers** = $60K+ MRR ($720K ARR)
- **10,000+ total trials** across all channels
- **80%+ annual retention rate**
- **LTV:CAC ratio of 3:1 or better**
- **10 enterprise customers** ($499/mo tier)

---

### Post-MVP Success Metrics (Deferred)

The following advanced metrics will be tracked after MVP launch to optimize product-market fit and growth:

**Agent-Specific Performance:**
- Approval rates by individual agent (Discovery, Requirements, Design, Architecture, Quality, Validation, Planning)
- Most/least valuable agents per user segment
- Agent interaction patterns and workflow completion rates

**Segment-Specific Conversion:**
- Conversion rates by persona (solo devs, PMs, SMs, POs, EMs, agencies)
- Segment-specific pricing tier preference
- Customer lifetime value (LTV) by segment

**Usage Depth Tracking:**
- Workflow stage completion rates (Discovery only vs. full Planning phase)
- Document types generated per project
- Feature adoption by tier (Starter vs. Professional vs. Enterprise)

**Cohort Retention Analysis:**
- Monthly retention by cohort (Month 1, 2, 3, etc.)
- Churn reasons by segment and tier
- Reactivation rates for churned users

**Distribution Channel Performance:**
- CAC by channel (Product Hunt, ChatGPT Apps, Claude MCP, organic, paid)
- Conversion rate by channel
- Channel-specific LTV and retention

---

## MVP Scope

### MVP Definition

**Agent-first approach:** 7 specialized AI agents (1 Discovery + 6 Planning) with web UI featuring three-column workspace, Project Brief generation, markdown export, 7-day free trial (limited to 1 Initiative with 1 Project Brief only), Stripe payment integration.

---

### Core Features (Must Have)

**1. Three-Column Workspace UI**

**Left Column:** Project selector + Initiative Workflow Navigator
- Project dropdown (e.g., "E-Commerce Platform MVP")
- Collapsible workflow stages (Discovery & Research, Product Definition, Design & Architecture, Validation & Handoff)
- Document hierarchy with approval status indicators

**Middle Column:** Live document preview
- Document title, version, status display
- Real-time progress indicators
- Notion-like markdown rendering (TipTap)
- Approval badges and section status

**Right Column:** Agent chat interface
- Active agent display with avatar and activity
- Chat-style interaction with numbered elicitation options (1-9)
- Agent message history
- "Previous Agents" and "View All Chats" navigation

---

**2. Seven Specialized AI Agents (Two-Phase Workflow)**

**PHASE 1: ANALYSIS & DISCOVERY**

**Discovery Agent (Business Analyst)**
- *Persona:* Analytical, curious, enthusiastic researcher
- *Abilities:* Brainstorming, market research, competitor analysis, project brief creation

**PHASE 2: PLANNING & EXECUTION READINESS**

**Requirements Agent (Product Manager)**
- *Persona:* Structured, pragmatic, collaborative PM
- *Abilities:* Create PRD from Brief (Fast Track), Interactive PRD Creation (detailed elicitation)

**Design Agent (UX Expert)**
- *Persona:* Creative, empathetic, user-focused UX designer
- *Abilities:* Create front-end specifications, generate UI prompts for Lovable/v0/Cursor, design component-level requirements

**Architecture Agent (Architect)**
- *Persona:* Systematic, detail-oriented, scalability-focused architect
- *Abilities:* Create architecture from PRD + UX Spec, design data models and tech stack recommendations

**Quality Agent (Quality Assurance)**
- *Persona:* Meticulous, proactive, quality-obsessed QA lead
- *Abilities:* Early test architecture input on high-risk areas, risk assessment on draft stories, test strategy and risk profile creation

**Validation Agent (Product Owner)**
- *Persona:* Strategic, decisive, business-focused PO
- *Abilities:* Run master checklist (PRD and User Story), update epics & stories, shard documents, validate story drafts against PRD and architecture

**Planning Agent (Scrum Master)**
- *Persona:* Organized, practical, delivery-focused Scrum Master
- *Abilities:* Review previous story dev/QA notes, draft next story from sharded epic + architecture, maintain workflow continuity

---

**3. Document Generation (MVP Scope)**

**Included in MVP:**

**Project Brief** (complete document with all sections):
- Executive Summary
- Problem Statement
- Proposed Solution
- Target Users
- Goals & Success Metrics
- MVP Scope
- Technical Considerations
- Constraints & Assumptions
- Risks & Open Questions
- Next Steps

**Available for Paid Tiers Only:**
- Product Requirements Document (PRD)
- Front-End Specification (UX)
- Architecture Document
- Test Strategy & QA Plan
- Epic & Story Generation
- Validation Checklists

---

**4. Workflow & Hierarchy Management**

- **Hierarchy Structure:** Project → Initiative → Epic → Feature → Story → Task
- **MVP Supports:** Project (with Brief) → Initiative (structure only, locked)
- **Paid Tiers Support:** Full hierarchy with Epic/Feature/Story/Task
- Create, navigate, edit, delete/archive initiatives and projects
- Version control and document history
- Approval workflow (draft → awaiting elicitation → approved)

---

**5. Workflow Navigator & Status Indicators**

- **Mode Toggle:** Interactive vs. YOLO mode (#yolo to toggle)
- **Phase Display:** Shows current workflow phase (e.g., "Discovery & Research - COMPLETE")
- **Progress Tracking:** Percentage complete with time estimates (e.g., "Planning: 35%, ~45 min remaining")
- **Active Agent Display:** Shows which agent is currently working (e.g., "PM - Product Manager Agent")
- **Status Badges:** Complete (✓), In Progress (⏳), Locked (🔒), Awaiting Elicitation (⚠️), Not Started (○)

---

**6. Export Capabilities**

**Free Trial:**
- View-only (no export)

**Paid Tiers:**
- **Markdown export:** Single file per document (e.g., `project-brief.md`, `prd.md`, `architecture.md`)
- **Per-document export:** Download individual documents
- **Future (Post-MVP):** Bulk export as zip archive, GitHub-ready folder structure

---

**7. Authentication & Payment**

- **Clerk:** Email/password, Google OAuth, GitHub OAuth
- **Stripe:** Subscription management (Starter $49, Professional $149, Enterprise $499)
- **Usage Credits:** Track and enforce credit limits per tier
- **Billing Portal:** Self-service subscription management

---

### 7-Day Free Trial Limits

- **1 Initiative only**
- **1 Project Brief only** (Discovery Agent access only)
- **View-only:** No export capabilities
- **No access to:** PRD, Architecture, UX Specs, QA Plans, Epics/Stories, or Planning Phase agents (Requirements, Design, Architecture, Quality, Validation, Planning)
- **Conversion Gate:** Must upgrade to paid tier to access Planning Phase agents and full document suite

---

### Out of Scope for MVP (Deferred to Post-MVP)

**Phase 1.0+ (Month 4-5):**
- ChatGPT Apps SDK distribution
- Claude Desktop MCP extension
- Adaptive approval buttons (context-aware CTA suggestions)
- Voice-to-text input
- **Gamification** (confetti animations, achievement badges, progress celebrations)

**Phase 1.5+ (Month 6-7):**
- Freemium tier (indefinitely free with limited features)
- Advanced elicitation methods (Tree of Thoughts, Red Team/Blue Team)
- Custom agent training on company-specific workflows

**Phase 2.0+ (Month 8-10):**
- Linear/Jira/Notion/Azure Boards bi-directional sync
- Real-time collaboration (multiple users editing simultaneously)
- Cascading change management (update PRD → auto-update affected stories)
- Advanced UI features:
  - Collapsible panels with saved preferences
  - Detail cards and hover previews
  - Keyboard shortcuts (Cmd+K command palette)
  - Canvas visualization (mind map view of project hierarchy)

**Long-Term (Year 2+):**
- **Execution Features:**
  - Triage Inbox for issue management
  - Cycles for sprint planning
  - Git Integration for code-to-planning linkage
- **Analytics & Collaboration:**
  - Core Analytics dashboard (velocity, burndown, cycle time)
  - Slack Integration for notifications
  - Team activity feeds
- **Pillar 3 (Full DevOps & Observability):**
  - Performance-to-ROI Mapping
  - Intelligent Defect Prevention
  - Automated deployment orchestration
  - Observability integration (Sentry, DataDog, etc.)

---

### Technical Architecture (MVP)

**Frontend:**
- **Next.js 14** (App Router, TypeScript, React Server Components)
- **Untitled UI** component library for professional, consistent design system
- **TipTap** for Notion-like markdown rendering in document preview
- **Turborepo** monorepo structure
- **Vercel** hosting for frontend

**Backend & AI Orchestration:**
- **CrewAI + FastAPI:** Multi-agent orchestration for all 7 specialized agents
- **Modal:** Serverless hosting for Python backend (CrewAI/FastAPI services)
- **Multi-Provider Access:** OpenRouter for unified LLM access across Anthropic, Google, OpenAI

**Database & Storage:**
- **Supabase:** PostgreSQL + pgvector (embeddings) + Realtime + Storage
- **Upstash Redis:** Serverless caching for performance optimization

**Supporting Services:**
- **Auth:** Clerk (email/password, Google OAuth, GitHub OAuth)
- **Payment:** Stripe (subscriptions + usage-based pricing)
- **Email:** Resend (React Email templates)
- **Analytics:** PostHog (product analytics + feature flags)
- **Monitoring:** Sentry (error tracking), Langfuse (LLM observability)
- **Real-time:** Pusher/Ably for streaming agent progress updates

---

### Notes for PRD Development Phase

**Discovery Agent Workflow Clarification:**
- **Phase 1: Analysis & Discovery** includes three business-focused activities within the Discovery Agent:
  1. **Brainstorming** - Ideation and concept exploration
  2. **Market Research** - Market analysis and opportunity validation
  3. **Competitor Analysis** - Competitive landscape assessment
  4. **Project Brief Creation** - Synthesis of above into comprehensive brief

**Document Type Specification:**
- Specific PRD sections, Architecture sections, UX Spec sections, and QA Plan sections will be defined during **PRD creation phase** with the Requirements Agent
- Each document template structure to be determined collaboratively based on BVSSH methodology

---

### MVP Success Criteria

- **20 paying customers** using web UI consistently
- **80%+ approval rate** on Discovery Agent-drafted Project Briefs
- Users **complete Project Brief in <2 hours** (vs. 8+ hours manual)
- **Trial-to-paid conversion:** 5%+ (400 trials → 20 paying)
- **NPS of 40+** from early users
- **<$500 CAC** through organic channels (Product Hunt, dev communities)

---

## Post-MVP Vision

### Phase 1.0: ChatGPT Apps SDK Integration (Month 4-5)

**Goal:** Tap into 800M+ ChatGPT user base for distribution

**Features:**
- ChatGPT App exposing RoadmapKO agent as native capability
- "Start planning a new project" → immediate agent conversation
- Seamless handoff to web UI for full workspace experience
- **Gamification:** Confetti animations, achievement badges, progress celebrations
- **Adaptive approval buttons:** Context-aware CTA suggestions
- **Voice-to-text input:** Conversational planning via voice

**Success Metrics:**
- **500+ trial signups** via ChatGPT Apps
- **50 paying customers** = $5-8K MRR (cumulative from MVP + Phase 1.0)
- **Featured in ChatGPT Apps Store**
- **Maintain 5%+ trial-to-paid conversion**

---

### Phase 1.5: Claude Desktop MCP Integration (Month 6-7)

**Goal:** Secondary distribution via Claude Desktop users

**Features:**
- MCP server exposing RoadmapKO agents as Claude Desktop tools
- Local-first workflows for privacy-conscious users
- Multi-provider distribution strategy (reduces platform risk)
- **Freemium tier:** Indefinitely free with limited features (1 Project, Brief only, no export)

**Success Metrics:**
- **200+ trial signups** via Claude Desktop MCP
- **100 paying customers** = $10-12K MRR (cumulative)
- **60%+ monthly retention** (Month 1 → Month 2 cohort)
- **Multiple distribution channels validated**

---

### Phase 2.0: Linear/Jira/Notion Integrations (Month 8-10)

**Goal:** Enable bi-directional sync with execution tools

**Features:**
- **Bi-Directional Sync Architecture:**
  - **Create new artifacts in RoadmapKO** and push to Linear, Jira, Notion, Azure Boards simultaneously
  - **RoadmapKO is always system of record** for planning artifacts
  - Platform migration safety (full project history preserved in RoadmapKO)
  - Sync status indicators and conflict resolution
- **Full Workflow Hierarchy:** Initiative → Epic → Feature → Story → Task (beyond Project + Initiative from MVP)
- **Advanced UI Features:**
  - Collapsible panels with saved preferences
  - Detail cards and hover previews
  - Keyboard shortcuts (Cmd+K command palette)
  - Canvas visualization (mind map view of project hierarchy)
- **Fully interactive 'Living Roadmap'** with drill-down modals
- **Advanced analytics dashboard** (velocity, burndown, cycle time)

**Success Metrics:**
- **Mid-size teams (10-50 people)** adopt RoadmapKO
- **3 integrations live:** Linear, Jira, Notion
- **Unlock expansion** to Linear/Jira Users segment
- **250 paying customers** = $30K+ MRR

---

### Long-Term Vision (Year 2+)

**Phase 3+: Evolve into Fully Autonomous Platform**

**1. Pillar 3: Full DevOps & Observability Automation**
- **Performance-to-ROI Mapping:** Link application performance metrics to business outcomes
- **Intelligent Defect Prevention:** AI-driven quality predictions based on planning artifacts
- **Automated deployment orchestration:** From story completion to production deployment
- **Observability integration:** Sentry, DataDog, New Relic linkage to planning context

**2. Execution Features (Compete with Linear)**
- **Triage Inbox:** Intelligent issue prioritization and assignment
- **Cycles:** Sprint planning and velocity tracking
- **Git Integration:** Code commits linked to stories and tasks
- **Real-time collaboration:** Multiple users editing simultaneously
- **Cascading change management:** Update PRD → auto-update affected stories

**3. Advanced Collaboration & Analytics**
- **Core Analytics dashboard:** Team velocity, burndown charts, cycle time analysis
- **Slack Integration:** Notifications and slash commands
- **Team activity feeds:** Real-time updates on planning activity
- **Advanced elicitation methods:** Tree of Thoughts, Red Team/Blue Team, Stakeholder Round Table

**4. Vertical-Specific Templates**
- **SaaS startups:** Pre-built templates for auth, payments, onboarding, multi-tenancy
- **E-commerce:** Product catalogs, checkout flows, inventory management, fulfillment
- **Fintech:** Compliance-aware templates with built-in security/audit requirements
- **Healthcare:** HIPAA-compliant templates with privacy-by-design patterns

**5. White-Label for Agencies**
- **Custom branding:** Agency logos, colors, and domain names
- **Multi-tenant client management:** Separate workspaces per client
- **Revenue sharing model:** Partner program for resellers
- **Client billing integration:** Pass-through or markup pricing

---

### Agent & Workflow Availability by Phase

**MVP (Month 3):**
- **Free Trial:** Discovery Agent only, Project Brief at Project level
- **Paid Tiers:** All 7 agents (Discovery, Requirements, Design, Architecture, Quality, Validation, Planning)
- **Hierarchy:** Project (with Brief) → Initiative (planned but locked)

**Phase 1.0 (Month 5):**
- **Paid Tiers:** Full Initiative → Epic workflow unlocked
- **Document Types:** Project Brief, PRD, Epic definitions

**Phase 2.0 (Month 10):**
- **Paid Tiers:** Full hierarchy unlocked (Project → Initiative → Epic → Feature → Story → Task)
- **Document Types:** All planning artifacts through Story and Task level
- **Integration:** Push to Linear/Jira/Notion

---

### Expansion Opportunities

**Market Evolution:**
- After mastering the "front-half," expand to compete directly with Linear on execution (Year 2+)
- Position for potential strategic acquisition by Atlassian, Linear, Notion, or Microsoft

**Competitive Moat:**
- **Network effects:** More tools integrate → more valuable for users
- **Switching costs:** RoadmapKO contains institutional knowledge spanning years of projects
- **Data moat:** Millions of planning documents train better agents over time
- **Distribution leverage:** ChatGPT Apps SDK + Claude MCP reach 800M+ users with zero acquisition cost

**Revenue Expansion:**
- **Vertical-specific templates** (Year 2): $199/mo tier for industry templates
- **White-label for agencies** (Year 2): $499-999/mo with revenue sharing
- **Enterprise tier with custom agents** ($999-1,499/mo): Company-specific workflow training

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
- Untitled UI component library + Tailwind CSS
- TipTap for Notion-like markdown rendering
- Turborepo monorepo structure
- Vercel hosting

**Backend & AI Orchestration:**
- **CrewAI + FastAPI:** Multi-agent orchestration for complex workflows
- **Modal:** Serverless Python backend hosting
- **Multi-Provider Access:** OpenRouter for unified LLM access across Anthropic, OpenAI, Google, Groq, Fireworks

**Database & Storage:**
- **Supabase:** PostgreSQL + pgvector (embeddings) + Realtime + Storage
- **Upstash Redis:** Serverless caching
- **Cloudflare R2:** Zero egress for document exports

**AI Models (Multi-Model Strategy):**

| Agent | Primary Model | Cost per 1M Tokens |
|-------|--------------|-------------------|\
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
User → Vercel (Next.js) → Modal (CrewAI + FastAPI)
                            ↓
                        OpenRouter
                            ├→ Anthropic (Claude)
                            ├→ Google (Gemini)
                            └→ OpenAI (GPT-4)
                            ↓
                        Supabase (PostgreSQL + pgvector)
```

**Rationale:**
- **Cost optimization:** Use cheap Gemini Flash for Discovery/QA, expensive Claude Sonnet only for critical planning
- **Flexibility:** OpenRouter provides unified access to 100+ models with automatic failover
- **Scalability:** Serverless-first architecture with zero fixed infrastructure costs
- **Performance:** CrewAI on Modal provides powerful orchestration for complex multi-agent workflows

---

### Repository Structure (Turborepo Monorepo)

```
roadmap-ko/
├── apps/
│   ├── web/                 # Next.js web app (MVP)
│   ├── chatgpt-app/         # ChatGPT Apps SDK (Phase 1.0)
│   └── mcp-server/          # Claude Desktop MCP (Phase 1.5)
├── packages/
│   ├── ui/                  # Shared Untitled UI components
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
- Modal: $0-30 (serverless Python backend)
- Supabase: $0-25
- Clerk: $0
- OpenRouter (AI models): $20-50
- Resend (email): $20
- Dev tools (PostHog, Sentry, Langfuse): $220
- **Total: ~$260-365/mo**

**Gross Margin at Scale:** 90-95% (SaaS model with minimal marginal costs, multi-model strategy keeps LLM costs at 10-15% of revenue)

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

Credit-based model aligned with **Lovable pricing strategy** drives higher revenue than pure fixed tiers.

---

### Pricing Tiers

**Free Trial: $0**
- 7-day trial (then pauses)
- 1 Initiative, 1 Project Brief only (Discovery Agent access only)
- No export capabilities
- Community support

---

**Starter: $49/month** ($470/year - save $118)

*Target: Solo developers, indie hackers*

- 3 Initiatives per month
- All 7 agents (Discovery, Requirements, Design, Architecture, Quality, Validation, Planning)
- All document types (Project Brief, PRD, Architecture, UX, Security, QA)
- Full hierarchy navigation (Project → Initiative → Epic)
- Markdown export (single file per document)
- 25 usage credits/month
- Email support (48-hour SLA)
- **Overage:** $5 per Initiative, $0.50 per credit

---

**Professional: $149/month** ($1,430/year - save $358)

*Target: Small dev teams, digital agencies*

- **Unlimited Initiatives**
- All 7 agents
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

- **Development Costs:** $260-365/mo (MVP), $770-1,070/mo (Month 6 at 150 customers)
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

- **Modal:** Serverless Python execution with per-request pricing
- **Vercel:** 10s timeout (Hobby/Pro tiers), 300s (Enterprise tier)
- **Supabase Free Tier:** 500MB database, 2GB bandwidth; Pro tier: 8GB database, 250GB bandwidth
- **OpenRouter Rate Limits:** Model-dependent, typically 60-100 req/min
- **LLM API Quotas:** Default $1K/month, can request increases

### Key Assumptions

**Product Assumptions:**
- **BVSSH/BMAD methodology can be successfully productized** into guided AI workflows
- **AI agents can achieve 80%+ approval rate** on generated documents with proper prompt engineering
- **Users want opinionated workflow** over maximum flexibility
- **Current AI agent frameworks (CrewAI) are mature enough** for production use

**Market Assumptions:**
- **Solo dev market is large enough** (50K+ globally actively building SaaS)
- **Users will pay $49-149/mo** for planning automation (10x ROI on time saved)
- **Credit-based model drives higher revenue** than pure fixed tiers (aligned with Lovable pricing strategy)
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
- **OpenRouter vs. direct LLM provider APIs?**
- **Neo4j vs. Weaviate vs. Cognee for knowledge graph?**

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
- Multi-agent frameworks (CrewAI) production-ready as of 2024
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
- CrewAI multi-agent orchestration guides
- OpenRouter API documentation
- Supabase architecture best practices
- Modal serverless Python hosting docs

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
   - **Initialize CrewAI + FastAPI on Modal architecture**

---

### Month 1-3: MVP Development (12 Weeks)

**Week 1-2: Foundation**
- Turborepo setup with apps/web, services/crewai-api, packages
- Supabase schema: users, projects, initiatives, documents, agents, credits
- Clerk authentication + Stripe payment integration
- Three-column workspace UI skeleton (Untitled UI + TipTap)

**Week 3-4: Agent Orchestration**
- **CrewAI orchestration layer on Modal + OpenRouter integration**
- Agent status indicators and phase transitions
- Multi-model routing (Gemini Flash vs Claude Sonnet)

**Week 5-6: Discovery Agent (Analysis Phase)**
- Discovery agent (Business Analyst persona)
- Brainstorming workflows
- Market research capabilities
- Competitive analysis workflows
- **Project Brief generation** (complete document with all sections)

**Week 7-8: Planning Phase Agents (Part 1)**
- Requirements agent (PM - PRD generation)
- Design agent (UX - front-end specs, Lovable/v0 prompts)
- Architecture agent (tech stack, data models)

**Week 9-10: Planning Phase Agents (Part 2)**
- Quality agent (QA - test strategy, risk assessment)
- Validation agent (PO - master checklist, story validation)
- Planning agent (SM - story drafting, workflow continuity)
- Hierarchy management (Project → Initiative structure)

**Week 11-12: MVP Polish & Private Beta**
- Design partner onboarding (10 users)
- Approval rate monitoring (target: 80%+)
- Bug fixes and UX refinements
- Self-service docs (Mintlify)
- **Single-file markdown export** per document

**MVP Success Gate:** 80%+ approval rate on Project Briefs, <2 hours avg completion time, NPS 40+ before public launch

---

### Month 4-5: Phase 1.0 - ChatGPT Apps SDK

- Build ChatGPT App exposing RoadmapKO agent
- "Start planning a new project" → immediate conversation
- Seamless handoff to web UI for full workspace
- **Gamification:** Confetti, badges, progress celebrations
- **Goal:** 500+ trial signups, 50 paying customers total, Product Hunt #1

---

### Month 6-7: Phase 1.5 - Claude Desktop MCP

- Build MCP server exposing RoadmapKO agents as Claude Desktop tools
- Local-first workflows for privacy-conscious users
- **Freemium tier launch**
- **Goal:** 200+ trial signups, 100 paying customers total, 60%+ retention

---

### Month 8-10: Phase 2.0 - Linear/Jira/Notion Integrations

- Bi-directional sync architecture implementation
- Create new in both systems simultaneously (RoadmapKO = system of record)
- **Full hierarchy unlocked:** Initiative → Epic → Feature → Story → Task
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

This **Project Brief for RoadmapKO** is now complete and ready for Product Requirements Document (PRD) development.

**Brief Summary:**
RoadmapKO is an AI-native SaaS platform that masters the "front-half" of the software development lifecycle, guiding teams from raw ideas to developer-ready backlogs using 7 specialized AI agents (Discovery, Requirements, Design, Architecture, Quality, Validation, Planning) working through a unified three-column workspace interface.

**Key Decisions Made:**
- **Product Positioning:** "Masters the front-half of SDLC" + complementary to Linear/Jira
- **Target Market:** Equal emphasis on solo developers AND modern software teams (PMs, SMs, POs, EMs)
- **7 Agents:** Discovery (Phase 1) + Requirements, Design, Architecture, Quality, Validation, Planning (Phase 2)
- **Hierarchy:** Project → Initiative → Epic → Feature → Story → Task
- **MVP Scope:** All 7 agents available to paid users; free trial = 1 Project Brief only
- **Pricing:** Starter $49, Professional $149, Enterprise $499 with usage credits (Lovable pricing model)
- **Tech Stack:** CrewAI + FastAPI on Modal → OpenRouter, Next.js on Vercel, Untitled UI, Supabase
- **Distribution:** Standalone web (MVP) → ChatGPT Apps (Phase 1.0) → Claude MCP (Phase 1.5) → Integrations (Phase 2.0)

**Next Phase:** Please start in **'PRD Generation Mode'**, review the brief thoroughly, and work with the user to create the PRD section by section as the template indicates, asking for any necessary clarification or suggesting improvements.

---

**End of Project Brief**

*Version 2.0 - Refined by Mary (Business Analyst Agent) - 2025-11-30*
