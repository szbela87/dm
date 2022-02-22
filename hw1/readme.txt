++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
dm_hw1_bjszekeres.ipynb
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

1st Exercise:
-------------


1st submission:
---------------
filename: submission_c1_t1_dectree_kaggle.csv

I used random forests with grid search cv after some data cleaning.
The best parameters were: max_depth=16, n_estimators=65.

kaggle score: 0.54967, rank: 4219

************************************************************************
2nd Exercise:
-------------


1st submission:
---------------
filename: submission_c2_t1_neural_kaggle.csv

I used a neural network here.

kaggle score: 0.58652, Hmmmmmm

!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
I guess, that I should check the scaling.
Maybe data are too clean
!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
dm_hw1_bjszekeres_v2.ipynb
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

I haven't submitted any Kaggle solutions, because the results weren't
better than earlier.

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
dm_hw1_bjszekeres_v3.ipynb
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Maybe we shouldn't take the log of the target `SalePrice`?
I checked, not this is the problem.

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
dm_hw1_bjszekeres_v4.ipynb
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
I'll use the approach of 
https://www.kaggle.com/pmarcelino/comprehensive-data-exploration-with-python

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
dm_hw1_bjszekeres_v5.ipynb
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Original approach.

`ExterCond_Po` is unnecessary. Its std is 0.0. Why???
I have to check the whole notebook carefully from the beginning.

Okay, I've found the problem:
when I push back the rows with missing categorical values,
I also dropped the non-missing columns of them.

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
dm_hw1_bjszekeres_v7.ipynb = dm_hw1_bjszekeres_final.ipynb
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Entries:
Stacked models:
1st competition: submission_1st_comp_3rd_trying.csv 
----------------
stacked random forests
2nd competition: submission_2nd_comp_2nd_trying.csv 
----------------
stacked by ridge regression: 2 xgb, 1 ridge, 3 svm
