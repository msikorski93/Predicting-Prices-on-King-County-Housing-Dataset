# Predicting-Prices-on-King-County-Housing-Dataset
![ alt text ](https://img.shields.io/badge/license-MIT-green?style=&logo=)
![ alt text ](https://img.shields.io/badge/-Jupyter-F37626?logo=Jupyter&logoColor=white)
![ alt text ](https://img.shields.io/badge/-NumPy-013243?logo=Numpy&logoColor=white)
![ alt text ](https://img.shields.io/badge/-TensorFlow-FF6F00?logo=TensorFlow&logoColor=white)
![ alt text ](https://img.shields.io/badge/-scikit--learn-F7931E?logo=scikitlearn&logoColor=white)

Predicting house prices using different regression analysis models.

### New notebooks for January 2024
A new regression task was introduced. Ten different models were fitted and performed with the following evaluation metrics:
| Model          | RMSE     | RMSLE  | R<sup>2</sup> | Adjusted R<sup>2</sup> | Variance<br>Regression | 5-Fold Cross-<br>Validation |
|----------------|----------|--------|---------------|------------------------|------------------------|-----------------------------|
| Neural Network | 110582.6 | 0.7188 | 0.8819        | 0.8812                 | 0.8837                 | 0.8717                      |
| Random Forest  | 105662.2 | 0.1678 | 0.8870        | 0.8863                 | 0.8870                 | 0.8868                      |
| Decision Tree  | 146264.0 | 0.2482 | 0.7835        | 0.7822                 | 0.7836                 | 0.7729                      |
| CatBoost       | 91614.5  | 0.1511 | 0.9151        | 0.9146                 | 0.9151                 | 0.9142                      |
| XGBoost        | 98811.4  | 0.1593 | 0.9012        | 0.9006                 | 0.9012                 | 0.8951                      |
| LightGBM       | 96765.5  | 0.1586 | 0.9052        | 0.9047                 | 0.9053                 | 0.9054                      |
| Polynomial     | 116431.2 | 0.1968 | 0.8628        | 0.8620                 | 0.8629                 | 0.8631                      |
| Lasso          | 110881.3 | 0.1833 | 0.8756        | 0.8749                 | 0.8756                 | 0.8745                      |
| Ridge          | 116619.7 | 0.1959 | 0.8624        | 0.8616                 | 0.8625                 | 0.8628                      |
| ElasticNet     | 119081.6 | 0.1966 | 0.8565        | 0.8557                 | 0.8566                 | 0.8592                      |

Among these chosen models, the CatBoost (categorical boosting) regressor outperformed all of the other regressors and was selected as the final model to predict house prices. The model was optimized with hyperparameter tuning and evaluated once more.
| RMSE     | RMSLE  | R<sup>2</sup> | Adjusted R<sup>2</sup> | Variance<br>Regression | 5-Fold Cross-<br>Validation |
|----------|--------|---------------|------------------------|------------------------|-----------------------------|
| 91404.4  | 0.1508 | 0.9155        | 0.9150                 | 0.9155                 | 0.8912                      |

This analysis concluded that for the King County area the most influencial price factors are:
* square footage of the real estate;
* location, exactly the combination of variables like: latitude, longitude, distance from downtown;
* the real estate's grade (general condition).
