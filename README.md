# Tip Amount Prediction for NYC Taxis

This project aims to predict taxi tips for rides in NYC using various regression models. It utilizes a comprehensive dataset and employs feature engineering techniques to enhance prediction accuracy.

## Project Overview

This repository includes the complete workflow for the forest cover type prediction task, organized as follows:

1. **Data Exploration and Feature Engineering**: 
   - Initial exploratory data analysis (EDA) to understand key variables and their distributions.
   - Feature engineering to create informative features from the raw topographical and environmental data.
   
2. **Model Training**: 
   - Various models are trained, from simpler classifiers to advanced algorithms capable of handling complex, non-linear relationships. Key models include
      - Linear Regression
      - ElasticNet Regression
      - Random Forest
      - XGBoost
      - CatBoost
      - Ensemble models (MetaLearner and Stacking)

3. **Ensemble and Meta-Learning**:
   - Different models were combined using ensemble techniques (such Stacking) to improve r2_score.
   - A meta-learner approach was implemented to combine predictions from multiple models, enhancing generalization.

4. **Evaluation Metrics**:
   - The model performance was evaluated using the r2 metric.

## Requirements

### Python Libraries

- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- xgboost
- shap
- geopandas

To install all dependencies, use: pip install -r requirements.txt

### Additional Requirements

## Usage

1. **Data Preparation**:
   - Add the train and test data in the data folder

2. **Model Training and Evaluation**:
   - Open `Data-Challenge_Tip.ipynb`, after loading the necessary packages and importing train and test data
     use the defined pipeline for preprocessing and lunch code in section final model and the end of the notebook.


## Model Performance

The table below summarizes the performance of each model based on weighted metrics:

| Model                                | r2-score |
|--------------------------------------|----------|
| Linear Regression                    |0.6087    |
| ElasticNet Regression                |0.6085    |
| Random Forest                        |0.7060    | 
| XGBoost Regressor                    |0.7085    |
| CatBoost Regressor                   |0.7087    |

## Final standings

!(Final_Standings)[image/Final_Standings.png]

## Authors

*Mohamed Badi* (mohamed.badi@etu-upsaclay.fr) and *Aymane Masrour* (aymane.masrour@etu-upsaclay.fr). 


## Contributing

Please feel free to submit a pull request if you'd like to add improvements or fix issues. All contributions are welcome!




