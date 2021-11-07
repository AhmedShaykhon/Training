# 1- What ’re the methods that you used ?

<ul>
  <li> Functions from the <b>Feature Engineering</b> </li>
  <ul>
    <li>ks = ks.query('state != "live"')</li>
    <li>ks = ks.assign(outcome=(ks['state'] == 'successful').astype(int))</li>
    <li>X_train.select_dtypes(exclude=['object']</li>
    <li>LabelEncoder()</li>
    <li>score_dataset(drop_X_train, drop_X_valid, y_train, y_valid)</li>
    <li>ks[cat_features].apply(encoder.fit_transform)</li>
    <li>lgb.train(param, dtrain, num_round, valid_sets=[dvalid], early_stopping_rounds=10)</li>
    <li>bst.predict(test[feature_cols])</li>
    <li>train_model(train, valid)</li>
    <li>count_enc.fit_transform(ks[cat_features])</li>
    <li>data.join(count_encoded.add_suffix("_count"))</li>
    <li>baseline_data.assign(category_country=label_enc.fit_transform(interactions))</li>
    <li>ks[cat_features].apply(encoder.fit_transform)</li>
    <li>clicks.sort_values('click_time')</li>
    <li>dtrain = lgb.Dataset(train[feature_cols], label=train['is_attributed'])</li>
    <li>dvalid = lgb.Dataset(valid[feature_cols], label=valid['is_attributed'])</li>
    <li>dtest = lgb.Dataset(test[feature_cols], label=test['is_attributed'])</li>
    <li>bst = lgb.train(param, dtrain, num_round, valid_sets=[dvalid], early_stopping_rounds=10)</li>
    <li>ypred = bst.predict(test[feature_cols])|Creating predictions variable</li>
    <li>score = metrics.roc_auc_score(test['is_attributed'], ypred)|variable for the score proportion</li>
    <li>CountEncoder()</li>
    <li>target_enc = ce.TargetEncoder(cols=cat_features)</li>
    <li>target_enc.fit(train[cat_features], train['is_attributed'])</li>
    <li>launched.rolling('7d').count() - 1</li>
    <li>model.fit(X_train,y_train)</li>
    </ul>
  </ul>

# 2- Explain each method ..

|            <b>Function</b>                |                                       <b>Discription</b>                                |
|-------------------------------------------|-----------------------------------------------------------------------------------------|
|ks = ks.query('state != "live"')|Drop live column in ks|
|ks = ks.assign(outcome=(ks['state'] == 'successful').astype(int))|Add outcome column, "successful" == 1, others are 0|
|X_train.select_dtypes(exclude=['object'])|drop the object columns |
|LabelEncoder() | convert the label name to numbers|
|score_dataset(drop_X_train, drop_X_valid, y_train, y_valid)|reports the mean absolute error (MAE) from a random forest model|
|ks[cat_features].apply(encoder.fit_transform)|Apply the label encoder to each column|
|lgb.train(param, dtrain, num_round, valid_sets=[dvalid], early_stopping_rounds=10)|training you model|
|bst.predict(test[feature_cols])|predict your score|
|train_model(train, valid)|Train a model (on the baseline data)|
|ce.CountEncoder()|Create the encoder|
|count_enc.fit_transform(ks[cat_features])|Transform the features|
|data.join(count_encoded.add_suffix("_count"))|rename the columns with the _count suffix, and join to dataframe|
|baseline_data.assign(category_country=label_enc.fit_transform(interactions))| label encode the interaction feature and add it to our data.|
|ks[cat_features].apply(encoder.fit_transform) ===> encoder = LabelEncoder()| convert the features in to numbers then apply this equation of the Xnew = (X - Xmean)/Xstd on all rows in the columns of (cat_features) which is cat_features = ['category', 'currency', 'country']|
|clicks.sort_values('click_time')|Sorting values of the column in click_time|
|dtrain = lgb.Dataset(train[feature_cols], label=train['is_attributed'])|Training model variable|
|dvalid = lgb.Dataset(valid[feature_cols], label=valid['is_attributed'])|validating model variable|
|dtest = lgb.Dataset(test[feature_cols], label=test['is_attributed'])|testing model variable|
|bst = lgb.train(param, dtrain, num_round, valid_sets=[dvalid], early_stopping_rounds=10)|Creating the model|
|ypred = bst.predict(test[feature_cols])|Creating predictions variable|
|score = metrics.roc_auc_score(test['is_attributed'], ypred)|variable for the score proportion|
|CountEncoder()|Count encoding replaces each categorical value with the number of times it appears in the dataset. or Target encoding replaces a categorical value with the average value of the target for that value of the feature|
|target_enc = ce.TargetEncoder(cols=cat_features)|For the case of categorical target: features are replaced with a blend of posterior probability of the target given particular categorical value and the prior probability of the target over all the training data. <br> For the case of continuous target: features are replaced with a blend of the expected value of the target given particular categorical value and the expected value of the target over all the training data.|
|target_enc.fit(train[cat_features], train['is_attributed'])|Learn encoding from the training set. Use the 'is_attributed' column as the target|
|launched.rolling('7d').count() - 1|creates a rolling window that contains all the data in the previous 7 days.|
|model.fit(X_train,y_train)|Training The model|





# 3- What’s new for you ?
> <ul>
> <li>ks = ks.query('state != "live"')</li>
> <li>ks = ks.assign(outcome=(ks['state'] == 'successful').astype(int))</li>
> <li>X_train.select_dtypes(exclude=['object']</li>
> <li>LabelEncoder()</li>
> <li>score_dataset(drop_X_train, drop_X_valid, y_train, y_valid)</li>
> <li>ks[cat_features].apply(encoder.fit_transform)</li>
> <li>lgb.train(param, dtrain, num_round, valid_sets=[dvalid], early_stopping_rounds=10)</li>
> <li>bst.predict(test[feature_cols])</li>
> <li>train_model(train, valid)</li>
> <li>count_enc.fit_transform(ks[cat_features])</li>
> <li>data.join(count_encoded.add_suffix("_count"))</li>
> <li>baseline_data.assign(category_country=label_enc.fit_transform(interactions))</li>
> <li>ks[cat_features].apply(encoder.fit_transform)</li>
> <li>clicks.sort_values('click_time')</li>
> <li>dtrain = lgb.Dataset(train[feature_cols], label=train['is_attributed'])</li>
> <li>dvalid = lgb.Dataset(valid[feature_cols], label=valid['is_attributed'])</li>
> <li>dtest = lgb.Dataset(test[feature_cols], label=test['is_attributed'])</li>
> <li>bst = lgb.train(param, dtrain, num_round, valid_sets=[dvalid], early_stopping_rounds=10)</li>
> <li>ypred = bst.predict(test[feature_cols])|Creating predictions variable</li>
> <li>score = metrics.roc_auc_score(test['is_attributed'], ypred)|variable for the score proportion</li>
> <li>CountEncoder()</li>
> <li>target_enc = ce.TargetEncoder(cols=cat_features)</li>
> <li>target_enc.fit(train[cat_features], train['is_attributed'])</li>
> <li>launched.rolling('7d').count() - 1</li>
> <li>model.fit(X_train,y_train)</li>
> </ul>

# 4- Resources ? 

> [https://www.w3resource.com/] 
> [https://docs.python.org/2/library/re.html]
> [https://pandas.org/doc/stable/] 
> [https://www.datacamp.com/]
> [http://rasbt.github.io/mlxtend/user_guide/preprocessing/minmax_scaling/]
> [https://contrib.scikit-learn.org/category_encoders/targetencoder.html]
> [https://kharshit.github.io/blog/2018/03/23/scaling-vs-normalization]
> [https://towardsdatascience.com/is-random-forest-better-than-logistic-regression-a-comparison-7a0f068963e4]
> [https://www.geeksforgeeks.org/python-pandas-dataframe-assign/#:~:text=assign()%20method%20assign%20new,of%20rows%20in%20the%20dataframe.]
