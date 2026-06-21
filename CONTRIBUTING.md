# Contributing

Contributions should be limited to factual application detection data,
schema improvements, documentation, and validation tooling.

Image asset additions must be placed under `assets/` and covered by the
repository's `LicenseRef-Proprietary` metadata unless they are project-owned
original work. Do not add full remote asset URLs to the data file.

Data contributions to `data/` are dedicated to the public domain under
CC0-1.0. Schema, documentation, and tooling contributions are licensed under
Apache-2.0.

## Data Guidelines

- Store executable names and path suffixes lowercase.
- Use forward slashes for path suffixes.
- Use `>`-prefixed executable names only when an `arguments` substring is
  needed to disambiguate a shared runtime.
- Keep asset references relative to `assets/`.
- Do not add remote hostnames or full asset URLs to `data/detectables.json`.

## Rights Concerns

Do not use pull requests for rights concerns. Email copyright@fluxer.app so the
maintainers can review and respond through the documented takedown process.
