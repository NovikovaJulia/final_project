# Project "Food delivery time prediction"

Delivery time prediction is an essential feature for services such as Deliveroo, Uber Eats, Just Eat and etc., which deliver food on demand. 

These services usually receive an order and     deliver it within 30 minutes.

In these situations +/- 5 minutes can make a big difference so, for customer satisfaction, it?s important that the initial prediction is accurate and that any delays are communicated effectively.

## Dataset 

Source: https://www.kaggle.com/datasets/gauravmalik26/food-delivery-dataset 

## Conclusions
Random Forest gives us the best result (R2 score train: 0.9847444915295399, R2 score test: 0.7069023417012161) with these parameters:

random_forest = RandomForestClassifier (n_estimators = 200, criterion='log_loss', min_samples_leaf=4, min_samples_split=4)
                               
train_and_validate_model(X, y, model=random_forest)

So we can use test set with the same model and predict food delivery time.

## Possible next steps:
Use OpenStreetMaps API to calculate distance between the restaurant and delivery location
