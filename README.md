Clarity

> AI-powered productivity assistant for consultants and client-facing professionals

[![Status](https://img.shields.io/badge/status-complete-green)]()
[![AI](https://img.shields.io/badge/AI-ChatGPT%20API-orange)]()
[![Built with](https://img.shields.io/badge/Built%20with-Lovable.ai-blue)]()

---

## Problem

Client-facing professionals waste **5-10 hours weekly** on repetitive tasks:
- Drafting client emails
- Summarizing messy meeting notes
- Planning daily schedules

**Clarity solves this** by automating all three in one workflow.

---

## Solution

Three AI-powered features:

| Feature | What It Does |
| :--- | :--- |
| 📧 **Smart Email Generator** | Drafts professional emails with tone control (formal/informal/persuasive) for any audience (client/manager/team) |
| 📝 **Meeting Notes Summarizer** | Converts messy notes into structured summaries: decisions, action items (with owners), risks, deadlines |
| 📅 **AI Task Planner** | Prioritizes tasks using Eisenhower Matrix and creates time-blocked daily schedules |

---

## Productivity Impact

| Task | Without AI | With Clarity | Time Saved |
| :--- | :--- | :--- | :--- |
| Draft client email | 10 min | 2 min | **80%** |
| Summarize meeting notes | 20 min | 3 min | **85%** |
| Plan daily schedule | 15 min | 5 min | **67%** |
| **Total per workflow** | **45 min** | **10 min** | **78%** |

---

## Tools Used

| Tool | Purpose |
| :--- | :--- |
| Lovable.ai | Build frontend UI and logic |
| ChatGPT API (GPT-3.5-turbo) | AI text generation for all features |
| GitHub | Version control & documentation |

---

## Sample Prompts Used

### Meeting Summarizer Prompt
Extract from meeting notes: (1) Key decisions (2) Action items with person + deadline (3) Risks. 
Never invent names/dates. Use "Not specified" if missing. Output as bullet points.

### Email Generator Prompt
Write a {tone} email to a {recipientType}. Context: {context}. 
Rules: Under 200 words, include subject line, clear CTA, use [Name] as placeholder for unknown names.

### Task Planner Prompt
Prioritize these tasks using Eisenhower Matrix. Return JSON with sections: 
doToday, scheduleThisWeek, delegate, postpone. Max 6 hours of focused work per day.

## Sample Prompts Used (Final Version)
Keep the tabs but add a DASHBOARD HOME page as the default view.

Create a new "Dashboard" tab as the first tab showing:
- Welcome message with user's name (let them set it)
- 3 stat cards:
  • Meetings summarized: 0 (click to go to Summarizer)
  • Emails drafted: 0 (click to go to Email)
  • Tasks planned: 0 (click to go to Planner)
- Recent activity feed (mock: "No activity yet - generate something!")

COLORS:
- Buttons: #3B82F6 (blue)
- Cards: white with shadow, border-radius 16px
- Background: #F1F5F9
- Accent: #8B5CF6 (purple)

Keep all three features working. Add emojis to all buttons for friendlier feel.

*(Full prompt evolution from V1→V5 documented in `PROMPTS.md`)*

---

## Challenges & Solutions

| Challenge | Solution |
| :--- | :--- |
| AI hallucinated deadlines | Added "Never invent dates - use 'TBD'" to prompt |
| Email tone inconsistent | Created tone matrix (formal/informal/persuasive/urgent) with examples |
| Task planner overloaded schedule | Added capacity rule: max 6 focused hours per day |

---

## Responsible AI

**⚠️ Disclaimer:** AI-generated content may contain errors or hallucinations. Always verify:
- Names and deadlines in meeting summaries
- Facts and tone in draft emails
- Priority assignments in task plans

**Limitations:**
- May invent information not in source notes
- Bias possible from training data
- Not a replacement for professional judgment

---

## Setup & Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/Clarity.git

# Navigate to project
cd Clarity

# Add your OpenAI API key in Settings panel
# No other dependencies required

## Live Demo
[Clarity App][https://consultant-ai-buddy.lovable.app]

---

## Project Details
**Author:** Sibulele Ngwane | **Program:** CAPACITI AI Skill Accelerator
