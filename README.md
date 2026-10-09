# MexEE 402: Data Preprocessing Case Study

MexEE Elective 2: Data Science and Machine Learning
Batangas State University, Alangilan Campus
1st Semester, AY 2026-2027

## Members

| Name | Student Number | Section |
|---|---|---|
| Camson, Aliyah Mae C. | 23-06309 | MEXE-4102 |
| Untalan, John Princelee C. | 23-05123 | MEXE-4102 |

## Notebook links

| Chapter | Links |
|---|---|
| Ch1_2_3 | [link](https://colab.research.google.com/drive/1TW0-XLTt3EezVuqt0ay6VD-X6fa4JTkE?usp=drive_link) |
| Ch4 | [link](https://colab.research.google.com/drive/1p00QmIVcKKz8-nXOTQH17w9ePRLfO89T?usp=drive_link) |
| Ch5 | [link](https://colab.research.google.com/drive/15oG9gIOiGRysxbQbKTZVd6NJ1pVsdKRp?usp=drive_link) |
| Ch6 | [link](https://colab.research.google.com/drive/1kR0XlrOFqsYOq1o3ATZ-SKbU8Z0GDONa?usp=drive_link) | 
| Ch7 | [link](https://colab.research.google.com/drive/1yrhrGq50aq-xgNCBRGibUFhPDCUgqSfN?usp=drive_link) |
| Ch8 | [link](https://colab.research.google.com/drive/1sa4yULtb0L2Bl6ScdL7sXjpEd6ZYIPYu?usp=drive_link) | 
| Ch9 | [link](https://colab.research.google.com/drive/1AkEIJsYW5aibTb5WOF0jEW4wji9UTRkc?usp=drive_link) | 
## What we learned

One short paragraph per chapter, Ch1_2_3 to Ch9. Say what the chapter taught
you and what surprised you. Not what the library does, but what you understood.

### Chapters 1–3

We learned that preprocessing is the work done before any analysis or model, like cleaning a messy kitchen before cooking. Raw data can contain missing values, duplicates, irrelevant columns, and unusual values that affect the results, so we checked the data first with head(), info(), and describe(). What surprised us was that even simple checks can reveal big problems in a dataset, and that there is no single right way to fix missing values. Deletion, imputation, and prediction each fit a different situation, and even removing the extreme sales values in the game dataset was a decision we had to think about.

### Chapter 4

We learned that feature engineering means creating new columns from the data we already have so that patterns are easier to see. Binning, interaction features, and encoding each present the data in a different way, and one-hot and ordinal encoding differ in whether the categories have an order. What surprised us was that dividing sales by temperature in the lemonade example gave a new kind of information, even though no new data was collected.

### Chapter 5

We learned that scaling puts features on a similar range so that a column with bigger numbers does not take over the model. StandardScaler centers the data around a mean of 0 with a standard deviation of 1, while MinMaxScaler squeezes it into 0 to 1. What surprised us was that scaling does not always mean changing everything to 0-1, and that it is not always needed. It depends on the algorithm and on how different the feature ranges are, so it should not be applied automatically.

### Chapter 6

We learned that an outlier is a value far from the rest of the data, and that Z-score and IQR are two ways to find one. Finding an outlier is only the first step, because we still have to choose between capping, transforming, or removing it. What surprised us was that the value 100 had a Z-score of only about 2.62, so the Z-score method with a cutoff of 3 missed it, while the IQR method caught it right away. It also showed us that an outlier should not be deleted automatically, since it may still contain useful information.

### Chapter 7

We learned that feature selection keeps only the features that actually help the prediction, and that filter, wrapper, and embedded methods each choose in a different way. The filter method scores features, RFECV removes them one by one, and LassoCV shrinks weak ones to zero. Correlation also helps show which variables are related. What surprised us was that the three methods gave three different answers on the same data. RFECV kept only one feature, and some variables that were related to the result still counted as less important when the features were evaluated together. This showed us that the result depends on the method and on how small the dataset is.

### Chapter 8

We learned that a pipeline connects the preprocessing steps in order, like a conveyor belt, so the data goes in raw and comes out ready for the model. Imputation and scaling can be placed in one pipeline instead of being done separately, and ColumnTransformer decides which columns the pipeline works on. What surprised us was how much shorter and cleaner the process was compared to doing every step by hand, and that the same pipeline can be reused on new data to keep the results consistent.

### Chapter 9

We learned how to put everything together on a real dataset, the Titanic data, by handling the numerical and categorical columns separately and then combining them with ColumnTransformer. Cleaning, transforming, reducing, discretizing, and encoding are connected steps rather than separate tasks. We also discretized Age into Child, Adult, and Elderly and plotted the results to check whether the preprocessing really worked. What surprised us was that the plots made the data easier to understand than the numbers did, and that preprocessing is not always a one-time process, because checking the result can show problems that need to be fixed before modeling.

## Errors we found

- Ch6, #1: The note says 100 is a clear outlier, but the cell above prints Outliers: [].
- Ch6, #2: The text says “median of halves”, but the output shows IQR = 9.25, which is the interpolated value.
- Ch7, #3: The text says assignments completed and grades are unrelated, but the printed correlation is 0.9565.
- Ch7, #4: The printed relevant_features list includes final grade itself, with correlation 1.0.
- Ch7, #6: The R-squared warnings are printed under the RFECV cell.
- Ch4, #12 and #13: The text says 1, 2, 3 and Sunny = [1,0,0], but the output shows 0.0, 1.0, 2.0, True/False, and the Weather columns in the order Cloudy, Rainy, Sunny.
- Ch1_2_3, #14: The FutureWarning is printed under the imputation cell.
- Ch9, #11: The Step 1 heading says Google Drive, but the code right below it uses files.upload().
- Ch8, #7 (the dropped columns): You can see it in the code. The ColumnTransformer lists only ['Age', 'Fare'].

## Note on AI tools

Yes, we used AI tools like Gemini and Claude while working on and reviewing our notebooks. Gemini mostly came in when our code gave us errors. It pointed out where the error was, explained why it happened, and gave us an idea of how to fix it. Claude, on the other hand, helped us understand the harder parts of the code and the concepts behind them, and we also used it to double-check our results and look for possible mistakes while going over the notebooks. Even with this help, our answers still came from the course chapters, our own implementations, and the results we got from running our notebooks.

## References

McKinney, W. (2021). Python for Data Analysis, 3rd ed. O'Reilly.
VanderPlas, J. Python Data Science Handbook.
Any other page or article you used.
