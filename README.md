Star Classification Using Machine Learning
Overview
This project uses machine learning techniques to classify stellar objects (stars, galaxies, and quasars) based on their features. The dataset used in this project is sourced from the Sloan Digital Sky Survey (SDSS), containing observations of 100,000 celestial objects. It aims to demonstrate feature analysis, data preprocessing, and building predictive models using Random Forests and Neural Networks.

Dataset Description
The dataset includes 100,000 entries, with each representing a celestial object. Each entry consists of 18 features and a target class. The key features are:

alpha: Right ascension angle of the object.
delta: Declination angle of the object.
u, g, r, i, z: Brightness in different wavelength filters.
redshift: A measure of the object's distance and recessional velocity.
Target Classes
GALAXY: A gravitationally bound system of stars, gas, and dark matter.
QSO: Quasi-stellar objects, extremely luminous active galactic nuclei.
STAR: Spheroidal plasma undergoing nuclear fusion.
Project Steps
Data Exploration

Visualization of feature distributions to understand the dataset better.
Identified important features using feature ranking.
Data Preprocessing

Encoded the target labels (GALAXY, QSO, STAR).
Dropped irrelevant columns (e.g., IDs and other non-predictive metadata).
Scaled numerical features for efficient model training.
Feature Importance Analysis

Used Random Forests to rank features based on their importance.
Selected the top 10 most important features for further model training.
Model Training and Evaluation

Trained a Neural Network with the top 10 features.
Evaluated the model using accuracy, confusion matrix, and classification reports.
Installation and Usage
Prerequisites
Python 3.8 or later
Required libraries:
pandas
numpy
matplotlib
scikit-learn
tensorflow
Installation
Clone the repository:
bash
Copy code
git clone https://github.com/Unmel5/Star_Classification.git
Navigate to the project directory:
bash
Copy code
cd Star_Classification
Install the dependencies:
bash
Copy code
pip install -r requirements.txt
Usage
Run the script to train and evaluate the model:

bash
Copy code
python star_classification.py
Results
Feature Importance
The top features contributing to the classification were:

redshift
i (Near-infrared brightness)
r (Red brightness)
g (Green brightness)
Model Performance

Neural Network Accuracy: ~98%
Detailed classification metrics and confusion matrix are displayed in the output.
Visualizations
Feature Distributions
The dataset feature distributions, as shown in the histograms, highlight:

The sky coordinates (alpha, delta) are spread uniformly.
Most objects have low brightness (u, g, r, i, z).
The redshift feature indicates most objects are close to Earth.
Feature Importance

Contributions
Feel free to fork the repository and submit pull requests for improvements or additional features.

