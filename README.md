We have a numerical feature and want to break it up into discrete bins, Depending on how we want to break up the data, there are two techniques we can use. First, we can
binarize the feature according to some threshold, Second, we can break up numerical features according to multiple thresholds, Note that the arguments for the bins parameter denote the left edge of each bin. For example, the 20
argument does not include the element with the value of 20, only the two values smaller than 20. We can switch this behavior by setting the parameter right to True Discretization can be a fruitful strategy when we have reason to believe that a numerical feature should
behave more like a categorical feature. For example, we might believe there is very little difference in
the spending habits of 19- and 20-year-olds, but a significant difference between 20- and 21-year-olds
(the age in the United States when young adults can consume alcohol). In that example, it could be
useful to break up individuals in our data into those who can drink alcohol and those who cannot.
Similarly, in other cases it might be useful to discretize our data into three or more bins.
In the solution, we saw two methods of discretization—scikit-learn’s Binarizer for two bins and
NumPy’s digitize for three or more bins—however, we can also use digitize to binarize features
like Binarizer by only specifying a single threshold
