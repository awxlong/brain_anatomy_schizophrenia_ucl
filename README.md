# Benchmarking models for predicting schizophrenia using brain anatomy

For a more detailed breakdown of the competition rationale, please visit the [original repository's README file](https://github.com/ramp-kits/brain_anatomy_schizophrenia)

This is our solution submitted to a competition hosted by [RAMP-Studio](https://ramp.studio/problems/brain_anatomy_schizophrenia). The relevant files are:

- brain_schizophrenia_f1.ipynb:
  - contains the main code for benchmarking a plethora of models with hyperparameters tuned via Bayesian optimization.
  - We also propose a more suitable scoring method using F1 for binary classification in addition to balanced accuracy, to replace ROC-AUC, which is flawed for not taking class imbalance into account
  - We also run experiments comparing standard K-Fold cross-validation, group-stratified K-Fold cross-validation
 
- log reg is all you need.pdf:
  - a brief presentation sharing my approach which achieved 3rd place before the RAMP-Studio competition deadline achieving a cross-validation score of 0.77 balanced accuracy.
 
- estimator.py:
  - contains several models we've submitted, with the best model (after the competition deadline) being an precomputed RBF-kernel SVM achieving a .82 cross-validation balanced accuracy

- PS: for you to rerun the brain_Schizophrenia_f1.ipynb notebook, you may have to use the skopt_edited library I uploaded. There is some deprecation warning issues when trying to use `BayesSearchCV`, please see this [StackOverflow question](https://stackoverflow.com/questions/76321820/how-to-fix-the-numpy-int-attribute-error-when-using-skopt-bayessearchcv-in-sci). 
 
