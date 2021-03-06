# Automatic Model Tuning<a name="automatic-model-tuning"></a>

Amazon SageMaker automatic model tuning, also known as hyperparameter tuning, finds the best version of a model by running many training jobs on your dataset using the algorithm and ranges of hyperparameters that you specify\. It then chooses the hyperparameter values that result in a model that performs the best, as measured by a metric that you choose\.

For example, suppose that you want to solve a binary classiﬁcation problem on a marketing dataset\. Your goal is to maximimize the area under the curve \(auc\) metric of the algorithm by training an [XGBoost Algorithm](xgboost.md) model\. You don't know which values of the `eta`, `alpha`, `min_child_weight`, and `max_depth` hyperparameters to use to train the best model\. To find the best values for these hyperparameters, you can specify ranges of values to search\. Hyperparameter tuning launches training jobs that use hyperparameter values in the ranges that you specified, and returns the training job with highest auc\. You can then deploy the trained model that training job created\.

You can use Amazon SageMaker automatic model tuning with built\-in algorithms, custom algorithms, and Amazon SageMaker pre\-built containers for machine learning frameworks\.

Before you start using hyperparameter tuning, you a well\-defined machine learning problem, including the following:
+ A dataset
+ An understanding of the type of algorithm you need to train
+ A clear understanding of how you measure success

You should also prepare your dataset and algorithm so that they work in Amazon SageMaker and successfully run a training job at least once\. For information about setting up and running a training job, see [Train a Model with a Built\-in Algorithm and Deploy It](ex1.md)\.

**Topics**
+ [How Hyperparameter Tuning Works](automatic-model-tuning-how-it-works.md)
+ [Defining Objective Metrics](automatic-model-tuning-define-metrics.md)
+ [Defining Hyperparameter Ranges](automatic-model-tuning-define-ranges.md)
+ [Example: Hyperparameter Tuning Job](automatic-model-tuning-ex.md)
+ [Design Considerations](automatic-model-tuning-considerations.md)