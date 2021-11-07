# 1- What ’re the methods that you used ?

<ul>
  <li> Functions from the <b>Heart Disease UCI</b> </li>
  <ul>
    <li>pd.crosstab(df.target,df.sex)</li>
    <li>sns.heatmap(corr_mat,annot=True,linewidths=0.5)</li>
    <li>np.random.seed(42)</li>
    <li>KNeighborsClassifier()</li>
    <li>np.logspace(-4,4,20)</li>
    <li>RandomizedSearchCV(LogisticRegression(),param_distributions=log_reg_grid,cv=5,n_iter=20,verbose=True)</li>
    </ul>
  </ul>

# 2- Explain each method ..

|            <b>Function</b>                |                                       <b>Discription</b>                                |
|-------------------------------------------|-----------------------------------------------------------------------------------------|
|pd.crosstab(df.target,df.sex)|Compute a simple cross tabulation of two (or more) factors. By default computes a frequency table of the factors unless an array of values and an aggregation function are passed.|
|sns.heatmap(corr_mat,annot=True,linewidths=0.5)|create heatmap|
|np.random.seed(42)|It's just to make sure that you obtain the same split everytime you run your script(To reproduced the randomized data again), a fixed value will guarantee that same sequence of random numbers are generated each time you run the code. And unless there is some other randomness present in the process, the results produced will be same as always. This helps in verifying the output.|
|KNeighborsClassifier()|train the model with the help of KNeighborsClassifier class of sklearn|
|knn.set_params(n_neighbors = i)|sets the parameter of the estimator using this dict. Return value must be estimator itself.|
|knn.fit(X_train,y_train)|sets data-independent parameters (overriding previous parameter values passed to __init__).|
|np.logspace(-4,4,20)|function return numbers spaced evenly on a log scale|
|RandomizedSearchCV(LogisticRegression(),<br> param_distributions=log_reg_grid,cv=5,n_iter=20,verbose=True)|Setup random hyperparameter search for RandomForestClassifier and implements a “fit” and a “score” method. It also implements “predict”, “predict_proba”, “decision_function”, “transform” and “inverse_transform” if they are implemented in the estimator used.The parameters of the estimator used to apply these methods are optimized by cross-validated search over parameter settings.|



# 3- What’s new for you ?
> <ul>
> <li>pd.crosstab(df.target,df.sex)</li>
> <li>sns.heatmap(corr_mat,annot=True,linewidths=0.5)</li>
> <li>np.random.seed(42)</li>
> <li>KNeighborsClassifier()</li>
> <li>np.logspace(-4,4,20)</li>
> <li>RandomizedSearchCV(LogisticRegression(),param_distributions=log_reg_grid,cv=5,n_iter=20,verbose=True)</li>
> </ul>

# 4- Resources ? 

> [https://www.w3resource.com/] 
> [https://docs.python.org/2/library/re.html]
> [https://pandas.org/doc/stable/] 
> [https://www.datacamp.com/]
> [http://rasbt.github.io/mlxtend/user_guide/preprocessing/minmax_scaling/]
