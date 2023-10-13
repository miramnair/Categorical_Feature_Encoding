# Categorical_Feature_Encoding
Categorical_Feature_Encoding techniques

Read: https://medium.com/@miramnair/an-illustrative-example-of-encoding-categorical-features-5b1e1bf726b4

Count/Frequency Encoding
When to use?

1) When the algorithm is tree-based, like Decision trees, SVM, etc.

2) When the cardinality of a categorical feature is high, it means that the feature has a large number of unique categories or levels relative to the total number of data points.

When NOT to use?

Distance-based algorithms like linear regression and k-nearest neighbour (k-nn).


One Hot Encoding
When to use?

Nominal Categorical Data: One-hot encoding is suitable for nominal categorical data, where the categories have no inherent order or ranking. For example, colour, country, or breed of a dog are nominal attributes.
Sparse Data: If you have a reasonably large dataset and most of the categorical variables have a limited number of unique values, one-hot encoding can be a good choice. It creates sparse binary features, which can be efficient in terms of memory usage.
When NOT to use?

High Cardinality: If a categorical variable has a very high cardinality (a large number of unique categories), one-hot encoding can lead to a high-dimensional dataset, making the model training time-consuming and potentially problematic.
Tree-Based Models: While tree-based models can handle one-hot encoded data, they may not benefit significantly from one-hot encoding, and it can increase the tree depth without a substantial gain in predictive power. In such cases, label encoding or target encoding may be more efficient.



Label Encoding
When to use?

Ordinal Data: Label encoding is appropriate when you have ordinal categorical data, where there is a clear and meaningful order or ranking among the categories. For example, “low,” “medium,” and “high” can be encoded as 0, 1, and 2, respectively.
When NOT to use?

Nominal Data: Label encoding is not suitable for nominal categorical data, where the categories have no inherent order or ranking.
While label encoding is suitable for some machine learning algorithms, such as decision trees, it may not be the best choice for algorithms that rely on distance measures or where the magnitude of the numbers can impact the model’s performance.


Target Encoding/ Mean Encoding
When to use?

Target encoding can be beneficial when dealing with categorical features with high cardinality (a large number of unique categories).
Target encoding can be used effectively with tree-based models like decision trees, random forests, and gradient boosting, as these models are less sensitive to the potential leakage introduced by target encoding.
Target encoding is most useful when the categorical feature has predictive power, and the mean of the target variable varies significantly among categories. This is often the case in classification tasks where you want to capture the relationship between the categorical feature and the target.
When NOT to use?

Target encoding is not suitable for nominal categorical data with no apparent predictive power or relationship with the target variable.
Linear Models and Distance-Based Models: Linear regression and other linear models, as well as distance-based algorithms like k-nearest neighbors (KNN), may not be the best choices for target encoding due to the potential risk of overfitting and multicollinearity.


