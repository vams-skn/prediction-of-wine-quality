# Prediction of Wine Quality
This project aims to predict the quality of white wine based on its **chemical properties** such as alcohol content, acidity levels, and pH. The model helps winemakers and consumers make informed decisions by classifying wines into quality categories.

The dataset used is the **[White Wine Vinho Verde dataset](https://www.kaggle.com/datasets/joebeachcapital/wine-quality)** from [Cortez et al., 2009](http://www3.dsi.uminho.pt/pcortez/wine/), which contains 4,898 samples with 11 numerical input variables (chemical properties) and one output variable (quality score).

## Dataset Details

Each wine sample has the following features:

* Fixed acidity
* Volatile acidity
* Citric acid
* Residual sugar
* Chlorides
* Free sulfur dioxide
* Total sulfur dioxide
* Density
* pH
* Sulphates
* Alcohol

**Output Variable:**

* Quality (score between 0 and 10)

To simplify and balance the classification task, quality scores were grouped into three classes:

* **Low Quality:** 0 - 4
* **Medium Quality:** 5 - 6
* **High Quality:** 7 - 10

---

## Model Training Process

### 1. **Data Preprocessing**

* Verified and confirmed that there are no missing values.
* Converted the multiclass target variable into three categories for classification.
* Performed train-test split and standardized the feature values using `StandardScaler`.

### 2. **Model Training**

#### Random Forest Classifier

* Provided the best results, with an **accuracy of 85.1%**.
* Performed well in identifying medium and high quality wines.

## Live Prediction

The script also supports user input for live predictions. Users are prompted to enter the 11 chemical properties (within realistic ranges), and the trained Random Forest model predicts the wine’s quality.

Example:

```
Please enter the following wine characteristics:
Fixed Acidity (Typical range: 3.8 - 14.2): 6.7
Volatile Acidity (Typical range: 0.08 - 1.1): 0.9
Citric Acid (Typical range: 0.0 - 1.66): 0.54
Residual Sugar (Typical range: 0.6 - 65.8): 56.8
Chlorides (Typical range: 0.009 - 0.346): 0.077
Free Sulfur Dioxide (Typical range: 2 - 289): 122
Total Sulfur Dioxide (Typical range: 9 - 440): 343
Density (Typical range: 0.9871 - 1.03898): 0.986
pH (Typical range: 2.72 - 3.82): 3.8
Sulphates (Typical range: 0.22 - 1.08): 0.87
Alcohol (Typical range: 8.0 - 14.2): 12.3

Predicted Wine Quality: Medium Quality
```