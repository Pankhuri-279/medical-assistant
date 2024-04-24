# Medical Assistant Tool
 
## Description
This project is part of the Google Girls Hackathon. Developed by Pankhuri Garg, this Medical Assistant Tool utilizes machine learning to assist in medical diagnostics, and it is designed to be run on Google Colab.
 
## Installation
To run this project, you do not need to install any software on your local machine. Instead, you will use Google Colab, a free cloud service that supports Jupyter notebooks.

## Getting Started
Click on the link to visit the [Google Colab Notebook](https://colab.research.google.com/drive/1HH460antljCLFaiZ9sJwqS27yikmPz8f?usp=sharing) and directly run it from there.

#### Alternatively
1. Visit [Google Colab](https://colab.research.google.com/).
2. Sign in with your Google account if not already signed in.
3. Click on `File` > `Open notebook`.
4. Select the `GitHub` tab in the dialogue box that appears.
5. Enter the URL of this GitHub repository and search.
6. Open the `medical_assistant.ipynb` notebook.
 
### Libraries
The necessary libraries are included in the Colab environment.
 
## Usage
Once the notebook is open:
1. You can run the entire notebook by selecting `Runtime` > `Run all` from the top menu.
2. Alternatively, you can run each cell individually by clicking the play button on the left side of each cell.

The script you provided, titled "medical-assistant.ipynb," is a sophisticated tool designed for medical diagnostics. Here's a concise technical summary of its functionality:
 
## Tool Overview
The tool takes user-inputted symptoms, processes them through a machine learning model, and predicts a potential disease. Based on the predicted disease, it then offers recommendations for specialists suited to treat the condition. This process involves several data transformations, model training, and prediction stages.
 
## Key Functions
1. **Data Preprocessing:**
   - Loads and preprocesses medical data, including symptoms and diseases.
   - Uses label encoding to transform categorical disease labels and symptoms into a numerical format that can be processed by machine learning models.
   - Applies one-hot encoding to transform symptom data into binary vectors, which are essential for the machine learning model input.
 
2. **Model Training:**
   - Splits the preprocessed data into training and testing subsets.
   - Constructs and trains a deep neural network using TensorFlow to predict diseases based on the encoded symptoms. The model architecture includes multiple dense layers with dropout and batch normalization to improve learning stability.
 
3. **Disease Prediction:**
   - After training, the model predicts the disease from a set of symptoms inputted by a user.
   - The prediction involves converting raw symptom input into the trained model's expected input format, predicting with the model, and then translating the numerical prediction back into a readable disease label using inverse label encoding.
 
4. **Doctor Recommendation:**
   - Based on the predicted disease, the script can recommend doctors by speciality. It utilizes a separate dataset containing doctor profiles, including their specialities and available schedules.
   - A RandomForest model predicts doctor ratings based on the available information, and the system recommends the highest-rated available doctors for the diagnosed condition.
 

