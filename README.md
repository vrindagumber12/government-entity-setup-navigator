# Government Entity Setup Navigator — MVP

A standalone front-end prototype for an AI-enabled government entity setup platform.

## What is included

- Project creation / project switching concept
- Evidence mode selector: selected documents, online research, or combined
- Local file upload metadata and evidence register
- 4-pillar / 12-component MECE institutional assessment
- Standard assessment logic for each component:
  - intended design
  - evidence
  - unresolved gap
  - risk/dependency
  - human action required
- “Ask why” explainability view
- “Challenge assessment” red-team interaction
- Human gate before Design Studio unlocks
- Institutional form option comparison and self-critique
- Setup roadmap with component ownership, evidence requirements and dependencies
- Launch readiness checks and critical-path logic
- Decision & Evidence Log / institutional memory
- JSON export of project state

## Important MVP limitation

This is a **front-end prototype**. It does not yet connect to:

- a real LLM or agent orchestration backend
- live web search
- document parsing / RAG
- authentication or secure storage
- multi-user approval workflows

Uploaded files remain in the browser session; the MVP uses file metadata only.

## Run locally

Open `index.html` directly in a modern browser.

For the most reliable local experience, run a small static web server in this folder, e.g.:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with Netlify

1. Unzip this folder.
2. Go to Netlify and create a new site with manual deployment.
3. Drag the whole folder into the deployment area.
4. Netlify will provide a public HTTPS URL.
5. Rename the Netlify subdomain under Domain Management if desired.

## Publish with Vercel

This is a static site. You can also place the folder in a GitHub repository and import the repo into Vercel.

## Suggested next production step

Add a secure backend with:

- project / source / assessment / issue / dependency / decision database tables
- encrypted document storage
- OCR / document parsing and chunking
- retrieval-augmented generation over approved sources
- official-source web search connector
- three agent workflows: Evidence & Institutional Intelligence; Organisation Design; Setup & Readiness Board
- server-side logs and approval gates
