Analyse this entire Discord bot repository and produce TWO Markdown files.

Do not modify any code.

Before producing either document, inspect the entire repository to determine exactly which privileged Gateway Intents are genuinely required.

Do not assume an intent is required simply because it is enabled in the Discord client. Trace the implementation and only include intents that are actually used by features within the bot.

Search the repository for:

- Discord client initialisation
- Enabled Gateway Intents
- Event handlers
- Slash commands
- Message handlers
- Scheduled/background tasks
- Database usage
- Logging
- Presence handling
- Member handling
- Message processing

Trace the code paths that depend on each privileged intent.

Do not expose secrets, tokens or configuration values.

---

# File 1

Create:

discord_intent_application.md

This document should contain ONLY the information required to complete Discord's Privileged Intent application form.

Follow the order of the Discord application.

## Application Details

Provide a concise description of:

- what the bot does
- who uses it
- major functionality
- why privileged intents are required overall

Target approximately 1,500–2,000 characters.

Do not include unnecessary implementation detail.

---

## Required Privileged Intents

Only include intents that are actually required.

For EACH required intent provide concise answers for every Discord form field.

### Why do you need this intent?

Explain:

- which feature requires it
- which Discord events/API are used
- why the intent is technically required
- what would stop working without it
- why a non-privileged alternative is insufficient

Target 800–2,000 characters.

---

### Screenshots

Provide only a short list of screenshots that should be linked from the supporting webpage.

For each screenshot include:

- title
- one sentence describing what it demonstrates

Do NOT describe testing procedures.

---

### Discord form questions

Where applicable, determine from the repository whether:

- API data is stored off-platform
- Member data is stored
- Presence data is stored
- Message content is stored
- Message content is used for AI or ML training
- Users can opt out

Only answer if it can be determined from the repository.

Otherwise write:

**Manual answer required**

---

Keep every answer concise and suitable for directly copying into the Discord Developer Portal text boxes.

---

# File 2

Create:

discord_intent_supporting.md

This document will become a GitHub Pages verification page for Discord reviewers.

Keep the entire document concise.

Assume the reviewer will spend less than two minutes reading it.

Avoid unnecessary implementation detail.

Use the following structure.

# Bot Overview

Briefly describe:

- what the bot does
- who uses it
- major features

Maximum 250 words.

---

# Required Privileged Intents

Only include intents confirmed as required.

For each intent include:

## Why this intent is required

One or two short paragraphs.

## Features using this intent

Short bullet list.

## Data accessed

Short bullet list.

## Data stored

Clearly state whether the data is:

- not stored
- temporarily processed
- stored

If stored, briefly explain what and why.

## Supporting screenshots

Provide a concise list of screenshots that should appear on the page.

For each screenshot include:

- title
- one sentence explaining what it demonstrates

Do not describe testing procedures.

---

# Privacy Summary

Summarise:

- what Discord data is processed
- what is retained
- what is not retained

Keep this brief.

---

# Reviewer Summary

Finish with a short paragraph explaining why the privileged intents are necessary, how they are used, and why they are the minimum required for the bot's functionality.

---

# Accuracy Requirements

- Inspect the full repository before producing either document.
- Confirm intent usage by tracing the implementation.
- Ignore intents that are enabled but unused.
- Do not invent features.
- Do not invent stored data.
- Clearly mark anything that cannot be confirmed from the repository.
- Do not expose secrets, credentials or private configuration.
- Write both documents specifically to maximise the likelihood of Discord privileged intent approval while remaining completely accurate to the implementation.