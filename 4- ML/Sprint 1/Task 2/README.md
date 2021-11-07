# 1- What ’re the methods that you used ?

<ul>
  <li> Functions used in <b> Machine Learning package:</b> </li>
  <ul>
    <li>sklearn.model_selection.train_test_split(*arrays, **options)</li>
  </ul>
 </ul>

# 2- Explain each method ..

|Parameters|            <b>sklearn.model_selection.train_test_split(*arrays, **options)</b>|
|----------|-------------------------------------------------|
|arrays: sequence of indexables with same length / shape[0] | Allowed inputs are lists, numpy arrays, scipy-sparse matrices or pandas dataframes.|
|test_size: float or int, default=None| If float, should be between 0.0 and 1.0 and represent the proportion of the dataset to include in the test split. If int, represents the absolute number of test samples. If None, the value is set to the complement of the train size. If train_size is also None, it will be set to 0.25.|
|train_size : float or int, default=None| If float, should be between 0.0 and 1.0 and represent the proportion of the dataset to include in the train split. If int, represents the absolute number of train samples. If None, the value is automatically set to the complement of the test size.|
|random_state : int or RandomState instance, default=None| Controls the shuffling applied to the data before applying the split. Pass an int for reproducible output across multiple function calls. See Glossary.|
|shuffle: bool, default=True| Whether or not to shuffle the data before splitting. If shuffle=False then stratify must be None.|
|stratify : array-like, default=None| If not None, data is split in a stratified fashion, using this as the class labels.|
|**Returns**||
|splitting: list, length=2 * len(arrays)| List containing train-test split of inputs.|
|New in version 0.16| If the input is sparse, the output will be a scipy.sparse.csr_matrix. Else, output type is the same as the input type.|

# 3- What’s new for you ?
> <ul>
> All Of Them is new for me.
> </ul>

# 4- Resources ? 

> [https://www.coursera.org/learn/python-machine-learning/ungradedLab/2mey1/module-1-notebook]
> [https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html]


