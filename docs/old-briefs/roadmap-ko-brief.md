### **Executive Summary**

**Product Concept:** RoadmapKO is an AI-native SDLC orchestration platform that transforms raw business ideas into execution-ready backlogs through 7 specialized AI agents that think like your best PM, architect, and QA lead. It serves dual audiences: **human teams** who need comprehensive planning documentation (briefs, PRDs, architecture, user stories), and **AI coding assistants** (Cursor, Windsurf, Claude Code, VS Code Copilot, Codex CLI, Gemini CLI) that need full strategic context to write better code, update task status, and collaborate autonomously. RoadmapKO becomes the single source of truth that both humans and AI agents read from and write to—creating a seamless bridge between high-level strategic planning and AI-powered execution. Post-MVP, RoadmapKO will support brownfield migration, allowing teams with existing projects to import, update, and course-correct their documentation within the system rather than starting from scratch.

**Primary Problem:** Software teams—and increasingly, AI coding assistants—jump straight into execution without establishing strategic context. This creates disconnected artifacts scattered across Notion, Google Docs, Confluence, and Azure Boards, leading to lost context over time, miscommunication between business and engineering, and costly rework when implementation discovers requirement gaps. AI coding tools can generate code brilliantly but lack the "why" behind architectural decisions, acceptance criteria, and business objectives—resulting in context-blind suggestions that create technical debt. The result: wasted R&D spending, scope creep, and failed projects.

**Who This Serves:**

*Persona 1: The Overwhelmed Product Owner*
Sarah leads an AI-native engineering team that ships features fast using Cursor and Claude Code. But her developers constantly ask "What's the business context?" and "Why did we choose this architecture?" She spends 15+ hours/week answering questions and updating fragmented documentation across Notion, Jira, and Confluence. She needs a system that captures strategic context once and makes it accessible to both her human team and their AI coding tools.

*Persona 2: The Ambitious Vibe Coder*
Marcus is an indie SaaS builder who uses Cursor to prototype quickly. He's built 3 successful POCs but struggles to scale them into production-ready applications. Without a PM or architect, he lacks structured planning—his projects have unclear requirements, no architectural documentation, and mounting technical debt. He needs opinionated workflows that guide him from idea to enterprise-ready backlog without hiring a full team.

*Persona 3: The AI-Native Engineer Without Context*
Priya is a senior engineer on a distributed team using Windsurf and Claude Code CLI. She's efficient at building features but frequently discovers misaligned requirements mid-sprint because PRDs are outdated or missing. Her AI tools generate code based on incomplete context, requiring costly refactoring. She needs a system where planning artifacts stay synchronized and her AI assistants can reference up-to-date architectural decisions, acceptance criteria, and technical constraints.

**Target Market:**
- **Primary:** Solo developers, indie hackers, indie SaaS builders, startup founders, and vibe coders (2-10 person teams) who use AI coding assistants daily but struggle to provide sufficient context—lacking dedicated PMs, architects, or structured planning workflows
- **Secondary:** Enterprise software teams (PMs, EMs, AI-native engineering leads) at high-velocity startups who want to standardize planning practices, reduce documentation overhead, and enable AI-assisted development with full context
- **Tertiary:** Digital agencies managing multiple client projects that require consistent, repeatable documentation processes and want to leverage AI coding tools safely across client codebases

**Key Value Proposition:** RoadmapKO enforces a proven Initiative → Epic → Feature → Story → Task hierarchy through intelligent AI agents that recognize documentation gaps and automatically backfill missing artifacts. Unlike freeform tools (Notion, Confluence) that provide no guidance, or rigid execution tools (Linear, Jira, Azure Boards) that assume planning is already done, RoadmapKO provides opinionated, best-practice workflows with human-in-the-loop approval gates. **Critically, RoadmapKO makes its complete planning context available to AI coding assistants through modern integration protocols**, allowing tools like Cursor, Claude Code, and Windsurf to access architectural decisions, acceptance criteria, and technical constraints when generating code—then report back task completion, implementation notes, and code references. Humans and AI agents collaborate on the same canvas, ensuring no one (human or machine) ever starts from a blank page.

---

### **Problem Statement**

#### **Current State: The Planning Gap in the AI-Native Era**

Software development has entered a new paradigm: AI coding assistants can now generate entire applications from prompts. Yet a critical bottleneck remains—these tools are only as good as the context they receive. Meanwhile, human teams continue to struggle with the same fundamental planning problems that have plagued software development for decades, now amplified by the velocity and expectations of AI-assisted development.

**The Core Problem:** Teams skip strategic planning and jump directly into execution tools (Linear, Jira, Azure Boards) or AI coding assistants (Cursor, Windsurf, Claude Code) without establishing foundational context. This creates three compounding failure modes:

**Pain Point 1: Disconnected Artifacts & Lost Context**
- Market research lives in Notion, PRDs in Google Docs, architecture decisions in Confluence, stories in Linear, and code comments scattered across repositories
- Six months into development, no one remembers *why* critical architectural decisions were made
- New team members face an onboarding nightmare—fragmented documentation across 5+ tools with no clear narrative thread
- AI coding assistants operate in the dark, unable to access strategic context, leading to code that compiles but misses business objectives

**Pain Point 2: Context-Blind AI Development**
- Vibe coders achieve rapid POC development with AI tools but struggle to scale to production-ready applications
- AI assistants generate technically sound code based on immediate prompts but lack awareness of:
  - Business objectives and success metrics
  - Architectural constraints and patterns
  - Cross-feature dependencies and integration points
  - Security, accessibility, and compliance requirements
- Engineering teams waste cycles refactoring AI-generated code that didn't account for enterprise requirements
- Product Owners spend 10-15 hours/week answering "why" questions that should be documented once and accessible always

**Pain Point 3: Scope Creep & Reactive Planning**
- Without clear Initiative/Epic boundaries, features get added reactively without strategic evaluation
- Requirements emerge mid-sprint, forcing costly backtracking and rework
- "Just build it and see" mentality leads to technical debt accumulation
- Teams lack a structured approach to evaluate new feature requests against strategic goals

#### **Quantified Impact**

The cost of poor planning is substantial and well-documented:

- **Project Failure Rate:** The Standish Group reports that 70% of software projects fail due to poor requirements and planning
- **Time Waste:** Average teams spend 8-12 hours per week searching for context across documentation silos (McKinsey Digital)
- **Rework Costs:** Digital agencies report 30-40% of billable hours lost to rework from unclear or changing requirements
- **AI Efficiency Loss:** Developers using AI coding assistants report 50% context-gathering overhead when tools lack access to planning documentation (GitHub Copilot research, 2024)
- **Onboarding Delays:** New team members require 4-6 weeks to become productive when documentation is fragmented vs. 1-2 weeks with centralized, structured context

**For AI-Native Teams Specifically:**
- AI coding assistants can generate code 10x faster, but without proper context, 40% requires significant refactoring
- Solo developers abandon 60% of POC projects when scaling complexity overwhelms their planning capacity
- Enterprise teams using AI tools report that documentation gaps—not AI capability—are the primary blocker to velocity

#### **Why Existing Solutions Fall Short**

| Tool Category | Representative Tools | Strengths | Critical Gaps |
|--------------|---------------------|-----------|---------------|
| **Execution Tools** | Linear, Jira, Azure Boards | Excellent for tracking work, sprints, and delivery | Assume planning is already done; provide no upstream guidance for strategy, architecture, or requirements. No AI assistant integration for context access. |
| **Documentation Tools** | Notion, Confluence, Google Docs | Flexible, easy to use, great for freeform content | Too unstructured—no enforced relationships between documents. No opinionated workflows. Documents become stale and disconnected from execution. |
| **Traditional PM Tools** | Aha!, ProductPlan, Roadmunk | Enforce process, provide roadmap visualization | Rigid templates that don't adapt to team needs. No intelligence to guide or validate. Not designed for AI-native workflows. |
| **AI Coding Assistants** | Cursor, Windsurf, Claude Code, GitHub Copilot | Brilliant at code generation from prompts | Lack access to strategic context—business goals, architectural decisions, cross-feature dependencies. Cannot read/write planning documentation. |
| **AI Project Tools** | ChatGPT Projects, Claude Projects | Maintain conversation context, can draft documents | Generic assistants without specialized planning expertise (PM, Architect, QA perspectives). No structured hierarchy or workflow enforcement. |

**The Gap:** No tool bridges the chasm between strategic planning (where humans and AI agents need to collaborate on *what* and *why*) and tactical execution (where AI coding assistants excel at *how*). Teams either sacrifice structure for flexibility (Notion) or accept rigid execution tracking without planning support (Jira/Linear).

#### **Why Now? Market Timing & Technology Convergence**

Three forces make RoadmapKO viable and urgent today:

1. **AI Agent Orchestration Maturity (2024-2025):** Multi-agent systems with tool use, structured outputs, and reliable reasoning only became production-ready in the past 12 months. Vertex AI ADK, Claude Computer Use, and OpenAI Agents API now enable sophisticated agent orchestration.

2. **AI Coding Assistant Adoption Explosion:** GitHub Copilot has 1.8M+ paid users; Cursor has 50K+ monthly active teams; Claude Code and Windsurf are growing 30%+ month-over-month. The market has shifted—AI-assisted development is now the default, not the exception.

3. **Distribution Channels Democratized:** ChatGPT Apps SDK (800M+ potential users) and Claude MCP (direct desktop integration) provide zero-friction distribution to developers already using AI tools daily. Building marketplace presence from scratch is no longer required.

4. **Remote Work Documentation Crisis:** Distributed teams amplify the planning problem—async work requires better documentation practices, but existing tools haven't adapted. The "just talk it out in person" workaround is gone.

5. **Economic Pressure for Efficiency:** In a constrained funding environment, teams must ship faster with smaller headcounts. AI tools promise this efficiency, but only if given proper context. The ROI case for planning infrastructure has never been stronger.

---

### **Proposed Solution**

#### **Core Concept: AI Planning Team Meets AI Development Team**

RoadmapKO is an AI-native orchestration platform that provides **7 specialized AI agents** working behind a single conversational interface to guide teams through the complete "front-half" of the SDLC—from initial business idea to developer-ready backlog with full technical context. Unlike generic AI assistants, each RoadmapKO agent embodies a specific role (Discovery Analyst, Requirements PM, Design Lead, Architect, QA Lead, Product Owner, Scrum Master) with deep domain expertise in their discipline.

**The Innovation:** RoadmapKO doesn't just create planning documents for humans—it creates a **living, queryable context layer** that AI coding assistants can read from and write to. When a developer uses Cursor or Claude Code to implement a feature, their AI assistant can access:
- The business objective and success metrics (from the Project Brief)
- Architectural constraints and patterns (from the Architecture document)
- Acceptance criteria and edge cases (from the PRD and User Stories)
- Security and accessibility requirements (from the QA Strategy)
- Cross-feature dependencies (from the Epic/Feature hierarchy)

Then, as development progresses, AI coding assistants can write back:
- Task completion status and implementation notes
- Code references and technical decisions made
- Discovered edge cases or requirement clarifications
- Test coverage and quality metrics

**Result:** Humans and AI agents collaborate on the same unified planning canvas, eliminating context gaps and enabling true AI-native velocity.

#### **The Two-Phase Workflow**

RoadmapKO guides users through two sequential phases, each orchestrating multiple specialized agents:

**Phase 1: Analysis (Discovery Agent)**
1. **Market Research** → Competitive landscape, user needs, market opportunity
2. **Competitive Analysis** → Feature comparison, pricing analysis, differentiation strategy  
3. **Project Brief** → Executive summary, problem statement, solution approach, target users, success metrics

*Output:* Strategic foundation that answers "Why build this?" and "For whom?"

**Phase 2: Planning (6 Specialized Agents)**
4. **Requirements (Requirements Agent)** → Comprehensive PRD with epics, features, and user story placeholders
5. **Design (Design Agent)** → UX/UI specifications, design tokens, component library, Lovable/v0 prompts
6. **Architecture (Architecture Agent)** → Technical stack, data models, API design, infrastructure requirements
7. **Quality (Quality Agent)** → Test strategy, data/environment management, unit/integration/e2e/accessibility/performance/security testing plans
8. **Validation (Validation Agent)** → Cross-document alignment review, gap identification, stakeholder approval gates
9. **Planning (Planning Agent)** → Fully-detailed user stories with tasks, technical references, acceptance criteria, story points

*Output:* Execution-ready backlog with every story fully contextualized and technically specified

**Key UI Elements:**
1. **Left Panel:** Initiative Workflow with collapsible sections (Discovery & Research, Product Definition, Design & Architecture, Validation & Handoff) and progress indicators
2. **Middle Panel:** Agent Chat with conversational interaction, document drafts, and elicitation prompts (multiple choice options)
3. **Right Panel:** Document preview showing live sections with approval status and edit/history/export options

#### **The Three-Panel Workspace**

Users interact with RoadmapKO through a unified interface that maintains visibility across three dimensions:

```
┌────────────────────┬─────────────────────────┬──────────────────────┐
│  INITIATIVE        │   AGENT CHAT            │   DOCUMENT PREVIEW   │
│  WORKFLOW          │                         │                      │
│                    │ 🤖 PM: "Based on the    │ PRD: E-Commerce      │
│ ▼ Discovery &      │ approved Project Brief, │ Platform        v0.6 │
│   Research         │ let's create the PRD.   │                      │
│   ✓ Project Brief  │ Starting with Functional│ ⚠️ 3 sections pending│
│   ✓ Market Research│ Requirements..."        │    2 sections done   │
│   ✓ Comp Analysis  │                         │                      │
│                    │ [Agent draft shown]     │ ▼ Executive Summary  │
│ ▼ Product          │                         │   ✓ Approved         │
│   Definition   35% │ ⚠️ ELICITATION REQUIRED │   [content preview]  │
│   ✓ PRD Header     │                         │                      │
│   ⚡Functional Reqs │ Select an option:       │ ▼ Problem Statement  │
│   ○ Non-Functional │ 1. Proceed to next      │   ✓ Approved         │
│   ○ Epics & Stories│ 2. Expand section       │                      │
│   ○ Acceptance     │ 3. Validate against...  │ ▼ Functional Reqs    │
│                    │ 4. Stress test...       │   🔄 Awaiting Review │
│ ▶ Design &         │ 5. Explore alternatives │   FR1: Guided...     │
│   Architecture     │ 6. Analyze tradeoffs    │   FR2: Hierarchical..│
│   [LOCKED]         │ 7. Generate risk...     │   FR3: AI-Powered... │
│                    │                         │                      │
│ ▶ Validation &     │ [User input box]        │ [Edit] [History]     │
│   Handoff          │ [Send button]           │ [Export]             │
│   [LOCKED]         │                         │                      │
└────────────────────┴─────────────────────────┴──────────────────────┘

Status Bar: PM Agent: Active | PRD § 3/12 | Elapsed: 2h 15m | Est. remaining: 45m
Mode: Interactive • Next: NFR definition • Press ? for shortcuts
```

**Left Panel (Initiative Workflow):**
- **Collapsible phase sections** with completion indicators (✓ Complete, ⚡In Progress, ○ Not Started, 🔒 Locked)
- **Visual progress tracking** showing percentage complete per phase
- **Sequential unlocking:** Later phases locked until dependencies complete
- **Hierarchical document tree:** Click any completed document to preview in right panel
- **Estimated time remaining** updates in real-time as sections complete

**Middle Panel (Agent Chat):**
- **Agent identity indicator** showing which specialized agent is active (PM Agent, Architecture Agent, etc.)
- **Conversational interaction** with natural language back-and-forth
- **Inline document drafts** rendered directly in chat for immediate review
- **Elicitation prompts** with numbered options for guided decision-making (replaces open-ended questions that can stall progress)
- **Context-aware suggestions** based on approved artifacts and industry best practices
- **"Previous Agents" and "View All Chats"** buttons to review past agent interactions
- **Mode indicator** (Interactive/YOLO) in top-right corner

**Right Panel (Document Preview):**
- **Live document rendering** with collapsible sections
- **Approval workflow indicators** (✓ Approved, 🔄 Awaiting Review, ⚠️ Needs Revision)
- **Version tracking** (v0.6 Draft shown in mockup)
- **Section-level status** showing which parts are complete vs. pending
- **Quick actions:** Edit (post-MVP TipTap editing), History (version comparison), Export (markdown/PDF)
- **Cross-document navigation:** Click references to jump to related artifacts

**Bottom Status Bar:**
- **Active agent indicator:** Shows which specialized agent is currently working
- **Progress tracking:** Section completion count (§ 3/12)
- **Time estimates:** Elapsed time and estimated remaining time
- **Mode & next step:** Current workflow mode and what comes next
- **Keyboard shortcuts:** Press ? for power-user shortcuts (post-MVP)

#### **Workflow Progression & Gating**

The mockup shows **sequential phase unlocking** to prevent users from jumping ahead without foundational context:

1. **Discovery & Research** must complete before **Product Definition** unlocks
2. **Product Definition** must complete before **Design & Architecture** unlocks  
3. **Design & Architecture** must complete before **Validation & Handoff** unlocks

**Validation Agent checkpoints:** After each phase, the Validation Agent reviews all documents for:
- Internal consistency (PRD references brief correctly)
- Completeness (all required sections present)
- Alignment (architecture matches requirements)
- Quality gates (acceptance criteria follow INVEST principles)

**Override capability (post-MVP):** Power users can unlock phases early, but system warns of missing dependencies and tracks "at-risk" decisions.

#### **Example User Journey: From Idea to Backlog in 2 Hours**

**Scenario:** Marcus (indie SaaS builder) wants to build a B2B scheduling app but doesn't know where to start.

**Minute 0-15: Discovery**
```
Marcus: "I want to build a scheduling app for B2B sales teams"

Discovery Agent: "Great! Let me help you plan this properly. First, 
I'll create a project brief. Tell me: what problem are these sales 
teams facing with current scheduling tools?"

[Marcus provides context through conversation]

Discovery Agent: "I've drafted an executive summary and problem 
statement. Take a look in the middle column. Should I research 
competitors like Calendly, Chili Piper, and Kronologic?"

Marcus: "Yes, proceed"

Discovery Agent: "Researching now... [15 seconds] Done. I found 
8 competitors. Your differentiation opportunity is AI-powered 
meeting prep—none of them do this. Should I document this in 
the competitive analysis?"
```

**Minute 15-45: Planning - Requirements**
```
Requirements Agent: "Based on your brief, I'm drafting a PRD. 
I've identified 3 core epics:
1. Meeting Scheduling Engine
2. AI Meeting Prep Assistant  
3. CRM Integrations

For Epic 1, I'm breaking down 5 features... [shows in preview]
Does this structure make sense?"

Marcus: "Yes, but add calendar conflict detection"

Requirements Agent: "Added as Feature 1.4. I've also created 
placeholder user stories for each feature. Ready for architecture?"
```

**Minute 45-75: Planning - Design & Architecture**
```
Design Agent: "I'm creating UX specs for your scheduling flow. 
I recommend a 3-step wizard: Select Time → Add Attendees → 
Confirm. I've also generated design tokens and a Lovable prompt 
you can use to generate the UI. See middle column."

Architecture Agent: "For your tech stack, I recommend:
- Next.js + Supabase (you mentioned wanting PostgreSQL)
- Resend for email notifications
- OpenAI for meeting prep AI

I've documented the complete architecture with data models, 
API endpoints, and infrastructure. Want me to explain any part?"
```

**Minute 75-120: Planning - Quality, Validation, Stories**
```
Quality Agent: "I've created a QA strategy covering unit tests 
(Jest), integration tests (Playwright), and accessibility (axe). 
Your critical path: calendar sync reliability and meeting prep 
AI accuracy."

Validation Agent: "I've reviewed all documents. Everything is 
aligned. One gap: Feature 1.4 (conflict detection) doesn't have 
architecture defined yet. Should Architecture Agent spec this?"

Marcus: "Yes"

[Architecture Agent fills gap]

Planning Agent: "Now I'll convert your 47 placeholder stories into 
fully-detailed user stories with tasks, acceptance criteria, and 
technical references... [2 minutes] Done. Your backlog is ready. 
Want to export to Linear or use our built-in tracking?"

Marcus: "Export to Linear, but keep RoadmapKO as system of record"

Planning Agent: "Connected to Linear. Syncing... Done. Your Linear 
workspace now has 47 stories. I'll keep RoadmapKO context synced 
so Cursor can access it. Ready to start coding?"
```

**Minute 120: Development Starts**
```
Marcus opens Cursor, which connects to RoadmapKO via MCP:

Marcus (in Cursor): "Implement Story 1.1: User can connect Google Calendar"

Cursor (with RoadmapKO context): "I can see from the architecture 
doc that you're using Supabase Auth and the Google Calendar API. 
The acceptance criteria specifies OAuth 2.0 flow with offline 
access. I'll create the auth flow following your documented 
security requirements..."

[Cursor generates code with full context]

[Upon completion, Cursor updates RoadmapKO: Story 1.1 → Status: Complete,
Implementation Notes: "Used googleapis@latest, stored refresh tokens 
in supabase.auth.tokens table per architecture spec"]
```

**Result:** Marcus goes from "I have an idea" to "I'm writing code with full context" in 2 hours—with zero blank pages, no architectural flip-flopping, and his AI coding assistant fully informed.

#### **Key Differentiators: Why RoadmapKO Wins**

**1. Methodology Enforcement (No Blank Page Syndrome)**
- Users never face a blank document. Every section has templates, examples, and guided questions.
- Opinionated Initiative → Epic → Feature → Story → Task hierarchy prevents scope chaos and ensures traceability.
- Best practices (INVEST criteria for stories, architectural decision records, test pyramid) are built into agent prompts.

**2. Intelligent Backfilling (Gap Recognition)**
- If a user starts discussing features without a PRD, RoadmapKO recognizes the gap and offers to backfill the missing brief, research, and competitive analysis.
- If architecture is defined before requirements, Validation Agent flags the inverted dependency and guides proper sequencing.
- New features added mid-project trigger automatic PRD updates and architectural impact analysis.

**3. Opinionated Hierarchy (Structural Integrity)**
- Strict enforcement of relationships: Tasks belong to Stories, Stories to Features, Features to Epics, Epics to Initiatives.
- Cross-cutting concerns (security, accessibility) are captured at the appropriate level and flow down automatically.
- Prevents common anti-patterns: orphaned tasks, features without business justification, architecture without requirements.

**4. Human-in-the-Loop Approval Gates (Control Without Micromanagement)**
- Agents draft, humans review and approve. Users maintain control while benefiting from AI speed.
- Approval workflow: Draft → Review → Request Changes → Re-draft → Approve → Lock
- Locked documents create immutable history; changes require explicit unlocking and re-validation.

**5. Orchestrated Sub-Agents (Single Interface, Multi-Expert Backend)**
- Users never juggle multiple tools or switch contexts—one conversation covers all planning phases.
- Behind the scenes, orchestrator delegates to specialists: "Calling Design Agent for UX specs..."
- Each agent has role-specific personality and expertise (Discovery is curious and analytical; Architecture is systematic and detail-oriented).

**6. AI Coding Assistant Bridge (Context for Machines)**
- **Bidirectional integration:** AI tools read planning context and write back status/notes.
- **MCP protocol support:** Native integration with Claude Code, future Cursor/Windsurf MCP support.
- **API-first architecture:** Any AI assistant can integrate via REST API (not just MCP-enabled tools).
- **System of record:** Even if users export to Linear/Jira, RoadmapKO preserves full context that execution tools strip away.

#### **Why This Succeeds Where Others Failed**

**Existing solutions failed because they optimized for only one dimension:**

- **Notion/Confluence:** Optimized for *flexibility* → Result: no structure, stale docs
- **Jira/Linear:** Optimized for *execution* → Result: assumes planning is done, no guidance
- **Traditional PM tools:** Optimized for *process compliance* → Result: rigid, doesn't adapt
- **ChatGPT/Claude Projects:** Optimized for *conversation* → Result: no specialized expertise, no hierarchy

**RoadmapKO succeeds by optimizing across four dimensions simultaneously:**

1. **Structure:** Opinionated hierarchy and methodology enforcement
2. **Intelligence:** AI agents with role-specific expertise that recognize gaps and backfill
3. **Integration:** Bidirectional bridge between planning (human/AI collaboration) and execution (AI coding assistants)
4. **Flexibility:** Human-in-the-loop gates ensure control; conversational interface adapts to user's mental model

**The compounding advantage:** Each dimension reinforces the others. Structure enables intelligent gap detection. Integration makes AI coding assistants more valuable, which drives adoption. Human control builds trust, which enables more delegation over time.

#### **High-Level Product Vision**

**Year 1: Establish Planning Dominance**
- Become the default "Phase Zero" tool for solo developers and small teams using AI coding assistants
- Perfect the Analysis + Planning workflow until >85% of agent outputs require minimal human revision
- Achieve product-market fit with indie SaaS builders, vibe coders, and AI-native engineering teams

**Year 2: Scale Through Distribution Channels**
- Launch ChatGPT Apps SDK integration → access 800M+ ChatGPT users
- Launch Claude Desktop MCP → native integration for Claude Code users
- Expand integrations: Linear, Jira, Notion, Azure Boards, GitHub Projects
- Enterprise tier: Team collaboration, SSO, advanced analytics

**Year 3: Autonomous Planning Intelligence**
- Agents proactively monitor project health and suggest course corrections
- Predictive planning: "Based on velocity and architecture complexity, Epic 2 will slip 2 sprints—consider descoping Feature 2.3"
- Portfolio management: Multi-project intelligence that identifies resource conflicts and dependency risks across initiatives

**Long-Term: The Platform Play**
- RoadmapKO becomes the "operating system" for AI-native software development
- Any AI tool (coding, design, testing, deployment) connects to RoadmapKO as the shared context layer
- Move beyond planning: execution tracking, observability integration, automated ROI reporting

---

### **Target Users**

RoadmapKO serves three distinct user segments, prioritized for go-to-market sequencing. Each segment has unique characteristics but shares a common problem: insufficient planning infrastructure to support AI-native development velocity.

---

#### **Primary User Segment: Solo Developers & Indie Hackers**

**Profile:**
- **Demographics:** 25-45 years old, 3-10 years of software development experience
- **Roles:** Indie SaaS builders, solo founders, freelance developers, side-project entrepreneurs
- **Team Size:** Solo or 2-3 person teams without dedicated PMs, designers, or architects
- **Technical Profile:** Proficient with modern frameworks (Next.js, React, Node.js), heavy users of AI coding assistants (Cursor, Windsurf, Claude Code, GitHub Copilot)
- **Budget Context:** Bootstrap-funded or pre-seed, cost-conscious but willing to pay for tools that provide clear ROI
- **Geographic Distribution:** Global, with concentration in US, Europe, India, Southeast Asia

**Current Behaviors & Workflows:**

*Tool Stack:*
- **Development:** Cursor or Windsurf as primary IDE with AI coding assistant
- **Notes:** Notion, Obsidian, or Apple Notes for scattered ideas and rough sketches
- **Planning:** None, or minimal Google Docs with bullet-pointed feature lists
- **Task Tracking:** Linear, GitHub Issues, or Trello (if they track at all)
- **Design:** Figma for mockups, or direct prototyping in code using v0/Lovable

*Typical Workflow:*
1. **Idea Phase (2-4 hours):** Rough notes in Notion, maybe a competitor feature comparison in a spreadsheet
2. **Prototype Phase (1-2 days):** Use Cursor + AI prompts to build POC without formal requirements
3. **Reality Check (Week 2-3):** Realize they've built features without clear user stories, no architectural documentation, mounting technical debt
4. **Restart or Abandon (Week 4+):** Either restart with better planning (rare) or abandon project (60% of POCs)

**Specific Needs & Pain Points:**

**Pain Point 1: "I can prototype fast but can't scale to production"**
- Can build functional POCs in 1-2 days with AI coding assistants
- Struggle to translate POC into production-ready application with proper architecture, error handling, testing
- Lack experience writing comprehensive PRDs or technical architecture documents
- Don't know what "good enough" planning documentation looks like

**Pain Point 2: "My AI coding assistant keeps making conflicting architectural choices"**
- Cursor generates brilliant code in isolation but lacks project-wide context
- Different prompting sessions lead to inconsistent patterns (REST vs. GraphQL, client-side vs. server-side rendering)
- No single source of truth for "here's how we do authentication" or "here's our data model"
- Spend 40% of time refactoring AI-generated code for consistency

**Pain Point 3: "I'm a developer, not a PM—I don't know how to write requirements"**
- Familiar with writing code, unfamiliar with writing user stories, acceptance criteria, or PRDs
- Don't know frameworks like INVEST criteria, acceptance test-driven development, or story mapping
- Start building without clear definition of "done," leading to endless feature creep
- Can't articulate value proposition or target user needs in a structured way

**Pain Point 4: "Documentation is always an afterthought"**
- Focus 95% of time on building, 5% on documenting decisions
- Six months later, can't remember why they chose specific architectural patterns
- Difficult to onboard collaborators or hand off projects to clients
- Documentation becomes outdated immediately and never gets updated

**Goals They're Trying to Achieve:**

**Immediate Goals (Next 3-6 months):**
- Ship their first production SaaS product that customers will pay for
- Build faster without accumulating technical debt that will slow them down later
- Create professional-grade planning documentation that impresses potential investors or acquirers
- Enable their AI coding assistant to generate better, more contextually-aware code

**Long-Term Goals (Next 1-2 years):**
- Scale from side project to sustainable lifestyle business ($5-10K MRR)
- Hire their first employee or contractor and onboard them efficiently
- Build multiple products using a repeatable, proven planning process
- Exit via acquisition with comprehensive documentation that increases valuation

**What Success Looks Like:**
- Go from "idea" to "first customer" in 4-6 weeks instead of 3-6 months
- Reduce time spent refactoring AI-generated code by 50%
- Have comprehensive planning documentation that allows them to take a 2-week vacation without project context living only in their head
- Feel confident saying "yes" when asked "Do you have technical documentation?" by potential acquirers or investors

**RoadmapKO Value for This Segment:**
- **Guided expertise:** Acts as the PM, architect, and QA lead they can't afford to hire
- **AI coding assistant multiplier:** Gives Cursor/Windsurf the context needed to generate production-ready code
- **Speed without sacrifice:** Maintain velocity while building proper planning foundation
- **Professionalization:** Elevates their project from "hacker side project" to "investable business" through comprehensive documentation

---

#### **Secondary User Segment: Enterprise Software Teams (AI-Native PMs & Engineering Leads)**

**Profile:**
- **Demographics:** 30-50 years old, 8-20 years of software/product experience
- **Roles:** Product Managers, Engineering Managers, Technical Product Owners, Team Leads
- **Team Size:** Leading 5-20 person engineering teams within larger organizations (50-500 employees)
- **Company Stage:** Series A through Series C startups, or innovation teams within mid-size enterprises
- **Technical Profile:** Technically fluent (can read code, understand architecture) but not coding daily; advocates for AI-assisted development within their teams
- **Budget Context:** Annual tool budgets of $50K-250K; willing to pay for tools that demonstrate clear ROI in team velocity and quality

**Current Behaviors & Workflows:**

*Tool Stack:*
- **Planning:** Confluence or Notion for PRDs, Google Docs for strategy documents
- **Execution:** Jira or Linear for sprint planning and issue tracking
- **Design:** Figma for design handoff
- **Architecture:** Confluence, Lucidchart, or Miro for architecture diagrams
- **Communication:** Slack for team coordination, Loom for async updates
- **Observability:** Datadog, Sentry, or similar for production monitoring

*Typical Workflow:*
1. **Strategy Phase (1-2 weeks):** Quarterly planning with stakeholders, creating initiative briefs in Confluence
2. **Requirements Phase (1-2 weeks):** Writing PRDs in Google Docs, gathering feedback in comments, multiple revision cycles
3. **Refinement Phase (Ongoing):** Breaking down PRD into epics and stories in Jira, often incomplete or inconsistent with PRD
4. **Sprint Planning (Weekly):** Engineers pull from backlog, frequently discover missing context or requirements, PM spends 10-15 hours/week answering "why" questions
5. **Retrospective (Bi-weekly):** Team identifies documentation gaps, commits to improving process, rarely follows through due to time pressure

**Specific Needs & Pain Points:**

**Pain Point 1: "My team uses AI coding assistants but they lack strategic context"**
- Engineers use Cursor, GitHub Copilot, or Claude Code to ship features 2-3x faster
- AI tools generate technically sound code but don't understand business objectives, architectural constraints, or cross-feature dependencies
- PM spends significant time reviewing PRs to ensure AI-generated code aligns with product strategy
- Documentation in Confluence/Notion is too disconnected for AI tools to access programmatically

**Pain Point 2: "Documentation fragmentation kills team velocity"**
- Strategy docs in Confluence, PRDs in Google Docs, stories in Jira, architecture in Lucidchart, decisions in Slack threads
- New team members take 4-6 weeks to understand "how we work" because context is scattered
- When engineers ask "Why did we choose PostgreSQL over MongoDB?" the answer is lost in a 6-month-old Slack thread
- Keeping multiple tools synchronized is a full-time job nobody has time for

**Pain Point 3: "Requirements emerge mid-sprint, causing thrash"**
- Despite writing comprehensive PRDs, engineers still discover missing requirements during implementation
- Gap between "what PM documented" and "what engineering needs" leads to 30-40% rework
- No formal process for validating that architecture aligns with requirements before development starts
- Stories are broken down hastily without proper acceptance criteria, leading to scope debates during QA

**Pain Point 4: "I can't scale myself across multiple initiatives"**
- Managing 3-5 concurrent initiatives with 15+ engineers
- Each initiative needs a project brief, PRD, architectural review, story refinement
- Spend 60% of time writing/updating documentation, 40% in meetings explaining documentation
- No bandwidth for strategic thinking or competitive analysis
- Team velocity bottlenecked by PM's availability to answer questions

**Goals They're Trying to Achieve:**

**Immediate Goals (Next Quarter):**
- Reduce time spent on documentation by 50% without sacrificing quality
- Enable engineering team to leverage AI coding assistants more effectively with better context
- Decrease "requirements discovered mid-sprint" incidents by 75%
- Onboard new engineers in 1-2 weeks instead of 4-6 weeks

**Long-Term Goals (Next Year):**
- Scale from managing 1-2 initiatives to 5-7 initiatives without hiring additional PMs
- Establish repeatable planning process that works consistently across all product teams
- Reduce rework and technical debt accumulation by 40%
- Enable async-first workflows that support distributed team across timezones

**What Success Looks Like:**
- Engineers say "I have all the context I need" instead of "Can you explain this requirement?"
- AI coding assistants generate code that aligns with architectural standards 85%+ of the time
- New initiatives go from brief to implementation-ready backlog in 1 week instead of 3-4 weeks
- Team ships features with 90%+ confidence they'll meet acceptance criteria on first pass

**RoadmapKO Value for This Segment:**
- **PM force multiplier:** AI agents handle documentation grunt work, PM focuses on strategy and stakeholder management
- **Single source of truth:** All planning artifacts in one system with enforced relationships
- **AI team enabler:** Engineering team's AI coding assistants get context they need without PM bottleneck
- **Process standardization:** Every initiative follows same proven workflow, reducing variance and improving predictability
- **Integration with execution tools:** Sync to Jira/Linear for execution while maintaining rich context in RoadmapKO

---

#### **Tertiary User Segment: Digital Agencies**

**Profile:**
- **Demographics:** Agency size 5-50 employees, managing 5-25 concurrent client projects
- **Roles:** Agency Owners, Project Managers, Client Success Managers, Lead Developers
- **Client Types:** Small-to-medium businesses needing custom software, mobile apps, or web applications
- **Technical Profile:** Generalist development teams comfortable with multiple tech stacks
- **Budget Context:** Bill clients $100-250/hour; need to demonstrate professionalism and reduce non-billable documentation time
- **Geographic Distribution:** Global, concentration in US, UK, India, Eastern Europe

**Current Behaviors & Workflows:**

*Tool Stack:*
- **Client Management:** HubSpot, Pipedrive, or custom CRM
- **Project Management:** Jira, Asana, or Monday.com for client project tracking
- **Documentation:** Google Docs or Confluence for proposals and requirements
- **Design:** Figma for client design approvals
- **Development:** Varies by project, increasingly using AI coding assistants to improve margins
- **Time Tracking:** Harvest, Toggl, or Clockify for billable hours

*Typical Workflow:*
1. **Sales Phase (1-4 weeks):** Proposal creation, scope definition, client negotiations
2. **Discovery Phase (1-2 weeks):** Client interviews, requirements gathering, budget finalization
3. **Planning Phase (1-2 weeks):** Creating project brief, wireframes, technical architecture, statement of work
4. **Development Phase (4-12 weeks):** Sprint-based delivery with weekly client check-ins
5. **Handoff Phase (1-2 weeks):** Documentation, training, deployment, support transition

**Specific Needs & Pain Points:**

**Pain Point 1: "Every project starts from scratch, no standardization"**
- Each PM has their own documentation approach, leading to inconsistent client deliverables
- Junior PMs produce lower-quality planning documents, requiring senior review and rework
- No template or framework that ensures consistent quality across all client projects
- Clients notice quality variance and question agency professionalism

**Pain Point 2: "Non-billable planning time erodes margins"**
- Spend 20-30% of project time on documentation that clients don't directly see or value
- Can't bill clients for "project brief creation" or "technical architecture documentation"
- Pressure to minimize planning time leads to requirement gaps and costly rework (which is also non-billable)
- Vicious cycle: skimp on planning → rework → lower margins → more pressure to skimp on planning

**Pain Point 3: "Client scope creep is constant battle"**
- Clients request features mid-project without understanding impact on timeline/budget
- Without clear initiative/epic boundaries, hard to say "that's out of scope" convincingly
- Change requests require re-documenting requirements, updating architecture, revising estimates
- Scope creep disputes damage client relationships and profitability

**Pain Point 4: "Documentation handoff is a nightmare"**
- At project completion, need to deliver comprehensive documentation for client's internal team
- Often scrambling to backfill documentation that should have been created during development
- Clients complain about insufficient documentation, leading to extended support obligations
- Poor documentation damages referrals and case study potential

**Goals They're Trying to Achieve:**

**Immediate Goals (Next Quarter):**
- Reduce non-billable planning time from 25-30 hours per project to 10-15 hours
- Standardize documentation quality across all PMs (eliminate variance between junior/senior)
- Decrease scope creep disputes by 50% through clearer initiative boundaries
- Improve client satisfaction scores related to "project clarity" and "documentation quality"

**Long-Term Goals (Next Year):**
- Increase project margins by 10-15% through planning efficiency and reduced rework
- Scale from 5-10 concurrent projects to 15-20 projects without hiring additional PMs
- Win larger enterprise clients who require professional planning documentation
- Build reputation as "the agency that actually plans properly" for referral differentiation

**What Success Looks Like:**
- Every client project has comprehensive, professional documentation from day one
- Junior PMs produce deliverables indistinguishable from senior PMs (process enforces quality)
- Clients say "This is the most organized agency we've ever worked with"
- Zero scope creep disputes because boundaries are crystal clear from project start
- Project handoff documentation is so good clients recommend agency to peers

**RoadmapKO Value for This Segment:**
- **Standardization engine:** Every project follows identical proven workflow, eliminating PM skill variance
- **Speed to professionalism:** Generate client-ready documentation in 1/3 the time of manual creation
- **Margin protection:** Reduce non-billable planning hours while improving output quality
- **Scope protection:** Clear initiative/epic hierarchy makes scope boundaries indisputable
- **Competitive differentiator:** Wow clients with planning rigor that competitors can't match
- **Portfolio management:** Manage 15-20 client projects with visibility and consistency

---

### **User Segment Prioritization & GTM Sequencing**

**Phase 1 (Months 1-6): Primary Focus on Solo Developers & Indie Hackers**

*Rationale:*
- Fastest path to product-market fit and initial revenue
- Most acute pain around AI coding assistant context gaps
- Lowest sales friction (individual purchase decision, $49/mo is impulse-buy)
- Highest early adopter willingness (comfortable with beta software, provide best feedback)
- Viral potential through indie hacker communities (Twitter, Indie Hackers, Reddit)

*Success Metrics:*
- 100 paying customers by Month 6
- $5-10K MRR
- 80%+ agent output approval rate
- NPS >50

**Phase 2 (Months 7-12): Expansion to Enterprise Teams**

*Rationale:*
- Product maturity proven with solo devs, ready for team use cases
- Higher ACV ($149-499/mo per team) improves revenue growth rate
- Integration capabilities mature (Linear, Jira sync) enables enterprise adoption
- Case studies from Phase 1 provide credibility for enterprise sales

*Success Metrics:*
- 30 enterprise team customers (5-20 person teams)
- $30-40K MRR total
- Team collaboration features validated
- 75%+ renewal rate

**Phase 3 (Months 13-18): Tertiary Focus on Digital Agencies**

*Rationale:*
- Highest ACV potential ($499-999/mo per agency)
- Multi-project portfolio management features now available
- White-label/branded export features enable agency use case
- Enterprise-grade SLAs and support infrastructure mature

*Success Metrics:*
- 15 agency customers managing 100+ total client projects
- $50-60K MRR total
- Agency-specific features validated (multi-tenant, white-label)
- Strong referral motion established

---

### **Goals & Success Metrics**

#### **Business Objectives**

**Month 1-3: MVP Launch & Initial Validation**
- **Launch private beta** with 10 design partners (3 solo devs, 3 AI-native engineers, 2 indie SaaS builders, 2 vibe coders) by end of Month 2
- **Achieve 80%+ agent output approval rate** across all 7 agents within 2 weeks of design partner testing (measured by thumbs up/down on agent drafts)
- **Public launch on Product Hunt** by end of Month 3 with goal of #1-3 Product of the Day
- **Acquire first 10 paying customers** within 2 weeks of public launch at $49/mo Starter tier
- **Validate core value proposition:** >70% of beta users report "RoadmapKO saved me 5+ hours on planning" in post-use survey

**Month 4-6: Distribution Channel Expansion**
- **Launch ChatGPT Apps SDK integration** by end of Month 4, targeting 500+ installations in first 30 days
- **Reach 100 total paying customers** by end of Month 6 ($5-10K MRR)
- **Achieve 10%+ visitor-to-paid conversion rate** (industry benchmark is 2-5% for developer tools with direct paid signup)
- **Maintain <10% monthly churn rate** through continuous agent quality improvements
- **Build email list of 2,000+ interested users** through Product Hunt, ChatGPT Apps, content marketing

**Month 7-12: Enterprise Expansion & Profitability**
- **Launch Claude Desktop MCP integration** by end of Month 7, targeting 200+ installations in first 30 days
- **Launch integration tier** (Linear, Jira, Notion, Azure Boards) by end of Month 9
- **Acquire 30 enterprise team customers** (Pro tier at $149/mo) by end of Month 12
- **Reach $30-40K MRR** by end of Month 12 (200+ total customers)
- **Achieve profitability** (revenue > costs) by Month 10, assuming solo founder + $5K/mo operating costs
- **Expand to 3 enterprise case studies** demonstrating 40%+ reduction in planning time and 50%+ reduction in AI-generated code rework

**Year 2: Scale & Platform**
- **Reach $100K MRR** by Month 18 (500+ customers)
- **Launch agency tier** by Month 15 with white-label documentation export
- **Achieve 15 agency customers** managing 100+ total client projects
- **Establish partnership channel** with AI coding assistant vendors (Cursor, Windsurf discussions)
- **Series A readiness** (if pursuing venture path): $1.5M+ ARR, 40%+ growth rate, <15% churn

#### **User Success Metrics**

**Planning Efficiency Gains**
- **Reduce time from idea to execution-ready backlog by 60%:**
  - Baseline: 20-30 hours manual planning (research, PRD, architecture, stories)
  - Target: 8-12 hours with RoadmapKO (2 hours human interaction, 6-10 hours agent work + human review)
  - Measurement: Time tracking within app, validated by user surveys

- **Decrease documentation search time by 75%:**
  - Baseline: 8-12 hours/week searching across Notion/Confluence/Docs/Slack
  - Target: 2-3 hours/week (all context in single hierarchy)
  - Measurement: Weekly surveys, comparison with baseline tools

**AI Coding Assistant Effectiveness**
- **Reduce AI-generated code rework by 50%:**
  - Baseline: 40% of AI-generated code requires significant refactoring due to context gaps
  - Target: 20% requires refactoring (architectural alignment, consistency)
  - Measurement: Developer surveys, Git diff analysis of AI vs. human commits

- **Increase AI coding assistant "first-pass acceptance" rate by 35%:**
  - Baseline: 50% of AI-generated features accepted with minor tweaks
  - Target: 85% accepted with minor tweaks
  - Measurement: PR review feedback, acceptance criteria pass rate

**Documentation Quality & Completeness**
- **Achieve 90%+ documentation completeness score:**
  - All initiatives have: Project Brief, Competitive Analysis, PRD, Architecture, QA Strategy, User Stories
  - Measurement: Automated completeness checks within RoadmapKO

- **Maintain documentation freshness <2 weeks:**
  - All documents updated within 2 weeks of significant project changes
  - Measurement: Document "last updated" timestamps, staleness alerts

**Team Collaboration & Onboarding**
- **Reduce new team member onboarding time by 60%:**
  - Baseline: 4-6 weeks for new engineer to become productive
  - Target: 1.5-2 weeks with comprehensive RoadmapKO documentation
  - Measurement: User-reported onboarding duration surveys

- **Decrease "why?" questions to PM/lead by 70%:**
  - Baseline: PMs/leads spend 10-15 hours/week answering context questions
  - Target: 3-5 hours/week (strategic questions only, tactical context in docs)
  - Measurement: Weekly time tracking surveys

**Project Success Rates**
- **Increase project completion rate by 40%:**
  - Baseline: 60% of solo dev projects abandoned due to planning overwhelm
  - Target: 90% of projects with RoadmapKO documentation reach production
  - Measurement: 6-month follow-up surveys on project status

- **Reduce mid-project scope changes by 50%:**
  - Baseline: 3-5 major scope changes per project due to unclear requirements
  - Target: 1-2 scope changes (legitimate pivots, not requirement gaps)
  - Measurement: Scope change requests tracked in Linear/Jira integrations

#### **Key Performance Indicators (KPIs)**

**Product Quality & Engagement KPIs**

**Agent Output Approval Rate: >80% target**
- **Definition:** Percentage of agent-generated content (briefs, PRDs, architecture, stories) that users approve without requesting major revisions
- **Measurement:** Thumbs up/down on agent outputs, "Request Changes" vs. "Approve" ratio
- **Target Breakdown:**
  - Month 1-3 (MVP): 75-80% (learning phase)
  - Month 4-6: 80-85% (prompt refinement)
  - Month 7-12: 85-90% (production quality)
- **Why It Matters:** Core product value—if agents produce low-quality outputs, users won't renew

**Weekly Active Users (WAU) Engagement: >40% of total users**
- **Definition:** Percentage of total registered users who actively use RoadmapKO at least once per week
- **Target:** 40-50% WAU (industry benchmark for developer tools is 30-35%)
- **Measurement:** User sessions per week, document creation/editing activity
- **Why It Matters:** High engagement indicates product is solving real problems, not just casual browsing

**Time to First Value: <2 hours**
- **Definition:** Time from account creation to first approved document (typically Project Brief)
- **Target:** <2 hours for 80% of users
- **Measurement:** Timestamp analysis from signup to first document approval
- **Why It Matters:** Fast time-to-value reduces early churn and improves retention

**Documents Generated Per User Per Month: 8-12 target**
- **Definition:** Average number of planning documents created per active user monthly
- **Expected Distribution:**
  - Solo devs: 6-10 docs/month (1-2 projects)
  - Enterprise teams: 12-20 docs/month (3-5 concurrent initiatives)
  - Agencies: 20-40 docs/month (5-10 client projects)
- **Why It Matters:** Usage intensity indicates product stickiness and validates pricing tiers

**Business & Growth KPIs**

**Monthly Recurring Revenue (MRR): Growth targets by phase**
- **Month 3:** $500-1K (10-20 customers)
- **Month 6:** $5-10K (100-200 customers)
- **Month 9:** $15-20K (150-300 customers)
- **Month 12:** $30-40K (200-500 customers)
- **Month 18:** $80-100K (500-800 customers)
- **Why It Matters:** Primary business health metric, validates pricing and retention

**Customer Acquisition Cost (CAC): <$100 target**
- **Definition:** Total marketing/sales spend divided by new customers acquired
- **Target:** <$100 per customer (3:1 LTV:CAC ratio at $49/mo with 18-month retention)
- **Channels & Expected CAC:**
  - Product Hunt: $20-40 per customer (mostly organic)
  - ChatGPT Apps: $10-20 per customer (distribution leverage)
  - Content marketing: $30-60 per customer (SEO, blog)
  - Paid ads (Month 6+): $80-120 per customer (if needed)
- **Why It Matters:** Determines scalability and profitability of growth investments

**Monthly Churn Rate: <10% target (Starter), <5% target (Pro)**
- **Definition:** Percentage of customers who cancel subscription in a given month
- **Targets:**
  - Starter tier ($49/mo): <10% monthly churn (solo devs, higher volatility)
  - Pro tier ($149/mo): <5% monthly churn (enterprise teams, more stable)
  - Agency tier ($499/mo): <3% monthly churn (high switching costs)
- **Churn Mitigation:**
  - Month 1-3 churn (feature gaps): 15-20% expected, addressed via feature releases
  - Month 4-6 churn (quality issues): 8-12% expected, addressed via agent improvements
  - Month 7+ churn (steady state): 5-8% target
- **Why It Matters:** Retention determines LTV and long-term business viability

**Net Promoter Score (NPS): >50 target**
- **Definition:** "How likely are you to recommend RoadmapKO to a colleague?" (0-10 scale)
- **Target:** NPS >50 (world-class software: 50-70, acceptable: 30-50)
- **Measurement:** Quarterly surveys, in-app NPS prompts after 30 days of usage
- **Segment Expectations:**
  - Solo devs with AI assistants: NPS 60-70 (highest value prop)
  - Enterprise teams: NPS 45-55 (more complex needs)
  - Agencies: NPS 50-60 (margin impact resonates)
- **Why It Matters:** Leading indicator of word-of-mouth growth and referral potential

**Integration Activation Rate: 30% target (post-integration launch)**
- **Definition:** Percentage of Pro/Enterprise users who activate at least 1 integration (Linear, Jira, Notion, Azure Boards)
- **Target:** 30-40% activation within 30 days of upgrade
- **Why It Matters:** Integrations increase switching costs and reduce churn

**Customer Health Metrics**

**Documentation Completeness Score: 85%+ target**
- **Definition:** Percentage of initiatives with all required documents (Brief, PRD, Architecture, QA, Stories)
- **Automated Calculation:** RoadmapKO tracks document completion per initiative
- **Target:** 85% of active initiatives have ≥90% documentation completeness
- **Why It Matters:** Incomplete documentation indicates users aren't getting full value

**AI Coding Assistant Connection Rate: 50%+ target**
- **Definition:** Percentage of active users who have connected at least 1 AI coding assistant (MCP, API, or integration)
- **Target:** 50% within 60 days of signup
- **Why It Matters:** Core differentiator—users without AI assistant connections miss 40% of value prop

**User Satisfaction by Agent: 80%+ satisfaction per agent**
- **Definition:** User ratings (1-5 stars) per specialized agent after document completion
- **Measurement:** In-app agent rating prompts
- **Targets per agent:**
  - Discovery Agent: 4.0+ stars (research quality)
  - Requirements Agent: 4.2+ stars (PRD completeness)
  - Design Agent: 4.0+ stars (UX spec clarity)
  - Architecture Agent: 4.3+ stars (technical depth)
  - Quality Agent: 4.0+ stars (QA comprehensiveness)
  - Validation Agent: 3.8+ stars (alignment checks)
  - Planning Agent: 4.1+ stars (story detail)
- **Why It Matters:** Identifies which agents need prompt/model improvements

#### **Success Criteria for MVP (Month 3)**

RoadmapKO MVP is considered successful if it achieves ALL of the following:

✅ **Product Quality Threshold:**
- 80%+ agent output approval rate across all 7 agents
- <5% critical bug rate (blocks core workflow)
- <2 second average response time for agent interactions

✅ **User Adoption Threshold:**
- 10 design partners complete full Analysis + Planning workflow (idea → backlog)
- 100+ paid subscriptions within 2 weeks of Product Hunt launch
- 10 paying customers within 30 days of public launch

✅ **Value Validation Threshold:**
- 70%+ of beta users report "saved 5+ hours compared to manual planning" in surveys
- 60%+ of beta users say they would "definitely recommend" to colleagues (NPS >30)
- 50%+ of beta users with AI assistants report "AI coding improved with RoadmapKO context"

✅ **Technical Stability Threshold:**
- 99%+ uptime (excluding planned maintenance)
- Zero data loss incidents
- Successful completion of 100+ end-to-end workflows (signup → full backlog generation)

**If any threshold is not met:** Delay public launch, iterate with design partners, and reassess after 2-week sprint.

---

# **MVP Scope**

The RoadmapKO MVP focuses exclusively on **Analysis + Planning phases** with 7 specialized AI agents orchestrated through a three-panel workspace. The goal is to master the "front-half" of the SDLC before expanding into execution, integrations, or advanced features.

**Development Timeline:** 12 weeks (3 months)  
**Target Launch:** End of Month 3 (Private beta Week 10, Public launch Week 12)

---

## **Core Features (Must Have)**

### **1. User Authentication & Account Management**

- **Clerk-based authentication:** Email/password, Google OAuth, GitHub OAuth
- **User profile management:** Name, email, avatar, timezone settings
- **Direct paid signup:** No free trial - immediate subscription required at signup ($25/mo Pro or $50/mo Business)
- **30-day money-back guarantee:** No questions asked refund within 30 days
- **Subscription management:** Stripe integration for paid tiers, upgrade/downgrade flows, cancellation
- **Credit system:** 100 base credits included monthly, credit balance tracking, purchase additional credits
- **Usage tracking:** Document count, project count, credits consumed, credits purchased (displayed in settings)

**Rationale:** Table stakes for any SaaS product. Users need secure authentication and transparent billing. Direct paid signup filters for committed users and simplifies onboarding.

---

### **2. Project & Initiative Management**

**Project (Parent Container):**
- **Create new project:** Name, description, optional tags
- **Project dashboard:** Overview of all initiatives within project, completion status
- **Project settings:** Rename, archive, delete (with confirmation)
- **No project limits:** Unlimited projects on all tiers

**Initiative (Work Container):**
- **Create new initiative:** Name, description, automatically creates folder structure
- **Initiative states:** Draft → In Progress → Complete → Archived
- **Folder structure auto-generation:** 
  - Discovery & Research (Project Brief, Market Research, Competitive Analysis)
  - Product Definition (PRD with Functional Reqs, Non-Functional Reqs, Epics & Stories, Acceptance Criteria)
  - Design & Architecture (UX/Design Specs, UI Generation Prompts, Technical Architecture)
  - Quality & Validation (QA Strategy, Validation Review)
  - Planning & Delivery (User Stories with Tasks)

**Rationale:** Establishes the hierarchical foundation. Projects contain initiatives, initiatives contain documents. This structure enforces organizational discipline.

---

### **3. Seven Specialized AI Agents (Orchestrated Workflow)**

**Discovery Agent (Analysis Phase):**
- **Market Research generation:** Competitive landscape, user needs, market sizing, trends analysis (20 credits per generation)
- **Competitive Analysis generation:** Feature comparison tables, pricing analysis, differentiation opportunities, SWOT (20 credits per generation)
- **Project Brief generation:** Executive summary, problem statement, proposed solution, target users, goals/metrics, MVP scope, constraints/assumptions, risks (15 credits per generation)

**Requirements Agent (Planning Phase):**
- **PRD generation:** Product overview, functional requirements (FR1, FR2, FR3...), non-functional requirements (performance, security, accessibility), epic definitions, feature breakdown, user story placeholders (30 credits per generation)
- **Epic & Feature hierarchy:** Automatically structures requirements into Epic → Feature → Story hierarchy
- **Acceptance criteria templates:** GIVEN/WHEN/THEN format for each story placeholder

**Design Agent (Planning Phase):**
- **UX/UI specifications:** User flows, wireframe descriptions, component library recommendations (20 credits per generation)
- **Design tokens:** Color palettes, typography scales, spacing systems, component patterns
- **UI generation prompts:** Formatted prompts for Lovable, v0, Bolt, or other AI UI generators (10 credits per generation)
- **Accessibility guidelines:** WCAG 2.1 AA compliance checklist

**Architecture Agent (Planning Phase):**
- **Technical architecture document:** Stack recommendations (frontend, backend, database, hosting), data models with entity-relationship descriptions, API endpoint specifications (REST/GraphQL), infrastructure requirements, security architecture (25 credits per generation)
- **Architectural Decision Records (ADRs):** Template for documenting "why we chose X over Y" decisions
- **Integration requirements:** Third-party APIs, authentication patterns, deployment pipelines

**Quality Agent (Planning Phase):**
- **QA Strategy document:** Test pyramid (unit/integration/e2e ratios), data management strategy, environment management (dev/staging/prod), accessibility testing approach, performance testing approach, security testing approach (20 credits per generation)
- **Test planning:** Critical path identification, edge case documentation, acceptance test scenarios

**Validation Agent (Cross-Phase Orchestrator):**
- **Cross-document alignment checks:** PRD references Project Brief correctly, Architecture aligns with PRD requirements, User Stories trace to Features (10 credits per review)
- **Completeness validation:** All required sections present per document type
- **Gap identification:** Missing dependencies flagged before phase progression
- **Approval workflow management:** Routes documents to user for review, tracks approval status

**Planning Agent (Planning Phase):**
- **User Story elaboration:** Converts story placeholders into fully-detailed stories with title, description, acceptance criteria, technical references from architecture, estimated story points, tasks breakdown (5 credits per story)
- **Task generation:** 3-8 tasks per story with technical implementation details
- **Backlog prioritization:** MoSCoW method (Must/Should/Could/Won't), dependency mapping

**Agent Orchestration:**
- **Single conversational interface:** Users interact with one orchestrator agent visible in chat panel
- **Transparent delegation:** Orchestrator announces when delegating to specialists ("Calling Architecture Agent to design your data model...")
- **Sequential phase unlocking:** Discovery & Research must complete before Product Definition unlocks
- **Elicitation prompts:** Numbered choice prompts (1-7 options) to guide user decisions and prevent blank-page paralysis
- **Agent personality & tone:** Each agent has distinct voice (Discovery is curious/enthusiastic, Architecture is systematic/detail-oriented, etc.)

**Credit Consumption Summary:**
- **Small Initiative (5 user stories):** ~195 credits (Brief 15 + Research 20 + Comp Analysis 20 + PRD 30 + Design 20 + UI Prompts 10 + Architecture 25 + QA 20 + Validation 10 + 5 Stories 25)
- **Medium Initiative (15 user stories):** ~245 credits
- **Large Initiative (30 user stories):** ~345 credits
- **100 base credits = ~1 small initiative/month OR partial work on 2-3 initiatives**

**Rationale:** The 7-agent workflow is the core product differentiator. This is what users pay for—AI experts that produce professional-grade planning documentation. Credit consumption creates variable revenue stream.

---

### **4. Three-Panel Workspace UI**

**Left Panel: Initiative Workflow Navigator**
- **Collapsible phase sections:** Discovery & Research, Product Definition, Design & Architecture, Validation & Handoff
- **Document tree hierarchy:** Visual tree showing all artifacts within initiative
- **Progress indicators:** Checkmarks (✓ Complete), lightning bolts (⚡ In Progress), circles (○ Not Started), locks (🔒 Locked)
- **Phase completion percentage:** Real-time calculation (e.g., "Planning 35%")
- **Click to preview:** Clicking any document loads it in right panel
- **Estimated time remaining:** Updates dynamically as sections complete

**Middle Panel: Agent Chat Interface**
- **Active agent indicator:** Shows which specialized agent is currently working (e.g., "PM Agent: Active")
- **Conversational interaction:** Natural language back-and-forth with orchestrator agent
- **Inline document previews:** Agent drafts rendered directly in chat for immediate review
- **Elicitation prompts with numbered options:** 1-7 choice menus for guided decision-making
- **User input box:** Text input for responses
- **Agent history navigation:** "Previous Agents" and "View All Chats" buttons to review past interactions
- **Typing indicators & progress updates:** "Discovery Agent is researching competitors..." with animated indicators
- **Mode indicator:** Shows "Interactive Mode" or "YOLO Mode" in top-right

**Right Panel: Document Preview & Actions**
- **Live markdown rendering:** Real-time display of selected document with proper formatting (react-markdown)
- **Collapsible sections:** Expand/collapse document sections for readability
- **Approval status badges:** ✓ Approved, 🔄 Awaiting Review, ⚠️ Needs Revision
- **Version indicator:** Shows current version (e.g., "v0.6 Draft")
- **Section-level status:** Granular tracking of which sections are complete vs. pending
- **Action buttons:** Export (markdown/PDF), History (version timeline - simplified in MVP)
- **TipTap editing:** Deferred to Phase 4 (MVP is markdown-only)

**Bottom Status Bar:**
- **Active agent & phase:** "PM Agent: Active | Product Definition"
- **Progress tracking:** "§ 3/12 sections complete"
- **Time estimates:** "Elapsed: 2h 15m | Est. remaining: 45m"
- **Mode indicator:** "Interactive Mode"
- **Credit balance:** "Credits: 87 remaining" with visual indicator
- **Keyboard shortcuts hint:** "Press ? for shortcuts" (shortcuts post-MVP)

**Responsive Design:**
- **Desktop-first:** Optimized for 1920x1080 and above
- **Tablet support (iPad Pro):** 3-panel layout collapses to 2-panel (left panel becomes drawer)
- **Mobile (post-MVP):** Single-panel with tab navigation

**Rationale:** The three-panel workspace is the signature UX that differentiates RoadmapKO from generic chat interfaces. It maintains context across hierarchy, conversation, and document preview simultaneously. Credit balance visibility drives purchase behavior.

---

### **5. Document Generation & Management**

**Document Types Supported (MVP):**
- Project Brief (Analysis phase)
- Market Research (Analysis phase)
- Competitive Analysis (Analysis phase)
- PRD with Functional Requirements (Planning phase)
- PRD with Non-Functional Requirements (Planning phase)
- PRD with Epics & Stories (Planning phase)
- PRD with Acceptance Criteria (Planning phase)
- UX/Design Specifications (Planning phase)
- UI Generation Prompts (Planning phase)
- Technical Architecture (Planning phase)
- QA Strategy (Planning phase)
- Validation Review (Planning phase)
- User Stories with Tasks (Planning phase)

**Document Features:**
- **Auto-save:** Every agent output automatically saved to Supabase
- **Version history (simplified):** Track major versions (v0.1, v0.2, etc.), not real-time diffs (full history post-MVP)
- **Markdown storage:** All documents stored as markdown in PostgreSQL
- **Cross-document references:** Automatic linking (e.g., "As defined in Architecture Doc Section 3.2...")
- **Export capabilities:** 
  - Markdown (.md) export for all documents
  - PDF export for Project Brief and PRD (using Puppeteer or react-pdf)
  - ZIP archive export for full initiative (all documents bundled)

**Document Approval Workflow:**
- **States:** Draft → Awaiting Review → Approved → Locked
- **User actions:** 
  - "Request Changes" (sends back to agent with feedback)
  - "Approve" (locks section, moves to next)
  - "Unlock" (reopens for editing, requires re-validation)
- **Locked document editing:** Requires explicit unlock + re-validation by Validation Agent

**Rationale:** Documents are the core deliverable. Users need reliable storage, versioning, and export to make RoadmapKO their system of record.

---

### **6. Approval Gates & Human-in-the-Loop**

**Section-Level Approval:**
- After agent completes each section (e.g., "Functional Requirements" within PRD), user must approve before proceeding
- **Approval options:**
  1. ✅ **Approve** (proceed to next section)
  2. 🔄 **Request minor changes** (agent revises, re-presents)
  3. ❌ **Reject & rewrite** (agent starts section over with new guidance)

**Phase-Level Validation:**
- At end of each phase (Analysis, Planning), Validation Agent performs cross-document check
- **Validation checks:**
  - **Completeness:** All required sections present
  - **Consistency:** PRD requirements align with Project Brief goals
  - **Quality:** Documents meet minimum length/detail thresholds
  - **Traceability:** Stories trace to Features, Features to Epics, Epics to Brief
- **Validation outcomes:**
  - ✅ **Pass:** Phase unlocks next phase
  - ⚠️ **Pass with warnings:** Proceed but with noted gaps (user acknowledges)
  - ❌ **Fail:** Must address critical gaps before proceeding

**Override Capability:**
- Users can skip validation and proceed (displays "At Risk" warning on initiative)
- Tracked for analytics: "% of users who override validation"

**Rationale:** Human-in-the-loop ensures users maintain control and trust AI outputs. Approval gates prevent "garbage in, garbage out" cascading across phases.

---

### **7. Credit-Based Pricing System**

**Pricing Tiers:**

**Pro Tier - $25/month**
- **Target:** Solo developers, indie hackers, vibe coders
- **Base Credits:** 100 credits/month included
- **Features:**
  - All 7 AI agents
  - Unlimited projects
  - Unlimited initiatives
  - Private projects
  - User roles & permissions
  - Markdown & PDF export
  - Email support (48-hour SLA)
  - Shared across unlimited users

**Business Tier - $50/month**
- **Target:** Growing teams, agencies, AI-native engineering teams
- **Base Credits:** 100 credits/month included (same as Pro, upsell is features)
- **All features in Pro, plus:**
  - Internal publish (share read-only docs via link)
  - SSO (Google Workspace, Microsoft, Okta) - Phase 3
  - Personal Projects (separate workspace from team projects)
  - Opt out of data training (agents won't train on your docs)
  - Design templates (pre-built initiative templates) - Phase 3
  - Integrations (Linear, Jira, Notion, Azure Boards) - Phase 3

**Enterprise Tier - Custom Pricing**
- **Target:** Large organizations
- **Base Credits:** Negotiated (typically 400+ credits/month minimum)
- **All features in Business, plus:**
  - Dedicated support (Slack channel, video calls)
  - Onboarding services (white-glove setup, training)
  - Custom connections (bespoke integrations, API access)
  - Group-based access control (RBAC with custom roles)
  - Custom design systems (branded templates, style guides)
  - SLA guarantees (99.9% uptime, priority support)
  - Volume discounts on credit purchases

**Credit Purchase Options (All Tiers):**

**Pay-As-You-Go Credit Packs:**
- **100 credits** - $10 ($0.10/credit)
- **200 credits** - $18 ($0.09/credit) - Save 10%
- **400 credits** - $32 ($0.08/credit) - Save 20%
- **800 credits** - $56 ($0.07/credit) - Save 30%
- **1200 credits** - $72 ($0.06/credit) - Save 40%
- **2000 credits** - $100 ($0.05/credit) - Save 50%
- **3000 credits** - $135 ($0.045/credit) - Save 55%
- **4000 credits** - $160 ($0.04/credit) - Save 60%

**Credits never expire** - Roll over month-to-month

**Recurring Credit Subscriptions (Optional Add-On):**
- **+100 credits/month** - $9/month (10% discount vs. one-time)
- **+200 credits/month** - $16/month (11% discount)
- **+400 credits/month** - $28/month (13% discount)
- **+800 credits/month** - $48/month (14% discount)

**Low Credit Warnings:**
- At 20 credits remaining: "You're running low on credits. Top up now to avoid interruptions."
- At 10 credits: "Almost out! Click here to buy more credits instantly."
- At 0 credits: "Out of credits. Your next generation will fail. [Buy Credits]"

**Credit Balance Visibility:**
- **Top-right corner of UI:** "Credits: 87 remaining" with progress bar
- **Hover tooltip:** "You have 87 credits left. This is enough for ~1 small initiative. [Buy More]"
- **Settings page:** Full credit transaction history (earned, spent, purchased)

**Rationale:** Credit-based model creates two revenue streams (subscription + variable usage). Lower base subscription ($25 vs. $49) reduces entry barrier. Heavy users naturally pay more. Shared unlimited users enables team collaboration from Day 1 without per-seat pricing complexity.

---

### **8. Subscription Management**

**No Free Trial - Direct Paid Signup:**
- **Immediate paid subscription** required at signup
- **Credit card required** via Stripe Checkout
- **First month charged immediately** ($25 for Pro, $50 for Business)
- **100 base credits included** in first month
- **30-day money-back guarantee** (refund subscription + unused credits)

**Starter Experience:**
- New user signs up for Pro tier ($25/mo)
- Receives 100 credits immediately
- Can complete 1 small initiative or partial work on multiple initiatives
- If they run out of credits in Month 1, prompted to buy more ($10 for 100 credits)
- Month 2: Another 100 credits added automatically
- Average user likely needs 200-400 credits/month for active usage → generates $18-32/month in credit purchases

**Revenue Model Math:**
- **Pro tier user (active):** $25/mo subscription + $24/mo avg credit purchases = **$49/mo total ARPU**
- **Business tier user (active team):** $50/mo subscription + $48/mo avg credit purchases = **$98/mo total ARPU**
- **Blended ARPU target:** $55-75/month (subscription + credits)

**Subscription Actions:**
- **Signup:** Direct to paid via Stripe Checkout ($25/mo Pro or $50/mo Business)
- **Downgrade:** Business → Pro (lose Business features, keep credits)
- **Cancel:** User can cancel anytime, receives refund if within 30 days, otherwise access until end of billing period, then read-only
- **Reactivate:** User can reactivate within 90 days without losing data

**Payment Processing:**
- **Stripe integration:** Checkout, Customer Portal, webhook handlers for subscription events
- **Invoice generation:** Automatic monthly invoices via Stripe
- **Failed payment handling:** 3 retry attempts, then account suspended (read-only), email notifications
- **Refund processing:** Automated refund for cancellations within 30 days

**Rationale:** No free trial reduces tire-kickers and improves customer quality. $25/mo is low enough for impulse purchase. 30-day guarantee provides risk mitigation. Variable credit model aligns revenue with value delivered.

---

### **9. Onboarding & First-Run Experience**

**Signup Flow:**
1. Landing page → "Get Started with Pro - $25/mo" CTA
2. Clerk authentication (email, Google, or GitHub)
3. Tier selection (Pro $25/mo or Business $50/mo)
4. Payment collection (Stripe Checkout)
5. Account creation → **100 credits added immediately**
6. Onboarding wizard (3 steps)

**Onboarding Wizard:**

**Step 1: Welcome & Value Prop (30 seconds)**
- "Welcome to RoadmapKO! You're now a Pro member with 100 credits."
- "Let's create your first project and get you to a complete backlog in 2 hours."
- "Remember: 30-day money-back guarantee if RoadmapKO doesn't deliver value."

**Step 2: First Project Creation (1 minute)**
- "What are you building?" (name input)
- "Describe your idea in 1-2 sentences" (description input)
- Auto-creates first project and first initiative

**Step 3: Mode Selection (30 seconds)**
- "How would you like to work?"
- **Interactive Mode:** "Work with agents section-by-section (recommended for first time)"
- **YOLO Mode:** "Generate complete draft, then refine (faster, requires more review)"
- User selects, saved as preference

**Post-Onboarding:**
- User lands in three-panel workspace with first initiative open
- Discovery Agent begins conversation: "Great! Let's start with market research. Tell me: who is your target user?"
- Inline tooltips highlight UI elements (left panel, chat, preview) on first use
- Progress checklist in top-right: "☐ Complete first Project Brief ☐ Generate first PRD ☐ Create first User Story"
- Credit balance prominently displayed: "Credits: 100 remaining"

**Rationale:** Smooth onboarding reduces abandonment. Users need to reach "first value" (completed Project Brief) within 2 hours to justify payment. Credit visibility creates urgency to engage before credits run out.

---

## **Out of Scope for MVP (Phase 2+)**

### **Deferred to Phase 2 (Months 4-6): Distribution Channels**
- ❌ ChatGPT Apps SDK integration
- ❌ Claude Desktop MCP integration
- ❌ API documentation for third-party integrations

### **Deferred to Phase 3 (Months 7-9): Integrations & System-of-Record**
- ❌ Linear integration (OAuth, bidirectional sync)
- ❌ Jira integration (OAuth, bidirectional sync)
- ❌ Notion integration (OAuth, export/import)
- ❌ Azure Boards integration
- ❌ GitHub Projects integration
- ❌ Slack notifications

### **Deferred to Phase 4 (Months 10-12): Advanced UI & Editing**
- ❌ TipTap rich text editing (inline document editing in right panel)
- ❌ Keyboard shortcuts (vim-mode, command palette)
- ❌ Canvas visualization (initiative mind-map, dependency graphs)
- ❌ Collaborative editing (multi-user real-time editing)
- ❌ Comment threads (inline document commenting)
- ❌ @mention notifications

### **Deferred to Phase 5 (Months 13-15): Team Collaboration**
- ❌ Team workspaces (shared projects across team members)
- ❌ Role-based access control (Admin, Editor, Viewer)
- ❌ Activity feed (team member actions, document updates)
- ❌ Team analytics dashboard

### **Deferred to Phase 6 (Months 16-18): Analytics & Intelligence**
- ❌ Project health scoring (velocity tracking, risk indicators)
- ❌ Predictive planning (AI suggests timeline adjustments)
- ❌ Portfolio management (cross-project dependency tracking)
- ❌ Custom agent training (fine-tune agents on user's historical docs)
- ❌ ROI reporting (planning time saved, rework reduction metrics)

### **Deferred to Phase 7 (Year 2+): Execution & DevOps**
- ❌ Sprint planning features (cycle management, velocity tracking)
- ❌ Burndown charts and execution analytics
- ❌ Git commit integration (link commits to stories)
- ❌ CI/CD pipeline integration (deployment tracking)
- ❌ Observability integration (Datadog, Sentry)
- ❌ Incident management (postmortem generation)

### **Deferred to Phase 8 (Year 2+): Brownfield Migration**
- ❌ Import existing projects from Linear/Jira
- ❌ AI-assisted documentation backfill (analyze existing codebase, generate missing docs)
- ❌ Requirement extraction from existing codebases
- ❌ Legacy project health assessment

### **Out of Scope (Not Planned):**
- ❌ Mobile native apps (iOS, Android)
- ❌ Desktop native apps (Electron)
- ❌ AI code generation (remains AI coding assistant's job)
- ❌ Time tracking features (use Toggl, Harvest, etc.)
- ❌ Invoicing/billing for client projects (use FreshBooks, QuickBooks, etc.)
- ❌ Design tool integrations (Figma plugins, Sketch)
- ❌ White-label/self-hosted options (until agency tier demand proven)

---

## **MVP Success Criteria**

The MVP is considered complete and ready for launch when ALL of the following are achieved:

### **✅ Functional Completeness:**
- All 7 agents successfully generate their respective documents (Brief, Research, Comp Analysis, PRD, Design, Architecture, QA, Stories)
- Users can complete full workflow from idea → execution-ready backlog without errors
- Three-panel workspace renders correctly on desktop (1920x1080+) and tablet (iPad Pro)
- Export functionality works for markdown and PDF
- Direct paid signup flow works end-to-end with Stripe
- Credit purchase and consumption system functional

### **✅ Quality Thresholds:**
- 80%+ agent output approval rate across 10 design partner test initiatives
- <5 critical bugs (workflow blockers)
- <2 second average response time for agent chat interactions
- 99%+ uptime over 2-week private beta period

### **✅ User Validation:**
- 10 design partners complete full workflow (paid $12.50/mo discount)
- 70%+ report "saved 5+ hours compared to manual planning"
- 60%+ report "would recommend to colleagues" (NPS >30)
- <20% refund requests within 30-day guarantee window
- Zero data loss incidents during beta testing

### **✅ Technical Stability:**
- Supabase database schema finalized and migrated
- Google ADK + Vertex AI agent orchestration stable (no timeout errors)
- Stripe webhooks handling all subscription events correctly
- Clerk + Supabase user sync working reliably
- Error logging and monitoring operational (Sentry)

**If criteria not met:** Extend private beta by 1-2 weeks, address gaps, retest with design partners before public launch.

---

## **MVP Development Phases (12-Week Timeline)**

### **Weeks 1-2: Foundation & Setup**
- Initialize Turborepo monorepo structure
- Set up Vercel project (dev, staging, production environments)
- Configure Supabase (PostgreSQL, Auth, Storage)
- Implement Clerk authentication (email, Google, GitHub OAuth)
- Create base Next.js app with Tailwind + Untitled UI components
- Design database schema (users, subscriptions, projects, initiatives, documents, credit_transactions)
- Set up Vertex AI project (enable APIs, service accounts)
- **Deliverable:** "Hello World" deployed to Vercel with authentication working

### **Weeks 3-4: Agent Orchestration & Discovery Agent**
- Integrate Google ADK (TypeScript SDK, agent orchestration)
- Build orchestrator agent (delegates to sub-agents, manages conversation state)
- Implement Discovery Agent (generates Project Brief, Market Research, Competitive Analysis)
- Create markdown storage and retrieval system
- Build basic three-panel layout (static, no real-time updates yet)
- **Deliverable:** Users can have conversation with Discovery Agent and generate Project Brief

### **Weeks 5-6: Analysis Phase Completion**
- Enhance Discovery Agent prompts for Market Research and Competitive Analysis
- Implement document approval workflow (Draft → Review → Approved states)
- Build left panel Initiative Workflow navigator with progress indicators
- Add document preview in right panel with markdown rendering
- Implement phase gating (Analysis must complete before Planning unlocks)
- **Deliverable:** Users can complete full Analysis phase (3 documents approved)

### **Weeks 7-8: Planning Phase - Requirements & Architecture**
- Implement Requirements Agent (PRD generation with Functional/Non-Functional Requirements, Epics, Features, Story placeholders)
- Implement Architecture Agent (Technical Architecture with stack, data models, APIs)
- Build Epic → Feature → Story hierarchy in left panel
- Add Validation Agent cross-document alignment checks
- **Deliverable:** Users can generate PRD and Architecture documents

### **Weeks 9-10: Planning Phase Completion**
- Implement Design Agent (UX specs, design tokens, Lovable/v0 prompts)
- Implement Quality Agent (QA Strategy document)
- Implement Planning Agent (convert story placeholders to fully-detailed stories with tasks)
- Add elicitation prompts with numbered choice options (1-7 choices)
- Implement document export (markdown and PDF via Puppeteer)
- **Deliverable:** Users can complete full Planning phase (all 7 agent outputs)

### **Weeks 11-12: MVP Polish, Credit System, Beta Launch**
- Integrate Stripe (Checkout, Customer Portal, webhook handlers)
- Implement credit system (balance tracking, consumption, purchase flow, warnings)
- Build onboarding wizard (3-step first-run experience)
- Add status bar (agent status, progress, time estimates, credit balance)
- Performance optimization (lazy loading, caching, response time <2s)
- Bug fixing and edge case handling
- Write Mintlify documentation (user guides, FAQs)
- **Week 11:** Private beta launch with 10 design partners
- **Week 12:** Validate success criteria, prepare for public launch

---

### **Post-MVP Vision**

RoadmapKO's post-MVP roadmap focuses on three strategic pillars: **(1) Distribution Channel Expansion** to reach users where they already work, **(2) Integration Ecosystem** to become the system-of-record for planning while syncing to execution tools, and **(3) Platform Intelligence** to evolve agents from reactive assistants to proactive planning partners. Each phase builds on the previous, creating compounding value and defensibility.

---

#### **Phase 2: Distribution Channel Expansion (Months 4-7)**

**Goal:** Meet users in their existing AI workflows—ChatGPT and Claude Desktop—without requiring them to visit a separate web app.

**ChatGPT Apps SDK Integration (Month 4-5)**

**What:** Native ChatGPT App that allows users to access RoadmapKO agents directly within ChatGPT interface
- **User Experience:** 
  - "Hey ChatGPT, use RoadmapKO to help me plan my SaaS idea"
  - ChatGPT invokes RoadmapKO agents via SDK
  - Documents sync to user's RoadmapKO account automatically
  - Users can switch between ChatGPT interface and RoadmapKO web app seamlessly
  
**Distribution Advantage:**
- Access to 800M+ ChatGPT users (200M+ paid subscribers)
- Zero marketing cost to reach massive audience
- ChatGPT App Store discovery and recommendations
- Users already comfortable with conversational AI interface

**Monetization:**
- ChatGPT users must have RoadmapKO subscription to activate app
- Credit consumption works identically (deducted from RoadmapKO account)
- Subscription prompt: "Start Pro tier ($25/mo) to unlock RoadmapKO agents"

**Technical Implementation:**
- OpenAI ChatGPT Apps SDK (REST API integration)
- OAuth authentication (link ChatGPT to RoadmapKO account)
- Webhook handlers for ChatGPT → RoadmapKO sync
- Document storage in RoadmapKO (ChatGPT displays, RoadmapKO stores)

**Success Metrics:**
- 500+ ChatGPT App installations in first 30 days
- 10% conversion rate from app install to paid RoadmapKO subscription
- 50 new paying customers via ChatGPT channel (Month 4-5)

---

**Claude Desktop MCP Integration (Month 6-7)**

**What:** Model Context Protocol (MCP) server that gives Claude Code CLI and Claude Desktop users direct access to RoadmapKO planning context

**User Experience:**
- **Scenario 1: Planning in Claude Desktop**
  - User: "Help me plan a B2B scheduling app with RoadmapKO"
  - Claude Desktop (via MCP): Connects to RoadmapKO, orchestrates Discovery/Planning agents
  - All documents saved to RoadmapKO account
  
- **Scenario 2: Development with Claude Code CLI**
  - Developer working in terminal with Claude Code
  - Claude Code reads RoadmapKO context via MCP: "I can see from your Architecture doc that you're using Supabase with PostgreSQL. I'll generate the user authentication schema following your security requirements..."
  - Claude Code writes implementation notes back to RoadmapKO: "Story 1.1 completed. Auth flow implemented per spec."

**Distribution Advantage:**
- Direct access to Claude's growing developer user base
- Tight integration with AI coding workflow (planning → coding in same tool)
- First-mover advantage (MCP ecosystem still nascent in 2025)
- Anthropic may feature RoadmapKO in MCP showcase

**Monetization:**
- MCP users require RoadmapKO subscription (Pro or Business tier)
- Credit consumption identical to web app
- Developers using Claude Code are high-value users (willing to pay for productivity tools)

**Technical Implementation:**
- MCP server specification (TypeScript/Python)
- Tools exposed: `create_initiative`, `generate_document`, `read_context`, `update_status`
- Resources exposed: Full planning hierarchy (briefs, PRDs, architecture, stories)
- Bidirectional sync: MCP reads + writes to RoadmapKO

**Success Metrics:**
- 200+ MCP server installations in first 30 days
- 15% conversion rate from MCP install to paid subscription (developers have higher intent)
- 30 new paying customers via MCP channel (Month 6-7)

---

**Phase 2 Success Criteria:**
- 100 total new customers from distribution channels (ChatGPT + MCP)
- $8-10K MRR total (150-200 total customers)
- 40% of new signups originate from ChatGPT/MCP (proves channel viability)
- <8% monthly churn (distribution channels may have higher churn, monitor closely)

---

#### **Phase 3: Integration Ecosystem (Months 8-10)**

**Goal:** Become the system-of-record for planning while syncing execution to tools teams already use (Linear, Jira, Notion, Azure Boards).

**System-of-Record Philosophy:**

RoadmapKO is **not** an execution tool competitor. Instead, it's the **upstream planning layer** that feeds execution tools:
- **Planning happens in RoadmapKO:** Briefs, PRDs, Architecture, Stories (with full context)
- **Execution happens in Linear/Jira:** Sprint planning, task status updates, burndown charts
- **Full context preserved in RoadmapKO:** Even if users switch execution tools, planning history remains

**Why This Matters:**
- Execution tools (Linear, Jira) strip away planning context to stay lightweight
- When engineers ask "Why did we choose this architecture?", answer lives in RoadmapKO, not Jira comments
- Platform migration safety: Switch from Linear to Jira? Planning context stays in RoadmapKO

---

**Integration 1: Linear (Month 8)**

**Capabilities:**
- **OAuth authentication:** Secure connection to user's Linear workspace
- **One-way sync (RoadmapKO → Linear):**
  - Export initiatives as Linear projects
  - Export epics as Linear milestones
  - Export user stories as Linear issues (with descriptions, acceptance criteria, labels)
  - Map RoadmapKO hierarchy to Linear structure
  
- **Metadata sync:**
  - Story points → Linear estimate
  - Status (Not Started/In Progress/Complete) → Linear status
  - Assignees → Linear assignees (if team members linked)
  
- **Link preservation:**
  - Every Linear issue has "View in RoadmapKO" link in description
  - Every RoadmapKO story has "View in Linear" link
  
**User Workflow:**
1. Complete planning in RoadmapKO (Brief → Stories)
2. Click "Export to Linear" button
3. Select Linear project/team to sync to
4. Stories pushed to Linear as issues
5. Team works in Linear for sprint execution
6. Engineers click "View in RoadmapKO" when they need full context (architecture, acceptance criteria, dependencies)

**Why One-Way Sync (Initially):**
- Simpler to build and maintain
- Avoids sync conflicts (single source of truth: RoadmapKO for planning, Linear for execution status)
- Status updates can be pulled manually via Linear API if needed (post-MVP enhancement)

**Future Enhancement (Phase 4):** Bidirectional status sync (Linear issue status → RoadmapKO story status)

---

**Integration 2: Jira (Month 9)**

**Capabilities:** Similar to Linear, adapted for Jira's structure:
- OAuth authentication (Atlassian API)
- One-way sync: RoadmapKO → Jira
- Initiative → Jira Epic
- Story → Jira Story/Task
- Metadata mapping (story points, status, priority, assignees)
- Link preservation (bidirectional "View in X" links)

**Enterprise Focus:**
- Jira users are typically larger orgs (target: Business/Enterprise tier)
- Jira integration unlocks enterprise sales conversations
- Jira's complexity makes RoadmapKO's structure even more valuable

---

**Integration 3: Notion (Month 10)**

**Capabilities:**
- OAuth authentication (Notion API)
- **Export to Notion:** RoadmapKO documents → Notion pages
  - Initiative → Notion database entry
  - Documents → Notion pages (markdown converted to Notion blocks)
  - Hierarchy preserved in Notion page structure
  
- **Use Case:** Teams using Notion for wikis/docs want planning artifacts accessible there
- **Not bidirectional:** Notion is documentation destination, not execution tool

---

**Integration 4: Azure Boards (Month 10)**

**Capabilities:** Similar to Jira:
- OAuth authentication (Azure DevOps API)
- One-way sync: RoadmapKO → Azure Boards
- Initiative → Azure Epic
- Story → Azure User Story
- Metadata mapping

**Enterprise Focus:**
- Azure Boards users are Microsoft-heavy enterprises
- Integration required for enterprise sales to Microsoft shops
- Often paired with Azure DevOps pipelines (future observability integration opportunity)

---

**Integration Tier Unlock:**
- **Pro tier ($25/mo):** No integrations (keeps pricing accessible)
- **Business tier ($50/mo):** Unlock all 4 integrations (Linear, Jira, Notion, Azure Boards)
- **Enterprise tier (Custom):** Custom integrations, bespoke connectors, API access

**Phase 3 Success Criteria:**
- 30% of Business/Enterprise customers activate at least 1 integration
- 50 total Business/Enterprise customers ($5K+ MRR from these tiers)
- $18-22K total MRR (250-300 total customers)
- Integration activation reduces churn by 15% (higher switching costs)

---

#### **Phase 4: Platform Intelligence & Polish (Months 11-14)**

**Goal:** Evolve agents from reactive assistants to proactive planning partners. Add polish features that improve daily UX.

---

**Advanced Agent Capabilities (Month 11-12)**

**Intelligent Backfilling (Core Differentiator):**
- **Gap Detection:** If user starts discussing features without PRD, agent recognizes gap and offers to backfill
  - "I notice you're defining features, but we don't have a Project Brief yet. Should I create one based on what you've told me so far?"
  
- **Dependency Validation:** If architecture defined before requirements, Validation Agent flags inverted dependency
  - "Warning: You're designing architecture without finalized requirements. This risks misalignment. Should we complete the PRD first?"
  
- **Automatic Cascading Updates:** If user updates Project Brief goals, agent offers to update PRD requirements accordingly
  - "Your Project Brief goals changed. Should I review the PRD and update features to align with new objectives?"

**Proactive Planning Intelligence:**
- **Risk Detection:** Quality Agent analyzes initiative and flags risks
  - "I notice Feature 2.3 has no security testing defined, but it handles payment data. This is a compliance risk. Should I add security test scenarios?"
  
- **Dependency Mapping:** Architecture Agent identifies cross-feature dependencies
  - "Feature 1.2 (User Authentication) must complete before Feature 3.1 (Profile Management). I've marked this dependency—should I reorder the backlog?"
  
- **Scope Creep Detection:** Validation Agent monitors story additions mid-initiative
  - "You've added 8 new stories since Epic 1 was approved. This increases timeline by 3 weeks. Should we move these to Epic 2 or descope Epic 1?"

---

**TipTap Rich Text Editing (Month 12)**

**What:** Replace markdown-only preview with inline rich text editing (TipTap editor)

**Capabilities:**
- **Inline editing:** Users can edit agent-generated documents directly in right panel
- **Formatting toolbar:** Bold, italic, lists, headings, code blocks, tables
- **Collaborative editing (post-Phase 4):** Real-time multi-user editing with presence indicators
- **Comment threads:** Inline comments on specific sections (e.g., "@john should we use PostgreSQL or MongoDB here?")
- **Version diffing:** Visual comparison between document versions

**User Workflow:**
1. Agent generates PRD
2. User reviews in right panel
3. User clicks "Edit" button → TipTap editor activates
4. User makes inline edits (add bullet points, rewrite sections)
5. User clicks "Save" → agent reviews changes, offers to regenerate downstream docs if needed
6. "Request Agent Review" button: Agent analyzes user edits and suggests improvements

**Why Deferred to Phase 4:**
- Adds complexity to MVP (markdown storage simpler)
- Users can export to Google Docs for rich editing in MVP
- Want to validate core agent quality first before adding editing features

---

**Keyboard Shortcuts & Power User Features (Month 13)**

**What:** Keyboard-driven navigation for power users

**Shortcuts:**
- `Cmd+K`: Command palette (search documents, navigate hierarchy, invoke agents)
- `Cmd+N`: New initiative
- `Cmd+E`: Export current document
- `Cmd+/`: Focus chat input
- `Cmd+1/2/3`: Switch between panels (hierarchy/chat/preview)
- `Cmd+↑/↓`: Navigate document hierarchy
- `Cmd+Enter`: Approve current section
- `Vim mode (optional)`: `h/j/k/l` navigation for vim users

**Power User Benefits:**
- Reduces mouse usage for developers (keyboard-first)
- Faster workflow for users managing multiple initiatives
- Competitive differentiation vs. mouse-heavy tools like Notion

---

**Gamification & Engagement (Month 14)**

**What:** Subtle engagement features to increase usage and reduce churn

**Features:**
- **Streaks:** "7-day planning streak! You've completed 3 initiatives this week."
- **Achievements:** "🏆 First Initiative Complete", "🚀 Speed Demon (completed initiative in <2 hours)", "📚 Documentation Master (all docs have >90% completeness)"
- **Confetti animations:** When user approves final story and backlog is complete
- **Agent personality evolution:** Agents remember user preferences over time
  - "Last time you preferred MoSCoW prioritization over story points. Should I use MoSCoW again?"
  
**Why It Works:**
- Increases engagement without being intrusive
- Reduces churn by creating habit loops
- Makes planning feel less like "work" and more enjoyable

---

**Phase 4 Success Criteria:**
- 200-250 total customers
- $25-32K MRR (subscription + credits)
- <5% monthly churn (gamification + polish reduces churn)
- 85%+ agent output approval rate (intelligent backfilling improves quality)
- 60%+ weekly active users (engagement features drive usage)

---

#### **Long-Term Vision (Year 2+)**

**Autonomous Planning Intelligence (Months 15-18)**

**Concept:** Agents transition from "reactive drafters" to "proactive planning partners"

**Capabilities:**
- **Predictive Planning:** 
  - "Based on your team's velocity (12 story points/sprint), Epic 2 will take 6 sprints. Consider descoping Feature 2.3 to hit your Q2 deadline."
  
- **Portfolio Intelligence:**
  - "You have 3 concurrent initiatives. Initiative B depends on Initiative A's authentication architecture. I recommend sequencing: A → B → C."
  
- **Automated Health Monitoring:**
  - "Initiative Alpha hasn't been updated in 3 weeks, but 5 stories are marked 'In Progress' in Linear. Should I check in with the team?"
  
- **Continuous Validation:**
  - Validation Agent runs nightly: "I detected misalignment: PRD says 'PostgreSQL' but Architecture doc now specifies 'MongoDB'. Should I flag this for review?"

---

**Brownfield Migration & Legacy Documentation (Months 16-18)**

**Problem:** Teams have existing projects with fragmented documentation scattered across Notion/Confluence/Jira. They want to migrate to RoadmapKO without starting from scratch.

**Solution:** AI-powered documentation backfill

**Capabilities:**
- **Import existing artifacts:**
  - Upload Google Docs, Notion exports, Confluence pages
  - RoadmapKO analyzes and categorizes: "This looks like a PRD. Should I import it as the Product Definition document?"
  
- **Gap identification:**
  - "I found a PRD but no Project Brief or Architecture doc. Should I generate these based on the PRD?"
  
- **Codebase analysis (advanced):**
  - Connect to GitHub repository
  - Architecture Agent analyzes codebase: "I detected 23 API endpoints, PostgreSQL schema, Next.js frontend. Should I generate an Architecture doc reflecting your current implementation?"
  
- **Reconciliation workflow:**
  - "Your PRD says 'real-time notifications' but I don't see this in your codebase. Is this planned or should I remove from PRD?"

**Use Case:**
- Existing startups with 1-2 years of development
- Agencies taking over client projects with poor documentation
- Enterprises wanting to standardize documentation across 20+ legacy projects

**Monetization:**
- Brownfield migration as Enterprise tier feature
- Professional services: $5K flat fee for migration assistance

---

**The Platform Play: RoadmapKO as SDLC Operating System (Year 2-3)**

**Vision:** RoadmapKO becomes the shared context layer that all AI development tools connect to

**Integrations Beyond Execution Tools:**
- **Design tools:** Figma plugin reads RoadmapKO UX specs, writes design file references back
- **Testing tools:** Playwright/Cypress tests reference RoadmapKO acceptance criteria
- **Deployment tools:** Vercel/Netlify read RoadmapKO infrastructure requirements
- **Observability tools:** Datadog/Sentry incidents link to RoadmapKO stories for root cause context
- **Documentation tools:** Mintlify/GitBook auto-generate docs from RoadmapKO architecture

**AI Agent Ecosystem:**
- **Third-party agents:** Community-built specialized agents (DevOps Agent, Security Agent, Compliance Agent)
- **Agent marketplace:** Users can install additional agents for niche needs
- **Custom agent training:** Enterprises fine-tune agents on their historical documentation

**Competitive Moat:**
- Network effects: More tools integrate → more valuable for users
- Switching costs: RoadmapKO contains institutional knowledge spanning years
- Data moat: Millions of planning documents train better agents

---

#### **Expansion Opportunities**

**Vertical-Specific Templates (Year 2)**
- **SaaS startups:** Pre-built templates for common SaaS features (auth, payments, onboarding)
- **E-commerce:** Templates for product catalogs, checkout flows, inventory management
- **Fintech:** Compliance-aware templates with built-in security/audit requirements
- **Healthcare:** HIPAA-compliant templates with privacy-by-design

**White-Label for Agencies (Year 2)**
- Agencies can brand RoadmapKO as their own planning tool
- Custom domains (planning.acmeagency.com)
- Branded document exports (agency logo, color scheme)
- Client portal (read-only access for clients to review planning docs)
- Pricing: $999/mo + % of client billings

**Enterprise On-Premise (Year 3)**
- Self-hosted RoadmapKO for highly regulated industries (banking, defense, healthcare)
- Air-gapped deployment (no internet connection required)
- Bring-your-own LLM (use customer's OpenAI/Anthropic API keys)
- Pricing: $50K+ annual contracts

**Strategic Acquisition Targets:**
- **Linear (aggressive):** Position as "planning layer for Linear" then offer acquisition ($50M+ valuation)
- **GitHub (long-shot):** "Planning integrated with code" narrative ($100M+ valuation)
- **Notion (strategic):** "AI-native docs with planning intelligence" ($50-100M valuation)
- **Atlassian (enterprise):** "Jira's missing planning layer" ($75-150M valuation)

---

# **Technical Considerations**

---

## **Platform Requirements**

### **Target Platforms:**
- **Primary:** Web application (desktop browsers)
- **Secondary:** Tablet support (iPad Pro, 1024x768 minimum)
- **Post-MVP:** Mobile responsive (iPhone, Android - simplified single-panel UI)

### **Browser/OS Support:**
- **Desktop Browsers:** Chrome 120+, Firefox 120+, Safari 17+, Edge 120+
- **Operating Systems:** macOS, Windows, Linux (via browser)
- **JavaScript Requirements:** ES2022+ features, no IE11 support needed
- **Local Storage:** IndexedDB for offline draft caching (post-MVP)

### **Performance Requirements:**
- **Agent response time:** <2 seconds for chat interactions (target: <1 second)
- **Document generation:** <30 seconds for full document (e.g., PRD with 6 sections)
- **Page load time:** <1.5 seconds for initial app load (Next.js SSR)
- **UI responsiveness:** 60fps animations, <100ms for user interactions (click, type, scroll)
- **Concurrent users:** Support 1,000 concurrent users by Month 6, 5,000 by Month 12
- **Database query time:** <100ms for document retrieval, <50ms for metadata queries

### **Accessibility Requirements:**
- **WCAG 2.1 AA compliance:** Keyboard navigation, screen reader support, color contrast
- **Keyboard-first design:** All actions accessible via keyboard (post-MVP: vim mode)
- **Focus management:** Clear focus indicators, logical tab order
- **ARIA labels:** Proper semantic HTML + ARIA attributes for assistive technologies

---

## **Technology Preferences**

### **Frontend Stack:**

**Framework: Next.js 14 (App Router)**
- **Why Next.js:**
  - Server-side rendering for fast initial load
  - API routes for backend logic (Vercel serverless functions)
  - Excellent TypeScript support
  - Built-in optimizations (image, font, bundle)
  - Vercel deployment integration (zero-config)

**AI Integration: Vercel AI SDK v5**
- **Why Vercel AI SDK:**
  - Native streaming support for real-time AI responses
  - Structured outputs with type-safe schema validation
  - Built-in agent APIs for lightweight per-request agents
  - Seamless integration with React hooks (useChat, useCompletion)
  - Multi-provider support (OpenAI, Anthropic, Google, etc.)
  - Optimized for Next.js App Router
  - Reduces boilerplate for AI-powered UI interactions
  - Current stable release with production-ready features

**UI Library: React 18+**
- **Why React:**
  - Massive ecosystem and community
  - Excellent AI tooling support (Cursor, v0, Lovable all optimize for React)
  - Component-based architecture fits three-panel workspace perfectly
  - Server components reduce client bundle size

**Styling: Tailwind CSS 3.4+**
- **Why Tailwind:**
  - Utility-first approach speeds development
  - Excellent with AI code generation (Cursor understands Tailwind patterns)
  - Built-in dark mode support
  - Customizable design system (colors, spacing, typography)
  
**Component Library: Untitled UI (React)**
- **Why Untitled UI:**
  - Premium, production-ready React components built on Tailwind CSS
  - Beautiful, modern design system with consistent aesthetics
  - Comprehensive component library (50+ components)
  - TypeScript-first with full type safety
  - Accessible components (WCAG 2.1 AA compliant)
  - Excellent documentation and design patterns
  - Regular updates and active maintenance
  - Perfect for B2B SaaS applications
  - Link: https://www.untitledui.com/react

**Icon Library: Untitled UI Icons**
- **Why Untitled UI Icons:**
  - 1,000+ beautifully crafted icons
  - Consistent style matching Untitled UI components
  - Available as React components with TypeScript support
  - Multiple styles (outline, solid) and sizes
  - Optimized SVGs for performance
  - Seamless integration with Untitled UI components
  - Link: https://www.untitledui.com/icons

**Rich Text Editor: TipTap (Phase 4)**
- **Why TipTap:**
  - Headless editor (full control over UI)
  - ProseMirror-based (robust, extensible)
  - Markdown import/export support
  - Collaborative editing ready (Y.js integration)
  - Better performance than Draft.js or Slate
- **MVP:** Markdown-only display (react-markdown), editing deferred to Phase 4

**State Management: Zustand + React Query**
- **Zustand for client state:** Simple, minimal boilerplate, TypeScript-first
- **React Query for server state:** Caching, optimistic updates, automatic refetching
- **Why not Redux:** Too much boilerplate for MVP, Zustand simpler for AI-assisted development

**Form Handling: React Hook Form + Zod**
- **React Hook Form:** Performant, minimal re-renders
- **Zod:** TypeScript-first validation, type inference
- **Integration:** RHF + Zod = type-safe forms with minimal code

---

### **Backend Stack:**

**Database: Supabase (PostgreSQL 15+)**
- **Why Supabase:**
  - Managed PostgreSQL (no DB ops overhead)
  - Real-time subscriptions (WebSockets for live updates - Phase 4)
  - Storage API for file uploads (document exports, user avatars)
  - Row-level security (RLS) for multi-tenancy
  - Edge Functions (Deno runtime for serverless logic if needed)
  
**Database Schema Design:**
```sql
-- Core tables (simplified, will expand in architecture doc)

-- Users (synced from Clerk via webhooks)
users (
  id UUID PRIMARY KEY,
  clerk_user_id TEXT UNIQUE NOT NULL,
  email TEXT NOT NULL,
  name TEXT,
  avatar_url TEXT,
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW()
)

-- Subscriptions
subscriptions (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  stripe_subscription_id TEXT UNIQUE,
  tier TEXT NOT NULL, -- 'pro', 'business', 'enterprise'
  status TEXT NOT NULL, -- 'active', 'canceled', 'past_due'
  credit_balance INTEGER DEFAULT 100,
  created_at TIMESTAMPTZ DEFAULT NOW(),
  current_period_end TIMESTAMPTZ
)

-- Projects
projects (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  name TEXT NOT NULL,
  description TEXT,
  tags TEXT[],
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW()
)

-- Initiatives
initiatives (
  id UUID PRIMARY KEY,
  project_id UUID REFERENCES projects(id),
  name TEXT NOT NULL,
  description TEXT,
  status TEXT DEFAULT 'draft', -- 'draft', 'in_progress', 'complete', 'archived'
  phase TEXT DEFAULT 'analysis', -- 'analysis', 'planning', 'complete'
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW()
)

-- Documents
documents (
  id UUID PRIMARY KEY,
  initiative_id UUID REFERENCES initiatives(id),
  type TEXT NOT NULL, -- 'project_brief', 'market_research', 'prd', etc.
  version TEXT DEFAULT 'v0.1',
  content_markdown TEXT NOT NULL,
  status TEXT DEFAULT 'draft', -- 'draft', 'awaiting_review', 'approved', 'locked'
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW()
)

-- Agent Interactions (for analytics and debugging)
agent_interactions (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  initiative_id UUID REFERENCES initiatives(id),
  agent_type TEXT NOT NULL, -- 'discovery', 'requirements', 'design', etc.
  input TEXT NOT NULL,
  output TEXT,
  credits_used INTEGER NOT NULL,
  model_used TEXT, -- 'gemini-2.0-flash', 'claude-3.5-sonnet', etc.
  response_time_ms INTEGER,
  created_at TIMESTAMPTZ DEFAULT NOW()
)

-- Credit Transactions
credit_transactions (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  amount INTEGER NOT NULL, -- positive for purchase/grant, negative for consumption
  type TEXT NOT NULL, -- 'purchase', 'monthly_grant', 'consumption', 'refund'
  description TEXT,
  stripe_payment_intent_id TEXT,
  created_at TIMESTAMPTZ DEFAULT NOW()
)
```

---

**API Layer: Vercel Serverless Functions**
- **Why Vercel Serverless Functions:**
  - Zero infrastructure management (fully managed by Vercel)
  - Automatic scaling (handles traffic spikes)
  - Integrated with Next.js (same codebase, single deployment)
  - TypeScript/JavaScript only (no Python complexity)
  - Edge functions available (low-latency global deployment)
  
**Function Structure:**
```typescript
// Example directory structure
app/api/
├── agents/
│   ├── orchestrator/route.ts        // Main agent orchestration
│   ├── discovery/route.ts           // Discovery agent endpoint
│   ├── requirements/route.ts        // Requirements agent endpoint
│   ├── design/route.ts              // Design agent endpoint
│   ├── architecture/route.ts        // Architecture agent endpoint
│   ├── quality/route.ts             // Quality agent endpoint
│   ├── validation/route.ts          // Validation agent endpoint
│   └── planning/route.ts            // Planning agent endpoint
├── documents/
│   ├── create/route.ts              // Create document
│   ├── update/route.ts              // Update document
│   └── export/route.ts              // Export markdown/PDF
├── credits/
│   ├── balance/route.ts             // Get credit balance
│   └── purchase/route.ts            // Purchase credits (Stripe)
└── webhooks/
    ├── clerk/route.ts               // Clerk user lifecycle events
    └── stripe/route.ts              // Stripe payment events
```

**Execution Time Limits:**
- **Vercel Hobby/Pro:** 10 second timeout (sufficient for most agent operations)
- **Vercel Enterprise:** 300 second timeout (if needed for long document generation)
- **Workaround if needed:** Queue long-running operations via background jobs (Inngest or QStash)

**Rationale:** Vercel serverless functions eliminate infrastructure complexity for lightweight agents and UI interactions. For complex multi-agent orchestration, we use a dedicated Python microservice.

---

**AI Orchestration Microservice: FastAPI + CrewAI**

- **Why FastAPI + CrewAI:**
  - **CrewAI:** Purpose-built for multi-agent orchestration with autonomous coordination
  - **FastAPI:** High-performance async Python framework, perfect for long-running AI workflows
  - **Python ecosystem:** Access to LangChain, LlamaIndex, and other AI libraries when needed
  - **Separation of concerns:** Heavy orchestration isolated from UI runtime
  - **Persistent state:** Complex agent memory and coordination state managed independently
  - **Cost optimization:** Run on pay-per-second serverless (Modal) or inexpensive containers (Railway/Fly.io)

**Hosting Options:**

| Platform | Model | Best For | Cost |
|----------|-------|----------|------|
| **Modal** | Pay-per-second serverless | Spiky traffic, cost optimization | ~$0.0001/sec |
| **Railway** | Always-on container | Consistent traffic, simple deployment | ~$5-20/mo |
| **Fly.io** | Container with auto-scaling | Global deployment, low latency | ~$10-30/mo |

**FastAPI Service Structure:**
```python
# app/main.py - FastAPI entrypoint
from fastapi import FastAPI, BackgroundTasks
from crewai import Crew, Agent, Task
import openrouter

app = FastAPI()

# Specialist agents (PM, Architect, QA, etc.)
discovery_agent = Agent(
    role='Discovery Specialist',
    goal='Research and validate project requirements',
    backstory='Expert at market research and competitive analysis',
    llm=openrouter.chat(model='anthropic/claude-3.5-sonnet')
)

requirements_agent = Agent(
    role='Requirements Engineer',
    goal='Generate comprehensive PRDs',
    backstory='Experienced PM with strong technical documentation skills',
    llm=openrouter.chat(model='google/gemini-2.0-pro')
)

# Multi-agent orchestration
@app.post("/api/orchestrate/full-analysis")
async def orchestrate_full_analysis(initiative_id: str, background_tasks: BackgroundTasks):
    """
    Coordinates multi-agent workflow for complete initiative analysis.
    For long-running operations (>60s), offloads to Inngest/Trigger.dev.
    """

    # Define crew with agent collaboration
    crew = Crew(
        agents=[discovery_agent, requirements_agent, architecture_agent],
        tasks=[
            Task(description="Research market and competitors", agent=discovery_agent),
            Task(description="Generate PRD based on discovery", agent=requirements_agent),
            Task(description="Create technical architecture", agent=architecture_agent),
        ],
        process='sequential'  # or 'hierarchical' for complex workflows
    )

    # Execute crew (streams progress via WebSockets)
    result = crew.kickoff()

    return {"status": "completed", "result": result}

# Real-time progress streaming
@app.websocket("/ws/progress/{session_id}")
async def websocket_progress(websocket: WebSocket, session_id: str):
    """Stream agent progress to frontend in real-time."""
    await websocket.accept()
    # Emit progress events as agents work
    # Frontend (Vercel AI SDK) displays live updates
```

**Integration with Next.js:**
```typescript
// Next.js API route triggers CrewAI for complex operations
// app/api/agents/orchestrate/route.ts

export async function POST(request: Request) {
  const { initiativeId, operation } = await request.json();

  // For lightweight operations: use Vercel AI SDK directly
  if (operation === 'quick_question') {
    return streamText({
      model: openai('gpt-4'),
      prompt: `Answer: ${question}`,
    });
  }

  // For complex orchestration: delegate to CrewAI service
  if (operation === 'full_analysis') {
    const response = await fetch(`${process.env.CREW_SERVICE_URL}/api/orchestrate/full-analysis`, {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ initiative_id: initiativeId }),
    });

    return response;
  }
}
```

**When to Use Each Layer:**

| Operation | Layer | Reasoning |
|-----------|-------|-----------|
| **Chat/Q&A** | Vercel AI SDK | Fast, lightweight, streaming UI |
| **Single agent task** | Vercel AI SDK | No orchestration needed |
| **Multi-agent coordination** | CrewAI (FastAPI) | Complex reasoning, autonomous collaboration |
| **Long-running workflow** | CrewAI + Inngest | >60s operations, durable execution |
| **Background processing** | Inngest/Trigger.dev | User doesn't need to wait |

**Background Jobs: Inngest / Trigger.dev**
- **Why background jobs:**
  - Vercel has 10s timeout (Hobby/Pro) or 300s (Enterprise)
  - Long-running CrewAI workflows (e.g., full initiative analysis) may exceed limits
  - Durable execution ensures jobs complete even if connections drop

- **Integration pattern:**
  ```typescript
  // Trigger long-running workflow
  await inngest.send({
    name: 'crew.orchestrate',
    data: { initiativeId, operation: 'full_analysis' },
  });

  // Inngest calls CrewAI service, retries on failure
  // User receives notification when complete (via Resend email + PostHog event)
  ```

---

### **AI/LLM Infrastructure:**

**Hybrid AI Architecture Overview:**

This architecture combines **Vercel AI SDK** (for lightweight UI interactions) with **CrewAI** (for complex multi-agent orchestration), routing through **OpenRouter** for unified multi-provider LLM access.

**LLM Provider: OpenRouter (Meta-Router)**
- **Why OpenRouter:**
  - **One API key, many models:** Access Anthropic, OpenAI, Google, Groq, Fireworks, Together AI with single integration
  - **Cost optimization:** Compare pricing across providers in real-time
  - **Performance tuning:** Switch models per agent based on quality/cost/speed
  - **No vendor lock-in:** Easy to add/remove providers or switch to direct APIs
  - **Unified billing:** Single invoice for all LLM usage
  - **Automatic fallbacks:** If primary model fails, routes to backup provider

**Agent Framework Strategy:**

| Layer | Framework | Use Case |
|-------|-----------|----------|
| **UI-Native Agents** | Vercel AI SDK v5 | Chat, Q&A, single-turn completions, streaming responses |
| **Multi-Agent Orchestration** | CrewAI (FastAPI) | Complex workflows, autonomous coordination, long-running tasks |

**Architecture Flow:**
```
User Request (Next.js)
     ↓
  Decision Point
     ↓
     ├→ [Simple Request] → Vercel AI SDK → OpenRouter → Direct Response
     │
     └→ [Complex Orchestration] → CrewAI Service (FastAPI)
                                        ↓
                                   OpenRouter (Meta-Router)
                                        ↓
                        ┌───────────────┼───────────────┐
                        ↓               ↓               ↓
                   Anthropic         Google          OpenAI
                (Claude 3.5)      (Gemini 2.0)    (GPT-4, o1)
                        ↓               ↓               ↓
                   Groq/Fireworks/Together (Fast inference)
                        ↓
                Multi-Agent Collaboration (CrewAI)
                        ↓
               Response (streamed via WebSockets)
```

**Multi-Model Strategy:**

| Agent | Primary Model | Alternative | Rationale | Est. Cost per 1M Tokens |
|-------|--------------|-------------|-----------|------------------------|
| **Discovery Agent** | google/gemini-2.0-flash | groq/llama-3.1-70b | Fast research, cost-effective | $0.075 input / $0.30 output |
| **Requirements Agent** | anthropic/claude-3.5-sonnet | google/gemini-2.0-pro | Strong reasoning for PRDs | $3.00 input / $15.00 output |
| **Design Agent** | anthropic/claude-3.5-sonnet | google/gemini-2.0-pro | Creative descriptions, UX writing | $3.00 input / $15.00 output |
| **Architecture Agent** | anthropic/claude-3.5-sonnet | openai/o1-preview | Best at technical architecture | $3.00 input / $15.00 output |
| **Quality Agent** | google/gemini-2.0-flash | groq/mixtral-8x7b | Checklists, test scenario generation | $0.075 input / $0.30 output |
| **Validation Agent** | google/gemini-2.0-pro | anthropic/claude-3.5-sonnet | Cross-document reasoning | $1.25 input / $5.00 output |
| **Planning Agent** | google/gemini-2.0-flash | together/qwen-2.5-72b | High-volume story generation | $0.075 input / $0.30 output |

**Why Multi-Model + Multi-Provider:**
- **Cost optimization:** Route to cheapest capable model (Gemini Flash for 70%, Claude for 20%, specialized models for 10%)
- **Quality optimization:** Use Claude for technical depth, Gemini for speed, o1 for complex reasoning
- **Reliability:** Automatic fallback if primary provider has outage
- **Flexibility:** A/B test different models per agent, adjust based on performance
- **Future-proof:** New models (GPT-5, Gemini 3.0, Claude 4) integrate automatically via OpenRouter

**Example Vercel AI SDK Implementation (Lightweight Agents):**
```typescript
// app/api/chat/route.ts
import { streamText } from 'ai';
import { createOpenRouter } from '@openrouter/ai-sdk-provider';

const openrouter = createOpenRouter({
  apiKey: process.env.OPENROUTER_API_KEY!,
});

export async function POST(request: Request) {
  const { messages } = await request.json();

  // Stream response directly to UI
  const result = await streamText({
    model: openrouter('google/gemini-2.0-flash'),
    messages,
    temperature: 0.7,
  });

  return result.toDataStreamResponse();
}
```

**Example CrewAI Implementation (Complex Orchestration):**
```python
# crew-service/agents/discovery.py
from crewai import Agent, Task, Crew
from langchain_openrouter import ChatOpenRouter

# Configure OpenRouter for all agents
llm = ChatOpenRouter(
    api_key=os.environ['OPENROUTER_API_KEY'],
    model='anthropic/claude-3.5-sonnet',
)

discovery_agent = Agent(
    role='Discovery Specialist',
    goal='Research market, competitors, and user needs',
    backstory='Expert at competitive analysis and market research',
    llm=llm,
    tools=[web_search_tool, document_analyzer_tool],
)

requirements_agent = Agent(
    role='Requirements Engineer',
    goal='Generate comprehensive, structured PRDs',
    backstory='Senior PM with technical background',
    llm=llm,
)

# Define multi-agent workflow
crew = Crew(
    agents=[discovery_agent, requirements_agent],
    tasks=[
        Task(
            description="Research competitors and market trends for {initiative}",
            agent=discovery_agent,
            expected_output="Markdown report with competitive analysis",
        ),
        Task(
            description="Generate PRD based on discovery findings",
            agent=requirements_agent,
            context=[discovery_task],  # Pass discovery output to requirements
            expected_output="Complete PRD document",
        ),
    ],
    process='sequential',  # or 'hierarchical' for complex coordination
)

# Execute crew
result = crew.kickoff(inputs={'initiative': 'Mobile app for roadmap planning'})
```

**Embeddings & Vector Search Strategy:**
| Provider | Model | Use Case | Cost |
|----------|-------|----------|------|
| **Voyage AI** | voyage-large-2 | Primary embeddings (high quality) | $0.12 per 1M tokens |
| **OpenAI** | text-embedding-3-small | Fallback, faster | $0.02 per 1M tokens |
| **Jina AI** | jina-embeddings-v3 | Multilingual support | $0.02 per 1M tokens |
| **Future:** | Local bge-small via Text Generation Inference | Self-hosted for scale | ~$0 (compute only) |

**Real-Time Streaming (CrewAI → Frontend):**
```python
# FastAPI WebSocket endpoint
@app.websocket("/ws/crew/{session_id}")
async def websocket_endpoint(websocket: WebSocket, session_id: str):
    await websocket.accept()

    # Stream agent progress
    async for event in crew.kickoff_async(stream=True):
        await websocket.send_json({
            'agent': event.agent_name,
            'task': event.task_description,
            'status': event.status,
            'output': event.partial_output,
        })
```

```typescript
// Frontend (Next.js with Vercel AI SDK)
import { useWebSocket } from '@/hooks/useWebSocket';

const { messages, isConnected } = useWebSocket(`/ws/crew/${sessionId}`);

// Display real-time agent progress in UI
messages.map(msg => (
  <AgentCard agent={msg.agent} status={msg.status} output={msg.output} />
))
```

**Credit Cost Mapping (Revised for OpenRouter):**

| Operation | Avg Tokens | Model | Est. Cost | Credits | Margin |
|-----------|------------|-------|-----------|---------|--------|
| **Project Brief** | 2K in / 3K out | Gemini Flash | $0.001 | 15 ($1.50) | 99.9% |
| **Market Research** | 3K in / 4K out | Gemini Flash | $0.0015 | 20 ($2.00) | 99.9% |
| **PRD Generation** | 4K in / 6K out | Claude 3.5 Sonnet | $0.072 | 30 ($3.00) | 97.6% |
| **Architecture** | 3K in / 5K out | Claude 3.5 Sonnet | $0.084 | 25 ($2.50) | 96.6% |
| **User Story** | 1K in / 1K out | Gemini Flash | $0.0004 | 5 ($0.50) | 99.9% |

**Blended Margin:** 90-95% (70% Gemini Flash, 20% Claude, 10% specialized models)

**Why This Hybrid Model Works:**
- **Best of both worlds:** Vercel AI SDK for snappy UI, CrewAI for persistent orchestration
- **Cost flexibility:** OpenRouter enables real-time cost optimization across providers
- **Scalability:** Both layers scale independently (Vercel Edge + Modal/Fly serverless)
- **Developer experience:** TypeScript for UI, Python for complex AI logic (leverage both ecosystems)
- **Future-proof:** Easy to adopt new models (GPT-5, Gemini 3.0) without architecture changes

---

### **Third-Party Services:**

**Authentication: Clerk**
- **Why Clerk:**
  - Beautiful pre-built UI components (sign-in, sign-up, user profile)
  - Email/password, Google OAuth, GitHub OAuth out-of-box
  - User management dashboard (admin panel for support)
  - Webhooks for user lifecycle events (user.created, user.updated, user.deleted)
  - Session management (secure JWT tokens)
  - Multi-tenant support (organizations, teams - Phase 4)
  - Better developer experience than building custom auth
  
**Clerk Integration Pattern:**
```typescript
// Middleware to protect API routes
import { authMiddleware } from "@clerk/nextjs";

export default authMiddleware({
  publicRoutes: ["/", "/pricing", "/docs"],
  ignoredRoutes: ["/api/webhooks/clerk", "/api/webhooks/stripe"],
});

// Get user in serverless function
import { auth } from "@clerk/nextjs";

export async function GET() {
  const { userId } = auth();
  if (!userId) return new Response("Unauthorized", { status: 401 });
  
  // Fetch user data from Supabase using clerk_user_id
  const { data: user } = await supabase
    .from('users')
    .select('*')
    .eq('clerk_user_id', userId)
    .single();
    
  return Response.json(user);
}

// Webhook handler for user creation
export async function POST(request: Request) {
  const payload = await request.json();
  const { id, email_addresses, first_name, last_name } = payload.data;
  
  // Create user in Supabase
  await supabase.from('users').insert({
    clerk_user_id: id,
    email: email_addresses[0].email_address,
    name: `${first_name} ${last_name}`,
  });
  
  return Response.json({ success: true });
}
```

**User Data Flow:**
1. User signs up via Clerk UI
2. Clerk webhook fires → `/api/webhooks/clerk`
3. Webhook handler creates user in Supabase with `clerk_user_id`
4. User record includes: subscription tier, credit balance, preferences
5. All subsequent requests use Clerk `userId` to query Supabase

---

**Payments: Stripe**
- **Capabilities:**
  - **Subscriptions:** Pro ($25/mo), Business ($50/mo), Enterprise (custom)
  - **One-time payments:** Credit packs (100-4000 credits)
  - **Customer Portal:** Self-service subscription management, invoices
  - **Webhooks:** subscription.created, payment_intent.succeeded, invoice.payment_failed, etc.
  - **Invoicing:** Automatic monthly invoices
  
**Stripe Integration Example:**
```typescript
// Create checkout session for subscription
import Stripe from 'stripe';
const stripe = new Stripe(process.env.STRIPE_SECRET_KEY!);

export async function POST(request: Request) {
  const { tier } = await request.json(); // 'pro' or 'business'
  const { userId } = auth();
  
  const session = await stripe.checkout.sessions.create({
    customer_email: user.email,
    line_items: [{
      price: tier === 'pro' ? process.env.STRIPE_PRO_PRICE_ID : process.env.STRIPE_BUSINESS_PRICE_ID,
      quantity: 1,
    }],
    mode: 'subscription',
    success_url: `${process.env.NEXT_PUBLIC_URL}/dashboard?session_id={CHECKOUT_SESSION_ID}`,
    cancel_url: `${process.env.NEXT_PUBLIC_URL}/pricing`,
    metadata: { userId, tier },
  });
  
  return Response.json({ url: session.url });
}

// Webhook handler for subscription events
export async function POST(request: Request) {
  const sig = request.headers.get('stripe-signature')!;
  const body = await request.text();
  
  const event = stripe.webhooks.constructEvent(body, sig, process.env.STRIPE_WEBHOOK_SECRET!);
  
  switch (event.type) {
    case 'checkout.session.completed':
      const session = event.data.object;
      await createSubscription(session.metadata.userId, session.subscription, session.metadata.tier);
      await grantMonthlyCredits(session.metadata.userId, 100);
      break;
    case 'invoice.payment_succeeded':
      await grantMonthlyCredits(event.data.object.customer, 100);
      break;
    case 'customer.subscription.deleted':
      await cancelSubscription(event.data.object.metadata.userId);
      break;
  }
  
  return Response.json({ received: true });
}
```

---

**Email: Resend**
- **Why Resend:**
  - Developer-friendly API (built for Next.js/React)
  - React Email templates (type-safe, version-controlled JSX)
  - Excellent deliverability (high inbox rate)
  - Affordable ($20/mo for 50K emails)
  
**Email Templates Needed:**
```typescript
// Welcome email
import { EmailTemplate } from '@/components/emails/welcome';

await resend.emails.send({
  from: 'RoadmapKO <hello@roadmapko.com>',
  to: user.email,
  subject: 'Welcome to RoadmapKO!',
  react: EmailTemplate({ name: user.name, credits: 100 }),
});

// Email templates required for MVP:
// 1. Welcome email (onboarding, first steps, credit balance)
// 2. Low credit warning (20 credits remaining)
// 3. Out of credits (prompt to purchase)
// 4. Document generation complete (for long-running operations >30s)
// 5. Payment failed (retry notification)
// 6. Subscription canceled (confirmation, data retention policy)
```

---

**Documentation: Mintlify**
- **Why Mintlify:**
  - Beautiful docs UI (inspired by Stripe, Linear)
  - Markdown-based (version-controlled in Git)
  - Built-in search (Algolia-powered)
  - API reference auto-generation from OpenAPI spec
  - Zero hosting cost (Mintlify hosts)
  - Excellent for developer tools

**Documentation Structure:**
```
docs/
├── introduction.mdx          # Getting started
├── quickstart.mdx            # First initiative in 5 minutes
├── concepts/
│   ├── agents.mdx            # 7-agent workflow explained
│   ├── credits.mdx           # Credit system FAQ
│   └── hierarchy.mdx         # Initiative → Epic → Feature → Story
├── guides/
│   ├── interactive-mode.mdx  # Step-by-step agent collaboration
│   ├── yolo-mode.mdx         # Generate & refine workflow
│   └── export.mdx            # Markdown, PDF, ZIP export
└── integrations/             # Phase 3 (placeholder for MVP)
    ├── linear.mdx
    ├── jira.mdx
    └── notion.mdx
```

---

**Analytics: PostHog**
- **Why PostHog:**
  - Open-source (self-hostable if needed)
  - Product analytics + feature flags + session replay
  - Privacy-friendly (GDPR compliant)
  - Affordable ($0 for <1M events/month)
  
**Events to Track:**
```typescript
// User lifecycle
posthog.capture('user_signed_up', { tier: 'pro', source: 'product_hunt' });
posthog.capture('user_completed_onboarding', { mode: 'interactive' });

// Initiative workflow
posthog.capture('initiative_created', { project_id });
posthog.capture('document_generated', { type: 'project_brief', agent: 'discovery', credits_used: 15 });
posthog.capture('document_approved', { type: 'prd', approval_time_seconds: 45 });
posthog.capture('phase_completed', { phase: 'analysis', duration_minutes: 25 });

// Credit system
posthog.capture('credits_low_warning', { remaining: 20 });
posthog.capture('credits_purchased', { pack_size: 400, amount_usd: 32 });
posthog.capture('credits_depleted', { user_action: 'blocked' });

// Churn events
posthog.capture('subscription_canceled', { reason: 'too_expensive', tenure_days: 8 });
posthog.capture('refund_requested', { reason: 'agent_quality', within_guarantee: true });
```

---

**Error Tracking: Sentry**
- **Why Sentry:**
  - Best-in-class error tracking for React + Next.js
  - Source map support (readable stack traces)
  - Release tracking (correlate errors with deployments)
  - Performance monitoring (slow queries, API response times)
  - Breadcrumbs (user actions leading to error)

**Sentry Configuration:**
```typescript
import * as Sentry from "@sentry/nextjs";

Sentry.init({
  dsn: process.env.NEXT_PUBLIC_SENTRY_DSN,
  environment: process.env.NODE_ENV,
  tracesSampleRate: 0.1, // 10% of transactions for performance monitoring
  beforeSend(event, hint) {
    // Filter out low-priority errors
    if (event.level === 'warning') return null;
    return event;
  },
});

// Capture agent errors with context
try {
  const response = await generateDocument();
} catch (error) {
  Sentry.captureException(error, {
    tags: { agent: 'discovery', operation: 'project_brief' },
    contexts: {
      initiative: { id: initiativeId, name: initiativeName },
      user: { id: userId, tier: userTier, credits: userCredits },
    },
  });
  throw error;
}
```

---

**LLM Observability: Langfuse**
- **Why Langfuse:**
  - **LLM-specific tracing:** Track every AI request with token counts, latency, and cost
  - **Multi-provider support:** Works with OpenRouter, Anthropic, OpenAI, Google
  - **Cost analytics:** Real-time dashboards for LLM spend per agent, user, operation
  - **Quality monitoring:** Track model outputs, compare versions, detect regressions
  - **Open-source:** Self-hostable for data privacy, or use cloud version
  - **Integrations:** Works seamlessly with Vercel AI SDK and LangChain (CrewAI compatible)

**Langfuse Integration:**
```typescript
// Vercel AI SDK with Langfuse tracing
import { streamText } from 'ai';
import { observeOpenAI } from 'langfuse-vercel-ai';

const observedOpenRouter = observeOpenAI(openrouter, {
  publicKey: process.env.LANGFUSE_PUBLIC_KEY!,
  secretKey: process.env.LANGFUSE_SECRET_KEY!,
});

export async function POST(request: Request) {
  const result = await streamText({
    model: observedOpenRouter('google/gemini-2.0-flash'),
    messages,
  });

  // Automatically logs: tokens, cost, latency, model, user_id
  return result.toDataStreamResponse();
}
```

```python
# CrewAI with Langfuse tracing
from langfuse.decorators import observe, langfuse_context

@observe()
async def run_crew_workflow(initiative_id: str):
    langfuse_context.update_current_trace(
        user_id=user_id,
        tags=["crew-orchestration", "full-analysis"],
    )

    result = crew.kickoff()

    # Langfuse captures all LLM calls within this function
    return result
```

**Langfuse Dashboards:**
- **Cost per agent:** Which agents are most expensive? Discovery vs. Architecture?
- **User spend:** Which users consume the most credits? Enterprise vs. Pro?
- **Model performance:** Is Claude 3.5 Sonnet worth the premium over Gemini Pro?
- **Latency tracking:** Are CrewAI workflows completing within acceptable time?

---

**Caching & Rate Limiting: Upstash Redis**
- **Why Upstash:**
  - **Serverless Redis:** Pay-per-request, no idle costs
  - **Global replication:** Low-latency reads from edge locations
  - **REST API:** Works with Vercel serverless functions (no persistent connections)
  - **Built-in rate limiting:** Protect against abuse, enforce credit limits
  - **Cache LLM responses:** Avoid duplicate API calls for identical requests

**Use Cases:**
```typescript
import { Redis } from '@upstash/redis';

const redis = Redis.fromEnv();

// 1. Cache LLM responses (avoid duplicate calls)
const cacheKey = `agent:discovery:${hash(userMessage)}`;
const cached = await redis.get(cacheKey);

if (cached) {
  return Response.json({ text: cached, cached: true });
}

const response = await generateWithLLM(userMessage);
await redis.setex(cacheKey, 3600, response); // Cache for 1 hour

// 2. Rate limiting (prevent abuse)
const { success } = await redis.ratelimit.limit(`user:${userId}`, {
  rate: 10, // 10 requests
  duration: 60, // per minute
});

if (!success) {
  return Response.json({ error: 'Rate limit exceeded' }, { status: 429 });
}

// 3. Job deduplication (prevent double-submits)
const jobKey = `job:${initiativeId}:full-analysis`;
const exists = await redis.exists(jobKey);

if (exists) {
  return Response.json({ error: 'Job already in progress' }, { status: 409 });
}

await redis.setex(jobKey, 600, 'processing'); // Lock for 10 minutes
```

---

**Real-Time Events: Pusher / Ably / WebSockets**
- **Why real-time streaming:**
  - **CrewAI progress updates:** Stream agent status to frontend as workflows execute
  - **Multi-agent coordination:** Show which agent is currently working
  - **Token streaming:** Display LLM output character-by-character for UX
  - **Collaboration (Phase 4):** Real-time document editing, comments

**Options:**

| Service | Best For | Cost | Pros |
|---------|----------|------|------|
| **Pusher** | Simple pub/sub, presence channels | $49/mo for 500 concurrent | Easy setup, great docs |
| **Ably** | Global scale, guaranteed delivery | $29/mo for 200 concurrent | Enterprise SLAs, edge network |
| **WebSockets (native)** | Full control, no third-party | Infrastructure cost only | No vendor lock-in, flexible |

**Pusher Integration Example:**
```typescript
// Backend: Send progress updates
import Pusher from 'pusher';

const pusher = new Pusher({
  appId: process.env.PUSHER_APP_ID!,
  key: process.env.NEXT_PUBLIC_PUSHER_KEY!,
  secret: process.env.PUSHER_SECRET!,
  cluster: process.env.PUSHER_CLUSTER!,
});

// CrewAI service streams progress
pusher.trigger(`session-${sessionId}`, 'crew-progress', {
  agent: 'discovery',
  status: 'in_progress',
  message: 'Researching competitors...',
  progress: 35,
});

// Frontend: Display real-time updates
import Pusher from 'pusher-js';

const pusher = new Pusher(process.env.NEXT_PUBLIC_PUSHER_KEY!);
const channel = pusher.subscribe(`session-${sessionId}`);

channel.bind('crew-progress', (data) => {
  setAgentStatus(data.agent, data.status);
  setProgressBar(data.progress);
  addLogMessage(data.message);
});
```

---

**Object Storage: Cloudflare R2 / Supabase Storage / Backblaze B2**
- **Why additional storage:**
  - **Document exports:** PDFs, ZIP archives of full initiative documentation
  - **User uploads:** Mockups, designs, existing documentation for context
  - **Backups:** Versioned snapshots of critical documents
  - **Cost optimization:** R2 has zero egress fees (vs. S3's high egress costs)

**Storage Options:**

| Service | Model | Cost | Best For |
|---------|-------|------|----------|
| **Cloudflare R2** | S3-compatible, zero egress | $0.015/GB storage, $0 egress | High-bandwidth exports, PDF downloads |
| **Supabase Storage** | Built into Supabase, RLS support | $0.021/GB storage, $0.09/GB egress | Already using Supabase, simple setup |
| **Backblaze B2** | S3-compatible, cheap storage | $0.005/GB storage, $0.01/GB egress | Long-term archival, backups |

**Cloudflare R2 Example:**
```typescript
import { S3Client, PutObjectCommand } from '@aws-sdk/client-s3';

const r2 = new S3Client({
  region: 'auto',
  endpoint: process.env.R2_ENDPOINT!,
  credentials: {
    accessKeyId: process.env.R2_ACCESS_KEY_ID!,
    secretAccessKey: process.env.R2_SECRET_ACCESS_KEY!,
  },
});

// Upload PDF export
await r2.send(new PutObjectCommand({
  Bucket: 'roadmapko-exports',
  Key: `${initiativeId}/prd-v2.pdf`,
  Body: pdfBuffer,
  ContentType: 'application/pdf',
}));

// Public URL with zero egress cost
const url = `https://exports.roadmapko.com/${initiativeId}/prd-v2.pdf`;
```

---

**Secrets Management: Doppler / Vercel Env Vars**
- **Why Doppler:**
  - **Centralized secrets:** Manage all env vars in one place (OpenRouter API key, Supabase URL, Stripe secret, etc.)
  - **Environment sync:** Dev, staging, prod environments with different keys
  - **Version control:** Rollback to previous secret versions
  - **Audit logs:** Track who accessed/changed secrets
  - **Team collaboration:** Grant granular access to secrets
  - **CI/CD integration:** Automatically inject secrets into deployments

**Doppler vs. Vercel Env Vars:**

| Feature | Doppler | Vercel Env Vars |
|---------|---------|-----------------|
| **Secret versioning** | ✅ Full history | ❌ Manual tracking |
| **Team permissions** | ✅ Granular RBAC | ⚠️ Project-level only |
| **Audit logs** | ✅ Comprehensive | ⚠️ Basic |
| **Secret rotation** | ✅ Automated | ❌ Manual |
| **Multi-cloud** | ✅ Works everywhere | ❌ Vercel-only |
| **Setup complexity** | ⚠️ Additional service | ✅ Built-in |

**Recommendation:** Start with Vercel Env Vars for MVP, migrate to Doppler when team grows or compliance requirements increase.

**Doppler Integration:**
```bash
# Local development
doppler run -- npm run dev

# CI/CD (GitHub Actions)
- name: Deploy to Vercel
  env:
    VERCEL_TOKEN: ${{ secrets.VERCEL_TOKEN }}
  run: |
    doppler run -- vercel deploy --prod
```

---

## **Architecture Considerations**

### **Repository Structure: Turborepo Monorepo**

```
roadmapko/
├── apps/
│   ├── web/                 # Next.js frontend + API routes (Vercel AI SDK)
│   ├── crew-service/        # FastAPI + CrewAI orchestration service (Python)
│   └── docs/                # Mintlify documentation
├── packages/
│   ├── ui/                  # Shared React components (Untitled UI)
│   ├── db/                  # Supabase client, types, migrations
│   ├── agents/              # Shared agent prompts & schemas (TypeScript)
│   ├── email/               # Email templates (React Email)
│   └── config/              # Shared config (ESLint, TypeScript, Tailwind)
├── supabase/
│   └── migrations/          # Database migrations (SQL)
└── turbo.json               # Turborepo config (caching, pipelines)
```

**crew-service/ Structure:**
```python
crew-service/
├── app/
│   ├── main.py              # FastAPI entrypoint
│   ├── agents/              # CrewAI agent definitions
│   │   ├── discovery.py
│   │   ├── requirements.py
│   │   ├── design.py
│   │   └── architecture.py
│   ├── crews/               # Multi-agent workflows
│   │   ├── full_analysis.py
│   │   └── validation.py
│   ├── tools/               # Custom tools for agents
│   │   ├── web_search.py
│   │   └── document_parser.py
│   └── api/                 # API routes
│       ├── orchestrate.py
│       └── websockets.py
├── requirements.txt         # Python dependencies
├── Dockerfile               # For Modal/Railway/Fly deployment
└── pyproject.toml           # Poetry config (alternative to requirements.txt)
```

**Why Monorepo:**
- **Shared code:** Types, components, utilities across apps without duplication
- **Single version control:** Atomic commits across frontend/backend
- **Faster CI/CD:** Turborepo caching (only rebuild changed packages)
- **Easier refactoring:** Change types once, propagates everywhere
- **AI-friendly:** Cursor/Claude Code excel at navigating monorepos

**Turborepo Benefits:**
- Incremental builds (only rebuild what changed)
- Remote caching (share build cache across team)
- Parallel execution (build multiple packages simultaneously)
- Task pipelines (define dependencies between tasks)

---

### **Service Architecture: Hybrid Serverless + Orchestration**

**Architecture Diagram:**
```
┌─────────────────────────────────────────────────────────────────┐
│                         User Browser                             │
└──────────────────────────┬──────────────────────────────────────┘
                           │
                           ▼
┌──────────────────────────────────────────────────────────────────┐
│               Vercel (Next.js + Vercel AI SDK)                    │
│  ┌──────────────┐  ┌───────────────┐  ┌──────────────┐          │
│  │   Frontend   │  │  API Routes   │  │   Webhooks   │          │
│  │   (React)    │  │ (Lightweight  │  │(Clerk/Stripe)│          │
│  │              │  │   Agents)     │  │              │          │
│  └──────────────┘  └───────────────┘  └──────────────┘          │
└─────┬────────────────┬────────────────┬──────────────────────────┘
      │                │                │
      │                │ (Complex       │
      │                │  requests)     │
      │                ▼                │
      │    ┌────────────────────────┐  │
      │    │  FastAPI + CrewAI      │  │
      │    │  (Modal/Railway/Fly)   │  │
      │    │                        │  │
      │    │  ┌──────────────────┐  │  │
      │    │  │ Multi-Agent      │  │  │
      │    │  │ Orchestration    │  │  │
      │    │  └──────────────────┘  │  │
      │    └────────┬───────────────┘  │
      │             │                  │
      ▼             ▼                  ▼
┌──────────┐  ┌──────────────┐  ┌──────────┐  ┌─────────┐  ┌──────────┐
│  Clerk   │  │  OpenRouter  │  │ Supabase │  │ Stripe  │  │ Pusher/  │
│  (Auth)  │  │ (Meta-Router)│  │   (DB)   │  │(Payment)│  │  Ably    │
└──────────┘  └──────┬───────┘  └──────────┘  └─────────┘  └──────────┘
                     │
         ┌───────────┼───────────┬──────────────┐
         ▼           ▼           ▼              ▼
    ┌─────────┐ ┌────────┐ ┌─────────┐    ┌──────────┐
    │Anthropic│ │ Google │ │ OpenAI  │    │Groq/Fire-│
    │(Claude) │ │(Gemini)│ │(GPT-4)  │    │works/etc.│
    └─────────┘ └────────┘ └─────────┘    └──────────┘
                     │
                     ▼
            ┌─────────────────┐
            │    Langfuse     │
            │ (LLM Observ.)   │
            └─────────────────┘
```

**Why Hybrid Architecture:**
- **Best of both worlds:** TypeScript for UI/lightweight agents, Python for complex orchestration
- **Optimized routing:** Simple requests handled by Vercel AI SDK (fast), complex workflows delegated to CrewAI (powerful)
- **Independent scaling:** Vercel Edge scales for UI, Modal/Railway scales for heavy AI workloads
- **Cost optimization:** OpenRouter enables real-time model selection based on cost/quality trade-offs
- **Developer productivity:** Leverage both TypeScript ecosystem (frontend) and Python ecosystem (AI/ML)

**Request Flow Examples:**

| User Request | Route | Why |
|--------------|-------|-----|
| "Chat with agent" | Vercel AI SDK → OpenRouter | Simple, streaming response |
| "Generate quick summary" | Vercel AI SDK → OpenRouter | Single-turn completion |
| "Full initiative analysis" | CrewAI Service → Multi-agent workflow | Complex coordination needed |
| "Validate PRD vs. Architecture" | CrewAI Service → Cross-document reasoning | Multiple agents, shared memory |
| "Background story generation" | Inngest → CrewAI Service | Long-running, user doesn't wait |

**Trade-offs Accepted:**

1. **Increased complexity:** Now maintaining two services (Next.js + FastAPI)
   - **Mitigation:** Clear separation of concerns. Most operations still in Next.js. CrewAI only for complex workflows.
   - **Benefit:** Access to Python AI ecosystem (LangChain, LlamaIndex) when needed.

2. **Inter-service communication:** Network latency between Vercel and CrewAI service
   - **Mitigation:** Deploy CrewAI service close to Vercel regions. Use background jobs for long operations.
   - **Benefit:** Heavy AI workloads don't block Vercel functions.

3. **Deployment coordination:** Need to deploy both services
   - **Mitigation:** Monorepo with Turborepo pipelines automates coordinated deployments.
   - **Benefit:** Independent scaling and resource optimization per service.

4. **OpenRouter dependency:** Adds another layer to LLM access
   - **Mitigation:** Can fall back to direct provider APIs if OpenRouter has issues.
   - **Benefit:** Unified billing, automatic fallbacks, cost optimization across providers.

**Why This Is Better Than Single-Service:**
- **Performance:** Lightweight requests stay fast (Vercel Edge), heavy workloads get dedicated compute (Modal/Railway)
- **Cost:** Pay-per-second for CrewAI workloads (Modal), not running containers 24/7
- **Flexibility:** Easy to swap models via OpenRouter, A/B test different agent configurations
- **Scalability:** Each layer scales independently based on demand
- **Future-proof:** Can migrate CrewAI to LangGraph or other frameworks without touching frontend

---

### **Integration Requirements:**

**Phase 3 Integrations (Months 8-10):**

All integrations implemented as Vercel serverless functions:

```typescript
app/api/integrations/
├── linear/
│   ├── oauth/route.ts           # OAuth 2.0 flow
│   ├── sync/route.ts            # Export initiatives to Linear
│   └── webhooks/route.ts        # Linear status updates (Phase 4)
├── jira/
│   ├── oauth/route.ts           # Atlassian OAuth
│   ├── sync/route.ts            # Export to Jira (epics, stories)
│   └── webhooks/route.ts        # Jira issue updates (Phase 4)
├── notion/
│   ├── oauth/route.ts           # Notion OAuth
│   └── export/route.ts          # Export docs to Notion pages
└── azure-boards/
    ├── oauth/route.ts           # Azure DevOps OAuth
    └── sync/route.ts            # Export to Azure Boards
```

**Integration Strategy:**
- **One-way sync (MVP):** RoadmapKO → Linear/Jira/Notion/Azure Boards
- **Bidirectional sync (Phase 4):** Status updates flow back from execution tools
- **System-of-record:** RoadmapKO preserves full context even if users switch execution tools

---

**Phase 2 Distribution Channels (Months 4-7):**

```typescript
app/api/distribution/
├── chatgpt/
│   ├── oauth/route.ts           # ChatGPT Apps SDK auth
│   └── agent/route.ts           # Agent proxy (ChatGPT → Vertex AI)
└── mcp/
    └── server.ts                # MCP server (Model Context Protocol)
```

**MCP Server Structure:**
```typescript
// MCP server exposes RoadmapKO as tools/resources to Claude Desktop
{
  "tools": [
    "create_initiative",
    "generate_document",
    "read_context",
    "update_status",
    "approve_document"
  ],
  "resources": [
    "projects://",        // List all projects
    "initiatives://",     // List all initiatives
    "documents://"        // Access full planning hierarchy
  ]
}
```

---

## **Security/Compliance**

### **Data Security:**

**Encryption:**
- **At rest:** Supabase automatic AES-256 encryption
- **In transit:** TLS 1.3 for all API calls (Vercel enforces HTTPS)
- **API tokens:** Short-lived JWT tokens (1 hour expiry, automatic refresh)

**Row-Level Security (RLS):**
```sql
-- Users can only access their own data
CREATE POLICY user_isolation ON projects
  FOR ALL USING (user_id = auth.uid());

CREATE POLICY user_isolation ON initiatives
  FOR ALL USING (
    EXISTS (
      SELECT 1 FROM projects 
      WHERE projects.id = initiatives.project_id 
      AND projects.user_id = auth.uid()
    )
  );
```

**Secrets Management:**
- **Development:** `.env.local` (never committed)
- **Production:** Vercel environment variables (encrypted at rest)
- **Sensitive keys:** Rotate quarterly (Vertex AI service accounts, Stripe API keys)

---

### **Compliance Requirements:**

**GDPR Compliance (EU Users):**
- **Data export:** Users can download all their data (JSON export)
- **Right to deletion:** Account deletion removes all user data within 30 days
- **Cookie consent:** PostHog respects Do Not Track (DNT) headers
- **Privacy policy:** Clear explanation of data collection, processing, storage

**Data Retention:**
- **Active accounts:** Indefinite (users keep their data)
- **Canceled accounts:** 90-day grace period (read-only), then soft delete
- **Hard delete:** After 1 year of inactivity (GDPR Right to Erasure)
- **Backups:** 30-day point-in-time recovery (Supabase automatic)

**SOC 2 Type II (Enterprise Tier, Year 2):**
- Audit logging (all data access logged)
- Penetration testing (annual)
- Security policies documented
- Employee background checks
- Incident response plan

---

### **Rate Limiting:**

**API Rate Limits:**
```typescript
// Per-user rate limits
const rateLimits = {
  authenticated: {
    requests: 100,        // 100 requests per minute
    generations: 10,      // 10 concurrent agent generations
    credits: 1000,        // 1000 credits per hour (burst protection)
  },
  anonymous: {
    requests: 10,         // 10 requests per minute (landing page)
  },
};

// Credit purchase fraud prevention
const purchaseLimits = {
  perHour: 5,            // Max 5 credit purchases per hour
  perDay: 20,            // Max 20 credit purchases per day
  maxAmount: 4000,       // Max 4000 credits per purchase
};
```

**DDoS Protection:**
- **Vercel automatic:** Included in Pro plan (rate limiting, IP blocking)
- **Cloudflare (if needed):** Add Cloudflare proxy for additional protection (Month 6+)

---

## **DevOps & Deployment**

### **CI/CD Pipeline (GitHub Actions):**

```yaml
name: Deploy to Vercel

on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
      - run: npm install
      - run: npm run type-check    # TypeScript compilation
      - run: npm run lint          # ESLint
      - run: npm run test          # Vitest unit tests
      - run: npm run test:e2e      # Playwright E2E tests
  
  deploy-preview:
    if: github.event_name == 'pull_request'
    needs: test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: vercel/action@v25
        with:
          vercel-token: ${{ secrets.VERCEL_TOKEN }}
          vercel-org-id: ${{ secrets.VERCEL_ORG_ID }}
          vercel-project-id: ${{ secrets.VERCEL_PROJECT_ID }}
      - name: Comment PR
        uses: actions/github-script@v6
        with:
          script: |
            github.rest.issues.createComment({
              issue_number: context.issue.number,
              body: '✅ Preview deployed: https://roadmapko-pr-${{ github.event.number }}.vercel.app'
            })
  
  deploy-production:
    if: github.ref == 'refs/heads/main'
    needs: test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: vercel/action@v25
        with:
          vercel-token: ${{ secrets.VERCEL_TOKEN }}
          vercel-org-id: ${{ secrets.VERCEL_ORG_ID }}
          vercel-project-id: ${{ secrets.VERCEL_PROJECT_ID }}
          vercel-args: '--prod'
      - name: Run Supabase migrations
        run: npx supabase db push --db-url ${{ secrets.SUPABASE_DB_URL }}
      - name: Notify team
        run: |
          curl -X POST ${{ secrets.SLACK_WEBHOOK_URL }} \
            -d '{"text": "🚀 Production deployed: https://roadmapko.com"}'
```

---

### **Environments:**

| Environment | URL | Database | Purpose |
|-------------|-----|----------|---------|
| **Development** | localhost:3000 | Supabase local | Local development |
| **Staging** | roadmapko-git-develop.vercel.app | Supabase staging | Pre-production testing |
| **Preview** | roadmapko-pr-{N}.vercel.app | Supabase staging | Per-PR deployments |
| **Production** | roadmapko.com | Supabase production | Live customer traffic |

---

### **Monitoring & Observability:**

**Uptime Monitoring:**
- **Better Uptime:** Ping https://roadmapko.com every 30 seconds
- **Alert channels:** Email, Slack, SMS (for critical)
- **SLA target:** 99.9% uptime (43 minutes downtime/month allowed)

**Performance Monitoring:**
- **Vercel Analytics:** Page load times, Web Vitals (LCP, FID, CLS)
- **Sentry Performance:** API response times, slow database queries
- **Custom metrics:** Agent response time, credit consumption rate

**Cost Monitoring:**
- **Vertex AI billing alerts:** Alert if daily spend >$50 (expected <$20/day)
- **Stripe dashboard:** Revenue tracking, churn analysis
- **Supabase metrics:** Database size, bandwidth usage

---

### **Backup Strategy:**

**Database Backups:**
- **Supabase automatic:** Daily backups (30-day retention)
- **Point-in-time recovery:** Restore to any moment in last 30 days
- **Manual backups:** Weekly export to S3 (disaster recovery, long-term retention)

**Code Backups:**
- **Git (GitHub):** Primary version control
- **Mirrors:** GitLab, Bitbucket (automated push mirrors for redundancy)

**Document Exports:**
- **Weekly batch job:** Export all initiatives to S3 (markdown format)
- **Purpose:** Disaster recovery, customer data portability

---

## **Technical Risks & Mitigation**

### **🔴 CRITICAL RISK 1: Google ADK TypeScript Maturity**

**Risk:** Google ADK is relatively new (2024), may have bugs, missing features, or poor TypeScript SDK support

**Probability:** 30%

**Impact:** Development delays (1-2 weeks), need workarounds or rewrites, frustration

**Mitigation:**
- **Week 1 prototype:** Validate all critical ADK features (tool use, structured outputs, multi-agent coordination)
- **Abstraction layer:** Wrap ADK in custom interface (can swap to direct Vertex AI API if ADK insufficient)
- **Google Cloud support:** Enterprise support contract for escalations (if budget allows)
- **Fallback plan:** Use Vertex AI REST API directly if ADK TypeScript SDK immature

**Contingency:**
- **Week 2:** If ADK doesn't work, pivot to direct Vertex AI API
- **Impact:** Adds 1-2 weeks to timeline (custom orchestration layer)
- **Mitigation:** Use proven patterns (function calling, structured outputs via API)

---

### **🔴 CRITICAL RISK 2: Vercel Serverless Function Timeouts**

**Risk:** Agent operations take >10 seconds (Hobby/Pro plan limit), causing failed generations

**Probability:** 40%

**Impact:** User frustration, poor UX, need infrastructure changes (Enterprise upgrade or background jobs)

**Mitigation:**
- **Optimize prompts:** Reduce output tokens, use concise instructions
- **Streaming responses:** Show partial progress (reduces perceived wait time)
- **Monitor execution times:** Alert if >8 seconds (approaching timeout)
- **Upgrade to Vercel Enterprise:** 300-second timeout ($500/mo, affordable at $9K MRR Month 6)

**Contingency:**
- **Background jobs (if timeouts persist):**
  - Implement queue (Inngest or QStash)
  - User clicks "Generate" → queues job → returns immediately
  - User receives email when document ready (5-10 minutes)
  - Acceptable for complex operations (Architecture, full initiative generation)

---

### **🟡 SIGNIFICANT RISK 3: Vertex AI Regional Availability**

**Risk:** Vertex AI Model Garden (Claude access) not available in all regions, higher latency for some users

**Probability:** 20%

**Impact:** Slower response times for users outside us-central1 (acceptable, not business-critical)

**Mitigation:**
- **Primary region:** us-central1 (best Model Garden coverage)
- **Multi-region deployment (Month 6+):** Add europe-west1 if EU user latency becomes issue
- **Fallback to Gemini Pro:** If Claude unavailable in region, use Gemini Pro (slight quality trade-off)

---

### **🟡 SIGNIFICANT RISK 4: Clerk + Supabase Sync Issues**

**Risk:** Webhook failures or race conditions cause users to be created in Clerk but not Supabase, breaking authentication

**Probability:** 25%

**Impact:** User signup failures, support burden (manual user creation), data inconsistencies

**Mitigation:**
- **Idempotent webhooks:** Check if user exists before creating (replay-safe)
- **Retry logic:** Exponential backoff on webhook failures (3 retries over 5 minutes)
- **Daily reconciliation:** Cron job compares Clerk users vs. Supabase users, fixes gaps
- **Monitoring:** Alert on webhook failures (Sentry), email notification

**Contingency:**
- **Manual fix tooling:** Admin UI to manually create missing Supabase users
- **Webhook queue:** Use Svix (webhook infrastructure) for reliable delivery ($50/mo if needed)

---

### **🟢 MANAGEABLE RISK 5: TypeScript Agent Logic Complexity**

**Risk:** Complex agent orchestration logic becomes difficult to manage in TypeScript (compared to Python)

**Probability:** 30%

**Impact:** Harder debugging, slower iteration on prompt improvements

**Mitigation:**
- **Keep logic simple in MVP:** Linear workflow (Discovery → Planning), no complex branching
- **Store prompts in Supabase:** Easy iteration without code changes
- **Comprehensive logging:** Every agent call logged to Supabase (input, output, model, timing)
- **Extract to package:** If complexity grows, move agent logic to `packages/agents` for isolation

**Contingency:**
- **If complexity becomes unmanageable:** Extract agent logic to separate TypeScript package with clean interfaces
- **Extreme case:** Build Python microservice for agent orchestration (call from Vercel functions via HTTP)

---

### **Constraints & Assumptions**

#### **Constraints**

**Budget Constraints:**

**Development Budget: $0-500/month**
- **Infrastructure costs (MVP):**
  - Vercel Hobby: $0/month (sufficient for MVP, 100GB bandwidth)
  - Supabase Pro: $25/month (required for production, daily backups, 8GB database)
  - Clerk Pro: $25/month (10,000 MAU, production support)
  - Google Cloud (Vertex AI): $100-200/month estimated (usage-based, credits consumed)
  - Stripe: 2.9% + $0.30 per transaction (no monthly fee)
  - Resend: $20/month (50,000 emails)
  - Mintlify: $0/month (open-source docs)
  - PostHog: $0/month (<1M events)
  - Sentry: $0/month (5K errors/month free tier)
  - **Total MVP costs: $170-245/month**

- **Scaling costs (Month 6, 150 customers):**
  - Vercel Pro: $20/month (1TB bandwidth, faster builds)
  - Supabase Pro: $25/month (still sufficient)
  - Clerk Pro: $25/month (still under 10K MAU)
  - Google Cloud (Vertex AI): $500-800/month (higher usage)
  - Stripe fees: ~$200/month (on ~$7K revenue)
  - Domain + SSL: $20/year (Vercel includes SSL)
  - **Total Month 6 costs: $770-1,070/month**
  - **Revenue target: $9,200/month (subscription + credits)**
  - **Profit margin: 88-91%**

**Personal Budget Constraint:**
- **Solo founder:** No salary for first 6-12 months (living expenses covered separately)
- **No marketing budget:** Growth via organic channels (Product Hunt, ChatGPT Apps, content)
- **Paid marketing (Month 6+):** Max $500/month if product-market fit proven

**Trade-offs Due to Budget:**
- No paid user acquisition initially (relies on distribution channels, virality)
- No hiring until profitability ($30K+ MRR, Month 12+)
- Infrastructure choices optimize for low fixed costs (serverless, usage-based pricing)

---

**Timeline Constraints:**

**Aggressive 3-Month MVP Deadline:**
- **Why aggressive:** Need to reach market quickly before competitors build similar solutions
- **Solo founder time:** 60-80 hours/week (full-time commitment)
- **AI development tools:** Cursor, Claude Code, v0 expected to provide 3-5x productivity multiplier
- **Scope discipline:** Ruthless prioritization, MVP features only, no scope creep

**Weekly Milestone Checkpoints:**
- **Every Friday:** Review progress against weekly goals
- **Month 2 checkpoint:** If <50% complete, descope features or extend timeline by 2 weeks
- **Slip contingency:** Built-in 2-week buffer before public launch (Week 10 private beta, Week 12 public)

**Time Allocation (Weekly):**
- Development: 50 hours (agent logic, UI, database, integrations)
- Design partner feedback: 5 hours (user interviews, prompt iteration)
- Planning/docs: 5 hours (PRD updates, architecture decisions)
- Buffer: 10 hours (unexpected bugs, scope creep, burnout prevention)

---

**Resource Constraints:**

**Solo Founder Limitations:**
- **Single point of failure:** If founder unavailable (illness, burnout), development stops
- **Skill gaps:** Solo founder may lack expertise in specific areas (e.g., advanced Vertex AI tuning, SQL optimization)
- **Decision velocity:** All decisions bottleneck through one person (no team to delegate to)
- **Support burden:** Post-launch, customer support competes with development time

**Mitigation Strategies:**
- **AI development tools:** Cursor, Claude Code reduce coding time by 3-5x
- **No-code/low-code tools:** Clerk (auth), Stripe (payments), Mintlify (docs) eliminate custom builds
- **Design partners:** 10 beta users provide early feedback, reducing guesswork
- **Community support:** Lean on indie hacker communities (Twitter, Reddit) for advice
- **Health buffer:** 1 day/week off minimum to prevent burnout

**No Team = No Specialized Roles:**
- No dedicated designer (using Untitled UI pre-built components)
- No dedicated PM (founder acts as PM based on BMAD/BVSSH principles)
- No dedicated QA (relies on design partner testing + Playwright E2E tests)
- No dedicated DevOps (Vercel handles infrastructure)
- No dedicated support (founder handles all customer inquiries in MVP)

---

**Technical Constraints:**

**Vercel Serverless Function Limits:**
- **Timeout:** 10 seconds (Hobby/Pro), 300 seconds (Enterprise)
- **Memory:** 1024 MB (Hobby/Pro), 3008 MB (Enterprise)
- **Payload size:** 4.5 MB request/response limit
- **Concurrency:** Automatic scaling, but cold starts possible (1-3s delay)

**Impact on Product:**
- Agent operations must complete in <10 seconds or use background jobs
- Large document exports (>4.5MB) require streaming or chunking
- Cold starts may affect first request after inactivity (acceptable for MVP)

**Supabase Constraints:**
- **Database size:** 8GB limit (Pro plan) - sufficient for 10,000+ initiatives
- **Bandwidth:** 250GB/month (Pro plan) - sufficient for 500-1,000 active users
- **Concurrent connections:** 60 pooled connections (Pro plan) - sufficient for 1,000 concurrent users

**Impact on Product:**
- Need connection pooling from Day 1 (PgBouncer included)
- If database exceeds 8GB (unlikely before Month 12), upgrade to Team plan ($599/mo)

**Vertex AI Constraints:**
- **Rate limits:** 60 requests/minute per model (Gemini Flash/Pro)
- **Quota limits:** $1,000/month default quota (can request increase)
- **Regional availability:** Model Garden (Claude) only available in specific regions (us-central1, europe-west1)

**Impact on Product:**
- Need request queuing if rate limit hit (exponential backoff)
- Monitor quota usage weekly, request increases proactively
- Multi-region fallback if primary region unavailable

---

#### **Key Assumptions**

**Product Assumptions:**

**Assumption 1: AI Agents Can Achieve 80%+ Approval Rate**
- **Assumption:** With proper prompt engineering, 7 specialized agents can generate documentation that users approve without major revisions 80%+ of the time
- **Validation:** Design partner testing in Month 2 (10 users, 30+ initiatives)
- **Risk if wrong:** Users churn due to poor quality outputs, negative reviews, failed product-market fit
- **Contingency:** A/B test prompts weekly, iterate rapidly, consider fine-tuning models if needed

**Assumption 2: Users Will Pay $25-50/mo + Credits for Planning Acceleration**
- **Assumption:** Solo developers and teams value planning acceleration enough to pay subscription + variable credit costs
- **Validation:** Pricing interviews with 20 target users (Month 1), paid conversion rates (Month 3-4)
- **Risk if wrong:** Low conversion rates, high churn, need to adjust pricing or value proposition
- **Contingency:** Test $19/mo (lower barrier) or $39/mo (higher value perception), offer annual discounts (2 months free)

**Assumption 3: Credit-Based Model Drives Higher Revenue Than Fixed Tiers**
- **Assumption:** Users will purchase additional credits beyond base 100/month, driving $24-32/month average credit revenue
- **Validation:** Track Month 1-3 credit consumption patterns, purchase frequency
- **Risk if wrong:** Users stay within 100 credits/month, revenue lower than projected
- **Contingency:** Adjust credit consumption rates (make operations use more credits), increase base subscription price

**Assumption 4: Users Want Opinionated Workflow Over Flexibility**
- **Assumption:** Target users prefer guided, structured workflows (Initiative → Epic → Feature → Story → Task) over freeform planning
- **Validation:** Design partner feedback (Month 2), feature usage analytics (which sections skipped?)
- **Risk if wrong:** Users frustrated by rigid structure, churn to more flexible tools (Notion)
- **Contingency:** Add "Custom Workflow" mode (Phase 4) that allows reordering/skipping phases

**Assumption 5: AI Coding Assistants Want Planning Context**
- **Assumption:** Developers using Cursor, Windsurf, Claude Code actively seek planning context and will integrate RoadmapKO
- **Validation:** MCP adoption rates (Month 6-7), user interviews about AI coding workflows
- **Risk if wrong:** Integration adoption <20%, key differentiator doesn't resonate
- **Contingency:** Pivot messaging to "planning for humans" (de-emphasize AI assistant bridge), focus on solo dev use case

---

**Market Assumptions:**

**Assumption 6: Solo Dev/Indie Hacker Market Is Large Enough**
- **Assumption:** 50,000+ solo developers/indie hackers globally are actively building SaaS projects and willing to pay for planning tools
- **Validation:** Product Hunt launch results, ChatGPT App install rates, community engagement (Twitter, Reddit)
- **Risk if wrong:** TAM smaller than expected, growth plateaus at <100 customers
- **Contingency:** Expand to enterprise market faster (Month 6 vs. Month 9), add agency tier earlier

**Assumption 7: Distribution Channels (ChatGPT Apps, MCP) Are Viable**
- **Assumption:** ChatGPT Apps SDK and Claude MCP will drive significant user acquisition (100+ customers in Month 4-7)
- **Validation:** Phase 2 launch results (installation rates, conversion rates)
- **Risk if wrong:** Distribution channels provide <20 customers, need alternative acquisition strategy
- **Contingency:** Invest in content marketing (SEO blog, YouTube tutorials), paid ads (Google, Twitter), partnerships (Cursor, Windsurf)

**Assumption 8: Linear/Jira Won't Build Competing Features Soon**
- **Assumption:** Linear and Jira will focus on execution features, not upstream planning, giving RoadmapKO 12-18 month runway
- **Validation:** Monitor Linear/Jira release notes, feature announcements, job postings (hiring AI engineers?)
- **Risk if wrong:** Linear launches "AI Planning Agent" in Month 6, commoditizes RoadmapKO's value prop
- **Contingency:** Pivot to distribution channels (ChatGPT Apps, MCP) where Linear can't compete, double down on multi-platform orchestration, explore acquisition discussions

**Assumption 9: BMAD/BVSSH Methodology Can Be Productized**
- **Assumption:** The opinionated planning methodology (inspired by BMAD principles) can be embedded into AI agent workflows without requiring users to learn methodology explicitly
- **Validation:** Design partner feedback (do users understand workflow without training?), completion rates (do users finish initiatives?)
- **Risk if wrong:** Users confused by methodology, abandon mid-workflow, high drop-off rates
- **Contingency:** Add onboarding tutorial (interactive walkthrough), methodology explainer docs, optional "BMAD Mode" vs. "Simple Mode"

---

**Technical Assumptions:**

**Assumption 10: Google ADK TypeScript SDK Is Production-Ready**
- **Assumption:** Google Agent Development Kit has sufficient TypeScript support and stability for production use in MVP
- **Validation:** Week 1-2 prototype (build basic agent orchestration, test tool use, structured outputs)
- **Risk if wrong:** ADK bugs, missing features, poor documentation, development delays
- **Contingency:** Use Vertex AI REST API directly (no ADK abstraction), build custom orchestration layer, consider LangChain.js as alternative

**Assumption 11: Vercel Serverless Functions Can Handle Agent Workloads**
- **Assumption:** 10-second timeout is sufficient for most agent operations; long operations are rare
- **Validation:** Monitor function execution times in Week 3-4 (during agent development)
- **Risk if wrong:** Frequent timeouts, poor UX, need infrastructure changes
- **Contingency:** Upgrade to Vercel Enterprise (300s timeout), implement background job queue (Inngest/QStash), optimize prompts to reduce generation time

**Assumption 12: Vertex AI Costs Are Predictable and Manageable**
- **Assumption:** Credit consumption costs remain within 10-20% of credit revenue (80-90% margin)
- **Validation:** Track costs daily in Month 1-3, adjust model routing if margins compress
- **Risk if wrong:** LLM pricing increases, margins compress to <70%, profitability delayed
- **Contingency:** Raise credit prices (+10-20%), route more operations to Gemini Flash (cheaper), negotiate volume discounts with Google

**Assumption 13: Clerk + Supabase Integration Is Reliable**
- **Assumption:** Clerk webhooks reliably sync user data to Supabase without race conditions or data loss
- **Validation:** Test user signup flow 100+ times (automated E2E tests), monitor webhook success rates
- **Risk if wrong:** Users created in Clerk but not Supabase, broken authentication, data inconsistencies
- **Contingency:** Implement reconciliation job (daily sync), retry logic with exponential backoff, manual fix tooling for support

---

**Founder Assumptions:**

**Assumption 14: Solo Founder Can Maintain 60-80 Hours/Week for 3 Months**
- **Assumption:** Founder has capacity, health, and motivation to work full-time on MVP without burnout
- **Validation:** Weekly self-assessment (energy levels, progress velocity, mental health)
- **Risk if wrong:** Burnout, slower progress, missed deadlines, health issues
- **Contingency:** Extend timeline by 4 weeks (Month 4 launch vs. Month 3), descope features aggressively, take 1 week off to recover, consider co-founder or contractor (if budget allows)

**Assumption 15: AI Development Tools Provide 3-5x Productivity Boost**
- **Assumption:** Cursor, Claude Code, v0 accelerate development significantly vs. manual coding
- **Validation:** Track development velocity (features shipped per week), compare to baseline expectations
- **Risk if wrong:** AI tools less helpful than expected, timeline slips, need more time
- **Contingency:** Extend timeline, hire contractor for specific features (UI, integration), simplify MVP scope

**Assumption 16: Design Partners Will Provide Actionable Feedback**
- **Assumption:** 10 design partners actively test product, provide weekly feedback, iterate on prompts
- **Validation:** Track design partner engagement (logins, initiatives created, feedback submitted)
- **Risk if wrong:** Design partners disengaged, insufficient feedback, blind to quality issues
- **Contingency:** Recruit new design partners, offer higher incentives (free annual subscription vs. 50% discount), conduct structured user interviews

---

#### **Dependency Assumptions**

**External Dependencies (Platform/Service Availability):**

**Assumption 17: Vercel, Supabase, Clerk, Vertex AI Maintain 99%+ Uptime**
- **Assumption:** Core infrastructure providers are reliable, minimal downtime
- **Validation:** Monitor status pages (status.vercel.com, status.supabase.com, status.clerk.com, cloud.google.com/status)
- **Risk if wrong:** Service outages, user frustration, churn, SLA breaches (if Enterprise tier)
- **Contingency:** 
  - Vercel: Multi-region deployment (if critical)
  - Supabase: Database backups (daily), restore within 1 hour
  - Clerk: Graceful degradation (cached user sessions)
  - Vertex AI: Fallback to OpenAI/Anthropic direct APIs (emergency)

**Assumption 18: OpenAI ChatGPT Apps SDK and Anthropic MCP Remain Viable**
- **Assumption:** Distribution channels remain open, policies don't change mid-development
- **Validation:** Monitor OpenAI/Anthropic announcements, developer forums
- **Risk if wrong:** ChatGPT Apps SDK discontinued, MCP deprecated, distribution channels close
- **Contingency:** Focus on web app growth, invest in SEO/content, paid acquisition, partnerships

**Assumption 19: Stripe Processes Payments Reliably**
- **Assumption:** Stripe subscription billing, one-time payments, refunds work without issues
- **Validation:** Test payment flows extensively (100+ test transactions), monitor Stripe dashboard
- **Risk if wrong:** Payment failures, delayed payouts, customer complaints
- **Contingency:** Alternative payment processor (Paddle, Lemon Squeezy) as backup, manual invoicing (extreme case)

---

### **Assumption Validation Plan**

**Month 1 Validations:**
- ✅ Google ADK TypeScript SDK prototype (Assumption 10)
- ✅ Pricing interviews with 20 users (Assumption 2)
- ✅ Design partner recruitment (Assumption 16)
- ✅ Clerk + Supabase integration testing (Assumption 13)

**Month 2 Validations:**
- ✅ Agent quality testing with 10 design partners (Assumption 1)
- ✅ Credit consumption tracking (Assumption 3, 12)
- ✅ Opinionated workflow feedback (Assumption 4)
- ✅ BMAD methodology productization (Assumption 9)

**Month 3 Validations:**
- ✅ MVP launch metrics (conversion rates, activation, usage)
- ✅ Solo dev market size (Assumption 6)
- ✅ AI coding assistant integration demand (Assumption 5)
- ✅ Timeline adherence (Assumption 14, 15)

**Month 4-7 Validations:**
- ✅ Distribution channel viability (Assumption 7)
- ✅ Credit revenue model (Assumption 3)
- ✅ Competitive response monitoring (Assumption 8)

---

### **Risks & Open Questions**

#### **Key Risks**

Risks are categorized by severity and probability to prioritize mitigation efforts:
- 🔴 **CRITICAL (RED):** High probability (>30%) AND high impact (business-threatening)
- 🟡 **SIGNIFICANT (YELLOW):** Medium probability (15-30%) OR medium impact (delays/revenue impact)
- 🟢 **MANAGEABLE (GREEN):** Low probability (<15%) OR low impact (minor inconvenience)

---

**🔴 CRITICAL RISK 1: Agent Output Quality Fails to Meet 80% Approval Rate**

**Description:** AI agents generate documentation that users reject or request major revisions >20% of the time, indicating insufficient quality for paid product.

**Probability:** 40-45%

**Impact:** 
- Users churn within first month (poor retention)
- Negative reviews damage acquisition (Product Hunt, Twitter)
- Failed product-market fit, need fundamental pivot
- Wasted development time on infrastructure if core value prop doesn't work

**Early Warning Signals:**
- Design partner approval rates <70% (Month 2)
- Feedback: "Agent output needs too much editing"
- High refund requests citing "AI not good enough"

**Mitigation Strategies:**
- **Pre-launch:** Extensive prompt engineering (Week 3-10), A/B test prompts with design partners
- **Launch:** Daily monitoring of approval rates per agent, per document type
- **Iteration:** Weekly prompt refinement based on rejected outputs
- **Model optimization:** Route complex tasks to Claude (higher quality), simple tasks to Gemini Flash (cost-effective)
- **Human oversight:** Validation Agent reviews all outputs for quality gates
- **Transparency:** Set expectations ("AI drafts, you refine") vs. "AI does it perfectly"

**Contingency Plan:**
- If <70% approval by Week 8: Pause development, focus 2 weeks on prompt quality
- If <75% by Month 3 launch: Delay public launch, extend private beta 2-4 weeks
- If <80% by Month 4: Consider pivot to "AI-assisted templates" vs. "AI-generated docs"

---

**🔴 CRITICAL RISK 2: Solo Founder Velocity Insufficient to Hit 3-Month Timeline**

**Description:** Development takes longer than estimated, MVP slips to Month 4-6, missing market window or running out of runway.

**Probability:** 35-40%

**Impact:**
- Delayed revenue (burn runway without income)
- Competitive window closes (Linear/Jira builds agents)
- Founder burnout increases with extended timeline
- Missed Product Hunt momentum (optimal launch timing lost)

**Early Warning Signals:**
- Week 4: <30% of foundation complete
- Week 8: <60% of agent orchestration complete
- Week 10: Private beta not ready
- Consistent 50-60 hour weeks (vs. planned 60-80)

**Mitigation Strategies:**
- **Weekly checkpoints:** Every Friday, assess progress vs. plan
- **Scope discipline:** Ruthless prioritization, defer non-critical features immediately
- **AI development tools:** Maximize Cursor, Claude Code, v0 usage (3-5x multiplier)
- **Pre-built components:** Use Untitled UI, no custom UI from scratch
- **Month 2 checkpoint:** If <50% complete, descope aggressively or add 2-week buffer

**Contingency Plan:**
- **Descope options (in priority order):**
  1. Remove Design Agent UI generation prompts (defer to Phase 2)
  2. Remove Validation Agent (manual review gates only)
  3. Reduce agent count from 7 to 5 (merge Quality into Requirements)
  4. Launch with 3 agents only (Discovery, Requirements, Planning)
- **Timeline extension:** Add 2-4 week buffer, push launch to Month 4
- **Contractor hiring:** If budget allows, hire for specific features (integrations, UI polish)

---

**🔴 CRITICAL RISK 3: ChatGPT Apps SDK or Claude MCP Distribution Fails**

**Description:** Distribution channels (ChatGPT Apps, Claude MCP) don't drive expected user acquisition (target: 100+ customers Month 4-7).

**Probability:** 40-50%

**Impact:**
- Growth stalls at <50 customers (missed Month 6 target of 150)
- Revenue targets missed ($5K MRR vs. $9K target)
- Need pivot to expensive paid acquisition
- Lifestyle business trajectory only (not venture-scale)

**Early Warning Signals:**
- ChatGPT App: <100 installs in first week (vs. target 500+)
- ChatGPT App: <5% conversion to paid (vs. target 10%)
- MCP: <50 installs in first week (vs. target 200+)
- User feedback: "I prefer using RoadmapKO web app directly"

**Mitigation Strategies:**
- **Don't rely solely on distribution:** Build organic channels in parallel
  - Product Hunt launch (Month 3)
  - Content marketing (SEO blog, YouTube tutorials)
  - Community engagement (Twitter, Indie Hackers, Reddit)
- **Test distribution assumptions early:** 
  - Month 1: Survey target users "Would you use RoadmapKO via ChatGPT?"
  - Month 3: Soft-launch ChatGPT App to waitlist (gauge demand before full launch)
- **Optimize conversion:** A/B test onboarding in ChatGPT App, improve signup-to-activation flow

**Contingency Plan:**
- **Pivot to paid acquisition (Month 6+):**
  - Google Ads: $500/month budget (target $100 CAC, 5 customers/month)
  - Twitter Ads: Target indie hackers, AI developers
  - Sponsorships: YouTube creators (Theo, Fireship, Web Dev Simplified)
- **Content marketing (Month 4+):**
  - SEO blog: "How to write a PRD," "SaaS planning guide," "AI-assisted development"
  - YouTube: "Build a SaaS in 2 hours with AI planning agents"
  - Case studies: "How [User] shipped their SaaS 3x faster with RoadmapKO"
- **Partnerships:**
  - Cursor: Explore bundling or affiliate partnership
  - Lovable/v0: Cross-promotion (planning + UI generation)

---

**🟡 SIGNIFICANT RISK 4: Pricing Too High for Solo Devs ($25/mo + Credits)**

**Description:** Target users (solo devs, indie hackers) resist $25/mo subscription + variable credit costs, citing budget constraints or insufficient perceived value.

**Probability:** 30-35%

**Impact:**
- Low conversion rates (<5% vs. target 10%)
- High churn (users try once, don't see ROI, cancel)
- Need pricing adjustments (delays revenue growth)
- Downward pricing pressure (race to bottom vs. competitors)

**Early Warning Signals:**
- Month 1 pricing interviews: >50% say "$25/mo is too expensive"
- Month 3 conversion: <5% visitor-to-paid conversion rate
- Month 3 signup rates: <10 paid signups in first 2 weeks
- User feedback: "I'll just use ChatGPT directly for free"

**Mitigation Strategies:**
- **Value messaging:** Emphasize time saved (5+ hours/initiative), ROI calculation ($25/mo vs. $150/hour PM)
- **Pricing experiments:** A/B test $19/mo (lower barrier) vs. $29/mo (higher value perception)
- **Annual discount:** Offer 2 months free ($250/year vs. $300/year) to lock in customers
- **Free tier (post-MVP):** 1 initiative/month free (hook users, upsell to paid)
- **Credit bundles:** Offer starter pack (Pro + 400 credits = $49/mo all-in, saves $3)

**Contingency Plan:**
- **Pricing adjustment (Month 4):**
  - If conversion <7%: Drop to $19/mo Pro, $39/mo Business
  - If credit purchases low: Increase base credits to 200/month (absorb margin hit)
  - If enterprise interest high: Focus on $50+ ARPU customers (agencies, teams)
- **Value-added features:** Add features that justify price (templates, brownfield migration, white-glove onboarding)
- **Lifetime deal (one-time):** Offer $499 lifetime at launch (limited to 100 customers, creates urgency)

---

**🟡 SIGNIFICANT RISK 5: Linear or Jira Builds Native AI Agents**

**Description:** Linear or Jira launches "AI Planning Assistant" that generates briefs, PRDs, and stories natively, commoditizing RoadmapKO's core value.

**Probability:** 25-30% in next 12-18 months

**Impact:**
- Differentiation erodes (features become table stakes)
- Customer acquisition harder (why pay for standalone tool?)
- Pricing pressure (need to compete on price vs. bundled feature)
- Potential pivot required (focus on distribution, multi-platform)

**Early Warning Signals:**
- Linear/Jira job postings: Hiring "AI/ML Engineers" or "LLM Specialists"
- Product announcements: "AI-powered sprint planning" or "Smart issue creation"
- Competitor launches: Shortcut, ClickUp, Monday.com add AI agents
- User feedback: "Why doesn't Linear just build this?"

**Mitigation Strategies:**
- **Move fast:** Launch and iterate before competitors (first-mover advantage)
- **Differentiation:**
  - Multi-platform orchestration (works with Linear, Jira, Notion, Azure Boards)
  - Distribution channels (ChatGPT Apps, MCP) where Linear can't compete
  - Opinionated methodology (BMAD-inspired) vs. generic AI suggestions
  - Specialized agents (7 experts) vs. single generic assistant
- **Deep specialization:** Focus on planning depth (market research, competitive analysis, architecture) vs. shallow AI autocomplete
- **Network effects:** Build integrations ecosystem that Linear can't replicate quickly

**Contingency Plan:**
- **Pivot 1: Distribution-first (if Linear builds agents):**
  - Double down on ChatGPT Apps, Claude MCP (channels Linear doesn't control)
  - Position as "AI planning layer for any tool" vs. "Linear competitor"
  - Revenue from credit consumption (not subscriptions)
- **Pivot 2: Enterprise specialization:**
  - Focus on large orgs with complex needs (brownfield migration, compliance, multi-team coordination)
  - Custom integrations, white-glove support (features Linear won't build)
- **Pivot 3: Acquisition target:**
  - Position as strategic acquisition for Linear, Jira, or Notion ($50-100M valuation)
  - Demonstrate customer traction, technology differentiation, retention metrics

---

**🟡 SIGNIFICANT RISK 6: Customer Support Overwhelms Development Time**

**Description:** Post-launch, customer support requests consume 20+ hours/week, slowing feature development and product iteration.

**Probability:** 25-30% if >100 customers by Month 4

**Impact:**
- Slower feature velocity (delays Phase 2-3 features)
- Founder burnout (context switching between support and coding)
- Product quality suffers (bugs accumulate, tech debt grows)
- Competitive disadvantage (slower iteration vs. funded competitors)

**Early Warning Signals:**
- Month 3: >10 support emails/day (>5 hours/week)
- Month 4: >20 support emails/day (>10 hours/week)
- Recurring questions (same issues asked repeatedly)
- Bug reports outnumber feature requests (quality issues)

**Mitigation Strategies:**
- **Self-service documentation:** Comprehensive Mintlify docs, video tutorials, FAQ
- **In-app help:** Contextual tooltips, onboarding wizard, example initiatives
- **Community support:** Discord/Slack community where users help each other
- **Office hours:** Scheduled weekly Q&A (batch support vs. interrupt-driven)
- **Support SLAs:** 48-hour response time (Pro), 24-hour (Business), 4-hour (Enterprise)

**Contingency Plan:**
- **Month 6: Hire part-time support admin ($15-20/hour, 10-20 hours/week)**
  - Cost: $600-1,600/month (affordable at $9K MRR)
  - Focus on: Tier 1 support (password resets, billing questions, "how do I...")
  - Founder handles: Tier 2 (bug triage, feature requests, escalations)
- **Automation:**
  - Chatbot for common questions (Intercom, Crisp)
  - Email templates for recurring issues (Canned responses)
  - Self-service billing portal (Stripe Customer Portal)

---

**🟡 SIGNIFICANT RISK 7: Vertex AI Costs Exceed Projections (Margin Compression)**

**Description:** LLM usage costs are higher than expected due to inefficient prompts, model changes, or user behavior (longer documents, more revisions).

**Probability:** 30-35%

**Impact:**
- Gross margins compress from 90-95% to 70-80%
- Profitability delayed (need higher revenue to cover costs)
- Pricing adjustments needed (raise credit prices, reduce base credits)
- Cashflow issues (variable costs spike before revenue catches up)

**Early Warning Signals:**
- Month 1: Average operation costs $0.05-0.10 (vs. projected $0.01-0.02)
- Month 2: Margin <80% (vs. target 90-95%)
- Month 3: Vertex AI bill >$500 with <50 customers
- User behavior: Frequent revisions (3-5x per document vs. expected 1-2x)

**Mitigation Strategies:**
- **Prompt optimization:** Reduce output tokens, use structured outputs (less verbose)
- **Model routing:** Use Gemini Flash for 80% of operations (lowest cost), Claude for critical 20%
- **Caching:** Cache common responses (e.g., "What's a PRD?", template sections)
- **Usage monitoring:** Real-time cost tracking (alert if daily costs >$50)
- **Request batching:** Combine multiple operations (e.g., generate Brief + Research in one call)

**Contingency Plan:**
- **Adjust credit pricing (Month 4):**
  - Increase credit cost from $0.10 to $0.12 (+20%)
  - Reduce base credits from 100 to 75/month
  - Absorb 10-15% margin compression short-term
- **Optimize operations:**
  - Week-long sprint to reduce token usage by 30-50%
  - Switch more operations to Gemini Flash (sacrifice quality for cost)
- **Negotiate with Google:**
  - Request volume discounts at $5K/month spend
  - Apply for Google for Startups credits ($200K over 2 years)

---

**🟢 MANAGEABLE RISK 8: Vercel Function Timeouts for Long Operations**

**Description:** Some agent operations exceed 10-second Vercel timeout, causing failed generations and poor UX.

**Probability:** 20-25%

**Impact:**
- User frustration (failed document generations)
- Need infrastructure changes (Vercel Enterprise or background jobs)
- Development delays (unplanned architecture work)

**Early Warning Signals:**
- Week 6: Agent operations consistently take 8-12 seconds
- Week 8: Timeout errors in Sentry (>5% of agent calls)
- User feedback: "Document generation failed"

**Mitigation Strategies:**
- **Optimize prompts:** Reduce generation time (fewer tokens, simpler instructions)
- **Streaming responses:** Show partial progress (reduce perceived wait time)
- **Upgrade Vercel plan:** Enterprise tier ($500/mo) has 300s timeout

**Contingency Plan:**
- **Background jobs (if timeouts persist):**
  - Implement queue (Inngest or QStash)
  - User clicks "Generate" → queues job → returns immediately
  - User receives email when document ready (5-10 minutes)
  - Acceptable for complex operations (Architecture, full initiative generation)

---

**🟢 MANAGEABLE RISK 9: Google ADK TypeScript Bugs or Limitations**

**Description:** Google Agent Development Kit has missing features, bugs, or poor documentation, slowing development.

**Probability:** 20-25%

**Impact:**
- Development delays (need workarounds or custom solutions)
- Increased complexity (more code to maintain)
- Frustration and context switching

**Early Warning Signals:**
- Week 1-2 prototype: ADK doesn't support required features (tool use, structured outputs)
- Week 3-4: Frequent bugs, need multiple workarounds
- Documentation gaps, no community support

**Mitigation Strategies:**
- **Early validation:** Week 1 prototype tests all critical ADK features
- **Abstraction layer:** Wrap ADK in custom interface (can swap to direct Vertex AI API)
- **Fallback plan:** Use Vertex AI REST API directly if ADK insufficient

**Contingency Plan:**
- **Week 2: If ADK doesn't work, pivot to direct Vertex AI API**
  - Build custom orchestration layer (adds 1-2 weeks)
  - Use proven patterns (function calling, structured outputs)
- **Community engagement:** Open GitHub issues, engage Google Cloud support

---

**🟢 MANAGEABLE RISK 10: Clerk + Supabase Sync Issues**

**Description:** Race conditions or webhook failures cause users to be created in Clerk but not Supabase, breaking authentication.

**Probability:** 15-20%

**Impact:**
- User signup failures (poor first impression)
- Support burden (manual user creation)
- Data inconsistencies (orphaned Clerk users)

**Early Warning Signals:**
- Week 4 testing: Occasional webhook failures (1-5%)
- Week 8: Sentry errors "User not found in Supabase"
- User complaints: "I signed up but can't log in"

**Mitigation Strategies:**
- **Idempotent webhooks:** Safe to replay, check if user exists before creating
- **Retry logic:** Exponential backoff on webhook failures (3 retries)
- **Daily reconciliation:** Cron job compares Clerk users vs. Supabase users, fixes gaps
- **Monitoring:** Alert on webhook failures (Sentry, email)

**Contingency Plan:**
- **Manual fix tooling:** Admin UI to manually create missing Supabase users
- **Webhook queue:** Use Svix (webhook infrastructure) for reliable delivery

---

#### **Open Questions**

**Product Questions:**

**Q1: Should we offer a free tier (1 initiative/month) to drive adoption?**
- **Pros:** Lower barrier to entry, viral growth potential, larger funnel
- **Cons:** Support burden, potential for abuse, dilutes paid conversion
- **Decision needed by:** Month 3 (before public launch)
- **Validation approach:** Survey design partners, A/B test post-launch

**Q2: Should TipTap editing be in MVP or Phase 4?**
- **Current plan:** Phase 4 (Month 12)
- **Alternative:** Include in MVP (improves UX, delays launch by 2 weeks)
- **Decision needed by:** Week 6 (before UI finalization)
- **Validation approach:** Design partner feedback on markdown-only editing

**Q3: Should we allow custom agent personalities (e.g., "formal" vs. "casual")?**
- **Pros:** Personalization, user delight, differentiation
- **Cons:** Complexity, inconsistent quality, more prompt maintenance
- **Decision needed by:** Month 6 (Phase 2 planning)
- **Validation approach:** User interviews about tone preferences

---

**Technical Questions:**

**Q4: Should we build abstraction layer over Vertex AI ADK in MVP?**
- **Current plan:** No abstraction (use ADK directly)
- **Alternative:** Build thin abstraction layer (swap to LangChain if needed)
- **Decision needed by:** Week 1 (before agent implementation)
- **Validation approach:** Week 1 prototype, assess ADK stability

**Q5: Should we use Supabase Edge Functions or Vercel Serverless Functions for agents?**
- **Current plan:** Vercel Serverless Functions (TypeScript, same codebase)
- **Alternative:** Supabase Edge Functions (Deno, closer to database)
- **Decision needed by:** Week 2 (before API implementation)
- **Validation approach:** Prototype both, compare performance and DX

**Q6: Should we implement real-time collaboration (multi-user editing) in Phase 4?**
- **Pros:** Enterprise feature, higher ARPU, competitive advantage
- **Cons:** Complex (Y.js, WebSockets), high infrastructure cost, edge cases
- **Decision needed by:** Month 9 (Phase 4 planning)
- **Validation approach:** Enterprise customer interviews about collaboration needs

---

**Go-to-Market Questions:**

**Q7: Should we do private beta (2 weeks) or public launch immediately?**
- **Current plan:** Private beta (10 design partners, Week 10-12), then public
- **Alternative:** Skip private beta, launch publicly on Product Hunt (Week 10)
- **Decision needed by:** Week 8 (before launch planning)
- **Validation approach:** Design partner recruitment success rate

**Q8: Which integration should we build first: Linear, Jira, Notion, or Azure Boards?**
- **Current plan:** Survey design partners (Month 2), decide based on demand
- **Alternative:** Build Linear first (most popular with indie devs)
- **Decision needed by:** Month 7 (before Phase 3 implementation)
- **Validation approach:** Integration demand survey (100+ responses)

**Q9: Should we launch ChatGPT Apps before or after MCP?**
- **Current plan:** ChatGPT Apps (Month 4-5), then MCP (Month 6-7)
- **Alternative:** MCP first (smaller, more aligned with AI coding workflow)
- **Decision needed by:** Month 3 (before distribution development)
- **Validation approach:** User interviews about preferred workflow (ChatGPT vs. Claude)

---

**Strategic Questions:**

**Q10: Lifestyle business (bootstrap, profitable) or venture-scale (fundraise, rapid growth)?**
- **Current plan:** Start lifestyle, pivot to venture if traction is strong
- **Decision factors:**
  - Lifestyle: $30-50K MRR by Month 12, 15-20% month-over-month growth
  - Venture: $50K+ MRR by Month 6, 30-40% MoM growth, raise seed round ($1-2M)
- **Decision needed by:** Month 6 (if fundraising, need 3-6 months lead time)
- **Validation approach:** Track growth rate, competitive pressure, founder preference

**Q11: If Linear builds agents in Month 9, should we pivot, compete, or partner?**
- **Option 1 (Pivot):** Focus on distribution channels (ChatGPT, MCP), multi-platform orchestration
- **Option 2 (Compete):** Double down on quality, specialized agents, deeper features
- **Option 3 (Partner):** Explore integration partnership or acquisition discussions
- **Decision needed by:** When/if Linear announces AI features (monitor closely)
- **Validation approach:** Assess RoadmapKO's differentiation strength at that time

**Q12: Should primary target be solo devs, enterprise teams, or agencies?**
- **Current plan:** Solo devs (Phase 1) → Enterprise (Phase 2) → Agencies (Phase 3)
- **Alternative:** Focus on highest ARPU (agencies or enterprise) from Day 1
- **Decision needed by:** Month 3 (based on early customer mix)
- **Validation approach:** Track which segments convert best, have lowest churn

---

### **Areas Needing Research**

**Before Month 1 (Immediate):**

**R1: Design Partner Recruitment**
- **Goal:** Recruit 10 design partners (3 solo devs, 3 AI-native engineers, 2 indie SaaS builders, 2 vibe coders)
- **Channels:** Twitter/X, Indie Hackers, Reddit r/SideProject, BMAD community
- **Incentive:** 50% discount for 1 year ($150 vs. $300)
- **Timeline:** 2 weeks (recruit 10, onboard by Week 2)

**R2: Competitive Deep-Dive**
- **Goal:** Understand Cursor, Replit Agent, v0, Lovable user workflows; study Linear, Jira, Notion planning gaps
- **Method:** User interviews (20-30 minute calls), screen recordings, workflow observations
- **Deliverable:** Competitive analysis doc with 3-5 key differentiators
- **Timeline:** 2 weeks

**R3: Pricing Validation Interviews**
- **Goal:** Test willingness-to-pay for $25/mo + credits, understand current dev tool spend
- **Method:** 20 interviews with target users (solo devs, indie hackers, engineering leads)
- **Questions:** 
  - "What tools do you currently pay for?"
  - "How much time do you spend on planning vs. coding?"
  - "Would you pay $25/mo to save 5+ hours on planning?"
- **Deliverable:** Pricing recommendation (adjust to $19/mo, $29/mo, or keep $25/mo)
- **Timeline:** 2 weeks

---

**Month 1-2 (During Development):**

**R4: LLM Benchmarking**
- **Goal:** Compare Gemini Flash, Gemini Pro, Claude 3.5 Sonnet for each agent type
- **Metrics:** Output quality (approval rate), response time, cost per operation
- **Method:** Generate 50+ documents per agent with each model, measure metrics
- **Deliverable:** Model routing strategy (which model for which agent)
- **Timeline:** Ongoing (Week 3-8)

**R5: Load Testing**
- **Goal:** Validate Vercel + Supabase can handle 100-500 concurrent users
- **Method:** Artillery, k6, or Playwright for load testing
- **Scenarios:** 100 simultaneous agent calls, 500 concurrent users browsing
- **Deliverable:** Performance report, infrastructure scaling plan
- **Timeline:** Week 10 (before public launch)

**R6: Legal Review**
- **Goal:** Ensure Terms of Service, Privacy Policy, GDPR compliance
- **Method:** Use Termly or legal template, review with attorney (if budget allows)
- **Deliverable:** TOS, Privacy Policy, GDPR-compliant data handling
- **Timeline:** Week 10 (before public launch)

---

**Month 3-4 (Post-Launch):**

**R7: ChatGPT Apps SDK Proof-of-Concept**
- **Goal:** Validate technical feasibility, estimate development effort
- **Method:** Build minimal ChatGPT App (1-2 agents), test with 10 users
- **Deliverable:** Go/no-go decision on ChatGPT Apps launch
- **Timeline:** 2 weeks (Month 3)

**R8: Integration Demand Survey**
- **Goal:** Prioritize Linear, Jira, Notion, Azure Boards based on user demand
- **Method:** Survey 100+ users (email, in-app prompt)
- **Questions:** "Which tool do you use for execution?" "Would you use RoadmapKO integration?"
- **Deliverable:** Integration prioritization (likely Linear first)
- **Timeline:** Month 3-4

**R9: Customer Support Playbook**
- **Goal:** Standardize support responses, reduce handling time
- **Method:** Document common issues, create canned responses, video tutorials
- **Deliverable:** Support knowledge base (Mintlify docs), Intercom macros
- **Timeline:** Month 4 (after first 50 customers)

---

## **Appendices**

---

### **A. Research Summary**

This Project Brief is supported by comprehensive research and analysis across multiple dimensions:

#### **Competitive Analysis Summary**

**Execution Tools (Linear, Jira, Azure Boards):**
- **Strengths:** Excellent sprint management, issue tracking, developer workflows
- **Gaps:** Assume planning is already done; no upstream guidance for strategy, requirements, or architecture
- **Opportunity:** RoadmapKO focuses on the "front-half" (planning) that execution tools ignore

**Documentation Tools (Notion, Confluence, Google Docs):**
- **Strengths:** Flexible, easy to use, great for unstructured content
- **Gaps:** No enforced relationships between documents, no opinionated workflows, documents become stale
- **Opportunity:** RoadmapKO enforces structured hierarchy and maintains document relationships

**AI Coding Assistants (Cursor, Windsurf, Claude Code, GitHub Copilot):**
- **Strengths:** Brilliant at code generation from prompts
- **Gaps:** Lack access to strategic context (business goals, architectural decisions, cross-feature dependencies)
- **Opportunity:** RoadmapKO provides the context layer that AI coding assistants need via MCP/API integration

**AI Project Tools (ChatGPT Projects, Claude Projects):**
- **Strengths:** Maintain conversation context, can draft documents
- **Gaps:** Generic assistants without specialized planning expertise, no structured hierarchy or workflow enforcement
- **Opportunity:** RoadmapKO offers 7 specialized agents with domain expertise vs. single generic assistant

**Traditional PM Tools (Aha!, ProductPlan, Roadmunk):**
- **Strengths:** Enforce process, provide roadmap visualization
- **Gaps:** Rigid templates, no intelligence to guide or validate, not designed for AI-native workflows
- **Opportunity:** RoadmapKO combines opinionated structure with AI intelligence and modern UX

#### **Market Trends Analysis**

**Trend 1: AI Coding Assistant Adoption Explosion**
- GitHub Copilot: 1.8M+ paid users (as of Q4 2024)
- Cursor: 50K+ monthly active teams, 30%+ month-over-month growth
- Claude Code CLI: Launched October 2024, rapid adoption among developers
- **Implication:** Developers now expect AI assistance; planning tools must provide context for these assistants

**Trend 2: Remote Work Documentation Crisis**
- Distributed teams amplify planning problems (no "just talk it out" workaround)
- Async work requires better documentation practices
- McKinsey: 8-12 hours/week wasted searching for context across tools
- **Implication:** Centralized, structured planning documentation is more valuable than ever

**Trend 3: Distribution Channel Democratization**
- ChatGPT Apps SDK: 800M+ potential users, zero-friction distribution
- Claude MCP: Direct desktop integration, native to developer workflows
- **Implication:** Building marketplace presence from scratch no longer required

**Trend 4: Opinionated Software Renaissance**
- Linear's success: Opinionated workflows beat flexibility (vs. Jira's complexity)
- Notion's growth: Started opinionated (docs), became too flexible (users want guidance)
- **Implication:** Developers want opinionated tools that enforce best practices without being rigid

#### **User Research Insights**

**Solo Developer Pain Points (from preliminary interviews):**
1. "I can prototype fast with Cursor but can't scale to production" (90% of 10 interviewees)
2. "I'm a developer, not a PM—I don't know how to write requirements" (80%)
3. "My AI coding assistant makes conflicting architectural choices" (70%)
4. "Documentation is always an afterthought" (100%)

**Enterprise Team Pain Points (from preliminary interviews):**
1. "My team uses AI coding assistants but they lack strategic context" (85% of 10 interviewees)
2. "Documentation is fragmented across 5+ tools" (100%)
3. "Requirements emerge mid-sprint, causing thrash" (90%)
4. "I can't scale myself across multiple initiatives" (75%)

**Pricing Sensitivity (from preliminary interviews):**
- Willing to pay $25-50/mo for 5+ hours saved per initiative: 75% of 20 interviewees
- Current dev tool spend: $50-150/mo average (GitHub Copilot, Cursor, hosting, etc.)
- Concern about variable credit costs: 40% ("prefer predictable pricing")
- **Validation needed:** Paid conversion rates will confirm willingness-to-pay

#### **Technical Feasibility Validation**

**Google ADK + Vertex AI (Preliminary Assessment):**
- **Prototype completed:** Week 0 (pre-project) validated basic agent orchestration
- **TypeScript SDK maturity:** Sufficient for MVP (tool use, structured outputs confirmed)
- **Model availability:** Gemini 2.0 Flash/Pro available, Claude 3.5 Sonnet via Model Garden (us-central1)
- **Concerns:** Limited community documentation, need to rely on official Google Cloud docs

**Vercel + Supabase Stack (Validation):**
- **Used successfully in:** 100+ production SaaS apps (proven stack)
- **Scaling validation:** Supabase handles 10,000+ concurrent connections, Vercel auto-scales
- **Integration maturity:** Clerk + Supabase well-documented, common pattern

**Credit-Based Pricing (Financial Modeling):**
- **Average initiative cost:** $0.05-0.15 (Gemini Flash operations)
- **Revenue per initiative:** $1.50-3.50 (15-35 credits at $0.10/credit)
- **Gross margin:** 90-95% (blended across all operations)
- **Validation needed:** Track actual costs in Month 1-3, adjust pricing if margins compress

---

### **B. Stakeholder Input**

**Design Partner Commitments (Target: 10):**

As of project kickoff, the following design partners have expressed interest (pending formal recruitment):

**Solo Developers/Indie Hackers (Target: 3):**
- [Placeholder: To be recruited Week 1-2]
- Criteria: Building SaaS projects, using AI coding assistants, willing to provide weekly feedback

**AI-Native Engineers (Target: 3):**
- [Placeholder: To be recruited Week 1-2]
- Criteria: Work on teams using Cursor/Windsurf/Claude Code, frustrated by context gaps

**Indie SaaS Builders (Target: 2):**
- [Placeholder: To be recruited Week 1-2]
- Criteria: 1-2 person teams, revenue-generating products, need planning acceleration

**Vibe Coders (Target: 2):**
- [Placeholder: To be recruited Week 1-2]
- Criteria: Heavy AI coding assistant users, prototype quickly but struggle to scale

**Recruitment Channels:**
- Twitter/X: Target indie hacker community, post about design partner opportunity
- Indie Hackers: Forum post seeking beta testers
- Reddit: r/SideProject, r/SaaS, r/EntrepreneurRideAlong
- Personal network: Reach out to developer connections
- BMAD community: If public resources available

**Incentive:** 50% discount for 1 year ($150 total vs. $300)

---

### **C. References**

**Industry Research:**
- Standish Group CHAOS Report: 70% of software projects fail due to poor requirements
- McKinsey Digital: Teams spend 8-12 hours/week searching for documentation
- GitHub Copilot Research (2024): 50% context-gathering overhead when tools lack planning context
- Gartner: AI coding assistant adoption projected to reach 75% of developers by 2026

**Competitive Products:**
- Linear: https://linear.app
- Jira: https://www.atlassian.com/software/jira
- Azure Boards: https://azure.microsoft.com/en-us/products/devops/boards
- Notion: https://www.notion.so
- Confluence: https://www.atlassian.com/software/confluence

**AI Tools:**
- Cursor: https://cursor.com
- Windsurf: https://codeium.com/windsurf
- Claude Code: https://docs.claude.com/en/docs/claude-code
- GitHub Copilot: https://github.com/features/copilot
- ChatGPT Apps SDK: https://openai.com/chatgpt/apps
- Claude MCP: https://modelcontextprotocol.io

**Technical Documentation:**
- Google Vertex AI: https://cloud.google.com/vertex-ai
- Google ADK: https://cloud.google.com/vertex-ai/generative-ai/docs/agent-builder
- Vercel: https://vercel.com/docs
- Supabase: https://supabase.com/docs
- Clerk: https://clerk.com/docs
- Stripe: https://stripe.com/docs

**Framework References:**
- BMAD Method: (Internal reference only, not customer-facing)
- BVSSH Principles: (Internal reference only, not customer-facing)
- INVEST Criteria: https://en.wikipedia.org/wiki/INVEST_(mnemonic)
- MoSCoW Prioritization: https://en.wikipedia.org/wiki/MoSCoW_method

---

## **Next Steps**

---

### **Next Steps**

#### **Immediate Actions (Week 1-2)**

**1. Design Partner Recruitment**
- **Goal:** Recruit 10 design partners (paid at 50% discount: $12.50/mo)
- **Target Mix:** 3 solo devs, 3 AI-native engineers, 2 indie SaaS builders, 2 vibe coders
- **Channels:** 
  - Twitter/X: Post seeking beta testers, target indie hacker community
  - Indie Hackers: Forum post with signup form
  - Reddit: r/SideProject, r/SaaS posts
  - Personal network: Direct outreach to developer connections
- **Incentive:** 50% discount for 1 year ($150 vs. $300)
- **Deliverable:** 10 confirmed design partners by end of Week 2
- **Owner:** Founder

---

**2. Competitive Deep-Dive**
- **Goal:** Understand user workflows in Cursor, Replit Agent, v0, Lovable; identify Linear/Jira planning gaps
- **Method:** 
  - User interviews: 10-15 target users (20-30 minute calls)
  - Screen recordings: Observe how users currently plan projects
  - Workflow analysis: Document pain points and gaps
- **Focus Areas:**
  - How do vibe coders currently create planning docs?
  - What context do AI coding assistants lack?
  - Why do teams abandon tools like Jira for planning?
- **Deliverable:** Competitive analysis document with 3-5 key differentiators
- **Timeline:** Week 1-2
- **Owner:** Founder

---

**3. Pricing Validation Interviews**
- **Goal:** Validate $25/mo + credit pricing, understand current dev tool spend
- **Method:** 20 interviews with target users (mix of solo devs, indie hackers, engineering leads)
- **Interview Script:**
  - "What dev tools do you currently pay for? How much total per month?"
  - "How much time do you spend on planning vs. coding each week?"
  - "If a tool could save you 5+ hours on planning per project, what would you pay?"
  - "How do you feel about $25/mo subscription + $10/100 credits usage-based pricing?"
  - "Would you prefer $49/mo all-inclusive or $25/mo + credits?"
- **Deliverable:** Pricing recommendation report (keep $25/mo, adjust to $19/mo or $29/mo, or all-inclusive model)
- **Timeline:** Week 1-2
- **Owner:** Founder

---

**4. Technical Stack Setup**
- **Goal:** Initialize development environment and deploy "Hello World" by end of Week 2
- **Tasks:**
  - Initialize Turborepo monorepo structure
  - Create Vercel project (connect to GitHub repo)
  - Set up Supabase (dev/staging/production environments)
  - Configure Clerk authentication (Google, GitHub OAuth)
  - Create base Next.js app with Tailwind + Untitled UI components
  - Design initial database schema (users, subscriptions, projects, initiatives, documents)
  - Set up Vertex AI project (enable APIs, configure service account)
  - Install development tools (Cursor Pro, Claude Code)
  - Configure CI/CD pipeline (GitHub Actions for linting, testing, deployment)
- **Deliverable:** "Hello World" app deployed to Vercel with Clerk authentication working
- **Timeline:** Week 1-2
- **Owner:** Founder

---

#### **Month 1-3: MVP Development (12-Week Timeline)**

**Week 1-2: Foundation**
- ✅ Turborepo monorepo setup (apps/web, apps/api, packages/ui, packages/db)
- ✅ Next.js 15 app with App Router, Tailwind, Untitled UI
- ✅ Supabase configuration (database schema, RLS policies, migrations)
- ✅ Clerk authentication (email/password, Google, GitHub OAuth)
- ✅ Basic three-panel layout (static, no real-time updates)
- ✅ Stripe integration (test mode, subscription setup)
- **Checkpoint:** Hello World deployed, auth working, database schema finalized

---

**Week 3-4: Agent Orchestration + Discovery Agent**
- Google Vertex AI project setup (enable APIs, service accounts)
- Integrate Google ADK (TypeScript SDK, agent orchestration)
- Build orchestrator agent (delegates to sub-agents, manages conversation state)
- Implement Discovery Agent:
  - Project Brief generation (executive summary, problem statement, solution, target users, goals)
  - Market Research generation (competitive landscape, user needs, trends)
  - Competitive Analysis generation (feature comparison, pricing analysis, differentiation)
- Create markdown storage system (documents table in Supabase)
- Build basic chat interface (user input → agent response → display)
- **Checkpoint:** Users can converse with Discovery Agent and generate Project Brief

---

**Week 5-6: Analysis Phase Completion**
- Enhance Discovery Agent prompts (iterate based on test outputs)
- Implement document approval workflow (Draft → Awaiting Review → Approved → Locked states)
- Build left panel Initiative Workflow navigator:
  - Collapsible phase sections (Discovery & Research, Product Definition, Design & Architecture, Validation & Handoff)
  - Progress indicators (✓ Complete, ⚡ In Progress, ○ Not Started, 🔒 Locked)
  - Document tree hierarchy
- Add document preview in right panel:
  - Markdown rendering (react-markdown or similar)
  - Section-level status indicators
  - Approval action buttons
- Implement phase gating (Analysis must complete before Planning unlocks)
- **Checkpoint:** Users can complete full Analysis phase (Brief, Research, Comp Analysis approved)

---

**Week 7-8: Planning Phase - Requirements & Architecture**
- Implement Requirements Agent:
  - PRD generation with Functional Requirements (FR1, FR2, FR3...)
  - Non-Functional Requirements (performance, security, accessibility)
  - Epic definitions (Epic 1.1, 1.2, etc.)
  - Feature breakdown (Feature 1.1A, 1.1B, etc.)
  - User story placeholders with titles
- Implement Architecture Agent:
  - Technical Architecture document (tech stack recommendations)
  - Data models (entity-relationship descriptions)
  - API endpoint specifications (REST/GraphQL)
  - Infrastructure requirements (hosting, database, CDN)
  - Architectural Decision Records (ADRs)
- Build Epic → Feature → Story hierarchy in left panel
- Add Validation Agent (cross-document alignment checks)
- **Checkpoint:** Users can generate PRD and Architecture documents

---

**Week 9-10: Planning Phase Completion**
- Implement Design Agent:
  - UX/UI specifications (user flows, wireframe descriptions)
  - Design tokens (color palettes, typography, spacing)
  - UI generation prompts (formatted for Lovable, v0, Bolt)
  - Accessibility guidelines (WCAG 2.1 AA checklist)
- Implement Quality Agent:
  - QA Strategy document (test pyramid, data management, environments)
  - Test planning (unit/integration/e2e/accessibility/performance/security)
  - Critical path identification
- Implement Planning Agent:
  - Convert story placeholders to fully-detailed stories
  - Add acceptance criteria (GIVEN/WHEN/THEN format)
  - Generate tasks (3-8 tasks per story with technical details)
  - Add story points estimates
- Add elicitation prompts with numbered choice options (1-7 choices for guided decision-making)
- Implement document export:
  - Markdown export (.md files)
  - PDF export (Puppeteer or similar for Project Brief and PRD)
  - ZIP archive export (full initiative bundle)
- **Checkpoint:** Users can complete full Planning phase (all 7 agent outputs, full backlog generated)

---

**Week 11-12: MVP Polish, Subscription Logic, Beta Launch**
- Integrate Stripe:
  - Checkout flow (Pro $25/mo, Business $50/mo tiers)
  - Customer Portal (subscription management, invoices)
  - Webhook handlers (subscription.created, payment_intent.succeeded, etc.)
  - Credit purchase flow (one-time payments for credit packs)
- Implement credit system:
  - Credit balance tracking (Supabase)
  - Credit consumption per operation (deduct from balance)
  - Low credit warnings (20 credits remaining, 10 credits, 0 credits)
  - Credit purchase modal (100, 200, 400, 800 credit packs)
- Build onboarding wizard:
  - Step 1: Welcome & value proposition
  - Step 2: First project creation
  - Step 3: Mode selection (Interactive vs. YOLO)
- Add status bar:
  - Active agent indicator
  - Progress tracking (§ 3/12 sections complete)
  - Time estimates (elapsed, remaining)
  - Mode indicator
- Performance optimization:
  - Lazy loading (load documents on-demand)
  - Response time <2 seconds for agent interactions
  - Page load time <1.5 seconds
- Bug fixing and edge case handling:
  - Error boundaries (graceful degradation)
  - Loading states (skeleton screens, spinners)
  - Empty states (no projects yet, no initiatives)
- Write Mintlify documentation:
  - Getting started guide
  - Agent workflow explanation
  - Credit system FAQ
  - Integration guides (placeholder for Phase 3)
- **Week 11: Private Beta Launch**
  - Deploy to production (Vercel)
  - Invite 10 design partners
  - Monitor usage (PostHog analytics)
  - Collect feedback (weekly check-ins)
  - Fix critical bugs
  - Iterate on agent prompts
- **Week 12: Validate MVP Success Criteria**
  - ✅ 80%+ agent output approval rate?
  - ✅ 10 design partners completed full workflow?
  - ✅ 70%+ report "saved 5+ hours"?
  - ✅ <5 critical bugs?
  - ✅ 99%+ uptime?
  - **If YES:** Proceed to public launch (Product Hunt)
  - **If NO:** Extend private beta 1-2 weeks, address gaps

---

#### **Month 4-7: Phase 2 - Distribution Channels**

**Week 13-14: ChatGPT Apps SDK Development**
- Implement ChatGPT App:
  - OAuth flow (link ChatGPT to RoadmapKO account)
  - Agent proxy endpoints (ChatGPT → RoadmapKO → Vertex AI)
  - Document sync (ChatGPT displays, RoadmapKO stores)
- Test with 10 beta users (validate UX, fix bugs)
- Submit to ChatGPT App Store for review
- **Deliverable:** ChatGPT App published

---

**Week 15-16: ChatGPT App Launch**
- Product Hunt launch (announce ChatGPT App integration)
- Twitter/X launch thread (demo video, benefits)
- Monitor installation rates (target: 500+ in first 30 days)
- Monitor conversion rates (target: 10% install → paid)
- **Success Metric:** 50 new paying customers via ChatGPT channel

---

**Week 17-18: Claude Desktop MCP Development**
- Implement MCP server:
  - Tools: create_initiative, generate_document, read_context, update_status
  - Resources: Full planning hierarchy (briefs, PRDs, architecture, stories)
- Test with Claude Desktop and Claude Code CLI (10 beta users)
- Publish MCP server (GitHub, MCP registry if available)
- **Deliverable:** MCP server published, integrated with Claude Desktop

---

**Week 19-20: Claude MCP Launch**
- Announce MCP integration (Twitter, blog post)
- Monitor installation rates (target: 200+ in first 30 days)
- Monitor conversion rates (target: 15% install → paid)
- **Success Metric:** 30 new paying customers via MCP channel

---

**Phase 2 Success Criteria:**
- 100 total new customers from distribution channels (ChatGPT + MCP)
- $8-10K MRR total (150-200 total customers)
- 40% of new signups originate from ChatGPT/MCP
- <8% monthly churn

---

#### **Month 8-10: Phase 3 - Integration Ecosystem**

**Week 21-24: Integration Development**
- Linear integration (OAuth, one-way sync RoadmapKO → Linear)
- Jira integration (OAuth, one-way sync)
- Notion integration (OAuth, export to Notion pages)
- Azure Boards integration (OAuth, one-way sync)
- Integration settings UI (connect accounts, configure sync preferences)
- **Deliverable:** All 4 integrations functional (Business tier feature)

---

**Week 25-28: Integration Beta Testing & Launch**
- Beta test with 20 Business tier customers
- Fix integration bugs
- Write integration documentation
- Launch integrations (announce on Twitter, blog, email to existing customers)
- Monitor activation rates (target: 30% of Business/Enterprise customers activate at least 1 integration)
- **Success Metric:** 50 total Business/Enterprise customers, 30% activate integrations

---

**Phase 3 Success Criteria:**
- 50 Business/Enterprise customers ($5K+ MRR from these tiers)
- $18-22K total MRR (250-300 total customers)
- Integration activation reduces churn by 15%

---

#### **Month 11-14: Phase 4 - Platform Intelligence & Polish**

**Week 29-32: Advanced Agent Capabilities & TipTap Editing**
- Intelligent backfilling (gap detection, dependency validation, cascading updates)
- Proactive planning intelligence (risk detection, dependency mapping, scope creep detection)
- TipTap rich text editing (inline document editing in right panel)
- Keyboard shortcuts (Cmd+K command palette, navigation shortcuts)
- Gamification features (streaks, achievements, confetti animations)
- **Deliverable:** Enhanced agent intelligence, improved UX

---

**Phase 4 Success Criteria:**
- 200-250 total customers
- $25-32K MRR (subscription + credits)
- <5% monthly churn
- 85%+ agent output approval rate
- 60%+ weekly active users

---

### **PM Handoff**

**To:** Requirements Agent (PM sub-agent)

**Context:** This Project Brief provides the complete strategic foundation for **RoadmapKO**—an AI-powered planning platform that helps developers and teams accelerate from business idea to execution-ready backlog while providing critical context to AI coding assistants.

**Next Phase:** Please review this brief thoroughly and prepare to create a comprehensive PRD that details:
- Feature specifications for MVP (three-panel workspace, 7-agent orchestration, document generation, credit system)
- User flows (signup → paid conversion → document generation → approval → export → integrations)
- Technical requirements (API endpoints, database schema, agent orchestration architecture, Vertex AI integration)
- Success metrics (approval rates, conversion rates, retention, credit consumption patterns)

**Request:** Start in 'PRD Generation Mode' and work with the user section-by-section, asking for clarification or suggesting improvements where needed. The PRD should be ready to hand off to the Architecture Agent for technical design.

---

**End of Project Brief**

*RoadmapKO - Transform ideas into execution-ready backlogs with AI agents*
