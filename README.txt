Open plotting.ipynb from this folder and run all cells in order.

Dependencies: NumPy, pandas, openpyxl, SciPy, xarray, Matplotlib, Basemap and cmocean.
Arial is used for figure text. EXPORT_SVG = True in the setup cell displays
the figures and exports SVGs to ./plottings. Set it to False to display only.
PLOTTING_DIR controls the output folder. Re-running with export enabled
replaces the corresponding SVGs in that folder. Text remains editable.
There are 25 SVG outputs, named by figure heading. Existing multi-panel
layouts remain together; Fig1a, Fig1c and Fig1d use Fig1a_1c_1d.svg.
SVG files omit creator and date metadata.
All files contain plotting-ready values.

The 22 NetCDF files have descriptive variable names, long_name and units attributes,
and named coordinate dimensions. Projection definitions and geographic coordinates
are included for projected maps. Depth coordinates retain the plotting convention;
the positive attribute states their direction. Transect coordinates describe the
Atlantic-Pacific layout and include geographic latitude and basin information.
NaN denotes masked or missing values. Ocean masks identify valid and invalid cells.
Letter prefixes identify panels within a figure.

The Excel workbook contains 11 sheets, one per retained curve panel, with units in
each column header. Blank cells denote missing values or unused rows of shorter
series. 


