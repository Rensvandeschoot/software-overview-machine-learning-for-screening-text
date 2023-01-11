# Overview of software for screening large amounts of textual data implementing machine learning

The repository aims to create an overview and comparison of software used for
systematically screening large amounts of textual data using machine learning.
The process of the initial selection of the software tools is described on the 
[Open Science Framework](https://osf.io/g3nkz/). We encourage users to contribute 
to the overview by adding new software by using the nclusion criteria:

- employs a Reasearcher-in-the-Loop [(RITL)-based active learning cycle](https://www.nature.com/articles/s42256-020-00287-7) for systematically screening large amounts of textual data
- has a Technology Readiness level of at least [TRL7](https://en.wikipedia.org/wiki/Technology_readiness_level)
- user-friendly software is available
- application is generic and is not restricted to the content of one specific field or type of intervention

# Overview

The table below provides a quick overview of the software. The following
properties are evaluated:

-   Is there a website?
-	Is the software [open-source](https://opensource.org/osd) (provide a :link: to the source code)?
-	Is the software peer-reviewed in a scientific article?
-	Is documentation or a manual available (provide a :link:)?
-	Is the full version of the software free of charge?

|            Software             |                           Website                            |                         Open-Source                         |                               Published                                                                                        |                                    Documentation                                    |            Free             |
|:-------------------------------:|:------------------------------------------------------------:|:-----------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|:---------------------------:|
|     [Abstrackr](#abstrackr)     |          [:link:](http://abstrackr.cebm.brown.edu)           |                             :x:                             | [![DOI](https://img.shields.io/badge/DOI-10.1145/2110363.2110464-green.svg)](https://doi.org/10.1145/2110363.2110464)          |                                         :x:                                         |     :white_check_mark:      |
|      [ASReview](#asreview)      |                [:link:](https://asreview.nl/)                |  :white_check_mark:[:link:](https://github.com/asreview/)   | [![DOI](https://img.shields.io/badge/DOI-10.1038/s42256--020--00287--7-green.svg)](https://doi.org/10.1038/s42256-020-00287-7) |            :white_check_mark:[:link:](https://asreview.readthedocs.io/)             |     :white_check_mark:      |
|       [Colandr](#colandr)       |      [:link:](https://hslib.jabsom.hawaii.edu/colandr)       |                             :x:                             | [![DOI](https://img.shields.io/badge/DOI-10.1111/cobi.13117-green.svg)](https://doi.org/10.1111/cobi.13117)                    | :white_check_mark:[:link:](https://hslib.jabsom.hawaii.edu/colandr/getting_started) |     :white_check_mark:      |
|  [DistillerSR](#distillersr)    | [:link:](https://www.evidencepartners.com/) | :x: | [![DOI](https://img.shields.io/badge/DOI-10.1016/j.vhri.2020.07.479-green.svg)](https://doi.org/10.1016/j.vhri.2020.07.479)| :white_check_mark:[:link:](https://www.evidencepartners.com/resources) | :x:|
| [EPPI-Reviewer](#eppi-reviewer) | [:link:](https://eppi.ioe.ac.uk/cms/Default.aspx?tabid=2914) |                             :x:                             |                                  :x:                                                                                           |   :white_check_mark:[:link:](https://eppi.ioe.ac.uk/cms/Default.aspx?tabid=3822)    |             :x:             |
|      [FASTREAD](#fastread)      |                             :x:                              | :white_check_mark:[:link:](https://github.com/fastread/src) | [![DOI](https://img.shields.io/badge/DOI-10.1007/s10664--017--9587--0-green.svg)](https://doi.org/10.1007/s10664-017-9587-0)   |         :white_check_mark:[:link:](https://github.com/fastread/src/#readme)         |     :white_check_mark:      |
|        [Rayyan](#rayyan)        |               [:link:](https://www.rayyan.ai/)               |                             :x:                             | [![DOI](https://img.shields.io/badge/DOI-10.1186/s13643--016--0384--4-green.svg)](https://doi.org/10.1186/s13643-016-0384-4)   |             :white_check_mark:[:link:](https://help.rayyan.ai/hc/en-us)             |             :x:             |
|  [RobotAnalyst](#robotanalyst)  |       [:link:](http://www.nactem.ac.uk/robotanalyst/)        |                             :x:                             | [![DOI](https://img.shields.io/badge/DOI-10.1002/jrsm.1311-green.svg)](https://doi.org/10.1002/jrsm.1311)                      |                                         :x:                                         | :grey_question:<sup>1</sup> |
| [SWIFT-Active Screener](#swift-activescreener) |    [:link:](https://www.sciome.com/swift-activescreener/)    |                             :x:                             | [![DOI](https://img.shields.io/badge/DOI-10.1016/j.envint.2020.105623-green.svg)](https://doi.org/10.1016/j.envint.2020.105623) | :white_check_mark:[:link:](https://www.sciome.com/swift-activescreener/knowledgebase/) |             :x:             |


:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:grey_question: Unknown (requires an issue).

<sup>1</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/29

# Installation

The table below provides an overview of options for how to install the software.

- Can the software be installed locally so that data and labeling decisions are only stored on the user's device (yes/no)?
- Is the software installable on a server (yes/no)?
- Is the software available as online service (software as a service - SAAS; yes/no; provide a link to the registration page)?

|                    Software                    |       Local        |       Server       |                                             Online Service                                              |
|:----------------------------------------------:|:------------------:|:------------------:|:-------------------------------------------------------------------------------------------------------:|
|            [Abstrackr](#abstrackr)             |        :x:         |        :x:         |                       :white_check_mark:[:link:](http://abstrackr.cebm.brown.edu)                       |
|             [ASReview](#asreview)              | :white_check_mark: | :white_check_mark: |                                                   :x:                                                   |
|              [Colandr](#colandr)               |        :x:         |        :x:         |                         :white_check_mark:[:link:](https://www.colandrapp.com/)                         |
|          [DistillerSR](#distillersr)           |        :x:         |        :x:         | :white_check_mark:[:link:](https://www.distillersr.com/products/distillersr-systematic-review-software) |
|        [EPPI-Reviewer](#eppi-reviewer)         |        :x:         |        :x:         |                           :white_check_mark:[:link:](https://eppi.ioe.ac.uk/)                           |
|             [FASTREAD](#fastread)              | :white_check_mark: | :white_check_mark: |                                                   :x:                                                   |
|               [Rayyan](#rayyan)                |        :x:         |        :x:         |                           :white_check_mark:[:link:](https://www.rayyan.ai/)                            |
|         [RobotAnalyst](#robotanalyst)          |        :x:         |        :x:         |              :white_check_mark:[:link:](http://www.nactem.ac.uk/robotanalyst/)<sup>1</sup>              |
| [SWIFT-Active Screener](#swift-activescreener) |        :x:         |        :x:         |                          :x:[:link:](https://swift.sciome.com/activescreener/)                          |  


:white_check_mark: Yes;
:x: No;
:grey_question: Unknown (requires an issue).

<sup>1</sup> To use RobotAnalyst, you need to request an account via email.

# Data

The table below provides an overview of input/output data.

- Which data formats can be imported?
- Can partly labeled data be imported (yes/no; if yes, as **S**(ingle) or **M**(ultiple) files)?
- Which data formats can be exported?
- Does the export file contain the labeling decisions?
- Can the export file be re-imported into the same software, retaining the labeling decisions (Re-Import-1: yes/no)?
- Can the export file be re-imported into reference manager software retaining, the labeling decision (Re-Import-2: yes/no)?

|                    Software                    |             Input data format             |                Partly labeled                 |     Output data format      |     Labeling decisions      |         Re-Import-1         |         Re-Import-2         |
|:----------------------------------------------:|:-----------------------------------------:|:---------------------------------------------:|:---------------------------:|:---------------------------:|:---------------------------:|:---------------------------:|
|            [Abstrackr](#abstrackr)             |         RIS, TAB, TXT<sup>1</sup>         |                      :x:                      |        CSV, XML, RIS        |     :white_check_mark:      |             :x:             |     :white_check_mark:      |
|             [ASReview](#asreview)              | RIS, TSV, CSV, XLSX, TAB, `+`<sup>2</sup> |     :white_check_mark:(S)`+`<sup>2</sup>      |  RIS, TSV, CSV, XLSX, TAB   |     :white_check_mark:      |     :white_check_mark:      |     :white_check_mark:      |
|              [Colandr](#colandr)               |               RIS, BIB, TXT               |             :white_check_mark:(M)             |             CSV             |     :white_check_mark:      |             :x:             |             :x:             |
|          [DistillerSR](#distillersr)           |            ENLX, RIS, CSV, ZIP            |             :white_check_mark:(M)             |    RIS, CSV, XLSX, Word     | :grey_question:<sup>4</sup> | :grey_question:<sup>4</sup> | :grey_question:<sup>4</sup> |
|        [EPPI-Reviewer](#eppi-reviewer)         |         RIS, TXT, `+`<sup>3</sup>         |             :white_check_mark:(M)             |          RIS, XLSX          | :grey_question:<sup>5</sup> | :grey_question:<sup>5</sup> | :grey_question:<sup>5</sup> |
|             [FASTREAD](#fastread)              |                    CSV                    |             :white_check_mark:(S)             |             CSV             |     :white_check_mark:      |     :white_check_mark:      |             :x:             |
|               [Rayyan](#rayyan)                |    RIS, ENW, BIB, CSV, XML, CIW, NBIB     |             :white_check_mark:(M)             |     RIS, BIB, ENW, CSV      |     :white_check_mark:      |             :x:             |     :white_check_mark:      |
|         [RobotAnalyst](#robotanalyst)          |                 RIS, NBIB                 | :white_check_mark::grey_question:<sup>6</sup> | :grey_question:<sup>6</sup> |     :white_check_mark:      | :grey_question:<sup>6</sup> |             :x:             |
| [SWIFT-Active Screener](#swift-activescreener) |           TXT, RIS, XML, BibTex           |             :white_check_mark:(M)             |          CSV, RIS           |     :white_check_mark:      | :grey_question:<sup>7</sup> |     :white_check_mark:      |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: Only for some extensions (add a footnote for more explanation);
:grey_question: Unknown (requires an issue).

<sup>1</sup> List of PubMed IDs

<sup>2</sup> ASReview provides several open-source tools to convert file formats (e.g., CSV->RIS or RIS->XLSX), combine datasets (labeled, partly labeled, or unlabeled), and deduplicate records based on title/abstract/DOI.

<sup>3</sup> EPPI-Reviewer provides a closed-source [online file converter](https://eppi.ioe.ac.uk/cms/Default.aspx?tabid=2934) to convert several file formats to RIS.

<sup>4</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/54

<sup>5</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/21

<sup>6</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/29

<sup>7</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/40




# Machine Learning Properties

The tables below provide an overview of the machine learning properties.


## Active Learning

### Training Data

- Can training data (prior knowledge) be selected by the user to train the first iteration of the model (yes/no)?
- What is the minimal training data size (provide a number for **R**elevant and **I**rrelevant records)?



|                    Software                    |        Tr.Data by user         |                 Minimum Tr.data                  |
|:----------------------------------------------:|:------------------------------:|:------------------------------------------------:|
|            [Abstrackr](#abstrackr)             |              :x:               |           :grey_question:<sup>1</sup>            |
|             [ASReview](#asreview)              |       :white_check_mark:       |                     ≥1R+≥1I                      |
|              [Colandr](#colandr)               |       :white_check_mark:       |                        10                        |
|          [DistillerSR](#distillersr)           |       :white_check_mark:       | 25 or 2%<sup>2</sup> :grey_question:<sup>3</sup> |
|        [EPPI-Reviewer](#eppi-reviewer)         |       :white_check_mark:       |                       ≥5R                        |
|             [FASTREAD](#fastread)              |       :white_check_mark:       |                       ≥1R                        |
|               [Rayyan](#rayyan)                |       :white_check_mark:       |                   ≥50 with ≥5R                   |
|         [RobotAnalyst](#robotanalyst)          |       :white_check_mark:       |                       ≥1R                        |
| [SWIFT-Active Screener](#swift-activescreener) | :white_check_mark:<sup>4</sup> |                 ≥1R<sup>5</sup>                  |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: With some effort (add a footnote for more explanation);
:grey_question: Unknown (requires an issue).

<sup>1</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/34

<sup>2</sup> Training takes place after screening 25 records or after screening 2% of the dataset, whichever is greater.

<sup>3</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/54

<sup>4</sup> Only relevant records can be provided as training data prior to screening.

<sup>5</sup> If no relevant records are uploaded prior to screening, training will be initiated after screening ≥30 records with atleast ≥1R and ≥1I.

### Model Selection

- Can the user select the active learning model (yes/no)?
- Can a user upload their own model (yes/no)?
- Can the feature extraction results be stored (yes/no)?
- Does (re-)training proceed **A**utomatically or is it triggered **M**anually?
- Can the user continue labeling during training (yes/no)?
- Can the user select batch size (yes/no; provide the default)?
- Is it possible to switch to a different model during screening (yes/no)?


|                    Software                    |    Select model    |     User model     | Store Feat.matrix  | Training |          Continue           | Batch size |      Switch       |
|:----------------------------------------------:|:------------------:|:------------------:|:------------------:|:--------:|:---------------------------:|:----------:|:-----------------:|
|            [Abstrackr](#abstrackr)             |        :x:         |        :x:         |        :x:         |    A     |     :white_check_mark:      |    :x:     |        :x:        |
|             [ASReview](#asreview)              | :white_check_mark: | :white_check_mark: | :white_check_mark: |    A     |     :white_check_mark:      |  :x: (1)   | :zap:<sup>1</sup> |
|              [Colandr](#colandr)               |        :x:         |        :x:         |        :x:         |    A     |     :white_check_mark:      |  :x: (10)  |        :x:        |
|          [DistillerSR](#distillersr)           |        :x:         |        :x:         |        :x:         |   A, M   |     :white_check_mark:      |    :x:     |        :x:        |
|        [EPPI-Reviewer](#eppi-reviewer)         |        :x:         |        :x:         |        :x:         |    M     |     :white_check_mark:      |    :x:     |        :x:        |
|             [FASTREAD](#fastread)              |        :x:         |        :x:         |        :x:         |    M     |             :x:             |    :x:     |        :x:        |
|               [Rayyan](#rayyan)                |        :x:         |        :x:         |        :x:         |    M     |     :white_check_mark:      |    :x:     |        :x:        |
|         [RobotAnalyst](#robotanalyst)          |        :x:         |        :x:         |        :x:         |    M     | :grey_question:<sup>2</sup> |    :x:     |        :x:        |
| [SWIFT-Active Screener](#swift-activescreener) |        :x:         |        :x:         |        :x:         |    A     | :grey_question:<sup>3</sup> |  :x: (30)  |        :x:        |

:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:zap: With some effort (add a footnote with more explanation);

<sup>1</sup> Switching to a different model in ASReview is available by exporting the data of the first model and importing the data back into ASReview.
The software will recognize all previous labeling decisions, and a new model can be trained.

<sup>2</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/29

<sup>3</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/40


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
**LL** = log linear;
**LR**= logistic regression;
**LSTM** = long short-term memory;
**NB** = naive Bayes;
**RF** =random forests;
**SGD** = stochastic gradient descent;
**SVM** = support vector machine;


- Which balancing strategies are available?
**S / Simple** = no balancing balance strategy;
**D / Double** = Double balance strategy;
**T / Triple** = Triple balance strategy;
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



|                    Software                    |            Feature Extr.             |           Classifiers            |          Balancing           |         Query Stra.         |
|:----------------------------------------------:|:------------------------------------:|:--------------------------------:|:----------------------------:|:---------------------------:|
|            [Abstrackr](#abstrackr)             |  TF-IDF :grey_question:<sup>1</sup>  |               SVM                | :grey_question:<sup>1</sup>  |           R, C, U           |
|             [ASReview](#asreview)              |  TF–IDF, Doc2Vec, sBert, TF-IDF, ML  | CNN, DNN, LR, LSTM, NB, RF, SVM  |          S, D, U, T          |       R, C, U, M, CL        |
|              [Colandr](#colandr)               | Word2Vec :grey_question:<sup>2</sup> | SGD :grey_question: <sup>2</sup> | :grey_question:<sup>2</sup>  |              C              |
|          [DistillerSR](#distillersr)           |     :grey_question:<sup>3</sup>      |   :grey_question:<sup>3</sup>    | :grey_question:<sup>3</sup>  | :grey_question:<sup>3</sup> |
|        [EPPI-Reviewer](#eppi-reviewer)         |                TF-IDF                |               SVM                | :grey_question:<sup>4</sup>  |          R, C, Cl           |
|             [FASTREAD](#fastread)              |                TF-IDF                |               SVM                |          S, A, W, M          |            C, U             |
|               [Rayyan](#rayyan)                |     :grey_question:<sup>5</sup>      |               SVM                | :grey_question:<sup>5</sup>  |            C, U             |
|         [RobotAnalyst](#robotanalyst)          |        TF-IDF + BOW + LDA2vec        |               SVM                | :grey_question:<sup>6</sup>  |         R, C, U, Cl         |
| [SWIFT-Active Screener](#swift-activescreener) |                TF-IDF                |                LL                | S:grey_question:<sup>7</sup> |              C              |  


:white_check_mark: Yes/Implemented;
:x: No/Not implemented;
:grey_question: Unknown (requires an issue).

<sup>1</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/34

<sup>2</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/16

<sup>3</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/54

<sup>4</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/21

<sup>5</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/19

<sup>6</sup> See issues https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/29

<sup>7</sup> See issues https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/40


## Supervised Learning

|                  Software                   | Feature Extr. |          Classifiers           |          Balancing          | Query Stra. |
|:-------------------------------------------:|:-------------:|:------------------------------:|:---------------------------:|:-----------:|
| [EPPI-Reviewer](#eppi-reviewer)<sup>1</sup> |    TF-IDF     | SVM:grey_question:<sup>2</sup> | :grey_question:<sup>2</sup> |  R, C, Cl   |

<sup>1</sup> EPPI-Reviewer offers the option to choose from, or use custom, pre-trained models to find a specific type of literature, e.g., for RCTs.

<sup>2</sup> See issue https://github.com/Rensvandeschoot/software-overview-machine-learning-for-screening-text/issues/21

## Unsupervised Learning

| Software |     Q1      |
|:--------:|:-----------:|

# Software

This section briefly describes the software in alphabetical order.

## [Abstrackr](https://github.com/bwallace/abstrackr-web)

Abstrackr is a collaborative (i.e., multiple reviewers can simultaneously
screen citations for a review), web-based annotation tool for the citation
screening task.

## [ASReview](www.asreview.nl)

ASReview, developed at Utrecht University, helps scholars and practitioners
to get an overview of the most relevant records for their work as efficiently
as possible while being transparent in the process. It allows multiple
machine learning models, and ships with exploration and simulation modes,
which are especially useful for comparing and designing algorithms.
Furthermore, it is intended to be easily extensible, allowing third parties
to add modules that enhance the pipeline with new models, data, and other
extensions.

## [Colandr](https://hslib.jabsom.hawaii.edu/colandr)

Colandr is a free, web-based, open-access tool for conducting evidence
synthesis projects.

## [DistillerSR](https://www.evidencepartners.com/products/distillersr-systematic-review-software)

DistillerSR automates the management of literature collection, screening, and assessment using AI and intelligent workflows. From a systematic literature review to a rapid review to a living review, DistillerSR makes any project simpler to manage and configure to produce transparent, audit-ready, and compliant results.


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

## [SWIFT-Active Screener](https://www.sciome.com/swift-activescreener/)

SWIFT-Active Screener (SWIFT is an acronym for “Sciome Workbench for Interactive
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
