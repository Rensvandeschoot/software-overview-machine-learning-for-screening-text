# Overview of machine learning for screening text software 

The repository aims to create an overview and comparison of software used for
systematically screening large amounts of textual data using machine learning.

# Overview

The table below provides a quick overview of the software. The following
properties are evaluated:

-	Is the software free and [open-source](https://opensource.org/osd) (provide a :link: to the source code)?
-	Is the software published in a scientific article (provide a :link: with the [DOI](https://www.doi.org/))?
-	Is documentation or a manual available (provide a :link:)?
-	What type of machine learning is applied in the software (choose from **S**upervised, **U**nsupervised, **A**ctive)? – more details are compared in the tables about the [ML-properties](machine-learning-properties)
-	Is the user in control of the machine learning (yes/no, add `+` if users can add their own models)?



| Software               | Open-Source                           | Published                                           | Documentation                            | Type of ML | Control over ML     | 
|:----------------------:|:-------------------------------------:|:---------------------------------------------------:|:----------------------------------------:|:----------:|:-------------------:|
| [ASReview](#asreview)  |[:link:](https://github.com/asreview/) |[:link:](https://doi.org/10.1038/s42256-020-00287-7) |[:link:](https://asreview.readthedocs.io/)|   **A**    |:white_check_mark:`+`|
| [Rayyan](#rayyan)  | [:link:](https://github.com/rayyansys) | [:link:](https://doi-org.proxy.library.uu.nl/10.1186/s13643-016-0384-4) | [:link:](https://help.rayyan.ai/hc/en-us) |  |  |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: With some effort (add a footnote with more explaination);
:grey_question: Unknown (requires an issue).

# Data

The table below provides an overview of input/output data.

- What type of data can be imported (RIS, TSV, CSV, XLSX, TAB)?
- Can partly labeled data be imported (yes/no)?
- Does the export file contain the labeling decissions?
- Does the export file contain the rank order of the unseen records (yes/no)?
- Can the export file be re-imported into same software retaining the labeling decissions (yes/no)?
- Can the export file be re-imported into reference manager software retaining the labeling decission (yes/no)?

| Software               | Type of Data            | Partly labelled  | Labeling decissions | Rank order       | Re-Import-1      | Re-Import-2      |
|:----------------------:|:-----------------------:|:----------------:|:-------------------:|:----------------:|:----------------:|:----------------:|
| [ASReview](#asreview)  |RIS, TSV, CSV, XLSX, TAB |:white_check_mark:|:white_check_mark:   |:white_check_mark:|:white_check_mark:|:white_check_mark:|

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: Only for some extensions (add a footnote for more explaination);
:grey_question: Unknown (requires an issue).

# Installation

The table below provides an overview of options how to install the software.

- Can the software be installed locally so that data and labeling decisions are only stored on the users' device (yes/no)?
- Can the software be installed on a server (yes/no)?
- Is a docker available (yes/no; provide a :link:)?
- Does the software run on a server with a SAAS (yes/no; provide a link to the registration page)?

| Software              | Locally          | Server           | Docker                                              | SAAS |
|:---------------------:|:----------------:|:----------------:|:---------------------------------------------------:|:----:|
| [ASReview](#asreview) |:white_check_mark:|:white_check_mark:|[:link:](https://hub.docker.com/r/asreview/asreview) | :x:  |

:white_check_mark: Yes;
:x: No;
:grey_question: Unknown (requires an issue).

# Machine Learning Properties

The tables below provides an overview of the machine learning properties.


## Active Learning

### Training Data

- Can training data (prior knowledge) be selected by the user to train the first iteration of the model (yes/no)?
- Can the software handle partly labelled data where the available labels are used to train the first model (yes/no)?
- What is the minimal training data size (provide a number for relevant and irrelevant records)?



| Software              | Tr.Data by user  | Party labeled Tr.data |  Minimum Tr.data |
|:---------------------:|:----------------:|:---------------------:|:----------------:|
| [ASReview](#asreview) |:white_check_mark:|:white_check_mark:     | 1+1              |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: With some effort (add a footnote for more explaination);
:grey_question: Unknown (requires an issue).


### Model Selection

- Can the user select the active learning model (yes/no)?
- Can a user upload their own model (yes/no)?
- Can the feature extraction results be stored (yes/no)?
- Is a-synchronic training - labeling available (yes/no)?
- Can the user select batch size (yes/no; provide the default)?
- Is it possible to switch to a different model during screening (yes/no)?


| Software               | Select model     | User model       |  Store Feat.matrix  | A-synchronic     |Batch size |Switch   |
|:----------------------:|:----------------:|:----------------:|:-------------------:|:----------------:|:---------:|:-------:|
| [ASReview](#asreview)  |:white_check_mark:|:white_check_mark:|     :zap:[^1]       |:white_check_mark:|   :x:     |:zap:[^2]|

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: With some effort (add a footnote with more explaination);
:grey_question: Unknown (requires an issue).

[^1]: Extracting the feature matrix in ASReview is available via an [extension](https://github.com/asreview/asreview-extension-vocab-extractor). 

[^2]: Switching to a different model in ASReview is available by exporting the data of the first model, and importing the data back into ASReview. The software will recognize all previous labeling decisions and a new model can be trained. 

### Overview of Available Models

- Which  feature extraction methods are available?
**BOW** = bag of words; 
**Doc2Vec** = document to vector; 
**sBERT** = sentence bidirectional encoder representations from transformers;
**TF–IDF** = term frequency–inverse document frequency; 
**Word2Vec** = words to vector; 
**ML** = Multi-language;

- Which classifiers are available?
**CNN** = convolutional neural network;
**DNN** = dense neural network; 
**LDA** = latent dirichlet allocation; 
**LR**= logistic regression; 
**LSTM** = long short-term memory; 
**NB** = naive Bayes; 
**RF** =random forests; 
**SGD** = stochastic gradient descent;
**SVM** = support vector machine; 


- Which balancing strategies are available?
**S / Simple** = no balancing balance strategy;
**D / Double** = Double balance strategy;
**T / Tripple** = Triple balance strategy;
**U / Under** = Undersampling balance strategy;


- Which query strategies are available?
**R / Random** = Records are selected randomly;
**C/ Certain** = Certainty based;
**U / Uncertain** = Uncertainty based;
**M / Mixed** = A combination of query strategies, for example 90% Certainty based and 10% Random;
**C / Clustering** = Clustering query strategy;



| Software              | Feature Extr.                    | Classifiers                    |  Balancing  | Query Stra. |
|:---------------------:|:--------------------------------:|:------------------------------:|:-----------:|:-----------:|
| [ASReview](#asreview) |TF–IDF, Doc2Vec, sBert, TF-IDF, ML|CNN, DNN, LR, LSTM, NB, RF, SVM | S, D, U, T  |R, C, U, M   |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:grey_question: Unknown (requires an issue).


## Supervised Learning

| Software | Q1          |
|:--------:|:-----------:|

## Unsupervised Learning

| Software | Q1          |
|:--------:|:-----------:|

# Software

This section briefly describes the software in alphabetical order.

## [ASReview](www.asreview.ai)

 ASReview, developed at Utrecht University, helps scholars and practitioners
 to get an overview of the most relevant records for their work as efficiently
 as possible while being transparent in the process. It allows multiple
 machine learning models, and ships with exploration and simulation modes,
 which are especially useful for comparing and designing algorithms.
 Furthermore, it is intended to be easily extensible, allowing third parties
 to add modules that enhance the pipeline with new models, data, and other
 extensions.

# Contributing

Do you know other software that meets the inclusion criteria? Please make a
Pull Request and add it to the overview. When there is missing, wrong, or
incomplete information, please start an issue. 

# Licence

This project is CC-BY 4.0 licensed.

# Contact

For any suggestions, questions, or remarks, please file an issue in the issue tracker.

This comparison is maintained by the ASReview team. We aim to make a fair comparison and we are not prejudiced. If there is any concern about the comparison, please file an issue in the issue tracker such that it can be openly discussed. 


