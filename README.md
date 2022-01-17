# Introduction

A large company named XYZ, employs, at any given point of time, around 4000
employees. However, every year, around 15% of its employees leave the company
and need to be replaced with the talent pool available in the job market. The
management believes that this level of attrition (employees leaving, either on
their own or because they got fired) is bad for the company, because of the
following reasons:

1. The former employees’ projects get delayed, which makes it difficult to meet
   timelines, resulting in a reputation loss among consumers and partners 

2. A sizeable department has to be maintained, for the purposes of recruiting
   new talent

3. More often than not, the new employees have to be trained for the job and/or
   given time to acclimatise themselves to the company

*The goal is to model the probability of attrition given the data at disposal.*

The results thus obtained will be used by the management to understand what
changes they should make to their workplace, in order to get most of their
employees to stay.

# Dataset

The dataset used in this study can be found on
[kaggle](https://www.kaggle.com/vjchoudhary7/hr-analytics-case-study) or here
(inside the dataset folder).

# Results

The results can be found in the notebook, but, in summary, in this study it was
possible to get a RandomForestClassifier (from sklearn) with 99 % accuracy, and
99 % precision, 96 % recall and 97 % f1-score macro averages validated with a 30
% split of the data.

# Model

The pre-trained model (trained with all the data) can be found under the model
folder, wich can be loaded with `pickle` like:

```python
import pickle

with open('./model/pretrained.pkl', 'rb') as f:
    model = pickle.load(f)
```

# Replicate

If you want to replicate the results you can by doing:

    git clone https://github.com/saul44203/HR-Analytics-Case-Study

and then executing the notebook provided inside the repository root with:

    jupyter-notebook notebook.ipynb

You can make sure you have all the necessary libraries first by doing:

    pip install -r requeriments.txt
