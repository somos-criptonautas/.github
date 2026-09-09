# Contributing to Criptonautas

Applies to every repo in [somos-criptonautas](https://github.com/somos-criptonautas)
that doesn't ship its own guide. The repo list lives on the
[org profile](https://github.com/somos-criptonautas).

## Before you open a PR

Most of our repos are forks. If your fix is not specific to our forum or site,
send it upstream instead — the parent repo is linked next to every fork on the
org profile. Upstream fixes reach everyone and keep our diff small enough to
rebase.

Naming convention: a `-nautas` suffix means a fork we carry patches on;
no suffix means the code is ours, or the upstream name was kept as is.

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
