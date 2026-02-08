# AI Programming Foundations Project — Meteorite Workflow

## Project Description

This project builds a reproducible data workflow for cleaning, exploring, and visualizing meteorite landing records. The dataset is treated as a proxy for noisy aerospace observation logs, allowing structured data hygiene, anomaly handling, and exploratory analysis. The workflow demonstrates how raw scientific data can be transformed into a reliable analytical pipeline.

Dataset used: NASA Meteorite Landings Dataset  
https://www.kaggle.com/datasets/nasa/meteorite-landings

---

## What I Built

I created a complete data workflow that includes:

- Data ingestion from a raw CSV dataset
- Cleaning functions to remove corrupted and incomplete records
- Exploratory analysis using reusable functions
- Visualizations that reveal patterns in mass, time, classification, and detection bias
- A structured notebook that runs top-to-bottom reproducibly

The notebook is designed as a foundation for future machine learning and AI workflows.

---

## How to Run

### Install dependencies

    pip install -r requirements.txt

The requirements file was generated using:

    pip freeze > requirements.txt

### Run the notebook

1. Clone or download this repository
2. Open `data_workflow.ipynb` in Jupyter Notebook or Google Colab
3. Run all cells from top to bottom

The notebook executes without hidden state and reproduces the full workflow.

#### Optional (Google Colab only):
If running in Colab with Google Drive storage, uncomment the setup cell at the top of the notebook.

---

## Reproducibility

This project emphasizes reproducible data science:

- All transformations are defined in functions
- The notebook runs top-to-bottom without manual intervention
- A requirements file captures the software environment
- Git version control tracks workflow changes

Another user can recreate the environment and rerun the analysis using only the repository contents.

---

## Bias Awareness

Data cleaning decisions can introduce bias. Removing meteorites without coordinates improves spatial consistency, but it may disproportionately exclude regions where precise location data was never recorded. Similarly, filtering invalid years assumes corrupted timestamps rather than rare historical events.

These choices increase analytical reliability but may reduce representation of certain records. Future work could investigate imputation strategies or metadata recovery to reduce bias introduced by cleaning.

---

## Reflection: ML Workflow Changes

If this dataset were used in a machine learning workflow, additional preprocessing would be required:

- Feature scaling for mass and geographic variables
- Encoding meteorite classes
- Handling class imbalance
- Splitting data into training and validation sets

The current workflow prepares clean structured inputs suitable for downstream ML pipelines.

---

## Reflection: Neural Network Preparation

Neural networks require consistent numeric inputs. Before training a model:

- Categorical variables would need embedding or one-hot encoding
- Missing values would require imputation strategies
- Geographic coordinates could be transformed into engineered spatial features

The cleaning stage performed here is a prerequisite for stable neural network training.

---

## Reflection: Agentic Automation Potential

This workflow could be automated as part of an agentic AI system that continuously ingests scientific datasets, validates anomalies, and produces updated analytical reports. The modular function structure supports automation, monitoring, and future integration into intelligent data pipelines.

---

## Repository Structure

```
📂 data/
   └── meteorite-landings.csv
📓 data_workflow.ipynb
📄 requirements.txt
📘 README.md
```

---

This repository demonstrates a professional, reusable data workflow that serves as a foundation for machine learning, deep learning, and autonomous analytical systems.
