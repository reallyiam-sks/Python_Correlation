# Movie Correlation Project in Python

This project analyzes correlations between various features of movies such as **budget, gross revenue, votes, and ratings** using Python. It’s a complete end-to-end data analytics project designed for your **data analyst portfolio**, demonstrating data cleaning, transformation, visualization, and correlation analysis.



##  Project Overview

The goal of this analysis is to identify what factors most strongly correlate with a movie’s gross revenue. By examining a dataset of global movie data, we aim to understand how variables such as production budget, company, and score impact performance.



##  Tools & Libraries Used

- **Python 3**
- **Pandas** – data manipulation and analysis  
- **NumPy** – numerical computing  
- **Seaborn** – data visualization  
- **Matplotlib** – plotting and graphing  



##  Dataset

- **Source:** [Kaggle - Movies Dataset](https://www.kaggle.com/danielgrijalvas/movies)
- **File:** `movies.csv`
- **Key Columns:**
  - `budget`
  - `gross`
  - `company`
  - `genre`
  - `runtime`
  - `score`
  - `votes`
  - `country`
  - `released`
  - `year`



## Project Steps

1. **Import Libraries**  
   Set up essential Python packages such as `pandas`, `numpy`, `matplotlib`, and `seaborn`.

2. **Load Data**  
   Read the dataset using:
df = pd.read_csv("movies.csv")



3. **Data Cleaning**
- Check for and handle missing values.
- Drop duplicates.
- Adjust data types (e.g., convert `budget` and `gross` to integers).
- Create a corrected `year` column from the `released` column for consistency.

4. **Data Exploration**
- View dataset structure using `df.info()` and `df.head()`.
- Understand numeric and categorical fields.

5. **Feature Engineering**
- Sort movies by gross revenue.
- Encode non-numeric (categorical) columns using the `.cat.codes` method to enable correlation analysis.

6. **Correlation Analysis**
- Compute correlation coefficients (Pearson, Kendall, Spearman).
- Identify which variables have the strongest correlation with `gross`.

correlation_matrix = df.corr(method='pearson')



7. **Data Visualization**
- Create a scatter plot and regression plot to show the relationship between `budget` and `gross`.
- Build a correlation heatmap for all numeric features using seaborn:
  ```
  sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm')
  plt.title('Correlation Matrix for Numeric Features')
  ```

8. **Insights**
- Movies with higher budgets generally have higher gross revenue.
- Votes and scores also show positive correlation with gross performance.
- Production company shows weak correlation to gross revenue.



##  Key Findings

- **Budget** has the **strongest positive correlation** with **gross revenue** (~0.71 Pearson).
- **Votes** also show moderate correlation with **gross revenue** (~0.63 Pearson).
- **Company** correlation is weak, suggesting brand alone doesn’t guarantee higher earnings.



##  Visualizations

Sample visualizations created in this project:
1. Scatter plot: **Budget vs. Gross**
2. Regression plot: **Trend line showing positive correlation**
3. Correlation heatmap: **Full dataset correlation matrix**



##  How to Run the Project

1. Clone the repository:
git clone https://github.com/yourusername/movie-correlation-project.git

text
2. Navigate to the folder:
cd movie-correlation-project

text
3. Install dependencies:
pip install pandas numpy seaborn matplotlib

text
4. Open the Jupyter Notebook:
jupyter notebook

text
5. Run the notebook cells sequentially.



##  Learning Outcomes

- Performing data cleaning and type conversions in pandas
- Visualizing and interpreting correlation matrices
- Automating categorical encoding for correlation analysis
- Creating professional, reproducible data analysis reports



##  Future Improvements

- Include more advanced statistical testing and regression modeling.
- Add a Power BI or Tableau visualization dashboard.
- Connect the project to an SQL backend for interactive analytics.



