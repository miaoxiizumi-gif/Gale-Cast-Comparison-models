# GALE-CAST model comparison methodology

Train: 2015-01-01–2020-12-31. Tune: 2021-01-01–2022-12-31.
Evaluate: 2023-01-01–2024-12-31, by target date.
2023–2024 was examined during earlier development. These results are retrospective.

Primary stations: NAIA, Sangley Point, Science Garden; 2,193 identical cases per lead.
Port Area is secondary: 304 cases per lead; record ends 2023-10-31.
Wind is the recorded daily value in m/s. Statistic, averaging period, height,
day boundary and reporting delay remain unverified; zero reporting delay was assumed.

Proxy event: recorded wind >= 10.8 m/s OR day-to-day MSLP fall >= 3 hPa.
The 20 primary evaluation positives are all pressure-fall cases, not verified gale winds.
Keep probability-threshold and predicted-weather event rules separate.
Relatively windy event: recorded wind >= station training-period 95th percentile:
NAIA 4, Sangley Point 5, Science Garden 2, Port Area 4 m/s.

Matrix rows: Actual No Event, Actual Event.
Columns: Predicted No Event, Predicted Event. Cells: [[TN, FP], [FN, TP]].
Accuracy=(TP+TN)/N; precision=TP/(TP+FP); recall=TP/(TP+FN);
F1=2TP/(2TP+FP+FN); false-alarm ratio=FP/(TP+FP); CSI=TP/(TP+FN+FP).
A zero denominator means Not defined, never a real zero.
These cards are descriptive calculations from saved aggregate counts only.
PR-AUC is copied from the saved compatible probability result, never computed from a matrix.

Wind skill = 1 - MAE(method)/MAE(reference); it is error reduction, not percentage accuracy.
Saved paired uncertainty uses 14-day moving blocks over target dates, 2,000 resamples,
seed 20261023. No established difference is not proof of equality.
The station-aware Phase 4 model was chosen on development mean MAE across leads;
a more complex candidate needed an improvement of at least 0.005 m/s.
The residual network's 0.0002 m/s development advantage was below that margin.

No observed 2023–2024 case reaches 10.8 or 17.2 m/s. Gale-detection skill is not established.
Historical production scores used a different, contaminated protocol and sample.
Phase 4 is a different wind-only architecture, not an improved original architecture.
Chapter 4 was unavailable; only Chapters 1–3 were reviewed.
No model was trained, tuned, recalibrated, rethresholded, predicted or rescored for this site.
Matching export hashes confirms file integrity, not scientific correctness by itself.
