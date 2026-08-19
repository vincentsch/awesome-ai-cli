# Criteria

This list is for CLIs that make agent-assisted development safer, clearer, or
faster. It is not a catalog of every tool developers run in a terminal.

The main question:

> Would this CLI give an agent a better path than clicking through the web app?

## What Makes A CLI Worth Listing

A candidate usually does several of these things:

- Replaces a dashboard, admin console, SaaS UI, or manual flow.
- Lets the caller choose the exact account, project, repo, dataset, queue,
  branch, region, namespace, or resource ID.
- Prints output a program can parse: JSON, YAML, SARIF, SPDX, CycloneDX, JUnit,
  NDJSON, HAR, VCR, or a stable text format.
- Runs unattended in CI or a non-TTY shell.
- Shows a plan, preview, diff, validation result, sandbox, emulator, fixture,
  dry-run, or generated artifact before risky changes.
- Works with scoped credentials such as profiles, service accounts, restricted
  tokens, or environment-specific API keys.
- Returns failures clearly enough to separate "not found" from "permission
  denied" from "validation failed."
- Has current docs and a practical install path.

A narrow CLI can belong when it covers a workflow that an agent should not
handle through a browser.

## What Usually Does Not Belong

- AI agent runtimes and chat tools.
- Package managers and language toolchains.
- Common Unix tools.
- Browser automation wrappers.
- Interactive-only TUIs.
- Abandoned unofficial wrappers around SaaS APIs.
- Marketing-only AI claims without a command surface worth reviewing.

## Caveats Matter

If a tool is good but dangerous, say why next to the tool. Examples:

- JSON is available only on some commands.
- A dry-run still reads live state.
- Sync can delete resources that are missing from a file.
- The tool needs broad credentials unless it is configured carefully.
- The command loads application code while running.
- Tests can call mutating API endpoints.

Short caveats make the list clearer and less like a vendor directory.

## Related Project

[rungrad](https://www.rungrad.com/) is Vincent Schmalbach's separate CLI
scoring project. This awesome list is not a rungrad leaderboard, and tools
listed here are not assumed to use rungrad.
