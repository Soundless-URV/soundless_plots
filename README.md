# Soundless Plots

This repository contains three Jupyter Notebooks that work together to process raw data and produce insightful visualizations about noise levels and train schedules.

## Notebooks

### 1. [process_data.ipynb](process_data.ipynb)

**Objective:**  
Read all the raw data from the dataset, perform the necessary calculations, and store the final results in a file called `data.pkl`.

**Key Steps:**
- Data extraction and filtering.
- Calculation of metrics (e.g., average dB levels, heart rate metrics, sleep incidents).
- Saving the processed data for plotting.

### 2. [plot_data.ipynb](plot_data.ipynb)

**Objective:**  
Read the processed data from `data.pkl` and generate the corresponding plots.

**Key Steps:**
- Loading the processed data.
- Generating visualizations for noise levels, heart rate and sleep data during different scenarios.
- Customized plotting using matplotlib.

### 3. [adif_data.ipynb](adif_data.ipynb)

**Objective:**  
Analyze and detect the hours when the most trains depart from Tarragona's port.

**Key Steps:**
- Reading and preprocessing Adif train schedule data.
- Filtering data to focus on trains departing to Tarragona.
- Plotting the number of trains by the hour.

## Data

The data used in these notebooks is stored in the `./soundless/data/` and `./soundless/history/` directories. The datasets include measurements of noise levels, heart rate, sleep stages, and train schedules.

## Usage

To run the notebooks, you need to have Jupyter Notebook installed along with the required Python packages. You can install the dependencies with: