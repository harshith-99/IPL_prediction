# 🏏 IPL Match Winner Prediction using Machine Learning  

This project analyzes Indian Premier League (IPL) cricket match data and predicts the match winner using various **Machine Learning classification algorithms**. It also includes **data cleaning, visualization, and exploratory data analysis (EDA)** to gain insights into IPL matches.  

---

## 📌 Project Overview  
The aim of this project is to:  
- Clean and preprocess the IPL dataset.  
- Perform **data visualization** to understand trends in toss decisions, match outcomes, and player performances.  
- Encode categorical features (teams, toss decisions, etc.) into numerical form.  
- Train different **ML models** to predict match winners.  
- Compare their performance and evaluate accuracy.  

---

## 📂 Dataset  
- File used: `ipl_dataset.csv`  
- Columns include:  
  - `team1`, `team2` → Competing teams  
  - `toss_winner`, `toss_decision` → Toss results  
  - `winner` → Match winner  
  - `player_of_match` → Best player of the match  
  - Other match-related details  

---

## ⚙️ Steps in the Project  

### 1. **Data Preprocessing**  
- Checked for missing values and filled them with `0`.  
- Dropped unnecessary columns: `method`, `neutral_venue`.  
- Converted categorical features (teams, toss decisions) into numeric values.  
- Balanced the dataset by ensuring equal distribution of match outcomes.  

### 2. **Exploratory Data Analysis (EDA)**  
- Visualized **matches won by each team**.  
- Analyzed **toss decisions (bat/field)** by different teams.  
- Created **bar charts and pie charts** for toss winners and decision patterns.  
- Displayed **top 10 players of the match**.  

### 3. **Feature Engineering**  
- Input features (`X`): `team1`, `team2`, `toss_decision`, `toss_winner`.  
- Target variable (`y`): `winner`.  
- Encoded toss decision:  
  - `field → 0`  
  - `bat → 1`  
- Converted toss_winner logic into binary.  

### 4. **Model Training & Evaluation**  
Applied 4 ML algorithms using `scikit-learn`:  
- ✅ Logistic Regression  
- ✅ K-Nearest Neighbor (KNN)  
- ✅ Decision Tree Classifier  
- ✅ Support Vector Machine (SVM)  

Compared models based on training accuracy.  

---

## 📊 Results  

| Model                  | Accuracy (%) |
|-------------------------|--------------|
| Support Vector Machine  | XX %         |
| K-Nearest Neighbor      | XX %         |
| Decision Tree           | XX %         |
| Logistic Regression     | XX %         |

*(Replace `XX %` with actual output from your run — e.g., 78.25, 80.50, etc.)*  

A bar chart is plotted for **Model vs Accuracy Score**.  

---

## 🚀 Prediction Example  
Test input format:  
```python
# (team1, team2, toss_won_team, toss_decision)
test = np.array([4, 2, 2, 0]).reshape(1,-1)
