# Lead Scoring Case Study

## Project Overview

This project develops a logistic regression-based lead scoring model to predict the probability of lead conversion and support data-driven lead prioritisation.

The analysis follows an end-to-end predictive modelling workflow, covering exploratory data analysis, data preparation, feature selection, model development, evaluation and probability-based scoring.

## Business Objective

The objective is to identify leads with a higher likelihood of conversion so that sales teams can prioritise their efforts more effectively.

Rather than treating all leads equally, the model assigns a probability of conversion that can be used to support lead segmentation and prioritisation.

## Analytical Approach

The project covers:

- Exploratory Data Analysis (EDA)
- Data cleaning and preparation
- Feature selection
- Logistic regression model development
- Model evaluation
- Probability-based lead scoring
- Interpretation of model outputs for business decision-making

## Key Analytical Concepts

The analysis demonstrates the application of:

- Logistic Regression
- Binary classification
- Feature selection
- Model evaluation
- Probability estimation
- Lead prioritisation

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Repository Contents

`lead-scoring-case-study.ipynb` — Complete analysis and modelling workflow.

`requirements.txt` — Python dependencies required to reproduce the analysis.

## Business Value

The resulting lead scores can support a more targeted sales strategy by helping organisations distinguish between higher- and lower-probability leads and allocate sales effort accordingly.

## Analytical Approach

The project follows an end-to-end predictive modelling workflow:

1. Exploratory Data Analysis
2. Data Preparation
3. Feature Selection
4. Multicollinearity Assessment
5. Logistic Regression Model Development
6. Model Evaluation
7. Probability-Based Lead Scoring

### Exploratory Data Analysis

The dataset was examined to understand lead characteristics, acquisition channels,
behavioural activity and their relationship with lead conversion.

Key variables included:

- Lead origin and lead source
- Last activity and last notable activity
- Total visits
- Total time spent on the website
- Page views per visit
- Specialization
- Lead engagement and behavioural attributes

### Feature Selection

Candidate predictors were assessed using exploratory analysis and correlation
analysis to identify variables relevant to lead conversion while avoiding
unnecessary redundancy.

### Model Development

A logistic regression model was developed to estimate the probability that an
individual lead would convert.

The model output is a conversion probability rather than simply a binary
classification, allowing leads to be prioritised according to their predicted
likelihood of conversion.

### Model Evaluation

Model performance was evaluated using the Receiver Operating Characteristic
(ROC) curve and the Area Under the Curve (ROC-AUC).

The model achieved a ROC-AUC of **0.86**, indicating good ability to distinguish
between converting and non-converting leads.

![ROC Curve](Visualization/ROC%20Curve.jpg)

## Probability Threshold Analysis

The predicted probabilities were evaluated across different classification
thresholds to examine the trade-off between accuracy, sensitivity and
specificity.

This provides a practical basis for selecting a probability threshold according
to the business objective and the relative cost of missed versus incorrectly
prioritised leads.

![Threshold Analysis](Visualization/Threshold%20Analysis.jpg)

## Business Insights

The analysis indicates that lead conversion is not evenly distributed across
lead acquisition channels and engagement behaviours.

### Lead Origin

Lead origin shows meaningful differences in conversion behaviour. In particular,
leads originating through the lead add form show a substantially higher
conversion proportion than the larger-volume acquisition channels.

![Lead Origin vs Conversion](Visualization/Lead%20Origin%20Vs%20Conversion.jpg)

### Lead Source

Conversion behaviour also varies across lead sources. While high-volume sources
generate a large number of leads, some lower-volume sources show comparatively
stronger conversion performance.

This highlights an important distinction between **lead volume and lead quality**:
the channel generating the most leads is not necessarily the channel generating
the highest proportion of conversions.

![Lead Source vs Conversion](Visualization/Lead%20Source%20Vs%20Conversion.jpg)

### Lead Prioritisation

The logistic regression model converts the available lead attributes into a
predicted probability of conversion. These probabilities can be used to rank
leads and help sales teams focus attention on leads with higher predicted
conversion likelihood.

## Key Results

- **Model:** Logistic Regression
- **Evaluation metric:** ROC-AUC
- **ROC-AUC:** **0.86**
- **Primary application:** Probability-based lead prioritisation
- **Key analytical areas:** Lead source, lead origin and behavioural engagement
- **Decision mechanism:** Conversion probability and classification threshold

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Repository Structure

```text
Lead-Scoring-Case-Study/
│
├── lead-scoring-case-study.ipynb
├── README.md
├── requirements.txt
│
└── Visualization/
    ├── Heatmap.jpg
    ├── Lead Origin Vs Conversion.jpg
    ├── Lead Source Vs Conversion.jpg
    ├── Outlier Detection.jpg
    ├── Pair Plots.jpg
    ├── ROC Curve.jpg
    └── Threshold Analysis.jpg

## Disclaimer

This project is presented as an analytical case study demonstrating the application of predictive modelling techniques to a lead-scoring problem.
