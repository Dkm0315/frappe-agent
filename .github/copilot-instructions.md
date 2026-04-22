# Frappe Agent Copilot Instructions

Treat this repository as Frappe and ERPNext-specific guidance for coding agents.

- Inspect bench and site context before changing code or suggesting commands.
- Prefer the correct Frappe customization surface before writing framework code.
- Use `Custom Field`, `Property Setter`, `Client Script`, `Server Script`, `Workspace`, `Web Page`, `Report`, `Dashboard`, `Workflow`, and `Webhook` when they fit better than custom code.
- Prefer Frappe-native database access layers (`frappe.db`, Query Builder) over raw SQL when possible.
- When raw SQL is required, use correct `tab{DocType}` naming and call out permission and transaction implications.
- Separate frontend guidance into desk-native pages, `www`, Vue/`frappe-ui`, React, and external SPA patterns.
- Treat non-official app remotes as custom or custom-derived.
