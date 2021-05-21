# datascience_challenge


## Overview:
This was a 2 day data science challenge that involved creating a machine learning model based off the train.txt data given, no other instructions were given. The dataset involved a list of words from a paragraph and The challenge goes through data cleaning, Exploratory Data Analysis, and touches on Natural Language Processing in order to create a usable model. As this was my first time using the NLTK package, I learned a lot about the package and basic NLP. 

## Dataset:
![Given Data](dataset.png "Data")

- word: contains a word from a collection of sentences
- label: a word chunk label similar to the ones used by SpaCy and NLTK (https://www.nltk.org/book/ch07.html)


## Programs used:
* Python
* Pandas
* Seaborn
* NLTK
* Scikit-Learn

## Final Findings:
### Accuracies
* Logistic Regression - 0.9538
* Random Forest - 0.9536
* Multinomial Naive Bayes - 0.9474

### Future Improvements:
If I had more time, here would be the following improvements that I would implement:
1. __Adding more Named Entity Recognizers__: Through research of named entities, I can across many other entity recognizers such as Spacy and monkeylearn. Unlike what I am used to, there wasn't much data to go off of for a singluar word. If I used other Named Entity Recognizers, perhaps could have made a better model.

2. __Named Entity Recognition Implementation__: While I did implement NLTK's ne_chunk, I could have done it much better. For one, I only applied ne_chunk to the 2 nearest words. If I could instead apply ne_chunk to the entire sentence, and then retrieved the category for each word respectively, that would return much better data. The main thing that stopped me from this implmentation is not knowing how to separate the sentences properly.

3. __Cross Validation__: Overall, I didn't really fine-tune my classification model, I simply used the defaults and picked the best model out of the three. It would have been much wiser to use cross validation during the training in order to get better model and to make sure that I don't overfit. 

4. __Balance Correction__: When looking at the categories/labels given in the original dataset, there were significantly more O categories than any other category. As a result, our model could have been unfairly biased towards 'O' category. Implementation of a balance correction method could help us make a better model. Currently I am mainly acquainted with SMOTE, which I don't think would be the best balance correction method for this task for we are only given a singular word.

5. __More Exploration of ML Models__: Due to time restraints preventing me research other classifier models, I only tested and used the ones that I was familar with
