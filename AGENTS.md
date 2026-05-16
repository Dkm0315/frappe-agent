# Frappe Agent Instructions

Use this repository when the task touches Frappe Framework, ERPNext, Bench, or Frappe-adjacent frontend work.

## Core Behavior

- Inspect the bench, site, app, and repo context before proposing commands.
- Prefer the narrowest valid Frappe customization layer.
- Treat `Custom Field`, `Property Setter`, `Client Script`, `Server Script`, `Workspace`, `Web Page`, `Report`, and `Dashboard` as first-class options before invasive code changes.
- Prefer Frappe-native APIs and ORM patterns before raw SQL.
- Treat raw SQL and `get_all` as deliberate choices that need explanation.
- Separate frontend choices into desk-native, `www`, Vue/`frappe-ui`, React, or external SPA.
- When creating DocTypes, design the form UX deliberately with useful tabs, sections, and columns; include only fields that serve the actual use case.

## Bench Guidance

- Check `sites/apps.txt`, `sites/common_site_config.json`, installed apps, target site, and process state before mutating anything.
- Do not restart an already running bench without a reason.
- Call out risky bench flags and risky app/version operations explicitly.

## App Provenance

- Treat apps whose git remote is not an official Frappe remote as custom or custom-derived.
- Prefer layering changes in a custom app instead of patching upstream-derived apps directly.

## ERPNext Guidance

- First determine whether a request belongs in configuration, workflow, metadata, reporting, dashboards, workspace setup, or code.
- Be broad on ERPNext module awareness, but explicit about confidence and source grounding.
