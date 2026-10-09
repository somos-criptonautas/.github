# Contributing to Criptonautas

Applies to every repo in [somos-criptonautas](https://github.com/somos-criptonautas)
that doesn't ship its own guide. The repo list lives on the
[org profile](https://github.com/somos-criptonautas).

## Before you open a PR

Several repos are forks. If your fix is not specific to our forum or site,
send it upstream instead — the parent repo is linked in the fork's README and
on the org profile. Upstream fixes reach everyone and keep our diff small enough
to rebase. A weekly job in [actions](https://github.com/somos-criptonautas/actions)
opens an issue when a fork falls behind its upstream.

Forks credit the original authors in `plugin.rb` / `about.json` as
"Original — Forked by Criptonautas", and their admin name ends in "Nautas".

## Working on one of ours

1. Fork the repo and branch off `main`.
2. Keep the diff minimal. On forks, do not reformat or reorganize upstream
   files — every unrelated line makes the next upstream merge harder.
3. Open the PR against `somos-criptonautas/<repo>:main`, and say what it changes
   and how you tested it.

## Discourse plugins and theme components

- **Theme components** — install the [theme CLI](https://github.com/discourse/discourse_theme)
  and run `discourse_theme watch .` against a test forum. Changes hot-reload.
- **Plugins** — clone into `plugins/` of a local Discourse dev install and run
  `bin/ember-cli -u`. On a production forum a plugin change needs a rebuild:
  `cd /var/discourse && ./launcher rebuild app`.
- Do not test on the live forum.

## Conventions

- **README** in English (`README.md`) and Spanish (`README.es.md`), each linking
  to the other on the first line, followed by "Maintained by Criptonautas. Not
  affiliated with or endorsed by Discourse (Civilized Discourse Construction Kit, Inc.)."
- **Screenshots** live in `docs/screenshots/`. Theme components regenerate them
  with the Screenshots workflow (Actions → Screenshots → Run workflow).
- **License.** Our own Discourse code is MIT. Forks keep the upstream license and
  copyright and add a line for our changes. README text is CC BY-NC-SA 4.0.
- **Comments** explain why, for the next person reading the code. No history,
  no tool tags.
- **AI agents.** Each repo keeps an `AGENTS.md` with how to run its checks and
  what a PR is reviewed against; `CLAUDE.md` only points to it. Personal notes,
  session logs and local paths stay out of the repo.

## Commits

Match what's already in these repos — Discourse's prefixes:

```
FEATURE: separate animated avatar for profile and user card
FIX: guard the route with requires_plugin
DEV: bump compatibility file
DOCS: trim the fork README to what the fork adds
```

Short subject, no body when the subject already says it.

## Questions

Open a [Discussion](https://github.com/orgs/somos-criptonautas/discussions).
