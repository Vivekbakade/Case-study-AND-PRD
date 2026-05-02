#  Case Study 3: SolvAI — AI Study Assistant for Indian Engineering Students
### AI Product Management Case Study | EdTech | New Product Design from Scratch

> **Domain:** EdTech | Generative AI | India Bharat Market
> **Role Simulated:** AI Product Manager
> **Type:** 0→1 New Product Build



##  STAR Summary *(Resume-Ready — copy this directly)*

| **S — Situation** | 8M+ engineering students in India lack access to personalized academic support. Existing tools (ChatGPT, Google) give generic answers — not aligned to university syllabus, local language, or exam pattern. 68% of engineering students fail at least one subject in 4 years. |
| **T — Task** | Design SolvAI — a syllabus-aware AI study assistant for Indian engineering students, from problem discovery to GTM strategy. |
| **A — Action** | Defined 3 user personas, built full PRD with AI architecture decisions, designed freemium business model, ran competitive analysis against existing players (Unacademy, Chegg, ChatGPT), and created 4-phase roadmap. |
| **R — Result** | Product concept targets ₹4,200 Cr addressable EdTech market. Projected 40% doubt resolution rate improvement over generic AI tools. GTM via college partnerships with <₹50 CAC. |



##  Problem Statement

India produces **1.5 million engineering graduates every year.** Yet:

- **68% fail at least one subject** in their 4-year degree
- Students spend **₹15,000–50,000/year** on coaching and tutors
- Available AI tools (ChatGPT) are **not syllabus-aligned** — give wrong formulas, wrong exam patterns
- **Regional language barrier:** 60% of students are more comfortable in Hindi/Marathi/Telugu than English
- **Doubt resolution time:** Average student waits 24–48 hours for a teacher to respond on WhatsApp groups

**Student Pain (direct quote from simulated user interview):**
> *"I ask ChatGPT a question from my exam paper and it gives an answer using a method we haven't studied. I don't know if it's right or wrong. Then I'm more confused than before."*

**The Gap:** Generic AI tools are not designed for curriculum-specific, exam-pattern-aware, regionally relevant education.



##  User Personas

| Persona | Profile | Academic Goal | Key Pain |
|---|---|---|---|
| **Arjun, 20 — 2nd Year ECE, Nagpur** | Hardworking, average grades, Hindi-medium background | Pass all subjects, get a decent placement | Can't afford tutors; ChatGPT gives confusing answers |
| **Sneha, 21 — 3rd Year CS, Pune** | High achiever, targets 8+ CGPA for MBA | Conceptual clarity, not just exam tricks | Existing apps are too shallow; wants to truly understand, not mug up |
| **Rohan, 22 — Final Year Mech, Nagpur** | Backlog in 2 subjects, panicking before exams | Clear backlogs, get degree | No targeted backlog-clearing support; previous year questions not organized |
| **Professor Desai, 54 — HOD, Government Engineering College** | Wants students to perform better | Reduce failure rates | No visibility into where students struggle most; can't give individual attention |



## Solution: "SolvAI" — The Syllabus-Smart AI Study Assistant

### Product Vision
> *"Every Indian engineering student deserves a personal AI tutor that knows their syllabus, speaks their language, and helps them actually understand — not just pass."*

### What Makes SolvAI Different from ChatGPT

| Feature | ChatGPT | SolvAI |
|---|---|---|
| Syllabus awareness |  Generic |  RTMNU, VTU, GTU, JNTU syllabi loaded |
| Previous year questions |  No |  10-year PYQ bank, pattern-analyzed |
| Regional language |  English-heavy |  Hindi, Marathi, Telugu, Tamil |
| Step-by-step exam method |  Gives shortcuts |  Follows university mark scheme |
| Backlog mode |  No |  Targeted revision plan for backlogs |
| Professor dashboard |  No |  Class-level weak topic analytics |

---

##  PRD — Product Requirements Document

**Product Name:** SolvAI
**Version:** 1.0 MVP
**PM:** Vivek [Your Last Name]
**Target Launch:** Q2 2025 (Pilot — 3 colleges, Nagpur/Pune)

### Core Features — V1

**1. Syllabus-Aware Q&A (RAG-Based)**
- Engineering syllabus PDFs indexed in vector database
- Student asks question → AI retrieves relevant syllabus section → generates answer using correct method
- AI explicitly states which unit/chapter it's referencing
- Technology: RAG pipeline (LangChain + university syllabus PDFs + GPT-4/Claude API)

**2. Previous Year Question (PYQ) Analyzer**
- 10-year PYQ bank for top 20 Indian universities
- Shows which topics appear most frequently
- Generates likely questions for upcoming exam based on pattern analysis
- "High probability topics" highlighted for each exam

**3. Multilingual Doubt Solving**
- Student can ask in Hindi/Marathi/English (mixed also supported — "Hinglish")
- AI responds in same language
- Technical terms kept in English; explanations in regional language

**4. Step-by-Step Solution Mode**
- Every solution shows full working — not just the answer
- Each step labeled (Step 1: Apply KVL formula; Step 2: Substitute values...)
- Marks allocated to each step shown (exam strategy)

**5. Backlog Rescue Mode**
- Student inputs their backlog subjects
- AI generates 7-day/15-day revision plan
- Daily practice questions with difficulty ramp-up
- Progress tracker

### User Stories

As a student, I want to type a question from my textbook in Hindi
so that I get an answer in a language I understand better.

As a student preparing for exams, I want to see which topics appear
most in previous year papers so that I can prioritize my revision.

As a student with a backlog, I want a structured 15-day plan
so that I know exactly what to study each day.

As a professor, I want to see which topics my class struggles with most
so that I can dedicate extra time in lectures to those areas.


### Technical Architecture Decision


Architecture: RAG (Retrieval-Augmented Generation)

Why RAG over fine-tuning?
- Fine-tuning: Expensive, slow to update when syllabus changes
- RAG: Cheap to update (just re-index new PDFs), more accurate citations

Stack:
├── Frontend: React Native (iOS + Android)
├── Backend: FastAPI (Python)
├── Vector DB: Pinecone / ChromaDB (syllabus + PYQ embeddings)
├── LLM: GPT-4o or Claude Sonnet (API)
├── Language Detection: IndicNLP / Bhashini API
├── Database: PostgreSQL (user data, progress)
└── Hosting: AWS / Google Cloud


### AI Limitations Acknowledged (PM Responsibility)
- **Hallucination risk:** AI may generate confident but wrong answers → Mitigation: Always cite syllabus source; add "verify with textbook" disclaimer
- **Outdated syllabus:** Universities update syllabi → Mitigation: Quarterly syllabus refresh process
- **Exam pattern changes:** New paper setters change patterns → Mitigation: Clear disclaimer that PYQ patterns are probabilistic, not guaranteed



##  Success Metrics & KPIs

| Metric | Target (3-month pilot) | Measurement |
|---|---|---|
| **Doubt Resolution Rate** | >75% (user marks as "helpful") | In-app thumbs up/down |
| **DAU/MAU Ratio** | >40% (sticky product) | Analytics |
| **Time-to-Answer** | <5 seconds | Backend monitoring |
| **Multilingual Usage** | >30% queries in non-English | Language detection log |
| **Backlog Completion Rate** | >50% complete 7-day plan | Progress tracker |
| **Exam Score Improvement** | 15%+ for active users vs control | Post-exam survey |
| **Professor Dashboard WAU** | >60% of pilot professors weekly active | Dashboard analytics |

**North Star Metric:** *Weekly active students who resolve at least 5 doubts per week*

---

##  Product Roadmap

```
Q1 2025 — MVP Build
├── Syllabus RAG for 5 universities (RTMNU, VTU, JNTU, GTU, Mumbai Univ)
├── English + Hindi support
├── PYQ analyzer (last 5 years)
├── Basic step-by-step solver
└── Web app (mobile-responsive)

Q2 2025 — Pilot Launch
├── Android app (PWA → Native)
├── Marathi + Telugu language support
├── Backlog Rescue Mode
├── 3-college Nagpur/Pune pilot (free)
└── Measure: Doubt resolution rate, DAU/MAU

Q3 2025 — Monetization
├── Freemium model launch (50 doubts/month free)
├── Professor dashboard (college B2B)
├── 5 more universities added
├── PYQ bank expanded to 10 years
└── First 500 paying students target

Q4 2025 — Scale
├── Tamil + Bengali support
├── Voice input (speak your doubt)
├── AI-generated mock tests with auto-evaluation
├── 50 college partnerships
└── Series A fundraise pitch ready


##  Business Model

### Freemium SaaS (B2C + B2B2C)

**Free Tier:**
- 50 doubt solutions per month
- Basic PYQ access
- Hindi/English only

**Pro Tier — ₹299/month:**
- Unlimited doubts
- All regional languages
- Backlog rescue mode
- Mock test generator
- Exam countdown planner

**College Tier — ₹50,000/college/year (B2B):**
- All students get Pro access
- Professor analytics dashboard
- Branded as "[College Name] AI Study Companion"
- Placement cell integration

### Market Sizing

TAM: India EdTech market — ₹60,000 Crore (2025)
SAM: Engineering student digital learning tools — ₹4,200 Crore
SOM: Year 1-2 target (tech + semi-urban students) — ₹85 Crore

Unit Economics:
CAC via college partnership: ₹40-50 per student
LTV (2-year average subscription): ₹600-900
LTV:CAC ratio: ~15:1 (excellent)


### GTM Strategy
1. **Month 1-2:** Free pilot at 3 Nagpur engineering colleges → word of mouth
2. **Month 3-4:** LinkedIn/Instagram content showing "SolvAI vs ChatGPT for engineering" → organic growth
3. **Month 5-6:** College ambassador program (1 student per college, free Pro account)
4. **Month 7+:** Direct college admin pitch → institutional license

## Risks & Mitigation

| Risk | Severity | Mitigation |
|---|---|---|
| AI gives wrong answer → student fails exam |  Critical | Cite syllabus source always; disclaimer on every answer; thumbs-down feedback loop |
| University sends copyright notice for syllabus |  High | Legal review; use only officially public syllabi; transform into embeddings (not reproduce) |
| ChatGPT becomes syllabus-aware (competition) |  High | Build moat in regional language depth + PYQ bank + professor dashboard |
| Students share Pro accounts |  Medium | Device-binding; 3-device limit |
| Low retention after exam season |  High | Year-round product: placement prep, internship skill building in off-season |


##  Competitive Analysis

| Player | Strength | Weakness | SolvAI Advantage |

| **ChatGPT** | General intelligence | Not syllabus-aware, no regional language depth | Syllabus RAG + PYQ + regional lang |
| **Unacademy** | Live classes, brand | Expensive (₹5,000-15,000/yr), not doubt-specific | 10x cheaper, on-demand, instant |
| **Chegg** | PYQ solutions | Mostly English, US-focused, expensive | India-first, regional language, affordable |
| **Google Search** | Free, familiar | Not conversational, requires sifting | Instant answer, step-by-step, contextual |
| **WhatsApp tutor groups** | Free, known interface | 24-48hr wait, inconsistent quality | Instant, 24/7, consistent quality |


##  Key PM Learnings

1. **"Generic AI" is not a product** — the value is in the vertical depth (syllabus, language, exam pattern)
2. **RAG over fine-tuning for fast-moving domains** — syllabi change yearly; RAG is cheaper and more accurate for this use case
3. **B2B2C GTM is faster than pure B2C** — one college deal = 1,000 users; direct acquisition = 1,000 individual conversions
4. **Acknowledge AI limitations in the PRD** — hallucination risk in education is a safety issue, not just a product bug
5. **North Star Metric aligns the team** — "weekly doubts resolved" focuses everyone on usage depth, not just sign-ups



*© Vivek 
*This is an independent product concept created for portfolio purposes. Not affiliated with any company.*
