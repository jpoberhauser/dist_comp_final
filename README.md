# Distributed Machine Learning with PySpark


This project takes in a csv of NBA data, with 128,069 rows and several features including:

1. Player that took the shot

2. Distance from the rim

3. Whether the player was being guarded and by who

4. Team data

5. Among other features


The goal of this project is to use PySpark and SparkML to make a *classifier* that returns the probability that a shot is made given a set of inout features. 


As one can see in the file `DataViz.ipynb`  (and almost expect), one of the most predictive features is the distance from the rim. 
In that notebook, I have included the distribution of the response based on that feature. 


Using the following spark modules and helpers to build classifiers with good accuracy and a prediction pipeline:

```from pyspark.ml.linalg import Vectors, VectorUDT
from pyspark.ml.evaluation import MulticlassClassificationEvaluator
from pyspark.ml.classification import GBTClassifier
from pyspark.ml import Pipeline
```

Along with the following modules to get cross validation errors and a parameter grid to do a hyper-parameter optimization grid. 

```
from pyspark.ml.tuning import CrossValidator
from pyspark.ml.tuning import ParamGridBuilder
```

Achieved area under the ROC curve of 0.63
