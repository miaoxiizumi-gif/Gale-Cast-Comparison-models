# GALE-CAST Model Comparison & Validation

A student research report based on saved, aggregate validation results. This repository contains only the dedicated static reporting site, not the production GALE-CAST application.

## Hosting

GitHub Pages publishing source: `main`, repository root. The expected report address after successful deployment is https://miaoxiizumi-gif.github.io/Gale-Cast-Comparison-models/ . Check repository Pages/deployment status for current availability.

## Read the report

Use the tabs to compare architectures, event matrices, ordinary wind forecasting, station differences, thesis claims and research decisions. Choose the same event definition, lead and sample before comparing products. Light/dark themes, text-only findings and aggregate CSV downloads are included.

## Evidence and limits

Source review: `mr-20261022T161445Z-86f544`, source commit `529747b62d80e5e70a127a79c4fc27387ec1c3a2`.
Phase 4 final run: `p4-final-p4-v1-20261022T135648Z-8e72c1`.
Phase 2: `p2-compare-p2-v1-20261022T095800Z-56a531`.

All 28 original export hashes matched the review manifest during preparation. This confirms integrity, not scientific correctness. All 153 event rows were checked. Derived accuracy/F1 cards use saved aggregate matrix counts; no models were trained or rescored.

2023?2024 was previously examined; its results are retrospective/exploratory. Phase 4 is a separate wind-only architecture. Gale-detection skill is not established. Chapter 4 was unavailable to the source review. This report is not an operational forecast or approval to replace production.

See `methodology.md` and `provenance.json`. No raw station records, case-level forecasts, models, credentials, private device paths or respondent data are included.
