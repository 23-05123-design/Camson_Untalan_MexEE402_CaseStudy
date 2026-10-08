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

**CAMSON** 
### Chapters 1–3

I learned that data needs to be properly prepared, understood, and cleaned before it can be used for analysis. I understood that raw data may contain missing values, duplicates, irrelevant information, or unusual values that can affect the results. What surprised me was that even simple checks and summaries can reveal important problems in a dataset, and that handling missing data requires choosing carefully between deletion, imputation, or prediction depending on the situation.

### Chapter 4

I learned that feature engineering can make existing data more useful by creating new information from it. I understood that techniques like binning, interaction features, and encoding help present data in a form that is easier for a model to interpret. What surprised me was that even a simple calculation between two existing values can reveal a different relationship or pattern in the data.

### Chapter 5

I learned that scaling and normalization are important when different features have very different numerical ranges. I understood that scaling can prevent a feature with larger values from having too much influence on a model. What surprised me was that scaling does not always mean changing everything to 0–1, since different methods can adjust the data in different ways depending on the algorithm being used.

### Chapter 6

I learned that outliers are values that are very different from most of the data and can affect how the results are interpreted. I understood that methods like Z-score and IQR can help identify these unusual values, while capping, transformation, or removal can be used to handle them. What surprised me was that an outlier should not automatically be deleted because it may still contain useful information.

### Chapter 7

I learned that choosing the right features is important because not all information in a dataset contributes equally to the result. I understood that correlation can help identify relationships between variables, while different feature selection methods can determine which information is more useful for prediction. What surprised me was that even when several variables are related to the final result, some can still be considered less important when the features are evaluated together.

### Chapter 8

This chapter taught me that preprocessing becomes easier to manage when the different steps are arranged into one continuous process. I realized that missing values and differences in feature scales can be handled together instead of doing each step separately. What surprised me was that the same process can be applied again to new data, which helps keep the results consistent.

### Chapter 9

This chapter helped me understand how different preprocessing techniques can be combined to prepare an actual dataset for analysis. I learned that cleaning, transforming, reducing, discretizing, and encoding data are connected steps rather than separate tasks. What surprised me was that preprocessing is not always a one-time process because the data may need to be checked and adjusted again before it is ready for further analysis.

**UNTALAN**

### Chapters 1–3

I learned that preprocessing is the work done before any analysis or model, like cleaning a messy kitchen before cooking. I understood that checking the data first with head(), info(), and describe() tells you what you are dealing with, and that cleaning means handling missing values, duplicates, irrelevant columns, and noisy data. What surprised me was that there is no single right way to fix missing values. Imputation, deletion, and prediction each fit a different situation, and even removing the extreme sales values in the game dataset was a decision I had to think about.

### Chapter 4

I learned that feature engineering means creating new columns from the data you already have so that patterns are easier to see. I understood that binning, interaction features, and encoding each present the data in a different way, and that one-hot and ordinal encoding differ in whether the categories have an order. What surprised me was that dividing sales by temperature in the lemonade example gave a new kind of information, even though no new data was collected.

### Chapter 5

I learned that scaling puts features on a similar range so that a column with bigger numbers does not take over the model. I understood that StandardScaler centers the data around a mean of 0 with a standard deviation of 1, while MinMaxScaler squeezes it into 0 to 1. What surprised me was that scaling is not always needed. It depends on the algorithm and on how different the feature ranges are, so it is not something to apply automatically.

### Chapter 6

I learned that an outlier is a value far from the rest of the data, and that Z-score and IQR are two ways to find one. I understood that finding an outlier is only the first step, and that I still have to choose between capping, transforming, or removing it. What surprised me was that the value 100 had a Z-score of only about 2.62, so the Z-score method with a cutoff of 3 missed it, while the IQR method caught it right away.

### Chapter 7

I learned that feature selection keeps only the features that actually help the prediction, and that filter, wrapper, and embedded methods each choose in a different way. I understood that the filter method scores features, RFECV removes them one by one, and LassoCV shrinks weak ones to zero. What surprised me was that the three methods gave three different answers on the same data. RFECV kept only one feature, which showed me that the result depends on the method and on how small the dataset is.

### Chapter 8

I learned that a pipeline connects the preprocessing steps in order, like a conveyor belt, so the data goes in raw and comes out ready for the model. I understood that imputation and scaling can be placed in one pipeline, and that ColumnTransformer decides which columns the pipeline works on. What surprised me was how much shorter and cleaner the process was compared to doing every step by hand, and that the same pipeline can be reused on new data.

### Chapter 9

I learned how to put everything together on a real dataset, the Titanic data, by handling the numerical and categorical columns separately and then combining them with ColumnTransformer. I understood that discretizing Age into Child, Adult, and Elderly and then plotting the results is how we check whether the preprocessing really worked. What surprised me was that the plots made the data easier to understand than the numbers did, and that checking the result after preprocessing can show problems that need to be fixed before modeling.

## Errors we found

List any mistake you found in the original notebooks, and the correct version.
There are real ones in there. Finding them earns points.

## Note on AI tools

Say whether you used an AI tool, and what for. This is not a penalty.
Hiding it is.

## References

McKinney, W. (2021). Python for Data Analysis, 3rd ed. O'Reilly.
VanderPlas, J. Python Data Science Handbook.
Any other page or article you used.
