# 🎬  Predicting Movie Rental Durations (Regression)

## 📌 Project Overview

A DVD rental company wants to improve **inventory planning** by predicting how long customers will keep rented DVDs. Using historical rental data, this project builds and evaluates **regression models** to predict the **number of days a DVD is rented**.

The business requirement is clear:

> ✅ **The selected model must achieve a Mean Squared Error (MSE) of 3 or less on the test set.**

The final model helps the company reduce inventory shortages, avoid overstocking, and plan rentals more efficiently.

---

## 🎯 Objective

* Predict **`rental_length_days`** for each rental transaction.
* Train and compare multiple regression models.
* Select a model that achieves **MSE ≤ 3** on unseen data.

---

## 📂 Dataset

**File:** `rental_info.csv`
Each row represents a single DVD rental transaction.

### 🎯 Target Variable

* **`rental_length_days`**
  Number of days between `rental_date` and `return_date`.

---

## 🧾 Feature Description

| Feature                     | Description                                              |
| --------------------------- | -------------------------------------------------------- |
| `rental_date`               | Date and time the DVD was rented                         |
| `return_date`               | Date and time the DVD was returned                       |
| `amount`                    | Amount paid by the customer                              |
| `amount_2`                  | Square of `amount`                                       |
| `rental_rate`               | Rental rate of the DVD                                   |
| `rental_rate_2`             | Square of `rental_rate`                                  |
| `release_year`              | Year the movie was released                              |
| `length`                    | Length of the movie (in minutes)                         |
| `length_2`                  | Square of `length`                                       |
| `replacement_cost`          | Cost to replace the DVD                                  |
| `special_features`          | Additional DVD features (e.g., trailers, deleted scenes) |
| `NC-17`, `PG`, `PG-13`, `R` | Dummy variables representing movie ratings               |

📌 **Notes**

* One rating category has already been dropped to avoid multicollinearity.
* Squared features are included to capture **non-linear relationships**.

---

## 🛠️ Project Workflow

1. **Data Loading & Exploration**

   * Inspect dataset structure and distributions
   * Parse date-time features

2. **Feature Engineering**

   * Compute `rental_length_days` from rental and return dates
   * Prepare numerical and categorical features

3. **Train–Test Split**

   * Split data into training and test sets to ensure unbiased evaluation

4. **Modeling**

   * Train and evaluate multiple regression models
   * Compare baseline and more advanced approaches

5. **Evaluation & Selection**

   * Evaluate models using **Mean Squared Error (MSE)**
   * Select the best-performing model based on test performance

---

✅ **Target Performance:**

* Test set **MSE ≤ 3**

---

## 🚀 Results

The final model meets the company’s performance requirement and can be used to:

* Predict rental durations accurately
* Improve DVD inventory planning
* Reduce operational inefficiencies

Detailed model comparisons and evaluation results are available in the notebook.

---

## 🧠 Key Insights

* Time-based feature engineering is critical for predicting rental behavior.
* Non-linear models benefit from squared features already present in the dataset.
* Careful model evaluation ensures business-aligned performance.

---

## 📦 Tech Stack

* **Python 3**
* **pandas**
* **NumPy**
* **scikit-learn**
* **Matplotlib / Seaborn** (visualization)

Developed as a machine learning regression project focused on solving a real-world business problem.

