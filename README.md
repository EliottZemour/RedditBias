# MasterThesis

The data preparation code is included in the directory - DataPreparation

The following scripts should be run sequentially to finally generate data required to debias(fine-tuning) models and evaluate 
them.

- DataPreparation/reddit_data.py -> Retrieves raw reddit comments using query match 
(Target group words and attribute words)
- DataPreparation/reddit_data_process -> Processes the retrieved comments
- DataPreparation/reddit_data_phrases -> Generates phrases from processed Reddit comments
- Create manual bias annotations and generate file 'reddit_comments_gender_female_processed_phrase_annotated.csv'
- DataPreparation/reddit_data_phrases_replace_target.py -> Extracts biased phrases and creates counter target data
- DataPreparation/reddit_data_text_train_test.py -> Creates train test split of biased phrases
- evaluation/measure_bias.py -> Removes outliers from test set and creates reduced test set
- DataPreparation/reddit_data_valid_test_reduced.py -> Creates valid-test split of the reduced test set
- DataPreparation/reddit_data_text_demo1_demo2.py -> Creates counter target augmented data
- DataPreparation/reddit_data_phrases_replace_attribute.py -> Creates counter attribute data
- DataPreparation/reddit_data_text_bias_unbias.py -> Creates test files of counter attribute augmented data