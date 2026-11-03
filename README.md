# GPS-Enhanced Horse Race Simulator

A collaborative portfolio project comparing traditional past-performance
features with GPS-derived race features, then visualizing race scenarios in an
interactive Dash app.

## What is included

- `gps_horse_race_simulator.ipynb` — feature engineering, model training and
  evaluation, upcoming-race scoring, and the Dash simulator.
- `css_block.txt` and `js_block.txt` — dashboard presentation and interaction
  assets used by the notebook.
- `requirements.txt` — Python dependencies.

The public repository deliberately excludes the supplied race datasets, the
course/competition brief, and saved notebook outputs. The notebook expects
authorized CSV files in `data/`; see [`data/README.md`](data/README.md) for the
expected filenames. Do not add source data unless its owner permits the
intended use and redistribution.

## Run locally

1. Use Python 3.10 or newer.
2. Create and activate a virtual environment.
3. Install dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Put the authorized CSV inputs listed in [`data/README.md`](data/README.md)
   into `data/`.
5. Start Jupyter from this repository's root and run the notebook cells in
   order:

   ```bash
   python -m pip install jupyter
   jupyter notebook gps_horse_race_simulator.ipynb
   ```

The final cell launches the dashboard at `http://127.0.0.1:8052`.

## Modeling overview

The notebook builds traditional past-performance aggregates and summaries of
horse-level GPS telemetry. It compares win and top-three Random Forest models
using a chronological 80/20 split and reports ROC AUC, accuracy, and log loss.
GPS features are missing for horses without GPS history; the model pipeline
imputes missing numeric values.

This is a portfolio demonstration, not betting advice. Results depend on the
authorized data supplied by the user and are not a guarantee of future
performance.

## Data handling

The required CSVs are not included because the source data's redistribution
rights are not established here. Obtain the files through an authorized source
and follow that source's terms. The repository ignores CSV files under `data/`
to help prevent accidental publication.

## Contribution and license

This collaborative project's source is shared for portfolio review. No
open-source license is granted by this repository.
