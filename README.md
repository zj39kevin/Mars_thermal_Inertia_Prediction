# Mars_thermal_Inertia_Prediction
A machine learning model to predict thermal inertia on Mars

Quick start (in Jupyter Notebook)

Step 1:
import joblib
rf_model_use=joblib.load("train_rf_model.m") # load the trained model

Step 2:      
input_params=[14.5,107,195,0.20,800,0.36,20] # Input Order: Local time (h), Season(Ls,degree), Surface temperature (K), Albedo, Surface pressure (Pa), Dust opacity, Latatude (degree)
input_params_array=np.array(input_params)
thIn_value=rf_model_use.predict(input_params_array) # output the predicted thermal inertia (tiu)
