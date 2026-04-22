# Frappe SQL

Handle the task as Frappe-native SQL and ORM work.

- Decide between `frappe.db`, Query Builder, and raw SQL deliberately.
- Prefer Frappe-native APIs when they express the query clearly.
- Treat `get_all` and raw SQL as deliberate choices that need explanation.
- If raw SQL is required, use correct `tab{DocType}` naming and explain permission and transaction implications.
