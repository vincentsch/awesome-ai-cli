# Contributing

This repo lists CLIs that are worth giving to AI coding agents. A tool needs
more than a terminal command to belong here.

Read [criteria.md](criteria.md) before proposing a tool.

## Pull Requests

- Add one tool per pull request.
- Link to the official project page or repository.
- Put the tool where a reader would look for it.
- Describe the workflow the CLI makes better.
- Mention the sharp caveat if the CLI has one.
- Leave out star counts, popularity claims, and vendor taglines.

## What Fits

A good candidate usually has several of these traits:

- It replaces a browser dashboard, admin console, or fragile manual flow.
- It can run without waiting for a prompt.
- It can print JSON, YAML, SARIF, SPDX, CycloneDX, JUnit, NDJSON, HAR, VCR, or
  another format a script can parse.
- It targets resources by IDs, paths, projects, namespaces, branches, profiles,
  regions, accounts, or environments.
- It offers a plan, preview, diff, validation, sandbox, emulator, fixture, or
  dry-run before risky changes.
- It works with scoped credentials that can be revoked.
- Its failures are clear enough for automation to branch on.
- It has current docs and an install path a maintainer can check.

Unofficial CLIs can fit. The repo should be active, the maintainer should not
hide that it is unofficial, and auth should be documented enough for scripts
and CI.

## What Does Not Fit

- AI agent runtimes
- interactive-only TUIs
- package managers
- common shell tools
- browser automation wrappers
- thin unofficial wrappers with unclear maintenance or auth behavior
- tools whose agent story is only marketing copy

## Style

Use a colon after the link:

```markdown
- [Tool Name](https://example.com/): What the CLI lets an agent inspect, test,
  deploy, export, replay, or change. Mention one caveat if it matters.
```

Keep descriptions about behavior. Do not copy vendor taglines.

## Evidence

For a new tool, include links that show the relevant parts:

- output mode
- non-interactive mode or non-TTY behavior
- auth method
- plan, preview, dry-run, diff, validation, or sandbox behavior
- error or exit-code behavior, when claimed

If the evidence is weak, leave the tool out for now or add it to the README's
`Still Looking For` section in plain English.
