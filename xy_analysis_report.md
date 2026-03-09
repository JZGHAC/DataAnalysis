# XY dataset analysis

## Files analyzed
- `2026-3-4-23-2-32 Left XY.csv`
- `2026-3-4-23-3-0 Right XY.csv`

## Method used
This reproduces the methodology in the attached `Data analysis XY 050326.docx`:
1. Trim and parse timestamps, reconstruct sub-second timing from sample order.
2. Invert the left-leg `angle1` and `angle2` signals to align sign conventions.
3. Remove outliers with `|angle| > 500°` and linearly interpolate.
4. Apply a 4th-order Butterworth low-pass filter with a 10 Hz cutoff.
5. Detect pedal cycles from peaks in filtered sagittal motion with a minimum spacing of 0.4 s.
6. Compute per-cycle sagittal ROM, sagittal variability, lateral ROM, and lateral variability.
7. Match left/right cycles by nearest cycle time within 0.5 s.
8. Use the first 5 minutes as baseline for z-score normalization.
9. Run:
   - Algorithm 1: threshold detection (2.0 SD in expected fatigue direction for 10 consecutive cycles)
   - Algorithm 2: EWMA control chart (alpha=0.1, UCL from baseline, 10 consecutive cycles)

## Dataset characteristics
- Left duration: 1835.0 s
- Right duration: 1861.7 s
- Estimated sample rate: 49.0 Hz (left), 49.0 Hz (right)
- Detected cycles: 2356 left, 2377 right
- Matched cycles used for bilateral analysis: 2337

## Main trends
| feature                      |   baseline_mean |   final_5min_mean |   slope_per_s |      p_value |
|:-----------------------------|----------------:|------------------:|--------------:|-------------:|
| Average sagittal ROM         |        51.242   |         49.7857   |  -0.000975576 | 1.47873e-44  |
| Average sagittal variability |        17.6524  |         16.6011   |  -0.000702658 | 3.92121e-202 |
| Average lateral ROM          |        36.8036  |         35.0044   |  -0.000883825 | 8.00969e-110 |
| Average lateral variability  |        13.2346  |         12.6275   |  -0.000298818 | 1.38379e-88  |
| ROM symmetry index           |         0.20013 |          0.215661 |   7.26209e-06 | 0.00502395   |

## Fatigue detection
| algorithm                                                                 |   detection_time_left_clock_s |   detection_time_min | trigger                             | note                                                       |
|:--------------------------------------------------------------------------|------------------------------:|---------------------:|:------------------------------------|:-----------------------------------------------------------|
| Threshold (2.0 SD, 10 consecutive cycles)                                 |                     1071.87   |            17.8645   | Left sagittal ROM decrease          | No detection at 2.5 SD                                     |
| EWMA (alpha=0.1, UCL=baseline mean + 3 sigma_EWMA, 10 consecutive cycles) |                       25.8433 |             0.430722 | Composite score sustained above UCL | Right-file elapsed time at detection = 24.32 s (~0.41 min) |

## Interpretation
The dataset shows gradual kinematic drift rather than abrupt breakdown. Average sagittal ROM, sagittal variability,
lateral ROM, and lateral variability all decline over time. ROM asymmetry increases slightly, indicating that the
right leg becomes progressively larger relative to the left in sagittal ROM.

Algorithm 1 detects sustained change late in the session, driven by a persistent decrease in **left sagittal ROM**.
Algorithm 2 fires almost immediately, which is consistent with the earlier report and suggests the EWMA is highly
sensitive to start-up adaptation rather than true physiological fatigue onset.

## Output files
- `threshold_plot.png`
- `ewma_plot.png`
- `trend_summary.csv`
- `detection_summary.csv`
