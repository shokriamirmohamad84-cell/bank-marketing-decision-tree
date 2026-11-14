# Bank Marketing Subscription Prediction – Decision Tree

## Project Overview

This project uses a **Decision Tree Classifier** to predict whether a bank customer will subscribe to a term deposit based on their personal information and marketing campaign data.

The model is implemented using Python and Scikit-learn.

## Dataset

The dataset is obtained from the **UCI Machine Learning Repository**.

- **Dataset:** Bank Marketing
- **Dataset ID:** 222
- **Total Records:** 45,211
- **Input Features:** 16
- **Target Variable:** `y`

### Target Variable

The target variable `y` indicates whether a customer subscribed to a term deposit:

- `yes`: Customer subscribed.
- `no`: Customer did not subscribe.

## Technologies & Libraries

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- UCI Machine Learning Repository (`ucimlrepo`)

## Project Workflow

The project follows these steps:

1. Import required libraries.
2. Load the Bank Marketing dataset.
3. Explore and select input features.
4. Handle missing categorical values.
5. Encode categorical features using LabelEncoder.
6. Encode the target variable.
7. Split the dataset into training and testing sets.
8. Build and train the Decision Tree model.
9. Make predictions on test data.
10. Evaluate model accuracy.
11. Visualize and save the decision tree.

## Data Preprocessing

Categorical variables are converted into numerical values using `LabelEncoder`.

Missing values in selected categorical columns are replaced with a separate `missing` category.

The target variable is encoded as:

| Original Value | Encoded Value |
|---|---:|
| no | 0 |
| yes | 1 |

## Model Configuration

The project uses Scikit-learn's `DecisionTreeClassifier`.

| Parameter | Value |
|---|---|
| Algorithm | Decision Tree |
| Criterion | Entropy |
| Maximum Depth | 4 |
| Test Size | 30% |
| Training Size | 70% |
| Random State | 3 |

The model uses Entropy to evaluate potential splits and identify informative decision rules.

## Model Evaluation

Model performance is evaluated using **Accuracy Score**.

The accuracy score measures the proportion of correct predictions on the testing dataset.

## Decision Tree Visualization

The trained model is visualized using Matplotlib and Scikit-learn's `plot_tree()` function.

The visualization displays:
- Decision rules
- Feature names
- Entropy values
- Number of samples in each node
- Predicted classes

The generated visualization is saved as:

`Decision_Tree.png`

## Project Structure

```text
Bank-Marketing-Decision-Tree/
│
├── Bank-Marketing-Decision-Tree.ipynb
├── Decision_Tree.png
└── README.md
```

## Installation

Install the required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib ucimlrepo
```

## How to Run

1. Clone or download this repository.
2. Install the required libraries.
3. Open the Jupyter Notebook.
4. Run the notebook cells in order.
5. View the model evaluation results and decision tree visualization.

## Limitations & Future Improvements

- Experiment with different maximum tree depths.
- Compare Entropy and Gini splitting criteria.
- Evaluate the model using Precision, Recall, F1-score, and Confusion Matrix.
- Improve categorical feature encoding using OneHotEncoder.
- Use a preprocessing Pipeline to avoid data leakage.
- Apply stratified train-test splitting.

**Important:** The current model includes the `duration` feature. UCI notes that call duration is only known after the call, so it should be excluded when building a model intended to predict subscription before a marketing call takes place.

## Dataset Reference

Moro, S., Rita, P., & Cortez, P. (2014).

*Bank Marketing Dataset.*

UCI Machine Learning Repository.

DOI: `10.24432/C5K306`

## Disclaimer

This project is developed for educational purposes to practice data preprocessing, classification, model evaluation, and machine learning visualization.
