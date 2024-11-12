# Forest Cover Type Prediction

This project aims to predict forest cover types based on topographical and environmental variables using machine learning. The primary goal is to accurately classify vegetation types within forested areas by leveraging a variety of machine learning models, with special emphasis on feature engineering, model selection, and hyperparameter optimization.

## Project Overview

This repository includes the complete workflow for the forest cover type prediction task, organized as follows:

1. **Data Exploration and Feature Engineering**: 
   - Initial exploratory data analysis (EDA) to understand key variables and their distributions.
   - Feature engineering to create informative features from the raw topographical and environmental data.
   
2. **Model Training**: 
   - Various models are trained, from simpler classifiers to advanced algorithms capable of handling complex, non-linear relationships. Key models include:
      - Logistic Regression
      - Decision Tree
      - Random Forest
      - Balanced Random Forest
      - AdaBoost
      - CatBoost
      - XGBoost
      - Ensemble models (MetaLearner and Stacking)

3. **Ensemble and Meta-Learning**:
   - Different models were combined using ensemble techniques (such as Hard Voting and Stacking) to improve overall accuracy, recall, and F1-score.
   - A meta-learner approach was implemented to combine predictions from multiple models, enhancing generalization, especially for underrepresented classes.

4. **Evaluation Metrics**:
   - The model performance was evaluated using weighted metrics, including precision, recall, and F1-score, with a final evaluation through a confusion matrix for clarity.

## Requirements

### Python Libraries

This project requires the following libraries:
- `numpy`
- `pandas`
- `scikit-learn`
- `xgboost`
- `catboost`
- `matplotlib`
- `seaborn`

To install all dependencies, use: pip install -r requirements.txt



### Additional Requirements

- **Google Colab with High-Performance Machine**: For inference using the final model, we recommend using Google Colab on a machine with high memory capacity. The XGBoost model in particular requires significant memory during inference due to its complexity and size.

## Usage

1. **Data Preparation**:
   - Add the train and test data in the data folder

2. **Model Training and Evaluation**:
   - Open `Data Challenge - Forest Cover Type.ipynb` and lunch code in section final model


## Model Performance

The table below summarizes the performance of each model based on weighted metrics:

| Model                                | Precision | Recall | F1-Score | Support | Dataset Type     |
|--------------------------------------|-----------|--------|----------|---------|------------------|
| Logistic Regression                  | 0.7009    | 0.5921 | 0.6214   | 20000   | Initial          |
| Decision Tree                        | 0.8610    | 0.8612 | 0.8611   | 20000   | Initial          |
| Random Forest                        | 0.9207    | 0.9207 | 0.9201   | 20000   | Initial          |
| Balanced Random Forest               | 0.7600    | 0.7000 | 0.7200   | 20000   | Initial          |
| AdaBoost                             | 0.8701    | 0.8705 | 0.8703   | 20000   | Initial          |
| CatBoost                             | 0.9221    | 0.9220 | 0.9220   | 20000   | Initial          |
| XGBoost                              | 0.9101    | 0.9101 | 0.9096   | 20000   | Initial          |
| MetaLearner (RF on curated datasets) | 0.9358    | 0.9360 | 0.9358   | 5000    | Curated          |
| Ensemble (Hard Voting - RF)          | 0.9215    | 0.9212 | 0.9209   | 5000    | Curated          |
| Enhanced MetaLearner (RF on curated) | 0.9417    | 0.9418 | 0.9417   | 5000    | Curated          |
| Voting Classifier (CatBoost & RF)    | 0.9300    | 0.9300 | 0.9300   | 20000   | Initial          |
| Enhanced MetaLearner (CatBoost & RF) | 0.9884    | 0.9884 | 0.9884   | 5000    | Curated          |
| Final Model                          | 0.9448    | 0.9450 | 0.9448   | 5000    | Curated + Full   |

## Authors

*Aymane Masrour* (aymane.masrour@etu-upsaclay.fr) and *Badi Mohamed* (mohamed.badi@etu-upsaclay.fr). 


## Contributing

Please feel free to submit a pull request if you'd like to add improvements or fix issues. All contributions are welcome!

## License

This project is licensed under the MIT License.






