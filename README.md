# Megathon 2023

Aryan Chandramania, Nanda Rajiv, Sanika Damle and Vedansh Agrawal

### dataset

each file contains keys `version` and `data`. `data` is a list. 

each element of data represents a "document". each document is represented by a dictionary. the keys for each document are `title` and `paragraphs`. title is a url. paragraphs is again a list of dictionaries (len 1). each dictionary has 
* qas: a dict with keys `question`, `id`, `answers`, `is_impossible`. `answers` is a dict-in-a-list with keys `answer_starts` and `text`. `answer_starts` is a list of pairs from `sent_starts` which constitute the answer. `text` is the answer.
* sent_list: a tokenized version of context split at '.'.
* context: all the data at the title url
* sent_starts: a list of tuples. each tuple is a pair of integers. the first integer is the start index of the sentence in the context. the second integer is the length of the sentence in the context. (index = char index)