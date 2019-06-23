# Binary-classifier-Widebot
* This is an evaluation task by Widebot. (https://widebot.net/)
* Using statistical machine learning models to fit the given training data and then evaluate models performance on the given Validation data.
* I didn't try using neural networks because they are data hungry and perform better than statistical algorithms only on large scale datasets.

## Assumptions:
* I assumed that we are more concerned with reducing false positives hence, focusing on predicting negative examples as negative.
* This assumption is based upon that the minor class is the negative ("No") class and it is more likely that learning algorithms just neglect the existance of the minor class and focus more on the major class.
## Metrics: (F0.5_score)
* Due to the unbalanced distribution of classes, where training examples belonging to class "YES" are much more than examples belonging to class "No", we cannot use accuracy as a metric because if we make a naive prediction that all examples belong to class "Yes", this would give a very high accuracy while in fact we are mispredicting all the negative examples.
* To tackle this problem, we shall use precision and recall or use Fbeta_score which is the harmonic mean of both precision and recall.
* I used beta=0.5 to give precision more weight thus fulfilling my assumption.

## Notes:
* An HTML version of the notebook is provided for viewing the project without need to install jupyter notebook.

## Requirements:

* To install all the requirements together, open command line and enter:
```bash
pip install -r requirements.txt
```
* You should also have jupyter notebook installed to run the notebook in edit mode.
