# JSC270_A4
## Final project for JSC270 Winter 2021
### Author: Rui Miao(Amy), Xinpeng Shan(Joy), Shiyuan Zhou(Eric)

File descriptions:

JSC270_A4_Report.pdf: The report of A4

JSC270_A4Q1.ipynb: the colab notebook including all the codes for question 1 

JSC270_A4Q2.ipynb: the colab notebook including all the codes for question 2

JSC270_A4Q2_presentation_slide.pdf: the slides for the presentation of question 2

JSC270_A4Q2_dataset_countryplot_neg.csv: dataset to plot the pie chart (The proportion of locations of people who support #maskoff) in A4Q2

JSC270_A4Q2_dataset_countryplot_pos.csv: dataset to plot the pie chart (The proportion of locations of people who support #maskon) in A4Q2

JSC270_A4Q2_dataset_mask.csv: dataset for the mask model in A4Q2

JSC270_A4Q2_dataset_vaccine.csv: dataset for the vaccine model in A4Q2

question_2_proportion.csv: dataset for calculating the proportion of people who supports wearing mask

# Evaluation Comments

## Q1

- Careful about using the max_features attribute in the CountVectorizer. This restricts your vocabulary. This is fine as a hyperparameter to tune, but the true vocabulary without constraint should be above 50,000. This will affect your accuracies later in the question, but you'll only lose a mark once.
- Instead of fitting a separate count vectorizer for each class, you could just use np.unique on your data directly to get token counts.
- The top 5 words for each class should be mostly covid related, with counts in the high thousands. Your top 5 seem to have a lower count. You may have some encoding problems that are affecting this.
- Note that ROC Curves are designed to measure TP and FP for binary classification. In this case a single ROC curve has no meaning; instead Sklearn will fit multiple pairwise curves and plot them together, or average them.

## Q2

- Great motivation of the problem and statement of questions
- It's okay if your study is limited. You do a great job of addressing possible pitfalls in your data before analyzing it
- Please don't include code in your report (only text and visuals)
- Are there any related works predicting tags generally (not necessarily COVID-related)?
- Excellent data description
- Which stopword list did you use, and how many stopwords did you remove?
- Are there any interesting patterns in your dataset? What are some descriptive statistics in terms of length, other tags, attitude, etc..?
- NLP is not itself a machine learning model. It is a collection of techniques for processing text as data (which may or may not use ML)
- What is the balance in attitudes, and how does it compare to your test accuracy?
- Precision and Recall would be useful metrics here
- Do your results change with a different train/test split?
- What can you conclude from this experiment?
- Excellent work




