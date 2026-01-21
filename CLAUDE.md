# Stroikos Project Instructions

## Repository Info
- **GitHub**: https://github.com/missioncritical842/Stroikos
- **GitHub Pages**: https://missioncritical842.github.io/Stroikos/
- **Current Version**: v1.6

## Grist Documents Using These Widgets

### Stroikos
- **Doc ID**: `8ApvMNhvYqr8R8A2NA1fdD`

## Widgets
| Widget | GitHub Pages URL |
|--------|------------------|
| Client Form | https://missioncritical842.github.io/Stroikos/client-form.html |
| Lights Invoice | https://missioncritical842.github.io/Stroikos/lights-invoice.html |
| Tree Invoice | https://missioncritical842.github.io/Stroikos/tree-invoice.html |

## Commit Requirements
- **Always increment version number** in commit message (e.g., "Description of changes (v1.1)")
- After committing, provide updated GitHub Pages URLs with new version as cache-busting parameter: `?v1.X`
- Push to origin after commit

## Grist MCP Integration - CRITICAL
When working with Grist data:
1. **Always use Grist MCP tools** (`list_tables`, `list_columns`, `list_records`) to verify actual table and column names
2. **Never create fallback or wildcard lookups** - reference exact column/table names from the schema
3. **Never guess column names** - query the schema first using `mcp__grist__list_columns`

### Common Column Lookup
Before referencing any column in widget code, run:
```
mcp__grist__list_columns(doc_id="8ApvMNhvYqr8R8A2NA1fdD", table_id="<table_name>")
```
