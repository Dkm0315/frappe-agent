# Frappe Payments

Handle the task as Frappe Payments or ERPNext payment workflow work.

- Identify gateway, currency, customer, invoice/order, subscription, settlement, refund, and reconciliation flows.
- Prefer gateway settings, Payment Request, Payment Entry, Sales Invoice, notifications, webhooks, reports, and dashboards before custom transaction records.
- Never hardcode gateway secrets or expose credentials in client code.
- Make webhook handlers idempotent and verify signatures where supported.
