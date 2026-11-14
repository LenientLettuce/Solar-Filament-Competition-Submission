# Competition submission

Install the dependencies in the Python environment used by Jupyter.

```sh
python -m pip install -r requirements.txt
```

Open `Pipeline_competition.ipynb` and run all cells. By default it uses the bundled weights and the checkpoint's 106-image validation split. Keep MAGFiLO beside the notebook or set `DATASET_ROOT`.

| Validation output | What it shows |
| --- | --- |
| [Dice](validation_analysis/dice_distribution.png) | Dice scores for matched filament pairs |
| [IoU](validation_analysis/iou_distribution.png) | IoU scores for the same pairs |
| [Splits and merges](validation_analysis/split_merge_distribution.png) | Counts per annotator drawing, including drawings with zero relations |

A pair is matched when IoU exceeds 0.5. A split or merge requires any pixel overlap with at least two instances on the other side. The [summary](validation_analysis/summary.json), [matched pairs](validation_analysis/matched_pairs.csv), and [per-drawing counts](validation_analysis/per_drawing.csv) accompany the figures.

Set `WRITE_TEST_SUBMISSION=True` to generate `submission.csv`. For test-only inference, also set `RUN_VALIDATION_ANALYSIS=False`.
