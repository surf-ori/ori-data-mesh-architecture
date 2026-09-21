# ORI Data Mesh Architecture

A proposal for the BROCCOLI data engineers: apply data mesh concepts (data products, data
contracts, a data marketplace) to the ORI DuckLake, using the medallion architecture
(staging, bronze, silver, gold) with dbt, DuckDB, DuckLake and the Data Contract CLI.

## Contents

- [`index.html`](index.html) — the blog post. Published with GitHub Pages, this is the site's
  home page: https://surf-ori.github.io/ori-data-mesh-architecture/
- [`contracts/`](contracts) — example ODCS v3.1.0 data contracts for the ORI Quality
  Monitoring use case (gold and silver). These are best-guess drafts rooted in the
  [ORI Quality Monitoring prototype](https://ori-dashboard.lovable.app) and the `sprouts-dev`
  DuckLake catalog. The gold and silver tables do not exist yet; see
  [`contracts/README.md`](contracts/README.md) for how each contract maps to the prototype
  and the catalog. All contracts pass `datacontract lint` (Data Contract CLI 1.2.0, ODCS v3.1.0).

## Related

- [surf-ori/ducklake-overview](https://github.com/surf-ori/ducklake-overview) — browse the
  public ORI DuckLake in the browser.
- [surf-ori/agentic-tools](https://github.com/surf-ori/agentic-tools) — the ORI DuckLake MCP
  server and other agentic tools.

## Publishing index.html with GitHub Pages

Settings → Pages → Source: `Deploy from a branch`, branch `main`, folder `/ (root)`.
The page is then served at `https://surf-ori.github.io/ori-data-mesh-architecture/`.

## License

TBD — add a LICENSE file before making this repository public, if it isn't already covered
by a SURF ORI organization-wide license.
