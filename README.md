# Frappe Agent for Codex

`frappe-agent` is a Codex plugin for Frappe Framework and ERPNext development. It makes Codex more aware of Frappe-specific patterns so it can inspect benches more safely, choose the right customization layer, and avoid generic framework mistakes.

## What It Covers

- Frappe full-stack reasoning across backend, frontend, customization, and bench work
- Bench-aware inspection before app installs, migrations, or environment changes
- Frappe-native SQL and ORM guidance
- Customization-layer routing for `Custom Field`, `Property Setter`, `Client Script`, `Server Script`, `Workspace`, `Web Page`, `Report`, `Dashboard`, and related surfaces
- ERPNext-aware guidance for deciding between configuration, metadata, workflow, and code changes
- Frontend guidance for Vue, React, `frappe-ui`, desk pages, `www`, and external SPA patterns

## Included Skills

- `frappe-fullstack`
- `frappe-backend`
- `frappe-frontend`
- `frappe-bench`
- `frappe-sql`
- `frappe-customization`
- `frappe-search`
- `frappe-erpnext`

## Installation

This repository currently ships:

- a real Codex plugin
- portable agent-instruction files for Claude Code, Cursor, and GitHub Copilot

It does not yet ship a full native Claude Code plugin package or a native Cursor/Copilot plugin package.

### Codex

Codex supports repo marketplaces and local plugin installation.

If you cloned this repository locally:

```bash
codex marketplace add /path/to/frappe-agent
```

Then enable `frappe-agent` from the added marketplace and restart Codex in a fresh session.

This repo includes:

- `.codex-plugin/plugin.json`
- `.agents/plugins/marketplace.json`

so it can act as a self-contained Codex plugin repository.

### Claude Code

Claude Code supports plugins, but this repository currently provides portable repo instructions rather than a native Claude plugin manifest.

Today, the practical setup is to copy or symlink the included `CLAUDE.md` into the target repository root:

```bash
ln -s /path/to/frappe-agent/CLAUDE.md /path/to/your-frappe-project/CLAUDE.md
```

or:

```bash
cp /path/to/frappe-agent/CLAUDE.md /path/to/your-frappe-project/CLAUDE.md
```

### Cursor

Cursor uses repository instructions such as `AGENTS.md`, `.cursor/rules`, and project commands.

You can reuse the included files in a target repository:

```bash
cp /path/to/frappe-agent/AGENTS.md /path/to/your-frappe-project/AGENTS.md
mkdir -p /path/to/your-frappe-project/.cursor/rules
cp /path/to/frappe-agent/.cursor/rules/frappe-agent.mdc /path/to/your-frappe-project/.cursor/rules/frappe-agent.mdc
```

### GitHub Copilot

Copilot uses repository custom instructions and agent instructions.

You can copy the included instruction file into a target repository:

```bash
mkdir -p /path/to/your-frappe-project/.github
cp /path/to/frappe-agent/.github/copilot-instructions.md /path/to/your-frappe-project/.github/copilot-instructions.md
```

You can also keep `AGENTS.md` in the target repository root for tools that support agent instruction files.

## Usage Examples

Ask Codex to use the plugin naturally in the prompt:

```text
Use Frappe Agent to inspect this bench before changing anything.
```

```text
Use Frappe Agent to choose the right Frappe customization layer for adding fields to Sales Order.
```

```text
Use Frappe Agent to review whether this Frappe SQL should use frappe.db, frappe.qb, or raw SQL.
```

```text
Use Frappe Agent to decide whether this UI should be a desk page, a www page, a Vue frappe-ui page, or a React SPA.
```

## Repository Layout

```text
frappe-agent/
├── .agents/
│   └── plugins/
│       └── marketplace.json
├── .cursor/
│   └── rules/
│       └── frappe-agent.mdc
├── .codex-plugin/
│   └── plugin.json
├── .github/
│   └── copilot-instructions.md
├── AGENTS.md
├── CLAUDE.md
├── skills/
│   ├── frappe-backend/
│   ├── frappe-bench/
│   ├── frappe-customization/
│   ├── frappe-erpnext/
│   ├── frappe-frontend/
│   ├── frappe-fullstack/
│   ├── frappe-search/
│   └── frappe-sql/
└── README.md
```

## Current Scope

This repository is the Codex-native plugin package plus a portable instruction bundle for Claude Code, Cursor, and Copilot.

Planned future work:

- native Claude Code plugin packaging
- richer Cursor command bundles
- deeper Copilot instruction coverage

## Design Goals

- Inspect first, mutate second
- Prefer Frappe-native customization surfaces before invasive code changes
- Separate ERPNext configuration work from framework-code work
- Respect bench context, app provenance, and version boundaries
- Help agents make fewer generic Python, JavaScript, SQL, and frontend mistakes in Frappe codebases

## Roadmap

- Add more first-class skills for custom fields, reports, workflows, dashboards, and upgrade planning
- Add better source-backed command and flag coverage for Bench
- Add distribution adapters for Claude Code, Cursor, and Copilot
- Add richer repo examples and team onboarding docs

## License

MIT
