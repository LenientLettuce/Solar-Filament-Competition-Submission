# Competition submission

1. From this folder create a venv enviornment, activate it,and then install the pinned packages.

   ```sh
   python -m pip install -r requirements.txt
   ```

2. Open `Pipeline_competition.ipynb` in Jupyter using the same Python environment and select **Run All**. The notebook loads the bundled model weights and writes `submission.csv`.

The notebook looks for the MAGFiLO dataset in this folder or a parent folder. If it lives elsewhere, set `DATASET_ROOT` in the first code cell.
