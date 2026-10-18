# n8n Automations

A collection of automation workflows I've built in **n8n** — exported as importable JSON with
write-ups. All company-specific data, emails, sheet IDs, and credentials have been removed; import a
workflow, connect your own accounts, and run it.

## Workflows

### 🔎 [AI Competitive Intelligence Research](competitive-intelligence/)
A weekly, two-agent AI pipeline: one agent **discovers** new competitors on the web, a second
**researches** each for reviews, pricing, address, and search-ranking visibility, then writes
structured results to Google Sheets and emails a summary. Runs on free-tier **Groq** (LLM) +
**Tavily** (web search), with anti-hallucination prompting and free-tier rate-limit handling.

### 🧑‍💼 [AI Résumé Intake & Scoring](ai-resume-scoring/)
A recruiting automation that watches an inbox for inbound applications, retrieves each résumé through
a primary path with two fallbacks, archives the PDF, and scores the candidate against role criteria
with an AI agent returning structured JSON — with an idempotent guard against reprocessing the same
application. 67 nodes.

### 📊 [Order Reporting Pipeline](order-reporting/)
A data-processing workflow that fetches orders and customers from an API, merges and enriches them,
calculates totals, summarizes by region, filters a segment, converts to CSV, posts a summary to
Discord, and uploads the report. A clean demonstration of n8n fundamentals — HTTP, Merge, transform,
branch, and multi-destination delivery.

## Importing a workflow

In n8n: **⋮ (top-right) → Import from File** → select the `workflow.json`. Then connect your own
credentials on the nodes that need them and replace any placeholder IDs. Each folder's README has
the specifics.

## License

MIT — see [LICENSE](LICENSE).
