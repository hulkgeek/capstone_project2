# 
Open-Domain Question Answering: Answer Sentence Selection

**Introduction**

Answer sentence selection is the task of identifying sentences that contain the answer to a given question. This is an important problem in its own right as well as in the larger context of open domain question answering. Question Answering uses either large-scale knowledge base (e.g., Freebase) or free, high-quality, reliable text (e.g., Wikipedia, news articles). In this project we use the latter (i.e., Wikipedia) to select the potential answers from.

**Problem Statement**

Given a factoid question, find the sentence in the candidate set that (1) contains the answer; and (2) can sufficiently support the answer. 

**Dataset: WikiQA Corpus**

WIKIQA is a dataset for open domain question answering. The dataset contains over 3,000 questions originally sampled from Bing query logs. Based on the user clicks, each question is associated with a Wikipedia page presumed to be the topic of the question. all the sentences in the summary paragraph of the page as the candidate answer sentences, with labels on whether the sentence is a correct answer to the question provided by crowdsourcing workers. Among these questions, about one-third of them contain correct answers in the answer sentence set.

**Metrics**

Precision, recall and F1 scores for answer triggering problem.

**Methodology**

After cleaning data and reading them into DataFrames from *.tsv files and some exploratory data analysis, we convert the texts to TF-IDF (for question query) and USE vectors (for sentece selction). We will then use Linear and Logistic Regression to match the questions and right answers. We will then a fit DNN model using Keras API to further improve the classification metrics.

**Files**
- /Data/WikiQA.tsv -- Data file
- project_2.ipynb -- Python codes in Jyputer notebook
- model.h5 -- trained Keras DNN model with pre-trained word embedding layares
