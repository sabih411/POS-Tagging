# POS-Tagging
Course Work of CMPSC-448 (The Pennsylvania State University)

Consider opening the .ipynb notebook on Goole Colab[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sabih411/POS-Tagging/blob/main/POS_TAGGING.ipynb) for best code-interface. Code is well structured in Sections and in cells under the corresponding sections. To Properly understand the organization of code in the .ipynb notebook, see the snippet below!

![image](https://github.com/sabih411/POS-Tagging/assets/47940851/c7bd5cf9-c830-43db-8a20-1d9eeed96ba9)

**Important Notes:** 
  * Five Models which integrate the whole solution are as follows:
      * (model_lr)        : A Logistic Regression Model trained with a big set of commonly used features.
      * (model_svm)       : A SVM Model trained with a big set of commonly used features.
      * (model_nb)        : A Multinomial Naive Bayes Model trained with a big set of commonly used features.
      * (model_nb_small)  : A Multinomial Naive Bayes Model trained with a appearance/styling related features.
      * (model_lr_vect)   : A Logistic Regression Model trained with a self trained word2vec analogous features.  
  * For testing alone, you have to have the dict vectorizers loaded to be able to transform the data, therefore you need to run the code segment under Model Initialization.
  * The model checkpoint files can be found in the [POST_TAGS_WEIGHT folder](https://drive.google.com/drive/folders/1a9RY7aDCHKERN2W486lcs5ojQdOhRwzu?usp=sharing). The organization of the weights folder is shown below. 
  ```
    |POS_TAGS_WEIGHT
      |->model_lr.pickle  
      |->model_svm.pickle
      |->model_nb.pickle
      |->model_nb_small.pickle
      |->model_lr_vect.pickle
      |->word2vec.model   #Weight file of gensim FastText
  ```
  * The code shows two evaluation strategies and based on Dev-set performance the  latter one (Best Probabilistic Difference strategy) was selected for evaluating the Test Data.
