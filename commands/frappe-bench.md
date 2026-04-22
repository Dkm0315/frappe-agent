# Frappe Bench

Handle the task as bench-aware Frappe operations work.

- Inspect bench root, target site, installed apps, app remotes, branches, `sites/apps.txt`, and `sites/common_site_config.json` before acting.
- Prefer read-only checks first.
- Explain why each bench command is appropriate.
- Call out risky flags and risky version or branch operations explicitly.
- Do not assume the bench is stopped or that the default site is the target site.
