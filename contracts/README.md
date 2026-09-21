# ORI Quality Monitoring data contracts (draft)

Best-guess contracts, rooted in reality. The gold and silver tables do not exist yet in the sprouts-dev catalog.

Gold contracts follow the datasets in the Data tab of the prototype at https://ori-dashboard.lovable.app. The prototype's column names are recorded as `businessName`. The three accuracy contracts are inferred from the Accuracy tab, because the prototype hard-codes those figures.

The silver contract is derived from the gold contracts and mapped to what is in sprouts-dev today: `openalex.works`, `openaire-11.1.1.publications` and `authorships`, `cris.publications`, `nl-orgs.baseline`, and `pid2portal` as the closest existing starting point. Crossref is not yet ingested. Records are matched across sources within an organisation: exactly on DOI, otherwise by exact and fuzzy matching on other identifiers and titles (see `match_cluster_id`, `match_method` and `match_score` in silver).

| Contract | Dashboard tab | Prototype dataset |
|---|---|---|
| gold/completeness-metrics | Completeness | Completeness metrics |
| gold/completeness-timeline | Completeness | Completeness timeline |
| gold/coverage-comparisons | Coverage | Coverage comparisons |
| gold/coverage-timeline | Coverage | Coverage timeline |
| gold/enrichment-entities | Enrichment | Enrichment entities |
| gold/detail-records | Coverage, Completeness | Detail records |
| gold/accuracy-agreement | Accuracy | Inferred from UI |
| gold/accuracy-timeline | Accuracy | Inferred from UI |
| gold/accuracy-conflict-records | Accuracy | Inferred from UI |
| gold/interventions | All tabs | Interventions |
| gold/organisations | About, filter bar | Organisations |
| gold/overview-cards | About | Overview cards |
| silver/publications | (input for all gold) | none |

All contracts follow ODCS v3.1.0 and pass `datacontract lint` (CLI 1.2.0). All SQL quality rules run in DuckDB. S3 locations are placeholders.
