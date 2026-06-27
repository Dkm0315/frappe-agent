# Frappe Agent Copilot Instructions

Treat this repository as Frappe, ERPNext, and Frappe ecosystem guidance for coding agents.

- Inspect bench and site context before changing code or suggesting commands.
- Prefer the correct Frappe customization surface before writing framework code.
- Use `Custom Field`, `Property Setter`, `Client Script`, `Server Script`, `Workspace`, `Web Page`, `Report`, `Dashboard`, `Workflow`, and `Webhook` when they fit better than custom code.
- Prefer Frappe-native database access layers (`frappe.db`, Query Builder) over raw SQL when possible.
- When raw SQL is required, use correct `tab{DocType}` naming and call out permission and transaction implications.
- Separate frontend guidance into desk-native pages, `www`, Vue/`frappe-ui`, React, and external SPA patterns.
- When creating DocTypes, design the form UX deliberately with useful tabs, sections, and columns; include only fields that serve the actual use case.
- Treat non-official app remotes as custom or custom-derived.
- Route app-specific work through the right ecosystem model: ERPNext, Helpdesk, CRM, LMS, Gameplan, Drive, HRMS, Insights, Builder, or Payments.
- Protect sensitive app data: customer tickets, CRM pipelines, learner records, private files, salary/payroll data, payment secrets, and analytics permissions.
