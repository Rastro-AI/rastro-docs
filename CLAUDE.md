# Rastro Docs

This is the Rastro API documentation site built with Mintlify.

## Commands

- `npx mintlify dev` - Run the docs locally at http://localhost:3000
- `npx mintlify broken-links` - Check for broken links

## Mintlify docs.json Format (February 2025+)

Mintlify migrated from `mint.json` to `docs.json` in February 2025. The key change is the navigation structure.

### Navigation Format

The `navigation` field MUST be an **object**, not an array. Choose one primary organizational pattern at the root level:

**Groups (current pattern used):**
```json
{
  "navigation": {
    "groups": [
      {
        "group": "Getting Started",
        "pages": ["introduction", "quickstart"]
      }
    ]
  }
}
```

**Other valid root patterns:**
- `pages` - Simple flat list of pages
- `tabs` - Separate sections with their own navigation
- `anchors` - Persistent sidebar items
- `dropdowns` - Expandable top-level menus
- `versions` - Different documentation versions
- `languages` - Localized content

### Common Mistake

The OLD format (mint.json style) used navigation as a direct array - this will FAIL:
```json
{
  "navigation": [
    { "group": "...", "pages": [...] }
  ]
}
```

The NEW format (docs.json) requires navigation as an object:
```json
{
  "navigation": {
    "groups": [
      { "group": "...", "pages": [...] }
    ]
  }
}
```

## File Structure

- `docs.json` - Main configuration file
- `*.mdx` - Documentation pages (MDX format)
- `/logo/` - Logo files (light.svg, dark.svg)
- `/favicon.svg` - Site favicon

## API Reference

Pages in `/enrich/`, `/flows/`, `/catalogs/` document the Rastro API.
API base URL: `https://catalogapi.rastro.ai/api`
