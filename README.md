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

### Local Marketplace Install

1. Add the containing marketplace to Codex.
2. Enable `frappe-agent` from that marketplace.
3. Restart Codex so the plugin is picked up in a fresh session.

If you are using this repository directly as a local plugin source, the plugin manifest lives at `.codex-plugin/plugin.json`.

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
├── .codex-plugin/
│   └── plugin.json
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

This repository is the Codex-focused plugin package. The broader product direction also includes future adapters for Claude Code, Cursor, and Copilot, but those host-specific integrations are not bundled here yet.

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
