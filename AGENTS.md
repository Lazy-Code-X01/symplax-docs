# Symplax docs: how to write them

These are the public docs for [Symplax](https://symplax.com), built on Mintlify. Pages are MDX
with YAML frontmatter; `docs.json` holds the theme and navigation.

## The one rule

Document only what Symplax actually does today, checked against the product's code, not
against old docs or what sounds plausible. If you are unsure whether something works, leave it
out. A missing sentence costs nothing; a wrong one sends a customer down a path that fails.

## Who reads these

Developers deploying their own apps, often moving off Vercel, Railway or DigitalOcean. Many
are in Nigeria and across Africa. They are smart and busy: get to the point.

## Style

- Second person, active voice: "Click **Deploy**", "You can roll back".
- Short sentences, one idea each. Sentence case for headings.
- Never use em dashes. Use a comma, a colon or a full stop instead.
- Bold for UI labels exactly as they appear: **Settings**, **Environment**.
- `Code formatting` for commands, file names, paths, env var names and values.
- Name things as the dashboard does: apps, servers, databases, teams.
- Lead with the task, then the details. Put limits and caveats in a `<Note>` or `<Warning>`,
  never buried in a paragraph.
- No marketing filler ("seamless", "powerful", "effortless", "blazing").

## Components

Use Mintlify's built-ins where they help the reader: `<Steps>`, `<Card>`/`<CardGroup>`,
`<Tabs>`, `<CodeGroup>`, `<Accordion>`, `<Tip>`, `<Note>`, `<Warning>`, `<Info>`. Images live in
`/images`; the Buddy mascot poses there are the house illustrations.

## Frontmatter

Every page has `title` and `description` (one sentence, used for search and SEO). Add `icon`
(a Font Awesome name) on section entry pages.

## Product facts worth knowing

- One app runs as one container on one server. A Docker Compose file is accepted only with exactly one app service plus up to 4 databases, which become managed databases.
- Apps deploy from GitHub (no GitLab or Bitbucket) or from a Docker image.
- Every app gets a free `*.symplax.app` subdomain with HTTPS; custom domains get Let's Encrypt.
- Plans: Free, Pro, Team for management; servers can also be bought pay-as-you-go from a wallet.
- Team roles: Owner, Admin, Developer, Viewer.
- The CLI is `symplax` on npm; API keys start with `sk_live_`.
