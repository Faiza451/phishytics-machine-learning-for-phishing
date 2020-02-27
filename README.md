# Phishytics - Machine Learning for Detecting Phishing Websites
Machine Learning and Random Forests with Byte Pair Encoding and TFIDF scores for Phishing Website Detection.

![Python 3.6](https://img.shields.io/badge/python-3.6-green.svg?style=plastic)

This repository contains code for the blog post [Phishytics – Machine Learning for Detecting Phishing Websites](https://faizanahmad.tech/blog/2020/02/phishytics-machine-learning-for-phishing-websites-detection/). Using Random Forests on top of Byte Pair Encoding and TFIDF scores, we can obtain a highly accurate model for predicting phishing websites. Pre-trained models are also provided for users and companies to use.

### Files Description
| Path | Description
| :--- | :----------
| phishytics-machine-learning-for-phishing | Main folder.
| &boxur;&nbsp; tokenizer | Folder to store the tokenizer output files.
| &boxur;&nbsp; labeled_data | Folder containing data for phishing and legitimate websites.
| &ensp;&ensp; &boxvr;&nbsp; phishing_htmls| HTML files of phishing web pages. Please do not change the folder names.
| &ensp;&ensp; &boxvr;&nbsp; legitimate_htmls| HTML files of legitimate web pages. Please do not change the folder names.
| &boxvr;&nbsp; train_phishing_detection_model.py | Train a phishing website detection model.
| &boxvr;&nbsp; test_model.py | Test a website for phishing using our pre-trained random forest model.

## Usage
### Packages
You will need to install the following package to train and test the models.
- [Scikit-learn](https://scikit-learn.org/)
- [Numpy](https://numpy.org/)
- [Tokenizers](https://github.com/huggingface/tokenizers)
- [Langdetect](https://pypi.org/project/langdetect/)
- [Joblib](https://joblib.readthedocs.io/en/latest/)
- [Requests](https://requests.readthedocs.io/en/master/)

### How to run
#### 1. Data Tokenization
In order to run the model, you first need to tokenize all the HTML files into tokens. Once the html files are in their respective folders, run the following command.
```
python3 create_data_for_tokenization.py --labeled_data_folder labeled_data --vocab_size 100 --min_frequency 3
```
The script takes three parameters as inputs:
- articles_per_author: How many articles do you want to use per author. The range can be anywhere between [10-Maximum Number of Articles per any Author]
- authors_to_keep: How many authors do you want in your attribution classifier. The range can be anywhere between [2-Total Authors]
- data_folder: Data folder containing a single directory for each author.


## License
[![MIT](https://img.shields.io/cocoapods/l/AFNetworking.svg?style=style&label=License&maxAge=2592000)](LICENSE)

Copyright (c) 2020-present, Faizan Ahmad