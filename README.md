# GlobalPath AI — Student University Recommendation System

> **Python for AI and Machine Learning — Microsoft & edX**  
> Final Year Project | Computer Science and Engineering  
> RTM Al-Kabir Technical University, Sylhet, Bangladesh

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com)
[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://python.org)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-orange.svg)](https://scikit-learn.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-In%20Progress-yellow.svg)]()

---

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Live Platform](#live-platform)
- [Features](#features)
- [Dataset](#dataset)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation and Setup](#installation-and-setup)
- [How to Run](#how-to-run)
- [Model Performance](#model-performance)
- [Results and Visualisations](#results-and-visualisations)
- [How to Use the Prediction Function](#how-to-use-the-prediction-function)
- [Course Information](#course-information)
- [Connected Project](#connected-project)
- [Author](#author)
- [Acknowledgements](#acknowledgements)

---

## Project Overview

**GlobalPath AI** is a machine learning-based university recommendation system developed as part of the **Microsoft Python for AI and Machine Learning** professional certificate program on **edX**.

The system uses supervised machine learning algorithms to predict the most suitable study destination for Bangladeshi students pursuing higher education abroad. By analysing a student's academic profile — including GPA, IELTS score, annual budget, and field of study — the model returns a ranked list of recommended countries with acceptance probability scores.

This notebook serves as the **AI backbone** of GlobalPath, a full study abroad consultancy platform currently under development as a Final Year Project at RTM Al-Kabir Technical University, Sylhet.

---

## Problem Statement

Every year, thousands of students in Bangladesh attempt to navigate the study abroad process with little to no structured guidance. The challenges they face include:

- Fragmented and unreliable information across multiple sources
- Expensive consultancy fees that are inaccessible to many students
- High margin for error — a single documentation mistake can delay admission by a full intake cycle
- No personalised, data-driven tool to match student profiles with suitable countries and universities

**GlobalPath AI addresses this by replacing guesswork with data-driven predictions built on real academic profiles.**

---

## Live Platform

The AI model developed in this notebook is connected to the GlobalPath web platform:

**Live Website:** [https://fyproteam.netlify.app](https://fyproteam.netlify.app)

The platform provides Bangladeshi students with:
- Step-by-step visa guidance for 8 countries
- University shortlisting based on academic profile
- Scholarship finder for CSE and engineering students
- Free consultation booking system
- Student journey dashboard

---

## Features

### Machine Learning Pipeline
- Complete end-to-end ML pipeline from raw data to prediction
- Two classification models with performance comparison
- Cross-validation for robust model evaluation
- Feature importance analysis

### Data Engineering
- Synthetic student dataset with 200 profiles
- Feature engineering and label encoding
- StandardScaler normalisation
- Stratified train-test split (80/20)

### Visualisations
- Student distribution by recommended country
- GPA distribution with mean indicator
- IELTS score distribution with mean indicator
- GPA vs IELTS scatter plot by country
- Budget range box plot by country
- Field of study pie chart
- Confusion matrices for both models
- Feature importance bar chart
- Model accuracy comparison chart

### Live Prediction
- Real-time country recommendation function
- Probability scores for all 8 countries
- Visual probability bar display

---

## Dataset

The dataset is synthetically generated to simulate real student profiles at GlobalPath.

| Feature | Type | Description |
|---|---|---|
| Student_ID | Integer | Unique student identifier |
| GPA | Float | Grade Point Average (2.0 — 4.0) |
| IELTS_Score | Float | IELTS band score (5.5 — 9.0) |
| Budget_USD | Integer | Annual budget in USD |
| Field | String | Field of study |
| Recommended_Country | String | Target study destination |

### Dataset Statistics

| Metric | Value |
|---|---|
| Total Records | 200 students |
| Features | 4 input features |
| Target Classes | 8 countries |
| Missing Values | None |
| Train Split | 160 samples (80%) |
| Test Split | 40 samples (20%) |

### Countries Covered

| Country | Region |
|---|---|
| United Kingdom | Europe |
| United States | North America |
| Canada | North America |
| Germany | Europe |
| Australia | Oceania |
| Netherlands | Europe |
| Sweden | Europe |
| France | Europe |

---

## Technology Stack

| Category | Technology | Version |
|---|---|---|
| Language | Python | 3.x |
| Data Manipulation | NumPy | Latest |
| Data Manipulation | Pandas | Latest |
| Machine Learning | Scikit-learn | Latest |
| Visualisation | Matplotlib | Latest |
| Visualisation | Seaborn | Latest |
| Environment | Google Colab | Cloud |
| Version Control | GitHub | — |

---

## Project Structure

```
globalpath-ai-recommendation/
│
├── CoPython_for_AI_and_Machine_Learning_GlobalPath.ipynb
│                           ← Main Jupyter notebook
│
├── README.md               ← This file
│
├── outputs/
│   ├── globalpath_analysis.png     ← Data analysis charts
│   ├── confusion_matrix.png        ← Model evaluation charts
│   ├── feature_importance.png      ← Feature importance chart
│   └── model_comparison.png        ← Accuracy comparison chart
│
└── LICENSE                 ← MIT License
```

---

## Installation and Setup

### Option A — Google Colab (Recommended)

No installation required. Open the notebook directly in Google Colab:

1. Click the **Open in Colab** badge at the top of this README
2. Sign in with your Google account
3. Click **Runtime → Run All**
4. All libraries install automatically

### Option B — Local Setup

If you prefer to run locally:

**Step 1 — Clone the repository**
```bash
git clone https://github.com/aminul-12/Aminul-12.git
cd Aminul-12
```

**Step 2 — Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate        # Mac / Linux
venv\Scripts\activate           # Windows
```

**Step 3 — Install dependencies**
```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

**Step 4 — Launch Jupyter Notebook**
```bash
jupyter notebook
```

**Step 5 — Open the notebook**
```
CoPython_for_AI_and_Machine_Learning_GlobalPath.ipynb
```

---

## How to Run

The notebook is divided into 10 sequential cells. Run them in order:

| Cell | Title | Description |
|---|---|---|
| 1 | Install and Import Libraries | Installs and imports all required packages |
| 2 | Create Student Dataset | Generates 200-student synthetic dataset |
| 3 | Data Exploration | Summary statistics and distribution analysis |
| 4 | Data Visualisation | 6 analytical charts |
| 5 | Data Preprocessing | Encoding, scaling, and train-test split |
| 6 | Model Training | Trains Random Forest and KNN models |
| 7 | Model Evaluation | Confusion matrices and classification report |
| 8 | Feature Importance | Identifies key prediction drivers |
| 9 | Live Prediction | Real-time student recommendation function |
| 10 | Accuracy Comparison | Side-by-side model performance chart |

**To run all cells at once:**
```
Runtime → Run All   (Google Colab)
Kernel  → Run All   (Jupyter Notebook)
```

---

## Model Performance

Two classification models were trained and evaluated:

### Random Forest Classifier

| Metric | Value |
|---|---|
| Algorithm | Ensemble — 100 decision trees |
| Max Depth | 10 |
| Test Accuracy | ~85% |
| Cross-Val Accuracy | ~83% |
| Random State | 42 |

### K-Nearest Neighbours

| Metric | Value |
|---|---|
| Algorithm | Instance-based learning |
| K Neighbours | 5 |
| Test Accuracy | ~78% |
| Cross-Val Accuracy | ~76% |

### Comparison Summary

| Model | Test Accuracy | Cross-Val | Verdict |
|---|---|---|---|
| Random Forest | ~85% | ~83% | Best Model |
| KNN | ~78% | ~76% | Baseline |

> **Note:** Exact accuracy values may vary slightly due to the synthetic nature of the dataset. Run Cell 6 to see your actual results.

---

## Results and Visualisations

The notebook generates the following output charts automatically:

**1. globalpath_analysis.png**
Six-panel data analysis dashboard showing country distribution, GPA histogram, IELTS distribution, GPA vs IELTS scatter, budget box plot, and field of study pie chart.

**2. confusion_matrix.png**
Side-by-side confusion matrices for Random Forest (blue) and KNN (orange) showing prediction accuracy per country.

**3. feature_importance.png**
Bar chart ranking all four features by their contribution to the country recommendation decision.

**4. model_comparison.png**
Grouped bar chart comparing test accuracy and cross-validation accuracy for both models.

All charts use the GlobalPath dark theme — matching the live platform's design system.

---

## How to Use the Prediction Function

The `predict_country()` function in Cell 9 accepts any student profile and returns a ranked recommendation.

### Function Signature

```python
predict_country(
    gpa        = 3.75,   # Float: 0.0 to 4.0
    ielts      = 7.0,    # Float: 0.0 to 9.0
    budget_usd = 25000,  # Integer: Annual budget in USD
    field      = 'Computer Science'
    # Options: 'Computer Science', 'Engineering',
    #          'Business', 'Data Science'
)
```

### Example Usage

```python
# Example 1 — High achieving CSE student
predict_country(
    gpa        = 3.90,
    ielts      = 7.5,
    budget_usd = 35000,
    field      = 'Computer Science'
)

# Example 2 — Mid-range Engineering student
predict_country(
    gpa        = 3.20,
    ielts      = 6.5,
    budget_usd = 20000,
    field      = 'Engineering'
)

# Example 3 — Budget-conscious Data Science student
predict_country(
    gpa        = 3.50,
    ielts      = 7.0,
    budget_usd = 12000,
    field      = 'Data Science'
)
```

### Example Output

```
=== GLOBALPATH STUDENT RECOMMENDATION ===
  GPA          : 3.75
  IELTS Score  : 7.0
  Budget       : $25,000 USD/year
  Field        : Computer Science

  Recommended Country : UK

  All Country Probabilities:
  UK              ##############################   42.0%
  Canada          ####################             28.0%
  Germany         ###########                      15.0%
  Australia       ######                           8.0%
  USA             ###                              4.0%
  Netherlands     ##                               2.0%
  Sweden          #                                1.0%
  France                                           0.0%
```

---

## Course Information

| Detail | Information |
|---|---|
| Course Name | Python for AI and Machine Learning |
| Issuing Organisation | Microsoft |
| Platform | edX |
| Credential Type | Professional Certificate |
| Status | In Progress |
| Topics Covered | Python, NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn, Deep Learning Foundations |

---

## Connected Project

This notebook is the AI component of **GlobalPath** — a full study abroad consultancy platform for Bangladeshi students.

| Detail | Link |
|---|---|
| Live Platform | https://fyproteam.netlify.app |
| Institution | RTM Al-Kabir Technical University, Sylhet |
| Degree | BSc Computer Science and Engineering |
| Expected Completion | June 2026 |

**GlobalPath Platform Features:**
- Visa Help Center — 8 countries
- University Matching Engine
- Scholarship Finder
- AI Study Assistant
- Appointment Booking System
- Student Journey Dashboard

---

## Author

Aminul Islam 
BSc Computer Science and Engineering  
RTM Al-Kabir Technical University, Sylhet, Bangladesh  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue.svg)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black.svg)](https://github.com/aminul-12)

---

## Acknowledgements

- **Microsoft and edX** — for the Python for AI and Machine Learning professional certificate program
- **Scikit-learn** — for the machine learning algorithms and evaluation tools
- **GlobalPath FYP Team** — for the collaborative final year project
- **RTM Al-Kabir Technical University** — for academic support and guidance

---

## License

This project is licensed under the MIT License.  
You are free to use, modify, and distribute this code with attribution.

---

*GlobalPath AI — Built for Bangladeshi students, powered by machine learning.*  
*Microsoft Python for AI and ML — edX | RTM Al-Kabir Technical University, Sylhet*
