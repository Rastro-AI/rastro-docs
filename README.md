# Rastro API Documentation

Official documentation for the Rastro API, built with [Mintlify](https://mintlify.com).

## Development

Install Mintlify CLI:

```bash
npm i -g mintlify
```

Run locally:

```bash
mintlify dev
```

Open http://localhost:3000

## Deployment

Documentation is automatically deployed when changes are pushed to `main`.

## Structure

```
├── introduction.mdx        # Getting started
├── quickstart.mdx          # Quick start guide
├── authentication.mdx      # Auth documentation
├── concepts/               # Core concepts
├── guides/                 # How-to guides
├── api-reference/          # API endpoint docs
│   ├── catalogs/
│   ├── items/
│   ├── products/
│   └── workflows/
└── sdks/                   # SDK documentation
```

## Contributing

1. Create a branch
2. Make changes
3. Run `mintlify dev` to preview
4. Submit PR
