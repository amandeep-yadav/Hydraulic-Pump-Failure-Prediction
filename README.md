# Hydraulic-Pump-Failure-Prediction

## Overview
This project focuses on predictive maintenance for a hydraulic system using data-driven approaches. Predictive maintenance aims to predict equipment failures before they occur, minimizing downtime and repair costs. This notebook explores various machine learning techniques to analyze and predict potential failures in hydraulic systems.

## Features
- Data preprocessing and feature engineering.
- Exploratory Data Analysis (EDA) to understand trends and relationships.
- Machine learning model development and evaluation for failure prediction.
- Visualization of model performance and insights.
- Deployment-ready predictive maintenance workflow.

## Dataset
Data Type: Multivariate, Time-Series
Task: Classification, Regression
Attribute Type: Categorical, Real
Area: CS/Engineering
Format Type: Matrix
Does your data set contain missing values? No

Number of Instances: 2205

Number of Attributes: 43680 (8x60 (1 Hz) + 2x600 (10 Hz) + 7x6000 (100 Hz))

Relevant Information:
The data set was experimentally obtained with a hydraulic test rig. This test rig consists of a primary working and a secondary cooling-filtration circuit which are connected via the oil tank [1], [2]. The system cyclically repeats constant load cycles (duration 60 seconds) and measures process values such as pressures, volume flows and temperatures while the condition of four hydraulic components (cooler, valve, pump and accumulator) is quantitatively varied. 

Attribute Information:
The data set contains raw process sensor data (i.e. without feature extraction) which are structured as matrices (tab-delimited) with the rows representing the cycles and the columns the data points within a cycle. The sensors involved are:
Sensor		Physical quantity		Unit		Sampling rate
PS1		Pressure			bar		100 Hz
PS2		Pressure			bar		100 Hz
PS3		Pressure			bar		100 Hz
PS4		Pressure			bar		100 Hz
PS5		Pressure			bar		100 Hz
PS6		Pressure			bar		100 Hz
EPS1		Motor power			W		100 Hz
FS1		Volume flow			l/min		10 Hz
FS2		Volume flow			l/min		10 Hz
TS1		Temperature			C		1 Hz
TS2		Temperature			C		1 Hz
TS3		Temperature			C		1 Hz
TS4		Temperature			C		1 Hz
VS1		Vibration			mm/s		1 Hz
CE		Cooling efficiency (virtual)	%		1 Hz
CP		Cooling power (virtual)		kW		1 Hz
SE		Efficiency factor		%		1 Hz

The target condition values are cycle-wise annotated in �profile.txt� (tab-delimited). As before, the row number represents the cycle number. The columns are

1: Cooler condition / %:
	3: close to total failure
	20: reduced effifiency
	100: full efficiency

2: Valve condition / %:
	100: optimal switching behavior
	90: small lag
	80: severe lag
	73: close to total failure

3: Internal pump leakage:
	0: no leakage
	1: weak leakage
	2: severe leakage

4: Hydraulic accumulator / bar:
	130: optimal pressure
	115: slightly reduced pressure
	100: severely reduced pressure
	90: close to total failure

5: stable flag:
	0: conditions were stable
	1: static conditions might not have been reached yet

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/amandeep-yadav/predictive-maintenance-hydraulic-system.git
   ```
2. Navigate to the project directory:
   ```bash
   cd predictive-maintenance-hydraulic-system
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Prerequisites
- Python 3.7 or above.
- Jupyter Notebook.
- Libraries used include:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn
  - xgboost
  - tensorflow/keras (if deep learning is used)

## Usage
1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook predictive-maintenance-of-hydraulic-system.ipynb
   ```
2. Follow the steps in the notebook to:
   - Preprocess the data.
   - Train machine learning models.
   - Evaluate performance metrics.
   - Visualize results.
3. Modify parameters or add new features as needed for experimentation.

## Results
- Detailed analysis of hydraulic system failures.
- Evaluation metrics such as accuracy, precision, recall, and F1-score for the predictive models.
- Visualizations showcasing the model's predictive capabilities.

## Folder Structure
```
├── data/                   # Dataset files
├── notebooks/              # Jupyter notebooks
├── models/                 # Saved models (if applicable)
├── results/                # Output results and plots
├── src/                    # Source code for preprocessing and model development
├── requirements.txt        # List of required dependencies
├── README.md               # Project documentation
```

## Contributing
Contributions are welcome! If you'd like to contribute, please fork the repository and submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- The dataset providers for making this project possible.
- Open-source libraries and tools used in the project.

## Author
**Amandeep Yadav**

For any questions or feedback, feel free to contact me or open an issue in the repository.

