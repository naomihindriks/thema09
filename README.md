# README Thema09: Building a classifier with Weka #

### What is this repository for? ###

This repository is made to publish the report that lead to the development of [this Breast Cancer Classifier](https://github.com/naomihindriks/java_wrapper). The log file [EDA_log_NaomiHindriks.pdf](https://github.com/naomihindriks/thema09/blob/main/EDA_log_NaomiHindriks.pdf) reports on the steps taken to explore and filter the data and test different learning algorithms. The subsequent report [Verslag_Naomi_Hindriks.pdf](https://github.com/naomihindriks/thema09/blob/main/Verslag_Naomi_Hindriks.pdf). These files can be rendered with the Rmarkdown files [EDA_log_NaomiHindriks.rmd](https://github.com/naomihindriks/thema09/blob/main/EDA_log_NaomiHindriks.rmd) and [Verslag_Naomi_Hindriks.Rmd](https://github.com/naomihindriks/thema09/blob/main/Verslag_Naomi_Hindriks.Rmd) respectively. The data folder contains all the data that is necessary to render the Rmarkdown files, below will follow a discription of these files. This repository is made to publish the report that lead to the development of [this Breast Cancer Classifier](https://github.com/naomihindriks/java_wrapper). The log file [EDA_log_NaomiHindriks.pdf](https://github.com/naomihindriks/thema09/blob/main/EDA_log_NaomiHindriks.pdf) reports on the steps taken to explore and filter the data and test different learning algorithms. The subsequent report [Verslag_Naomi_Hindriks.pdf](https://github.com/naomihindriks/thema09/blob/main/Verslag_Naomi_Hindriks.pdf). These files can be rendered with the Rmarkdown files [EDA_log_NaomiHindriks.rmd](https://github.com/naomihindriks/thema09/blob/main/EDA_log_NaomiHindriks.rmd) and [Verslag_Naomi_Hindriks.Rmd](https://github.com/naomihindriks/thema09/blob/main/Verslag_Naomi_Hindriks.Rmd) respectively. The data folder contains all the data that is necessary to render the Rmarkdown files, below will follow a discription of these files. The ieee.csl and references.bib files are used in the report to cite the resources that were used. The report is published under the  [GNU GENERAL PUBLIC LICENSE](https://github.com/naomihindriks/thema09/blob/main/LICENSE).

Data folder:

- [breast-cancer-wisconsin.data](https://github.com/naomihindriks/thema09/blob/main/data/breast-cancer-wisconsin.data)
  - This is the file that contains the original data downloaded from the [UCI machine learning repository](https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+%28original%29)
- [breast-cancer-wisconsin.names](https://github.com/naomihindriks/thema09/blob/main/data/breast-cancer-wisconsin.names)
  - This is the file that contains information about the original data, explaining the different attributes. Also downloaded from the [UCI machine learning repository](https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+%28original%29)
- [attribute_info.csv](https://github.com/naomihindriks/thema09/blob/main/data/attribute_info.csv)
    - CSV file with information derived from [breast-cancer-wisconsin.names](https://github.com/naomihindriks/thema09/blob/main/data/breast-cancer-wisconsin.names) to be used to couple the correct data to the correct attribute name.
- [filtered_data.arff](https://github.com/naomihindriks/thema09/blob/main/data/filtered_data.arff)
  - The breast-cancer-wisconsin data after the filtering steps as described in the [EDA_log_NaomiHindriks.pdf](https://github.com/naomihindriks/thema09/blob/main/EDA_log_NaomiHindriks.pdf) is saved in this file.
- [Classification_options_experiment.exp](https://github.com/naomihindriks/thema09/blob/main/data/Classification_options_experiment.exp)
  - The options of the first experiment that can be loaded into weka as explained in the [EDA_log_NaomiHindriks.pdf](https://github.com/naomihindriks/thema09/blob/main/EDA_log_NaomiHindriks.pdf).
- [ROC.arff](https://github.com/naomihindriks/thema09/blob/main/data/ROC.arff)
  - File that holds information to make ROC curve for final algorithm exported from weka while running cross validation on final algorithm.
- [ROC-curve.png]()
  - Image used in [EDA_log_NaomiHindriks.pdf](https://github.com/naomihindriks/thema09/blob/main/EDA_log_NaomiHindriks.pdf), [this is where is was downloaded from](https://commons.wikimedia.org/wiki/File:Roc-draft-xkcd-style.svg)
- All the other ARFF files are the experiments that were run in Weka and loaded into [EDA_log_NaomiHindriks.pdf](https://github.com/naomihindriks/thema09/blob/main/EDA_log_NaomiHindriks.pdf) to evaluate the performance of the different algorithms:
  - [weka_experiment.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment.arff)
  - [weka_experiment_IBK_KNN.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_IBK_KNN.arff)
  - [weka_experiment_IBK_attributeSelect.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_IBK_attributeSelect.arff)
  - [weka_experiment_IBK_boosting.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_IBK_boosting.arff)
  - [weka_experiment_IBK_crossValidate.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_IBK_crossValidate.arff)
  - [weka_experiment_IBK_distanceMetric.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_IBK_distanceMetric.arff)
  - [weka_experiment_IBK_distanceWeight.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_IBK_distanceWeight.arff)
  - [weka_experiment_naive_bayes_boosting.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_naive_bayes_boosting.arff)
  - [weka_experiment_naive_bayes_useSupervisedDiscretization.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_naive_bayes_useSupervisedDiscretization.arff)
  - [weka_experiment_voting.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_voting.arff)
  - [weka_experiment_voting_cost.arff](https://github.com/naomihindriks/thema09/blob/main/data/weka_experiment_voting_cost.arff)

### Contact information ###

Naomi Hindriks
n.j.hindriks@st.hanze.nl