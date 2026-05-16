# Frappe Agent for Claude Code

This repository contains Codex-native plugin assets plus portable Frappe/ERPNext development guidance.

When working in a Frappe or ERPNext codebase:

- Inspect bench and site state before suggesting commands.
- Prefer configuration and metadata-driven customization before code overrides.
- Consider `Custom Field`, `Property Setter`, `Client Script`, `Server Script`, `Workspace`, `Web Page`, `Report`, `Dashboard`, `Workflow`, and `Webhook` before editing framework code.
- Use Frappe-native ORM or Query Builder when possible.
- If raw SQL is necessary, use correct `tab{DocType}` naming and explain permission implications.
- Distinguish desk-native Vue and `frappe-ui` patterns from React or external SPA work.
- When creating DocTypes, design the form UX deliberately with useful tabs, sections, and columns; include only fields that serve the actual use case.
- Treat forked or custom-remote apps as custom-derived apps and be careful with upstream patching.
