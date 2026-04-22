# Frappe Backend

Treat the task as Frappe backend work.

- Use Python-first reasoning with deliberate permission handling.
- Check whether the request should use metadata or admin customization surfaces instead of backend code.
- Keep hooks, whitelisted methods, patches, scheduler logic, and service logic clearly separated.
