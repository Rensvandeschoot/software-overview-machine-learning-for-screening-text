# Overview of software for screening large amounts of textual data implementing machine learning 

The repository aims to create an overview and comparison of software used for
systematically screening large amounts of textual data using machine learning.

# Overview

The table below provides a quick overview of the software. The following
properties are evaluated:

-   Is there a website?
-	Is the software free and [open-source](https://opensource.org/osd) (provide a :link: to the source code)?
-	Is the software published in a scientific article (provide a :link: with the [DOI](https://www.doi.org/))?
-	Is documentation or a manual available (provide a :link:)?
-	What type of machine learning is applied in the software (choose from **S**upervised, **U**nsupervised, **A**ctive)? – more details are compared in the tables about the [ML-properties](machine-learning-properties)
-	Is the user in control of the machine learning (yes/no, add `+` if users can add their own models)?




|            Software             |                           Website                            |                            Open-Source                            |                               Published                                |                                    Documentation                                    | Type of ML |    Control over ML    | 
|:-------------------------------:|:------------------------------------------------------------:|:-----------------------------------------------------------------:|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|:----------:|:---------------------:|
|      [ASReview](#asreview)      |                [:link:](https://asreview.nl/)                |     :white_check_mark:[:link:](https://github.com/asreview/)      | :white_check_mark:[:link:](https://doi.org/10.1038/s42256-020-00287-7) |            :white_check_mark:[:link:](https://asreview.readthedocs.io/)             |   **A**    | :white_check_mark:`+` |
|     [Abstrackr](#abstrackr)     |          [:link:](http://abstrackr.cebm.brown.edu)           |     :zap:[:link:](https://github.com/bwallace/abstrackr-web)      |  :white_check_mark:[:link:](https://doi.org/10.1145/2110363.2110464)   |                                         :x:                                         |   **A**    |          :x:          |
|       [Colandr](#colandr)       |      [:link:](https://hslib.jabsom.hawaii.edu/colandr)       | :zap:[:link:](https://github.com/datakind/permanent-colandr-back) |     :white_check_mark:[:link:](https://doi.org/10.1111/cobi.13117)     | :white_check_mark:[:link:](https://hslib.jabsom.hawaii.edu/colandr/getting_started) |   **A**    |          :x:          |
| [EPPI-Reviewer](#eppi-reviewer) | [:link:](https://eppi.ioe.ac.uk/cms/Default.aspx?tabid=2914) |                                :x:                                |                                  :x:                                   |   :white_check_mark:[:link:](https://eppi.ioe.ac.uk/cms/Default.aspx?tabid=3822)    |  **A, S**  |          :x:          |
|      [FASTREAD](#fastread)      |                             :x:                              |    :white_check_mark:[:link:](https://github.com/fastread/src)    | :white_check_mark:[:link:](https://doi.org/10.1007/s10664-017-9587-0)  |         :white_check_mark:[:link:](https://github.com/fastread/src/#readme)         |   **A**    |          :x:          |
|        [Rayyan](#rayyan)        |               [:link:](https://www.rayyan.ai/)               |            :zap:[:link:](https://github.com/rayyansys)            | :white_check_mark:[:link:](https://doi.org/10.1186/s13643-016-0384-4)  |             :white_check_mark:[:link:](https://help.rayyan.ai/hc/en-us)             |   **A**    |          :x:          |
|  [RobotAnalyst](#robotanalyst)  |       [:link:](http://www.nactem.ac.uk/robotanalyst/)        |                                :x:                                |     :white_check_mark:[:link:](https://doi.org/10.1002/jrsm.1311)      |                                         :x:                                         |   **A**    |          :x:          |
|  [SWIFT-Review](#swift-review)  |        [:link:](https://www.sciome.com/swift-review/)        |                                :x:                                | :white_check_mark:[:link:](https://doi.org/10.1186/s13643-016-0263-z)  |                                         :x:                                         |            |                       |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: Some open-source repositories are publicly available, but not the core engine;
:grey_question: Unknown (requires an issue).


# Installation

The table below provides an overview of options for how to install the software.

- Can the software be installed locally so that data and labeling decisions are only stored on the user's device (yes/no)?
- Can the software be installed on a server (yes/no)?
- Is a docker available (yes/no; provide a :link:)?
- Does the software run on a server with a SAAS (yes/no; provide a link to the registration page)?

|            Software             |      Locally       |       Server       |                        Docker                        |                                     SAAS                                      |
|:-------------------------------:|:------------------:|:------------------:|:----------------------------------------------------:|:-----------------------------------------------------------------------------:|
|      [ASReview](#asreview)      | :white_check_mark: | :white_check_mark: | [:link:](https://hub.docker.com/r/asreview/asreview) |                                      :x:                                      |
|     [Abstrackr](#abstrackr)     |        :x:         |        :x:         |                         :x:                          |          :white_check_mark:[:link:](http://abstrackr.cebm.brown.edu)          |
|       [Colandr](3colandr)       |        :x:         |        :x:         |                         :x:                          |            :white_check_mark:[:link:](https://www.colandrapp.com/)            |
| [EPPI-Reviewer](#eppi-reviewer) |        :x:         |        :x:         |                         :x:                          |              :white_check_mark:[:link:](https://eppi.ioe.ac.uk/)              |
|      [FASTREAD](#fastread)      | :white_check_mark: |        :x:         |                         :x:                          |                                      :x:                                      |
|        [Rayyan](#rayyan)        |        :x:         |        :x:         |                         :x:                          |              :white_check_mark:[:link:](https://www.rayyan.ai/)               |
|  [RobotAnalyst](#robotanalyst)  |        :x:         |        :x:         |                         :x:                          | :white_check_mark:[:link:](http://www.nactem.ac.uk/robotanalyst/)<sup>1</sup> |
|  [SWIFT-Review](#swift-review)  |                    |                    |                                                      |                                                                               |  

:white_check_mark: Yes;
:x: No;
:grey_question: Unknown (requires an issue).

<sup>1</sup> To use RobotAnalyst, you need to request an account via email.

# Data

The table below provides an overview of input/output data.

- What type of data can be imported (RIS, TSV, CSV, XLSX, TAB)?
- Can partly labeled data be imported (yes/no)?
- Does the export file contain the labeling decisions?
- Does the export file contain the rank order of the unseen records (yes/no)?
- Can the export file be re-imported into the same software, retaining the labeling decisions (Re-Import-1: yes/no)?
- Can the export file be re-imported into reference manager software retaining, the labeling decision (Re-Import-2: yes/no)?

|            Software             |               Type of Data                |                Partly labeled                 |     Labeling decisions      |         Rank order          |         Re-Import-1         |         Re-Import-2         |
|:-------------------------------:|:-----------------------------------------:|:---------------------------------------------:|:---------------------------:|:---------------------------:|:---------------------------:|:---------------------------:|
|      [ASReview](#asreview)      | RIS, TSV, CSV, XLSX, TAB, `+`<sup>1</sup> |       :white_check_mark:`+`<sup>1</sup>       |     :white_check_mark:      |     :white_check_mark:      |     :white_check_mark:      |     :white_check_mark:      |
|     [Abstrackr](#abstrackr)     |         RIS, TAB, TXT<sup>2</sup>         |                      :x:                      |     :white_check_mark:      |     :white_check_mark:      |             :x:             |     :white_check_mark:      |
|       [Colandr](#colandr)       |               RIS, BIB, TXT               |               :zap:<sup>3</sup>               |     :white_check_mark:      |             :x:             |             :x:             |             :x:             |
| [EPPI-Reviewer](#eppi-reviewer) |         RIS, TXT, `+`<sup>4</sup>         |               :zap:<sup>3</sup>               | :grey_question:<sup>5</sup> | :grey_question:<sup>5</sup> | :grey_question:<sup>5</sup> | :grey_question:<sup>5</sup> |
|      [FASTREAD](#fastread)      |                    CSV                    |              :white_check_mark:               |     :white_check_mark:      | :grey_question:<sup>6</sup> |     :white_check_mark:      |     :white_check_mark:      |
|        [Rayyan](#rayyan)        |    RIS, ENW, BIB, CSV, XML, CIW, NBIB     |               :zap:<sup>3</sup>               |     :white_check_mark:      |             :x:             |             :x:             |     :white_check_mark:      |
|  [RobotAnalyst](#robotanalyst)  |                 RIS, NBIB                 | :white_check_mark::grey_question:<sup>7</sup> |     :white_check_mark:      | :grey_question:<sup>7</sup> | :grey_question:<sup>7</sup> |             :x:             |
|  [SWIFT-Review](#swift-review)  |                                           |                                               |                             |                             |                             |                             |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: Only for some extensions (add a footnote for more explanation);
:grey_question: Unknown (requires an issue).

<sup>1</sup> ASReview provides several open-source tools to convert file formats (e.g., CSV->RIS or RIS->XLSX), combine datasets (labeled, partly labeled, or unlabeled), and deduplicate records based on title/abstract/DOI.

<sup>2</sup> List of PubMed IDs

<sup>3</sup> It is possible to upload all records of the same label (relevant/irrelevant/unlabeled) as separate files.

<sup>4</sup> EPPI-Reviewer provides a closed-source [online file converter](https://eppi.ioe.ac.uk/cms/Default.aspx?tabid=2934) to convert several file formats to RIS.

<sup>5</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/21

<sup>6</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/24

<sup>7</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/29



# Machine Learning Properties

The tables below provide an overview of the machine learning properties.


## Active Learning

### Training Data

- Can training data (prior knowledge) be selected by the user to train the first iteration of the model (yes/no)?
- What is the minimal training data size (provide a number for **R**elevant and **I**rrelevant records)?



|            Software             |  Tr.Data by user   | Minimum Tr.data |
|:-------------------------------:|:------------------:|:---------------:|
|      [ASReview](#asreview)      | :white_check_mark: |     ≥1R+≥1I     |
|     [Abstrackr](#abstrackr)     |        :x:         |       :x:       |
|       [Colandr](#colandr)       | :white_check_mark: |       10        |
| [EPPI-Reviewer](#eppi-reviewer) | :white_check_mark: |       ≥5R       |
|      [FASTREAD](#fastread)      | :white_check_mark: |       ≥1R       |
|        [Rayyan](#rayyan)        | :white_check_mark: |  ≥50 with ≥5R   |
|  [RobotAnalyst](#robotanalyst)  | :white_check_mark: |       ≥1R       |
|  [SWIFT-Review](#swift-review)  |                    |                 |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: With some effort (add a footnote for more explanation);
:grey_question: Unknown (requires an issue).


### Model Selection

- Can the user select the active learning model (yes/no)?
- Can a user upload their own model (yes/no)?
- Can the feature extraction results be stored (yes/no)?
- Is a-synchronic training - labeling available (yes/no)?
- Can the user select batch size (yes/no; provide the default)?
- Is it possible to switch to a different model during screening (yes/no)?


|            Software             |    Select model    |     User model     | Store Feat.matrix  |    A-synchronic    | Batch size |      Switch       |
|:-------------------------------:|:------------------:|:------------------:|:------------------:|:------------------:|:----------:|:-----------------:|
|      [ASReview](#asreview)      | :white_check_mark: | :white_check_mark: | :white_check_mark: | :white_check_mark: |  :x: (1)   | :zap:<sup>1</sup> |
|     [Abstrackr](#abstrackr)     |        :x:         |        :x:         |        :x:         | :white_check_mark: |    :x:     |        :x:        |
|       [Colandr](#colandr)       |        :x:         |        :x:         |        :x:         | :white_check_mark: |  :x: (10)  |        :x:        |
| [EPPI-Reviewer](#eppi-reviewer) |        :x:         |        :x:         |        :x:         | :white_check_mark: |    :x:     |        :x:        |
|      [FASTREAD](#fastread)      |        :x:         |        :x:         |        :x:         | :white_check_mark: |    :x:     |        :x:        |
|        [Rayyan](#rayyan)        |        :x:         |        :x:         |        :x:         | :white_check_mark: |    :x:     |        :x:        |
|  [RobotAnalyst](#robotanalyst)  |        :x:         |        :x:         |        :x:         |        :x:         |    :x:     |        :x:        |
|  [SWIFT-Review](#swift-review)  |                    |                    |                    |                    |            |                   |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: With some effort (add a footnote with more explanation);

<sup>1</sup> Switching to a different model in ASReview is available by exporting the data of the first model and importing the data back into ASReview.
The software will recognize all previous labeling decisions, and a new model can be trained.


### Overview of Available Models

- Which feature extraction methods are available?
**BOW** = bag of words; 
**Doc2Vec** = document to vector; 
**sBERT** = sentence bidirectional encoder representations from transformers;
**TF–IDF** = term frequency–inverse document frequency; 
**Word2Vec** = words to vector; 
**ML** = Multi-language;

- Which classifiers are available?
**CNN** = convolutional neural network;
**DNN** = dense neural network; 
**LDA** = latent Dirichlet allocation; 
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
**A / Aggressive** = Aggressive undersampling balance strategy (after classifier is stable); 
**W / Weighting** = Weighting for data balancing (before and after classifier is stable);
**M / Mixing** = Mixing: weighting is applied before the classifier is stable and aggressive undersampling is applied after the classifier is stable;


- Which query strategies are available?
**R / Random** = Records are selected randomly;
**C / Certain** = Certainty based;
**U / Uncertain** = Uncertainty based;
**M / Mixed** = A combination of query strategies, for example 90% Certainty based and 10% Random;
**Cl / Clustering** = Clustering query strategy;



|            Software             |            Feature Extr.             |           Classifiers            |          Balancing          |  Query Stra.   |
|:-------------------------------:|:------------------------------------:|:--------------------------------:|:---------------------------:|:--------------:|
|      [ASReview](#asreview)      |  TF–IDF, Doc2Vec, sBert, TF-IDF, ML  | CNN, DNN, LR, LSTM, NB, RF, SVM  |         S, D, U, T          | R, C, U, M, CL |
|     [Abstrackr](#abstrackr)     |                TF-IDF :grey_question:<sup>1</sup>               |               SVM                |             :grey_question:<sup>1</sup>             |    R, C, U     |
|       [Colandr](#colandr)       | Word2Vec :grey_question:<sup>2</sup> | SGD :grey_question: <sup>2</sup> |             :grey_question:<sup>2</sup>             |       C        |
| [EPPI-Reviewer](#eppi-reviewer) |                TF-IDF                |               SVM                | :grey_question:<sup>3</sup> |    R, C, Cl    |
|      [FASTREAD](#fastread)      |                TF-IDF                |               SVM                |         S, A, W, M          |      C, U      |
|        [Rayyan](#rayyan)        |     :grey_question:<sup>4</sup>      |               SVM                | :grey_question:<sup>4</sup> |      C, U      |
|  [RobotAnalyst](#robotanalyst)  |        TF-IDF + BOW + LDA2vec        |               SVM                | :grey_question:<sup>5</sup> |  R, C, U, Cl   | 
|  [SWIFT-Review](#swift-review)  |                                      |                                  |                             |                |  


:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:grey_question: Unknown (requires an issue).

<sup>1</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/34

<sup>2</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/16

<sup>3</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/21

<sup>4</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/19

<sup>5</sup> See issues https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/29


## Supervised Learning

|                  Software                   | Feature Extr. |          Classifiers           |          Balancing          | Query Stra. |
|:-------------------------------------------:|:-------------:|:------------------------------:|:---------------------------:|:-----------:|
| [EPPI-Reviewer](#eppi-reviewer)<sup>1</sup> |    TF-IDF     | SVM:grey_question:<sup>2</sup> | :grey_question:<sup>1</sup> |  R, C, Cl   |

<sup>1</sup> EPPI-Reviewer offers the option to choose from, or use custom, pre-trained models to find a specific type of literature, e.g., for RCTs.

<sup>2</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/21

## Unsupervised Learning

| Software |     Q1      |
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

## [Abstrackr](https://github.com/bwallace/abstrackr-web)

Abstrackr is a collaborative (i.e., multiple reviewers can simultaneously
screen citations for a review), web-based annotation tool for the citation
screening task.

## [Colandr](https://hslib.jabsom.hawaii.edu/colandr)

Colandr is a free, web-based, open-access tool for conducting evidence
synthesis projects. 

## [EPPI-Reviewer](https://eppi.ioe.ac.uk/cms/Default.aspx?tabid=2914)

EPPI-Reviewer is a web-based software program for managing and analysing data
in literature reviews. It has been developed for all types of systematic
review (meta-analysis, framework synthesis, thematic synthesis etc) but also
has features that would be useful in any literature review. It manages
references, stores PDF files and facilitates qualitative and quantitative
analyses such as meta-analysis and thematic synthesis. It also contains some
new ‘text mining’ technology which is promising to make systematic reviewing
more efficient.

## [FASTREAD](https://github.com/fastread/src)

FASTREAD (FAST2) is a tool to support primary study selection in systematic
literature review.

## [Rayyan](https://www.rayyan.ai/)

Rayyan is a free web and mobile app, that helps expedite the initial screening 
of abstracts and titles using a process of semi-automation while incorporating 
a high level of usability.

## [RobotAnalyst](http://www.nactem.ac.uk/robotanalyst/)

RobotAnalyst was developed as part of the Supporting Evidence-based Public
Health Interventions using Text Mining project to support the literature
screening phase of systematic reviews.

## [SWIFT-Review](https://www.sciome.com/swift-review/) 

SWIFT-Review (SWIFT is an acronym for “Sciome Workbench for Interactive
computer-Facilitated Text-mining”) is a freely available interactive workbench
which provides numerous tools to assist with problem formulation and
literature prioritization.

# Contributing

Do you know other software that meets the inclusion criteria? Please make a
Pull Request and add it to the overview. When there is missing, wrong, or
incomplete information, please start an issue. 

# Licence

This project is CC-BY 4.0 licensed.

# Contact

For any suggestions, questions, or remarks, please file an issue in the issue
tracker.

This comparison is maintained by Rens van de Schoot. I aim to make a fair
comparison and not to be prejudiced. If there is any concern about the
comparison, please file an issue in the issue tracker such that it can be
openly discussed. 


