# basic overview of the competition

competition page: https://www.kaggle.com/competitions/feedback-prize-english-language-learning/overview

Given an paragraph written by an english language learner, build a model that is able to score the essay on 6 criteria - cohesion, syntax, grammar, vocabulary, phraseology, conventions. 

# basic overview of my solution 

used a regression model that took the following inputs:
- bert inputs (input_ids, attention_mask, token_type_ids)
- array of the jaccard similarities between two consecutive sentences over the entire paragraph (i.e. [similarity between sentence 1 & 2, similarity between sentence 2 & 3, ...]
- frequency ratio of each words used in the paragraph (i.e. total count of a word / total word count)
- array of the simple part of speech (pos in spacy) of each the words in the paragraph
- array of the detailed part of speech (tag in spacy) of each the words in the paragraph
- array of the syntactic dependency (dep in spacy) of each the words in the paragraph


