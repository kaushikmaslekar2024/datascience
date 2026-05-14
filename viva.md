Assignment 1: Data Wrangling I (Iris Dataset & Basics)
How do you load a CSV file into your code? Ans: Using pd.read_csv('filename.csv').

What does df.head() do? Ans: It shows the first 5 rows of your dataset.

How do you check the size (rows and columns) of your dataset? Ans: Using df.shape.

How do you check for missing values in your code? Ans: Using df.isnull().sum().

What does pd.get_dummies() do in your code? Ans: It performs One-Hot Encoding (converts text categories into 1s and 0s).

Why did you use the columns=['species'] parameter inside get_dummies()? Ans: To tell Pandas exactly which column to convert into 1s and 0s.

How do you check the data types of your columns? Ans: Using df.dtypes or df.info().

What library did you import for preprocessing? Ans: from sklearn import preprocessing.

What does import pandas as pd do? Ans: It imports the Pandas library and gives it a shortcut name pd.

How do you select just one column, like 'sepal_length'? Ans: By using brackets: df['sepal_length'].

Assignment 2: Data Wrangling II (Academic Performance & Outliers)
What does np.nan represent in your code? Ans: It represents a missing or blank value.

How do you fill missing values with the mean? Ans: df['column'].fillna(df['column'].mean()).

How do you calculate the median in Pandas? Ans: df['column'].median().

What exact function did you use to draw a boxplot to find outliers? Ans: df[['Math_Score', 'Reading_Score']].boxplot().

What library did you use to show the plot? Ans: import matplotlib.pyplot as plt.

What does plt.show() do? Ans: It actually displays the plot on your screen.

How did you calculate Q1 (the 25th percentile) in your code? Ans: Q1 = df['column'].quantile(0.25).

How do you calculate the IQR in Python? Ans: IQR = Q3 - Q1.

How do you apply a Log Transformation in your code? Ans: Using numpy's log function: np.log(df['column']).

How do you calculate the Z-score in Python? Ans: Using scipy.stats.zscore().

Assignment 3: Descriptive Statistics (Titanic Dataset)
How do you load the built-in Titanic dataset? Ans: sns.load_dataset('titanic').

How do you calculate the average of a column? Ans: df['column'].mean().

How do you calculate the standard deviation? Ans: df['column'].std().

How do you calculate the variance? Ans: df['column'].var().

What does df.describe() do? Ans: It automatically prints out the mean, count, min, max, and percentiles for all number columns.

How do you find the minimum value in a column? Ans: df['column'].min().

How do you find the maximum value in a column? Ans: df['column'].max().

How do you group data by a category (like 'Sex' or 'Class')? Ans: df.groupby('category_column').

How do you get the 50th percentile (which is also the median)? Ans: df['column'].quantile(0.50).

What is sns short for in your imports? Ans: The Seaborn library (import seaborn as sns).

Assignment 4: Linear Regression (Boston Housing)
How do you import Linear Regression? Ans: from sklearn.linear_model import LinearRegression.

What function did you use to split your data? Ans: train_test_split().

What does test_size=0.2 mean in your code? Ans: It means 20% of the data is saved for testing, and 80% is used for training.

How do you initialize the model? Ans: model = LinearRegression().

What code trains the model? Ans: model.fit(X_train, y_train).

What code makes predictions? Ans: model.predict(X_test).

How do you check the Mean Squared Error? Ans: mean_squared_error(y_test, y_pred).

How do you check the R-squared score? Ans: r2_score(y_test, y_pred).

What is X and y in your code? Ans: X holds the input features (like number of rooms), y holds the target you want to predict (house price).

How do you print the coefficients (weights) of your model? Ans: print(model.coef\_).

Assignment 5: Logistic Regression (Bank Marketing)
How do you import Logistic Regression? Ans: from sklearn.linear_model import LogisticRegression.

What does StandardScaler do in your code? Ans: It scales the numbers so that large numbers don't mess up the model.

How do you apply the scaler to your data? Ans: scaler.fit_transform(X).

What is LabelEncoder used for here? Ans: To change text labels (like "yes" and "no") into numbers (1 and 0).

How do you generate a confusion matrix? Ans: confusion_matrix(y_test, y_pred).

How do you check the model's accuracy? Ans: accuracy_score(y_test, y_pred).

What function prints precision, recall, and f1-score all at once? Ans: classification_report(y_test, y_pred).

What are y_test and y_pred? Ans: y_test are the actual answers, y_pred are the answers your model guessed.

Do you use model.fit() for Logistic Regression too? Ans: Yes, model.fit() is used to train almost all sklearn models.

How do you apply LabelEncoder to a column? Ans: le.fit_transform(df['column_name']).

Assignment 6: Naive Bayes (Iris Dataset)
How do you import Naive Bayes? Ans: from sklearn.naive_bayes import GaussianNB.

Why did you use GaussianNB? Ans: Because the Iris dataset features (length and width) are continuous numbers.

How do you initialize the Naive Bayes model? Ans: model = GaussianNB().

Can you use accuracy_score for Naive Bayes? Ans: Yes, because it is a classification problem.

Does Naive Bayes require you to scale the data with StandardScaler? Ans: No, Naive Bayes doesn't strictly require feature scaling.

How do you train this model? Ans: model.fit(X_train, y_train).

What library do accuracy_score and confusion_matrix come from? Ans: sklearn.metrics.

Why do we encode the "Species" column in Iris? Ans: Because machine learning models need numbers (0, 1, 2) instead of text ('setosa', 'virginica').

What does the random_state parameter do in train_test_split? Ans: It locks the random seed so you get the exact same split every time you run the code.

If you have 3 classes of Iris flowers, what size is your confusion matrix? Ans: It will be a 3x3 matrix.

Assignment 7: Text Analytics
What is NLTK? Ans: Natural Language Toolkit, a library used for text processing.

How do you download stopwords in your code? Ans: nltk.download('stopwords').

What is the code to tokenize text (split it into words)? Ans: nltk.word_tokenize(text).

How do you import the TF-IDF tool? Ans: from sklearn.feature_extraction.text import TfidfVectorizer.

How do you initialize the TF-IDF vectorizer? Ans: vectorizer = TfidfVectorizer().

How do you convert your text documents into a TF-IDF matrix? Ans: vectorizer.fit_transform(corpus).

What is a "corpus" in your code? Ans: It is simply a list containing your text documents (e.g., corpus = [docA, docB]).

How do you view the TF-IDF output as a normal array? Ans: By using .toarray() on the matrix.

How do you get the actual words (feature names) from the vectorizer? Ans: vectorizer.get_feature_names_out().

Are commas and periods removed automatically by TfidfVectorizer? Ans: Yes, it automatically removes basic punctuation and makes text lowercase.

Assignment 8 & 9: Data Visualization I & II (Titanic & Seaborn)
What is the code to create a basic histogram? Ans: sns.histplot(data=df, x='column_name').

How do you add that smooth curve line to a histogram? Ans: By adding kde=True inside the histplot() function.

How do you create a scatter plot? Ans: sns.scatterplot(x='col1', y='col2', data=df).

How do you color data points based on a category (like Male/Female)? Ans: By using the hue parameter: hue='Sex'.

What does sns.pairplot(df) do? Ans: It automatically plots scatter plots for all numerical columns against each other.

How do you create a heatmap? Ans: sns.heatmap(data).

What do we usually pass into the heatmap function? Ans: The correlation matrix: df.corr().

How do you show the numbers inside the heatmap colored boxes? Ans: By using annot=True.

How do you change the size of your plot? Ans: plt.figure(figsize=(10, 6)).

How do you add a title to your plot? Ans: plt.title("My Plot Title").

Assignment 10: Data Visualization III (Iris Outliers & Subplots)
How do you create multiple plots at the same time? Ans: fig, axes = plt.subplots(nrows, ncols).

How do you draw a boxplot using Seaborn? Ans: sns.boxplot(x='species', y='sepal_length', data=df).

How do you tell seaborn to put a plot in a specific subplot box? Ans: By passing the ax=ax parameter.

What does plt.tight_layout() do in your code? Ans: It fixes the spacing between subplots so titles and labels don't overlap.

How did you filter the dataset to find rows less than the lower bound? Ans: df[df['column'] < lower_bound].

What does the pipe symbol | mean when filtering for outliers? Ans: It stands for "OR" (e.g., less than lower bound OR greater than upper bound).

What is the code formula for the lower bound? Ans: lower_bound = Q1 - 1.5 \* IQR.

What is the code formula for the upper bound? Ans: upper_bound = Q3 + 1.5 \* IQR.

How do you loop over columns in Python to make plots? Ans: for col in features:.

How do you print the number of outliers found? Ans: print(len(outliers)).
