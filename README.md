# ContextForge

ContextForge is a tiny offline-first developer utility for beginners who want clearer, more token-efficient prompts for coding-capable LLMs.

It does not call an LLM, GitHub, an API, or a backend. The application generates prompts entirely in your browser and stores optional state in `localStorage`.

## Workflow

1. Enter the coding task.
2. Answer a few plain-language project questions.
3. Optionally use the discovery workflow to have your external coding LLM inspect the project first.
4. ContextForge builds a structured implementation prompt locally.
5. Copy the prompt and paste it into your preferred coding assistant.

## Run offline

Open `index.html` in your browser.

No server, package manager, build step, CDN, external font, or network connection is required.

## Discovery workflow

Choose “Help me inspect the project” to generate a read-only discovery prompt. Copy it into your external coding LLM, ask it to inspect the project without making changes, then paste its analysis back into ContextForge. The pasted response is treated as plain project context; V1 does not attempt to parse it.

## Local storage

ContextForge saves current form state, workflow selections, recent tasks/settings, and recent generated prompts in your browser using `localStorage`. Stored data is never uploaded. Use **Clear saved data** to remove ContextForge's saved state and history.

## Privacy

Everything stays in your browser. ContextForge does not send your project information anywhere.

## Project structure

```text
contextforge/
├── index.html
├── style.css
├── app.js
└── README.md
```

## Customize the prompts

Prompt wording is intentionally local and readable. Edit the template strings in `app.js` to change discovery or implementation prompt sections.

## Product boundary

This MVP does not scan or clone repositories, contact GitHub, call an LLM, run agent integrations, use a backend, create accounts, or collect analytics. It is deliberately just:

`FORM → PROMPT GENERATOR → COPY → USER PASTES INTO LLM`
