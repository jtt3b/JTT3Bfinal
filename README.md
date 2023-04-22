Final 2 pager
==============================
      For my project I chose to explore the BigMart dataset. This interested me as I am into logistics and retail. The business problem I came up with was that sales prediction is necessary to predict the buying of unnecessary stock which remains accumulated in a store without being sold. So, to prevent having too much backstock or spoilage, we need to predict the demand of each product in a store. After completing exploratory data analysis and doing some modeling, the aim was to have a high R squared score.
	EDA summary: from the graphs we saw that Item_Weight and Item_MRP were evenly distributed. Also, we saw that the distribution of Item_Outlet_Sales was distributed over a wide range, hence we took the square root of all those values. The highest selling items were dairy, meat, and soft drinks. Most stores were established from 1985-1990 and 1995-2000. No new stores were established between 1990-1995.
	Since there were many categorical features, I used label encoding and one hot encoding so that the categorical data could be converted to integer values and could provide to the models to give and improve the predictions.
	Since my business problem was a regression problem, I chose all the possible machine learning models that perform the best on regression problems. Out of all of the models, the more explainable ones were linear regression and support vector regression (SVR). The reason is that they are base models while xgboost, random forest, and decision trees are a combination of various base models, making them more complex and less explainable.
	For explaining in lay terms to an audience or executive team, I would say that the process typically involves collecting and analyzing data on past sales, current inventory levels, and customer demand patterns. Machine learning algorithms can then be used to develop predictive models that can forecast future demand and optimize inventory levels.

      The output of the data might be a set of recommendations for inventory management policies that can help the grocery store reduce waste, minimize out-of-stock situations, and increase profits. For example, the project might recommend using just-in-time inventory management techniques to keep inventory levels low and reduce waste, or developing a dynamic pricing strategy that adjusts prices based on demand patterns. The goal is to improve their bottom line and provide better customer experiences. Also, I think that going through the whole notebook sequentially with an executive team would be easy to understand for them and quite comprehensible when explained step by step.
      As far as a situation where a lesser-performing model would be chosen, I would say no because the metric I have chosen is R squared and out of all the models, boosted models such as xgboost and random forest usually perform better and have a higher R squared score, so those models would be my first choice.
      The performance measure used to determine which model was better was the R squared score and it is used to evaluate the performance of a linear regression model. It is the amount of variation in the output dependent attribute which is predictable from the input independent variable(s). It is used to check how well-observed results are reproduced by the model, depending on the ratio of total deviation of results described by the model. The formula is R squared = 1 – the sum of squares of the residual errors divided by the total sum of the errors.
      In the notebook, the R squared score for xgboost with cross validation was 0.66. So, it can be inferred that 66% of the changeability of the dependent output attribute can be explained by the model while the remaining 34% of the variability is unaccounted for. R squared indicates the proportion of data points which lie within the line created by the regression equation. A higher R squared is more desirable as it indicates better results. 
The model performance comparison from highest R squared to lowest R squared was xgboost(cv)>RandomForest>xgboost>LinearRegression>SVR(cv)>DecisionTree.
      It is likely that showing a model with a high R squared score would resonate with executive leadership, as R-squared is a common metric used to evaluate the performance of statistical models. Performance measures are essential for businesses as they allow for the evaluation of strategies and initiatives. They provide a means for organizations to determine areas where they are performing well and areas that require improvement, as well as inform decision-making processes. However, it is crucial to select the appropriate performance measures that align with the business context and avoid relying too heavily on a single metric. Also, it's important to interpret performance measures in the broader context of the organization's goals and strategies.




Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
