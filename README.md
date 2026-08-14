# ContextOS

ContextOS is a small, offline-first web application that helps developers prepare an existing software project for an external AI coding workflow.

It is intentionally **not** a repository analyzer. It does not contact GitHub, call an LLM, upload files, require an account, or use a backend.

## What it does

### Prepare my project

Enter a GitHub repository URL and a little context about the project. ContextOS generates a bootstrap prompt that instructs ChatGPT to inspect the repository and create:

- `AGENTS.md`
- `SPEC.md`
- `PLAN.md`
- `PROGRESS.md`
- `DECISIONS.md`
- `LESSONS.md`

The prompt explicitly preserves the existing repository structure and asks the external AI not to modify application code while creating the project context layer.

### Prepare a coding task

Create a focused implementation prompt with:

- repository reference
- task
- project type
- known context or an offline-generated discovery prompt
- relevant files
- acceptance criteria
- additional instructions
- Fast, Careful, or Thorough workflow presets
- optional advanced controls

If the user does not understand the project yet, ContextOS generates a discovery prompt. The user can paste the external AI's analysis back into ContextOS before generating the final coding prompt.

## Offline and private

All functionality runs in the browser:

- no network requests
- no GitHub API
- no OpenAI or LLM API
- no telemetry or analytics
- no accounts or backend
- local persistence with `localStorage`

## Run

No installation or build process is required. Open `index.html` directly from disk.

## Files

```text
ContextOS/
├── index.html
├── style.css
├── app.js
└── README.md
```

## Manual checks

Open `index.html` directly and verify project preparation, coding-task generation, discovery analysis, prompt copying, Fast/Careful/Thorough presets, advanced options, persistence, clearing saved data, and mobile layout.
