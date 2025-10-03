# Bangalore House Price Prediction

This project is a machine learning model designed to predict real estate prices in Bangalore, India. It utilizes a linear regression model trained on a comprehensive dataset of house prices. The project features a user-friendly web interface that allows users to input property details and receive an estimated price.

**Live Demo:** [https://avinash0508.github.io/Banglore-Home-Price-Prediction/app.html](https://avinash0508.github.io/Banglore-Home-Price-Prediction/app.html)

> **Important Note:** The live demo is a frontend application hosted on GitHub Pages. For it to be fully functional, the Python Flask server (`server.py`) must be running on your local machine to provide the backend API for price predictions.

## Features
- Predicts house prices based on:
  - Total square feet area
  - Number of Bedrooms (BHK)
  - Number of Bathrooms
  - Location within Bangalore

## How To Set Up and Run the Project

Follow these steps to run the application on your local machine.

### 1. Prerequisites
Ensure you have the following installed:
- Python 3.x
- `pip` (Python package installer)

### 2. Clone the Repository
Clone this repository to your local machine:

```bash
git clone [https://github.com/avinash0508/Banglore-Home-Price-Prediction.git](https://github.com/avinash0508/Banglore-Home-Price-Prediction.git)
cd Banglore-Home-Price-Prediction

Install the necessary Python libraries using pip:

Bash

pip install -r requirements.txt
(If you do not have a requirements.txt file, you can install the packages manually):

Bash

pip install flask scikit-learn pandas numpy

Start the Flask backend server by running the server.py script from the terminal:

Bash

python server.py
You will see a confirmation message in the terminal, indicating that the server is running and ready to handle requests (e.g., Starting the server for the price prediction).

5. Use the Web Application
With the server running, open the app.html file in your web browser. You can now input the property details and click "Estimate Price" to get a prediction from your local model.

Project Structure
.
├── artifacts
│   ├── Bangalore_Home_Prices_model.pickle  # Trained linear regression model
│   └── columns.json                      # Feature columns used for prediction
├── app.css                               # Stylesheet for the web app
├── app.html                              # Frontend web page
├── app.js                                # JavaScript for frontend logic
├── bhp.ipynb.ipynb                       # Jupyter Notebook with the full model building process
├── server.py                             # Flask server for the backend API
└── util.py                               # Helper functions for loading artifacts and making predictions
Model Details
The prediction model is a Linear Regression algorithm built using Scikit-learn. The Jupyter Notebook (bhp.ipynb.ipynb) details the complete workflow, which includes:

Data Cleaning: Handling NaN values and removing features not relevant to the model.

Feature Engineering: Creating new features like price_per_sqft to aid in analysis and outlier detection.

Outlier Removal: Using domain knowledge (e.g., removing properties with an unusually low sqft-to-bedroom ratio) and statistical methods (standard deviation) to clean the data.

Dimensionality Reduction: Consolidating rare location categories into a single "other" category to simplify the model.

One-Hot Encoding: Converting the categorical location data into a numerical format suitable for the model.

Technologies Used
Backend: Python, Flask

Machine Learning: Scikit-learn, Pandas, NumPy

Frontend: HTML, CSS, JavaScript (with jQuery)

Development Environment: Jupyter Notebook
