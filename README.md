# Lagrangian India

This repository contains the scripts that perform all the data processing for the paper titled: “Influence of fires on air-quality in six major Indian cities using a Lagrangian framework.” The Lagrangian framework scripts can be found in the data availability statement of: https://doi.org/10.1016/j.scitotenv.2023.167350. The scripts included here reproduce all diagnostics and analyses used in the study, including plume detection, pollutant composites, and model validation against observations.

## Main scripts
### Lagrangian_India.ipynb
This notebook implements the Lagrangian plume identification framework used to detect and track pollution plumes associated with biomass burning. The method applies threshold-based segmentation and connected-component labeling to gridded atmospheric composition data (PM$_{2.5}$, PM$_{10}$, and CO) to identify coherent pollution structures. Using spatial filtering and morphological operations, the algorithm isolates plume-like objects and allows their evolution to be analyzed across time. The script produces the labeled plume datasets that are later used to construct composite plume maps and quantify the transport of fire-related pollution toward major Indian cities.

### Validate_CAMS_and_baseline.ipynb
This notebook evaluates the performance of the CAMS atmospheric composition data used in the study. It compares model-derived pollutant concentrations with ground-based observations from monitoring stations in six major Indian cities (Bengaluru, Chennai, Delhi, Hyderabad, Kolkata, and Mumbai). The script computes a suite of statistical performance metrics (e.g., normalized mean bias, RMSE, correlation coefficient, FAC2, index of agreement) and assesses the ability of the dataset to reproduce observed pollution variability. Additionally, it constructs baseline pollution estimates and diagnostic plots that are used to evaluate model performance and support the interpretation of the Lagrangian plume analysis.
