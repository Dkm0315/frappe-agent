# Frappe Backend

Handle the task as Frappe backend work.

- Treat Frappe backend as Python-first with important JavaScript touchpoints.
- Prefer framework APIs and deliberate permission handling.
- Check whether the change should instead be handled by `Custom Field`, `Property Setter`, `Client Script`, `Server Script`, `Workflow`, `Report`, or `Workspace`.
- Keep controllers, hooks, whitelisted methods, patches, scheduler jobs, and service logic clearly separated.
