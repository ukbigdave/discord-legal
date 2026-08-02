Analyse this Discord bot repository and create a concise verification evidence document that I can use to build a Discord privileged-intent review webpage.

Do not modify the bot code.

Create a Markdown file named:

DISCORD_VERIFICATION_EVIDENCE.md

Required output

1. Bot summary

Provide:

* Bot name
* High-level description of what the bot does
* Main user groups or servers it supports
* Whether it uses slash commands, message commands, events, scheduled tasks or background processing

Do not invent information that is not present in the repository.

2. Privileged intents

Identify whether the bot requires any of:

* GUILD_MEMBERS
* MESSAGE_CONTENT
* GUILD_PRESENCES

For each required intent, provide:

* Why the intent is technically required
* The exact features that depend on it
* Relevant Discord events, client methods or code paths
* What would stop working without the intent
* Why a non-privileged alternative is insufficient

Include relevant source file names and function names.

Do not claim an intent is required merely because it is enabled in the client configuration. Confirm that repository features actually use it.

3. Suggested screenshots

For each intent, propose 2–5 screenshots that would clearly prove the feature to a Discord reviewer.

For each screenshot, specify:

* What action should be performed
* What should be visible before the action
* What result should be visible afterwards
* Which Discord channel, role, command, log or audit entry should be shown
* A suggested file name

Use names such as:

01-member-joins.png
02-role-granted.png
03-sync-log.png

4. Suggested evidence flow

Describe the simplest test sequence I can perform to capture the screenshots.

Example:

1. Give a test user the source role.
2. Join or update the linked server member.
3. Show the resulting role in the destination server.
4. Show the bot log confirming the synchronisation.

5. Data handling

Based only on the repository, identify:

* Discord data read
* Data stored
* Database tables or files used
* Whether message content is stored or only processed temporarily
* Logging performed
* Any visible retention or deletion logic

Clearly mark anything that cannot be confirmed.

6. Reviewer-ready copy

Finish with concise website-ready wording containing:

* A short bot summary
* One section per required privileged intent
* Why each intent is required
* Features using it
* Data accessed
* Whether the data is stored
* A short reviewer summary

Keep this section concise enough to fit comfortably on one webpage.

7. Missing information

List anything that must be supplied manually, such as:

* Discord application ID
* Contact email
* Privacy policy URL
* Terms URL
* Data-retention period
* External services not visible in the repository
* Screenshots or video links

Accuracy requirements

* Inspect the full repository before producing the document.
* Search for Discord client intent configuration and all related event handlers.
* Trace feature usage rather than relying only on filenames.
* Distinguish required intents from intents that are enabled but apparently unused.
* Do not expose secrets, tokens, credentials or private configuration values.
* Do not include real Discord user IDs, server IDs or channel IDs unless essential; describe them generically instead.
