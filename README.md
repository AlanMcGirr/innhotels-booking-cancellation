# innhotels-booking-cancellation
Predicting hotel booking cancellations using logistic regression and decision trees. Includes EDA, pruning techniques, and business insights for INN Hotels.
# INN Hotels: Booking Cancellation Prediction
 Hotel Booking Cancellation Predictor

**Live Demo**: [Try it here](https://claude.ai/public/artifacts/5a173a58-6ea9-41e2-bd03-602988cc8834)

This project predicts the probability of a hotel booking being canceled, along with confidence scores and actionable recommendations.
## Project Overview
This project focuses on predicting hotel booking cancellations using supervised learning techniques. By analyzing booking-related data, we aim to identify key factors that influence cancellations and recommend actionable strategies to reduce them.

---

## Dataset
The dataset was provided as part of the **INN Hotels case study** in the UT DSBA program.

- **Target Variable:** `booking_status` (0 = Not Canceled, 1 = Canceled)
- **Features:** Guest details, booking preferences, room types, price, lead time, etc.
- **Size:** ~36,000 rows

---

## Solution Approach

### Exploratory Data Analysis (EDA)
- Outlier detection and removal
- Class imbalance observation
- Feature transformation and engineering

### Modeling Techniques
- **Logistic Regression**
  - Evaluated using ROC-AUC, F1, and confusion matrix
  - Checked for multicollinearity using VIF
- **Decision Tree Classifier**
  - Unpruned, pre-pruned (hyperparameter tuning), and post-pruned (cost complexity pruning)
  - Compared performance using F1 and recall

### ⚙️ Evaluation Metrics
- Accuracy
- Recall (important for capturing cancellations)
- Precision
- F1 Score

---

## Key Results

| Model            | F1 Score (Test) | Recall (Test) | Accuracy (Test) |
|------------------|----------------|---------------|-----------------|
| Logistic Regression | 79.6%         | 81%           | 86.5%           |
| Decision Tree (Post-Pruned) | 79.5%     | 81%           | 86.5%           |

- **Selected Model:** Post-Pruned Decision Tree
- **Why:** Simple, interpretable, similar performance, and easier to deploy

---

## Business Recommendations
- Offer incentives for high lead-time bookings to reduce cancellations
- Focus on bookings with special requests — these tend to cancel less
- Reconsider pricing strategies for `Room_Type 1` and specific meal plans

---

## Repository Structure
📁 notebooks/ — Contains the main Jupyter notebook with full code, EDA, model building, and results
📁 presentation/ — Final presentation PDF and slides
📄 README.md — This file
---

## How to Run This Project

1. Clone or download the repository.
2. Navigate to the `notebooks/` folder and open the Jupyter Notebook.
3. Run the cells sequentially from top to bottom.
4. (Optional) Install required packages using `pip install -r requirements.txt`.

---

## Acknowledgements

This project was completed as part of the **University of Texas - Data Science & Business Analytics** program in partnership with **Great Learning**.

Gratitude to instructors, reviewers, and study peers for feedback and support throughout the project.

---

## License

This project is licensed under the [Apache License 2.0](LICENSE).
