# Awesome AI CLI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

CLIs that play nicely with AI coding agents.

This list is for command-line tools that let an agent inspect or change a repo,
service, dataset, product account, or infrastructure account without driving a
browser. Tools should expose names, IDs, files, logs, diffs, plans, previews,
or JSON.

Good candidates target a project or resource explicitly, run in CI or a non-TTY
shell, and show a dry-run, diff, validation result, sandbox, or local artifact
before a command changes state.

This list leaves out AI agent apps, package managers, interactive-only TUIs,
common shell tools, and browser automation.

Unofficial CLIs are fine when the repo is maintained, the credential flow is
documented, and scripts can read the output without scraping a screen.

## Contents

- [Source Control, Reviews, And CI](#source-control-reviews-and-ci)
- [Infrastructure And Cloud](#infrastructure-and-cloud)
- [Containers, Kubernetes, And Gateways](#containers-kubernetes-and-gateways)
- [Databases, Data, And Storage](#databases-data-and-storage)
- [Queues, Streams, And Realtime](#queues-streams-and-realtime)
- [Observability And Incidents](#observability-and-incidents)
- [Security, Secrets, And Supply Chain](#security-secrets-and-supply-chain)
- [API Contracts, Testing, And Replay](#api-contracts-testing-and-replay)
- [Content, CMS, And Media](#content-cms-and-media)
- [Workspace, CRM, Email, And Messaging](#workspace-crm-email-and-messaging)
- [Payments, Commerce, And Finance](#payments-commerce-and-finance)
- [Still Looking For](#still-looking-for)

## Source Control, Reviews, And CI

- [GitHub CLI (`gh`)](https://cli.github.com/): Issues, pull requests,
  releases, Actions runs, repo settings, and GraphQL or REST calls. Many
  commands support `--json` and `--jq`.
- [GitLab CLI (`glab`)](https://docs.gitlab.com/cli/): GitLab issues, merge
  requests, pipelines, releases, and API calls. `glab api` covers gaps in the
  higher-level commands and returns JSON.
- [Atlassian CLI (`acli`)](https://developer.atlassian.com/cloud/acli/reference/commands/):
  Jira work items, boards, projects, sprints, and JQL queries from the
  terminal.
- [CircleCI CLI](https://circleci.com/docs/local-cli/): Config validation,
  reusable config packing, local job execution where supported, and CI setup
  checks before a YAML change is pushed.
- [Buildkite CLI (`bk`)](https://buildkite.com/docs/platform/cli): Builds,
  jobs, pipelines, annotations, artifacts, clusters, agents, and JSON output
  for list or view commands.
- [TeamCity CLI (`teamcity`)](https://www.jetbrains.com/help/teamcity/teamcity-cli.html):
  Builds, queues, agents, logs, artifacts, remote agent terminals, and direct
  TeamCity REST calls.
- [GitHub Actions `act`](https://github.com/nektos/act): Local runs for many
  GitHub Actions jobs. It does not match GitHub-hosted runners exactly, but it
  catches a lot before hosted CI starts.
- [Sentry CLI](https://docs.sentry.io/cli/): Releases, commits, deploys,
  source maps, debug files, and event lookup from scripts.

## Infrastructure And Cloud

- [Terraform](https://developer.hashicorp.com/terraform/cli): The familiar
  plan and apply loop, with change review before infrastructure is touched.
- [OpenTofu](https://opentofu.org/docs/cli/): Terraform-compatible
  infrastructure commands with the same plan-first shape.
- [Pulumi CLI](https://www.pulumi.com/docs/iac/cli/): Infrastructure previews,
  diffs, stack outputs, and updates from programs written in normal languages.
- [AWS CLI](https://aws.amazon.com/cli/): AWS resources with JSON output,
  profiles, regions, JMESPath queries, and IAM-based credential scoping.
- [Azure CLI (`az`)](https://learn.microsoft.com/en-us/cli/azure/): Azure
  resources with JSON output, JMESPath queries, and service-principal auth.
- [Google Cloud CLI (`gcloud`)](https://cloud.google.com/sdk/gcloud): Google
  Cloud projects, accounts, IAM, deploys, logs, and service-account flows. Pin
  the project and account on every run.
- [DigitalOcean CLI (`doctl`)](https://docs.digitalocean.com/reference/doctl/):
  Droplets, databases, Kubernetes, domains, firewalls, registries, and account
  resources with JSON output.
- [Hetzner Cloud CLI (`hcloud`)](https://github.com/hetznercloud/cli):
  Hetzner Cloud servers, networks, firewalls, volumes, load balancers, SSH
  keys, primary IPs, DNS zones, and project contexts.
- [Linode CLI](https://techdocs.akamai.com/cloud-computing/docs/getting-started-with-the-linode-cli):
  Linode instances, Kubernetes, volumes, firewalls, images, domains, object
  storage, and JSON output.
- [Vultr CLI (`vultr-cli`)](https://github.com/vultr/vultr-cli): Instances,
  Kubernetes, load balancers, DNS, firewalls, object storage, and text, JSON,
  or YAML output.
- [Render CLI](https://render.com/docs/cli): Services, deploys, logs, Postgres
  queries, Blueprint validation, non-interactive mode, and JSON or YAML output.
- [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli): Apps,
  releases, config vars, add-ons, logs, Postgres, pipelines, and JSON output
  on many management commands.
- [Railway CLI](https://docs.railway.com/cli): Projects, services, deploys,
  logs, variables, shell sessions with service env, and CI tokens.
- [Fly.io `flyctl`](https://fly.io/docs/flyctl/): App deploys, machines,
  volumes, secrets, releases, logs, and WireGuard.
- [Fly.io Sprites CLI (`sprite`)](https://docs.sprites.dev/cli/commands/):
  Persistent Linux environments for agents, with command execution, console
  access, URL management, checkpoints, restore, and token setup for CI.
- [Fastly CLI](https://www.fastly.com/documentation/reference/cli/): Fastly
  Compute, VCL services, domains, backends, dictionaries, ACLs, packaging, and
  deploys.
- [Vercel CLI](https://vercel.com/docs/cli): Deployments, env vars, project
  linking, logs, aliases, and preview deployments.
- [Netlify CLI](https://docs.netlify.com/cli/get-started/): Local dev, deploy
  previews, env vars, functions, forms, and site management from the terminal.
- [Cloudflare Wrangler (`wrangler`)](https://developers.cloudflare.com/workers/wrangler/):
  Workers, Pages, D1, KV, R2, Queues, deploys, local dev, and dry-run
  compilation.
- [Firebase CLI](https://firebase.google.com/docs/cli): Firebase deploys,
  emulators, project config, functions, Firestore indexes, and CI auth.
- [Laravel Forge CLI (`forge`)](https://laravel.com/forge/docs/cli): Forge
  servers, sites, deployments, environment variables, deployment logs, resource
  logs, resource status, restarts, SSH checks, and remote command execution.
- [Coolify CLI (`coolify`)](https://github.com/coollabsio/coolify-cli):
  Coolify cloud and self-hosted servers, projects, apps, databases, services,
  contexts, JSON output, and token overrides.
- [SST CLI (`sst`)](https://sst.dev/docs/reference/cli/): App deploys, stages,
  secrets, logs, stage removal, and deployment diffs before a stage changes.
- [Tailscale CLI](https://tailscale.com/docs/reference/tailscale-cli): Tailnet
  status, peers, SSH, serve, funnel, file transfer, and JSON status for
  automation. Funnel can expose a local service to the public internet.
- [Nomad CLI](https://developer.hashicorp.com/nomad/commands/job/plan): Job
  planning, allocation diffs, and a plan index that protects an apply from
  racing cluster state.

## Containers, Kubernetes, And Gateways

- [Docker CLI and Compose](https://docs.docker.com/reference/cli/docker/):
  Container inspection, image builds, Compose config rendering, and Compose
  dry-runs.
- [`kubectl`](https://kubernetes.io/docs/reference/kubectl/): Kubernetes
  objects, namespaces, diffs, dry-runs, logs, events, and JSON or YAML output,
  with context and namespace set explicitly.
- [Helm](https://helm.sh/): Chart rendering, generated Kubernetes manifests,
  and release diff review before cluster changes.
- [Argo CD CLI](https://argo-cd.readthedocs.io/en/stable/user-guide/commands/argocd/):
  GitOps app inspection, diffs, syncs, rollbacks, and app state.
- [Kong decK](https://developer.konghq.com/deck/): Kong Gateway export,
  validation, diff, and sync through declarative files.
- [Cilium CLI](https://docs.cilium.io/en/stable/gettingstarted/k8s-install-default/):
  Cilium install checks, connectivity tests, and network troubleshooting for
  Kubernetes clusters.

## Databases, Data, And Storage

- [Supabase CLI](https://supabase.com/docs/guides/local-development/cli/getting-started):
  Local Supabase stacks, database diffs, migrations, generated types, and
  dry-run pushes.
- [MongoDB Atlas CLI](https://www.mongodb.com/docs/atlas/cli/current/): Atlas
  projects, clusters, users, backups, alerts, and raw Atlas API calls.
- [Neon CLI](https://neon.com/cli): Neon projects, branches, connection
  strings, database branching, and project linking.
- [PlanetScale CLI (`pscale`)](https://planetscale.com/docs/cli): MySQL
  branching, deploy requests, service tokens, and safer read-only SQL defaults.
- [Turso CLI](https://docs.turso.tech/cli): SQLite databases, branches,
  replicas, tokens, orgs, and locations from scripts.
- [Convex CLI](https://docs.convex.dev/cli/overview): Projects, deployments,
  functions, data inspection, logs, env vars, imports, exports, and codegen.
- [Upstash CLI](https://upstash.com/docs/agent-resources/cli): Redis, Vector,
  Search, QStash, teams, JSON output by default, and dry-runs on destructive
  commands.
- [Databricks CLI](https://docs.databricks.com/aws/en/dev-tools/bundles/direct):
  Bundle validation, JSON deployment plans, and replay of an approved plan.
- [Snowflake CLI](https://docs.snowflake.com/en/developer-guide/snowflake-cli/index):
  SQL, stages, Snowpark, Streamlit apps, and object management.
- [DuckDB CLI](https://duckdb.org/docs/current/clients/cli/arguments): Local
  SQL over CSV, JSON, Parquet, SQLite, Postgres exports, and remote files.
- [sqlite-utils](https://sqlite-utils.datasette.io/en/stable/cli.html): Import
  CSV, JSON, and JSONL into SQLite, reshape tables, add full-text search, and
  query the database as JSON.
- [Datasette](https://docs.datasette.io/): A local SQLite database exposed as a
  searchable JSON API.
- [Steampipe](https://steampipe.io/docs): Cloud and SaaS APIs exposed as SQL
  tables, with plugin and rate-limit caveats.
- [Dolt](https://www.dolthub.com/docs/cli-reference/cli/): SQL data with
  Git-like branches, commits, row diffs, merges, and rollback.
- [dbmate](https://github.com/amacneil/dbmate): Database migrations, schema
  dumps, migration status, rollback, and checks without tying the project to
  one app framework.
- [MinIO Client (`mc`)](https://docs.min.io/aistor/reference/cli/): S3-compatible
  object storage inspection, copy, mirror, and management. The mirror dry-run
  is the main reason to hand it to an agent.
- [Backblaze B2 CLI (`b2`)](https://www.backblaze.com/docs/cloud-storage-command-line-tools):
  B2 buckets, files, keys, replication, sync, removals, and JSON output.
- [s5cmd](https://github.com/peak/s5cmd): High-volume S3 operations with
  command files, dry-runs, and structured logs.
- [rclone](https://rclone.org/commands/rclone/): Copy, compare, check, and sync
  files across many storage providers.
- [restic](https://restic.readthedocs.io/en/stable/075_scripting.html):
  Encrypted backups with addressable snapshots, checks, restores, and JSON
  output for scripting.

## Queues, Streams, And Realtime

- [NATS CLI](https://github.com/nats-io/natscli): Streams, consumers, KV,
  object stores, schemas, events, messages, benchmarks, and named contexts.
- [Redpanda `rpk`](https://docs.redpanda.com/streaming/current/reference/rpk/):
  Kafka-compatible topics, records, offsets, consumer groups, schemas, and
  cluster analysis. Record consumption can be bounded and emitted as JSON.
- [RabbitMQ `rabbitmqadmin`](https://www.rabbitmq.com/docs/management-cli):
  Broker inspection plus definition export and import workflows. Treat imports
  as live mutations.
- [ntfy CLI](https://docs.ntfy.sh/subscribe/cli/): Notification publishing and
  subscription streams from shell scripts.

## Observability And Incidents

- [Grafana CLI (`gcx`)](https://github.com/grafana/gcx): Grafana resources,
  contexts, validation, dry-run pushes, and scriptable output.
- [Grafana LogCLI](https://grafana.com/docs/loki/latest/query/logcli/getting-started/):
  Bounded LogQL queries against Loki with JSONL output.
- [New Relic CLI](https://docs.newrelic.com/docs/new-relic-solutions/build-nr-ui/newrelic-cli/):
  NRQL, NerdGraph, entities, workloads, deployments, profiles, and JSON output
  by default.
- [Datadog `datadog-ci`](https://docs.datadoghq.com/continuous_testing/cicd_integrations/configuration/):
  Targeted Synthetic test runs from CI with JSON and JUnit reports.
- [Elastic `ecctl`](https://www.elastic.co/docs/reference/ecctl/): Elastic
  Cloud deployment inspection and management with explicit deployment IDs and
  JSON output.
- [Axiom CLI](https://axiom.co/docs/reference/cli): Query, stream, and ingest
  Axiom datasets from the terminal.
- [Tailpipe](https://tailpipe.io/docs): External logs collected into a local
  analytical store and queried with SQL.

## Security, Secrets, And Supply Chain

- [1Password CLI (`op`)](https://developer.1password.com/docs/cli/): Secret
  references, vault items, service accounts, `op run`, and JSON output. Prefer
  injection over printing secrets.
- [Bitwarden CLI (`bw`)](https://bitwarden.com/help/cli/): Vault items,
  folders, collections, organizations, Send objects, JSON templates, `jq`
  workflows, and scripted unlock sessions. Treat `bw serve` as local secret
  exposure unless you control the machine.
- [Vault CLI](https://developer.hashicorp.com/vault/docs/commands): Vault
  paths, policies, auth methods, leases, and JSON output. It belongs with
  narrow tokens.
- [Infisical CLI](https://infisical.com/docs/cli/overview): Secret sync,
  injection, project and environment targeting, and CI auth.
- [Doppler CLI](https://docs.doppler.com/docs/cli): Secrets, projects,
  configs, audit logs, `doppler run`, secret downloads, per-command config,
  and service token auth.
- [SOPS](https://getsops.io/): Encrypted YAML, JSON, ENV, INI, and binary files
  with reviewable diffs.
- [Gitleaks](https://github.com/gitleaks/gitleaks): Git history, worktrees,
  files, and stdin secret scans with JSON, CSV, JUnit, and SARIF reports.
- [TruffleHog](https://github.com/trufflesecurity/trufflehog): Git, GitHub,
  GitLab, S3, Docker, filesystem, and CI secret scans with verification and
  JSON output.
- [Trivy](https://trivy.dev/): Vulnerability, misconfiguration, secret, SBOM,
  filesystem, repo, and image scans with JSON and SARIF output.
- [Semgrep](https://github.com/semgrep/semgrep): Structural code search and
  security rules with parseable findings.
- [Snyk CLI](https://docs.snyk.io/developer-tools/snyk-cli/snyk-cli/cli-commands-and-options-summary):
  Dependency, code, container, IaC, license, and SBOM scans with JSON and SARIF
  output.
- [Syft](https://github.com/anchore/syft): SBOM generation for containers and
  filesystems in JSON, SPDX, and CycloneDX formats.
- [Grype](https://github.com/anchore/grype): Vulnerability scans for images and
  SBOMs with JSON output and severity gates.
- [Cosign](https://docs.sigstore.dev/quickstart/quickstart-cosign/):
  Container image and blob signing, verification, attestations, and keyless
  Sigstore workflows.
- [OpenSSF Scorecard](https://github.com/ossf/scorecard): Repository
  supply-chain checks for GitHub or local repos, with JSON output for policy
  gates.
- [Checkov](https://www.checkov.io/2.Basics/CLI%20Command%20Reference.html):
  Infrastructure-as-code policy checks with JSON, SARIF, JUnit, and CI exits.
- [TFLint](https://github.com/terraform-linters/tflint): Terraform linting with
  provider-aware rules before a full plan.

## API Contracts, Testing, And Replay

- [oasdiff](https://github.com/oasdiff/oasdiff/blob/main/docs/DIFF.md):
  Semantic OpenAPI diffs, breaking-change checks, changelogs, JSON or YAML
  reports, and CI exits.
- [Redocly CLI](https://redocly.com/docs/cli/commands): OpenAPI, AsyncAPI, and
  Arazzo linting and bundling with configurable rules and parseable output.
- [Vacuum](https://quobix.com/vacuum/commands/): OpenAPI, AsyncAPI, and JSON
  Schema linting with Spectral-compatible rules and parseable reports.
- [Buf CLI](https://buf.build/docs/reference/cli/buf/breaking/): Protobuf
  linting, formatting, generation, and breaking-change detection with JSON,
  JUnit, GitHub Actions, and GitLab output formats.
- [Schemathesis](https://schemathesis.readthedocs.io/en/stable/reference/cli/):
  Property-based tests from OpenAPI or GraphQL, with JUnit, VCR, HAR, and
  NDJSON reports. Filter mutating endpoints unless they are part of the test.
- [Postman CLI](https://learning.postman.com/docs/postman-cli/postman-cli-overview/):
  Collection runs, API tests, spec linting, monitors, Postman workspace sync,
  and JSON, JUnit, or HTML reports.
- [Newman](https://learning.postman.com/docs/reference/newman-cli/newman-built-in-reporters/):
  Postman collection runs from local files or URLs with CLI, JSON, JUnit,
  and progress reports.
- [k6](https://grafana.com/docs/k6/latest/): Scriptable load tests with
  thresholds, summaries, and JSON or NDJSON result streams.
- [Hurl](https://hurl.dev/docs/running-tests.html): Plain-text HTTP requests
  with captures, assertions, and report formats.
- [Bruno CLI (`bru`)](https://docs.usebruno.com/v2/bru-cli/overview): Local
  runs for Git-friendly API collections, with JSON, JUnit, and HTML reports.
- [Insomnia CLI (`inso`)](https://docs.insomnia.rest/inso-cli/introduction):
  Insomnia collection runs, spec linting, config generation, and API test
  suites for CI.
- [Hoverfly `hoverctl`](https://docs.hoverfly.io/en/latest/pages/reference/hoverctl/hoverctlcommands.html):
  HTTP capture, simulation, diff, and replay using portable simulation files.
- [Mockoon CLI](https://mockoon.com/cli/): Headless mock APIs from Mockoon or
  OpenAPI definitions.

## Content, CMS, And Media

- [Sanity CLI](https://www.sanity.io/docs/cli-reference/documents): Query,
  inspect, export, and manage Sanity datasets and documents from scripts.
- [Contentful CLI](https://www.contentful.com/developers/docs/tutorials/cli/import-and-export/):
  Contentful space and environment export, migration, and import through JSON
  files.
- [Directus schema tooling](https://directus.com/docs/tutorials/migration/promoting-changes-between-environments-in-directus):
  Directus schema snapshot, diff, and apply between environments.
- [WP-CLI](https://developer.wordpress.org/cli/commands/): WordPress content,
  users, plugins, themes, options, cron, cache, and database operations. The
  `search-replace --dry-run` path is worth special attention.
- [Cloudinary CLI (`cld`)](https://cloudinary.com/documentation/cloudinary_cli):
  Cloudinary asset search, export, upload, transform, and management.
- [Mux CLI](https://www.mux.com/docs/integrations/mux-cli): Video assets, live
  streams, playback IDs, signed URLs, and local webhook listen, replay, and
  trigger flows.
- [Shopify CLI](https://shopify.dev/docs/api/shopify-cli): Apps, themes,
  extensions, functions, deploys, and local previews for Shopify projects.
- [Ghost CLI](https://docs.ghost.org/ghost-cli): Ghost install, upgrade,
  backup, restart, logs, and diagnostics.

## Workspace, CRM, Email, And Messaging

- [Slack CLI (`slack`)](https://docs.slack.dev/tools/slack-cli/): Slack apps,
  manifests, triggers, workflows, datastores, app deploys, local run, and logs.
- [Google Workspace CLI (`gws`)](https://github.com/googleworkspace/cli): Drive,
  Gmail, Calendar, Sheets, Docs, Chat, and Admin APIs with JSON-first output.
  It is pre-1.0 and community-run.
- [CLI for Microsoft 365 (`m365`)](https://pnp.github.io/cli-microsoft365/):
  Microsoft 365, Entra ID, Teams, SharePoint, Planner, and Outlook automation
  with JSON output and JMESPath queries.
- [Notion CLI (`ntn`)](https://developers.notion.com/cli/get-started/overview):
  Notion auth, API requests, data sources, file uploads, and Notion Workers.
- [Airtable MCP CLI (`airtable-mcp`)](https://github.com/Airtable/airtable-mcp-cli):
  Airtable bases and records through Airtable's MCP server, with profiles, JSON
  tool discovery, stdin JSON input, and changing server-side tool schemas.
- [Linear CLI (`linear`)](https://github.com/schpet/linear-cli): Unofficial
  Linear issues, teams, projects, milestones, documents, comments, attachments,
  branches, and JSON output on query, list, and view commands.
- [HubSpot CLI (`hs`)](https://developers.hubspot.com/docs/developer-tooling/local-development/hubspot-cli/reference):
  HubSpot apps, CMS assets, developer projects, serverless functions, uploads,
  downloads, and account auth.
- [Salesforce CLI (`sf`)](https://developer.salesforce.com/docs/platform/salesforce-cli-reference/guide/cli_reference_project.html):
  Orgs, metadata, scratch environments, deploy validation, and JSON output.
- [Twilio CLI](https://www.twilio.com/docs/twilio-cli/general-usage/output-formatting-and-filtering):
  Twilio resources through generated commands, profiles, test credentials, and
  full JSON API responses.
- [Mattermost `mmctl`](https://docs.mattermost.com/administration-guide/manage/mmctl-command-line-tool.html):
  Server administration over local socket or remote API with JSON output.
- [notmuch](https://notmuchmail.org/doc/latest/man1/notmuch-search.html):
  Search, thread, tag, dump, and restore for a local mail corpus, with stable
  message and thread IDs.
- [Himalaya](https://pimalaya.org/himalaya/): IMAP and Maildir operations from
  the terminal. Test error behavior on your setup before relying on it.
- [Resend CLI](https://github.com/resend/resend-cli): Domains, API keys,
  contacts, broadcasts, emails, and webhooks with JSON mode outside a TTY.
- [Postmark CLI (`postmark`)](https://github.com/ActiveCampaign/postmark-cli):
  Transactional email sends, server lookup, and template pull or push for CI.
  It is narrower than Resend.

## Payments, Commerce, And Finance

- [Stripe CLI](https://docs.stripe.com/stripe-cli): Webhooks, test events,
  fixtures, logs, and sandboxed Stripe flows. Keep agents in test mode unless
  live access is intentional.
- [Ramp CLI](https://docs.ramp.com/developer-api/v1/cli): Ramp finance flows
  with `--agent`, `--no-input`, pagination, dry-runs for common actions, and a
  sandbox-first setup.

## Still Looking For

Gaps to research next: maintained CLIs for PagerDuty or Opsgenie incident work,
HubSpot CRM data, Help Scout or Zendesk queues, ad platforms, analytics
exports, product analytics, warehouse migrations, data lineage, marketplace
operations, and niche CLIs people actually use with agents.

## Contributing

Add CLIs that are worth giving to an AI agent. A tool does not belong here just
because it has a command.

See [criteria.md](criteria.md). One tool per pull request. Link the primary
docs, and mention the sharp caveat.

## Maintainer

Maintained by [Vincent Schmalbach](https://www.vincentschmalbach.com/)
([rungrad](https://www.rungrad.com/)).

Vincent builds Go CLIs, SaaS automation, and internal developer tools for
clients.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
