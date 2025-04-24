# Elevatelabs-Task1
 Task 1: Data Cleaning & Preprocessing
Objective:
To clean and prepare raw data for Machine Learning using tools like Pandas, NumPy, Matplotlib, and Seaborn.

Tools Used:
Python (programming language)
Pandas (for data manipulation)
NumPy (for numerical operations)
Matplotlib/Seaborn (for visualization)
Scikit-learn (for scaling data)

Dataset Used:
We used a sample version of the Titanic dataset (manually created with missing values and categorical data to simulate real-world preprocessing tasks).

🔧 Steps Performed:
1. Imported the dataset & explored basic information
Loaded the Titanic dataset into a Pandas DataFrame.
Used .info() and .isnull().sum() to inspect:
Data types
Missing values
Shape and structure

2. Handled Missing Values
Age column: Missing values were filled with the median of the column.
Embarked column: Missing values were replaced with the mode (most frequent value).
Cabin/Deck columns: Dropped if they had too many missing values (not useful).

3. Converted Categorical Features to Numeric
Applied One-Hot Encoding using pd.get_dummies() to convert:
Sex (male/female) into numeric binary columns
Embarked (C, Q, S) into dummy variables

4. Standardized Numerical Features
Applied StandardScaler to scale numerical columns like Age and Fare so they have:
Mean = 0
Standard deviation = 1
This makes features comparable and improves model performance.

5. Visualized & Removed Outliers
Created boxplots using Seaborn to visually identify outliers in Age and Fare.
Applied the IQR (Interquartile Range) method to detect and remove rows with extreme outliers.
