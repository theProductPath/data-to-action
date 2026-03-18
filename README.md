# Data to Action

Drop in your data files. Get back insights, reports, and deliverables — no coding, no data science background needed.

This repo shows what happens when you point [Claude](https://claude.ai) at unfamiliar data and ask it to figure out what's useful. It analyzes your files, finds the connections between them, and builds an interactive walkthrough that lets you pick exactly what you want produced — risk reports, dashboards, action lists, executive summaries, and more.

Everything you need to try it is included. No setup, no installs.

---

## Getting Started

### 1. Download this repo

Clone or download the ZIP and save it somewhere on your computer.

### 2. Open the folder in Claude

Open the Claude desktop app (with Cowork mode enabled) and select this folder as your workspace. Then type:

> *"What can you do with these files?"*

That's it. Claude will see the data files, read the README, and walk you through what's possible. You can also be more specific:

> *"Review the documents in Example-A-Indexed"*

### 3. Explore the app

Claude will analyze your files behind the scenes and generate an interactive HTML app. Open it in your browser and click through three phases:

- **Assess** — See what Claude found in each file: what it is, what it contains, what it's for
- **Connect** — Choose which connections between your data sources interest you
- **Act** — Pick the outputs you want: reports, dashboards, emails, action lists, and more

At the end, the app gives you a ready-to-paste prompt. Copy it back into the chat, and Claude builds everything you selected.

### 4. Bring your own data

Once you've seen how it works with the examples, drop your own files into the `Your-Data/` folder — Excel, CSV, PDF, Markdown, anything structured — and ask Claude to analyze them. It works the same way.

---

## Example Data Sets

### Example A: Clean Join (Indexed)
📁 `Example-A-Indexed/`

Two files that connect cleanly via a shared Customer ID:

- **crm_customers_250.xlsx** — A CRM customer master list with 250 active accounts across Enterprise, Mid-Market, and SMB segments. Annual revenue ranges from ~$25K (SMB) to ~$2M (Enterprise), spanning 30+ industries.
- **support_tickets_A_250.xlsx** — 250 support tickets with Customer IDs that match the CRM exactly. 229 are still open/in-progress, 51 flagged Critical. Tickets are weighted toward higher-revenue customers, which mirrors how real support demand typically works.

This is the easier of the two examples — great for a first run. The skill will identify renewal risks, support backlogs, and revenue-weighted priorities.

### Example B: Fuzzy Join (Messy Names)
📁 `Example-B-Fuzzy/`

Same data concept, but the company names in the ticket file are inconsistent:

- **crm_customers_250.xlsx** — Same clean CRM master list.
- **support_tickets_B_250.xlsx** — 250 tickets where company names have been entered inconsistently: some are truncated ("Phoenix" instead of "Phoenix Global"), some drop suffixes ("Inc.", "LLC"), some abbreviate ("Mfg.", "Tech", "Fin."), and some are just the first word of the name.

This is a harder test. There's no shared ID to link the files — the skill has to figure out the connection through fuzzy name matching. Good for seeing how the skill handles messy, real-world data.

---

## What It Can Build

Depending on your data, Claude can produce:

- **Risk reports** — Accounts at risk, renewal alerts, priority lists ranked by revenue impact
- **Dashboards** — Formatted Excel workbooks with breakdowns by segment, category, priority
- **Action lists** — Follow-up items organized by owner, with suggested next steps
- **Draft emails** — Personalized outreach for account managers or stakeholders, using real names from your data
- **Executive summaries** — Concise memos a leader can skim in two minutes
- **Merged datasets** — Clean, joined files ready for further analysis

---

## Requirements

- Claude desktop app with **Cowork mode** enabled
- Two or more structured data files (Excel, CSV, PDF, or Markdown) — or just use the included examples

---

## Tips

- **You don't need to know what's in your files.** The whole point is discovery. Drop in files you work with every day and let Claude tell you what's possible.
- **The interactive app is shareable.** The HTML file Claude generates is self-contained — you can send it to a colleague and they can click through the analysis in their browser.
- **You can skip the app.** If you already know what you want, just tell Claude directly: "Build me a dashboard comparing these two files by department."
- **Start with Example A.** It's the cleanest data and will give you the best sense of what's possible before you bring your own files.

---

## Found this useful? Install the skill.

If you liked what you saw, you can install the Data to Action skill so it's always available — even outside this folder. Just drag the `data-to-action.skill` file into any Claude chat and it installs automatically. From then on, you can point it at any folder with data files and get the same experience.
