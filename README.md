# Movie-Dataset-Analysis
## This project analyzes a dataset of movies using Python to uncover patterns and correlations between features such as budget, gross earnings, score, and more.
## Features
- Data Cleaning & Preprocessing
- Visualizations (scatter plots, regression plots, heatmaps)
- Correlation Analysis
- Feature Encoding for categorical data
## Dataset columns
- `name`, `rating`, `genre`, `year`, `released`, `score`, `votes`, `director`, `writer`, `star`, `country`, `budget`, `gross`, `company`, `runtime`
## Visualization
- Budget vs Gross Earnings (scatter & regplot)
# Python code for scatter plot
plt.scatter(x=df['budget'], y=df['gross'])

plt.title('Budget vs Gross earnings')

plt.xlabel('Gross earnings')

plt.ylabel('Budget for films')

plt.show()
  ![Screenshot 2025-05-18 191022](https://github.com/user-attachments/assets/2d42299b-affd-4312-a955-c73c4123c76b)
  # Python code  for seaborn
  sns.regplot(x='budget', y='gross', data=df, scatter_kws={"color":"red"}, line_kws={"color":"blue"})
  ![Screenshot 2025-05-18 191036](https://github.com/user-attachments/assets/ae039fd5-e9ee-4295-9eb6-b284a40fb789)
- Correlation Matrix Heatmap
  # Python code for numerical correlation
  correlation_matrix = df.select_dtypes(include='number').corr(method='pearson')

sns.heatmap(correlation_matrix, annot= True)

plt.title('Correlation matrix for Numeric Features')

plt.xlabel('Movie features')

plt.ylabel('Movie features')

plt.show() 
  ![Screenshot 2025-05-18 191051](https://github.com/user-attachments/assets/79672a3f-8592-4c4c-a5de-b5e6d1df95fe)
  # Python code for Numeric features
  correlation_matrix = df_numerized.corr(method='pearson')

sns.heatmap(correlation_matrix, annot= True)

plt.title('Correlation matrix for Numeric Features')

plt.xlabel('Movie features')

plt.ylabel('Movie features')

plt.show() 
  ![Screenshot 2025-05-18 191110](https://github.com/user-attachments/assets/1b067b61-5b66-49e0-94fb-e7b2a63bf86d)

## Key Insights
- High correlation between budget and gross.
- Votes also strongly correlate with gross.
- Encoding categorical features can uncover hidden relationships.
