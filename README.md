# GPS Enhanced Horse Race Simulator

A project built for The Econ Games 2026 at the University of Kentucky (Lexington, KY) by Ethan Brown and Aiden. It compares traditional past performance features with GPS derived race features and presents race scenarios in an interactive Dash app.

## Question

Do GPS telemetry features improve predictions of race outcomes beyond what past performance data already provides?

## Why it matters

Past performance records summarize what a horse has done, while GPS telemetry captures how it runs. If telemetry adds predictive information, it changes what analysts and handicappers should measure.

## Approach

The notebook builds past performance aggregates and horse level summaries of GPS telemetry. It compares win and top three Random Forest models using a chronological 80/20 split and reports ROC AUC, accuracy, and log loss. Horses without GPS history have missing GPS features, which the pipeline imputes. The final cell launches the dashboard at `http://127.0.0.1:8052`.

This is a demonstration, not betting advice. Results depend on the supplied data and do not guarantee future performance.

## What is included

- `gps_horse_race_simulator.ipynb`: feature engineering, model training and evaluation, scoring of upcoming races, and the Dash simulator.
- `css_block.txt` and `js_block.txt`: dashboard styling and interaction assets used by the notebook.
- `requirements.txt`: Python dependencies.

## Run locally

1. Use Python 3.10 or newer and create a virtual environment.
2. Install dependencies: `python -m pip install -r requirements.txt`
3. Place the authorized CSV inputs listed in [`data/README.md`](data/README.md) in `data/`.
4. Install Jupyter (`python -m pip install jupyter`), open `gps_horse_race_simulator.ipynb` from the repository root, and run the cells in order.

## Data handling

The race datasets, the competition brief, and saved notebook outputs are excluded because redistribution rights are not established. CSV files under `data/` are ignored by Git to prevent accidental publication.

## License

Source is shared for portfolio review. No open source license is granted.
