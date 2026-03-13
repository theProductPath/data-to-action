# Data to Action

Drop in your data files. Get back insights, reports, and deliverables — no coding, no data science background needed.

This project is a skill for [Claude](https://claude.ai) that turns unfamiliar data files into concrete, useful outputs. It works by analyzing your files, figuring out what they are and how they connect, and then building an interactive walkthrough that lets you choose exactly what you want produced.

---

## Getting Started

### 1. Install the Skill

Open Claude (desktop app with Cowork mode), then drag and drop the `data-to-action.skill` file into the chat. Claude will install it automatically.

### 2. Add Your Data

You have three options:

**Try the included examples** — Two pre-loaded example folders are ready to go. Just point Claude at one:

> *"Use the skill in this folder to review the documents in Example-A-Indexed"*

**Bring your own data** — Create a new folder, drop in two or more data files (Excel, CSV, PDF, Markdown — anything structured), and tell Claude to analyze them:

> *"Use the data-to-action skill to review the files in my-folder"*

**Start from scratch** — Just upload files directly into the chat and say something like:

> *"What can you do with these?"*

### 3. Explore the App

Claude will analyze your files behind the scenes and generate an interactive HTML app. Open it in your browser and click through three phases:

- **Assess** — See what Claude found in each file: what it is, what it contains, what it's for
- **Connect** — Choose which connections between your data sources interest you
- **Act** — Pick the outputs you want: reports, dashboards, emails, action lists, and more

At the end, the app gives you a ready-to-paste prompt. Copy it back into the chat, and Claude builds everything you selected.

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

## What the Skill Can Build

Depending on your data, the skill can produce:

- **Risk reports** — Accounts at risk, renewal alerts, priority lists ranked by revenue impact
- **Dashboards** — Formatted Excel workbooks with breakdowns by segment, category, priority
- **Action lists** — Follow-up items organized by owner, with suggested next steps
- **Draft emails** — Personalized outreach for account managers or stakeholders, using real names from your data
- **Executive summaries** — Concise memos a leader can skim in two minutes
- **Merged datasets** — Clean, joined files ready for further analysis

---

## Requirements

- Claude desktop app with **Cowork mode** enabled
- The `data-to-action.skill` file (included in this repo)
- Two or more structured data files (Excel, CSV, PDF, or Markdown)

---

## Tips

- **You don't need to know what's in your files.** The whole point of the skill is discovery. Drop in files you work with every day and let Claude tell you what's possible.
- **The interactive app is shareable.** The HTML file Claude generates is self-contained — you can send it to a colleague and they can click through the analysis in their browser.
- **You can skip the app.** If you already know what you want, just tell Claude directly: "Build me a dashboard comparing these two files by department." The skill is flexible.
- **Start with Example A.** It's the cleanest data and will give you the best sense of what the skill can do before you bring your own files.
