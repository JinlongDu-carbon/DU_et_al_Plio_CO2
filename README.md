# DU_et_al_Plio_CO2

Plotting-ready data and a notebook for the main-text and supplementary manuscript figures.

## Contents

- `plotting.ipynb`: loads the bundled data and generates all 25 figure outputs.
- `*.nc`: 22 NetCDF files with variable names, units, coordinates and projection information.
- `curves.xlsx`: 11 sheets of curve data, with units in the column headers.
- `plottings/`: 25 exported SVGs, including Fig3a and the red–blue FigS4 maps.
- `README.txt`: detailed data conventions, units and figure coverage.
- `requirements.txt`: Python packages used by the notebook and JupyterLab.

## Run the notebook

The notebook was verified with Python 3.10. Start JupyterLab from the repository
directory so that its working directory contains `curves.xlsx` and the NetCDF files.

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab plotting.ipynb
```

Run all cells in order. No original model-output files are required. The notebook
uses Arial; installing that font preserves the intended typography.

## SVG export

The setup cell contains:

```python
EXPORT_SVG = True
PLOTTING_DIR = DATA_DIR / 'plottings'
```

Set `EXPORT_SVG = False` to display figures without writing image files. With export
enabled, re-running replaces the corresponding SVGs in `plottings/`. Text remains
editable, and existing multi-panel layouts stay together. Fig1a, Fig1c and Fig1d
are exported together as `Fig1a_1c_1d.svg`.

Figure S1 is excluded. Figure S2 has no plotting block in this collection. Other
figure numbers are retained.
