# Mars_thermal_Inertia_Prediction

Machine learning techniques, showing high automation and efficiency in handling large amounts of observation data, have been applied to predict the thermal inertia of Mars. We created a large data set from well-established KRC thermal model. Using this data set, we trained random forest models using latitude, time of day, season, surface kinetic temperature, albedo, surface pressure and visible dust optical depth as inputs to the model. The output is thermal inertia.

Quick start (in Jupyter Notebook)

Step 1:

import joblib

rf_model_use=joblib.load("train_rf_model.m") # load the trained model

Step 2:      

#Input Order: Local time (h), Season(Ls,degree), Surface temperature (K), Albedo, Surface pressure (Pa), Dust opacity, Latatude (degree)

input_params=[14.5,107,195,0.20,800,0.36,20]

input_params_array=np.array(input_params)

thIn_value=rf_model_use.predict(input_params_array) # output the predicted thermal inertia (tiu)
