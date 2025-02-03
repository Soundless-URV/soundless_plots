# Soundless Plots

This repository contains a series of Jupyter Notebooks for analyzing and visualizing data related to noise levels and their impact on sleep. The analysis is based on data collected from various sources, focusing on different aspects such as average noise levels, incidents during sleep, and the number of trains passing through Tarragona's port.

## Notebooks

### 1. awakenings.ipynb

**Objective:** Analyze the number of awakenings during the night and their correlation with noise levels.

- **Functions:**
  - `remove_initial_neg(df: pd.DataFrame) -> pd.DataFrame`: Removes initial negative sleep stages.
  - `read_data(files_name: list[str]) -> pd.DataFrame`: Reads and processes data files.
  - `incidents_sleep(sleepStage: list[int]) -> list[int]`: Detects sleep incidents.
  - `get_timestamps_incident(signals: list[int], timestamps: list[int]) -> list[int]`: Gets timestamps of sleep incidents.

- **Key Steps:**
  - Data filtering and preprocessing.
  - Calculation of mean dB values for noisy and quiet nights.
  - Detection and plotting of sleep incidents.

### 2. mean_dB.ipynb

**Objective:** Show the average dB value of the dataset, both when the user is confirmed to be sleeping and when the user is not.

- **Functions:**
  - `remove_initial_neg(df: pd.DataFrame) -> pd.DataFrame`: Removes initial negative sleep stages.
  - `read_data(files_name: list[str]) -> pd.DataFrame`: Reads and processes data files.

- **Key Steps:**
  - Data filtering and preprocessing.
  - Calculation of average dB values.
  - Plotting of average dB levels with bar and line plots.

### 3. nights_with_ilegal_levels.ipynb

**Objective:** Show the number of nights where the noise levels exceed the legal limits set by the WHO (40 dB) during sleep.

- **Functions:**
  - `remove_initial_neg(df: pd.DataFrame) -> pd.DataFrame`: Removes initial negative sleep stages.
  - `read_data(files_name: list[str]) -> pd.DataFrame`: Reads and processes data files.
  - `calculate_recording_duration(df)`: Calculates total and average recording durations.
  - `incidents_sleep(sleepStage: list[int]) -> list[int]`: Detects sleep incidents.
  - `get_timestamps_incident(signals: list[int], timestamps: list[int]) -> list[int]`: Gets timestamps of sleep incidents.

- **Key Steps:**
  - Data filtering and preprocessing.
  - Calculation of nights with noise levels above 40 dB.
  - Plotting the distribution of nights by sound level.

### 4. noisy_quiet_dB_and_hR_levels.ipynb

**Objective:** Compare the differences between quiet and noisy nights in terms of average noise levels and heart rate levels.

- **Functions:**
  - `remove_initial_neg(df: pd.DataFrame) -> pd.DataFrame`: Removes initial negative sleep stages.
  - `read_data(files_name: list[str]) -> pd.DataFrame`: Reads and processes data files.

- **Key Steps:**
  - Data filtering and preprocessing.
  - Calculation of mean dB and heart rate values for noisy and quiet nights.
  - Plotting the differences between noisy and quiet nights.

### 5. number_trains.ipynb

**Objective:** Analyze and detect the hours when the most trains depart from Tarragona's port.

- **Key Steps:**
  - Reading and preprocessing Adif data.
  - Filtering data for trains departing to Tarragona.
  - Plotting the number of trains by hour.

## Data

The data used in these notebooks is stored in the `./soundless-data/` and `./soundless-history/` directories. The data includes noise levels, heart rate, sleep stages, and train schedules.

## Usage

To run the notebooks, you need to have Jupyter Notebook installed. You can install the required Python packages using the following command:

```sh
pip install pandas matplotlib numpy