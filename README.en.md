[Versión en Español](README.md)

# Hershey's_Inventory_Optimization_Project 🍫
This Data Science project presents a comprehensive, end-to-end solution for optimizing inventory management for a retail company like Hershey's. It demonstrates a full data pipeline, from raw data ingestion and exploratory analysis to predictive modeling and business-driven optimization.    

The primary goal is to answer the critical question: "What is the optimal stock level for each product and store to minimize total costs (holding and stockout costs)?" The solution combines a machine learning model to predict demand with a linear programming model to find the most cost-effective inventory level.   

## Project Structure 📁
Is organized into modular files to ensure clarity and scalability.  
- main.py: The orchestrator script that runs the entire data pipeline.
- app.py: The Streamlit web application that serves as the interactive dashboard for stock recommendations.
- config.py: A centralized configuration file for all business parameters, file paths, and model constants.
- data_utils.py: A module for data ingestion, cleaning, and exploratory data analysis (EDA).
- model_utils.py: A module for model training, prediction, and the core inventory optimization logic using PuLP.
- mlruns/: A directory created by MLflow to track model experiments and save the trained model.

## Technologies Used 🐍
- Pandas: For data manipulation, cleaning, and analysis.
- NumPy: For efficient numerical operations.
- Scikit-learn: For building the machine learning pipeline and the Gradient Boosting Regressor model.
- MLflow: To manage the machine learning lifecycle, tracking experiments and registering the production model.
- PuLP: A linear programming library used to solve the inventory optimization problem.
- Streamlit: For building an interactive and user-friendly web dashboard.
- Matplotlib & Seaborn: For data visualization during EDA.
- SQLite3: To manage the weather data in a simple database.

## Installation Notes ⚙️
- Clone the repository (Bash):  
git clone https://github.com/ADAA-404/Proyecto-de-optimizacion-de-inventario-de-Hershey.git   
cd Proyecto-de-optimizacion-de-inventario-de-Hershey

- Create a virtual environment (optional but highly recommended for library compatibility):    
python -m venv venv  
source venv/bin/activate  # On macOS/Linux  
venv\Scripts\activate      # On Windows  

- Install dependencies:  
pip install pandas numpy scikit-learn matplotlib MLflow PuLP Streamlit Seaborn SQLite3

- Download the data:
For this script, we use databases in different formats that you can find in the repository. Otherwise, provide your own data if you have documents of this type.

- Configure the data path (if you need it):  
DATA_FOLDER_PATH = r"ruta/a/la/carpeta/data"

This code was written in a Python Jupyter Notebook.

## How it works 📎
This project requires four data files to be present in the root directory: sales_data.csv, marketing_campaigns.json, products_info.json, and weather_data.db.  
These files are not included in this repository. Ensure you have these files in the same directory as the project scripts.    

- Run the Main Pipeline: Execute the main script to perform the data ETL, EDA, model training, and save the model using MLflow. This step will also print key insights and the final optimization results to the console.   
- Launch the Interactive Dashboard: Once the model has been trained and saved, launch the Streamlit application to interact with the model and generate real-time recommendations.

## Contributions 🖨️
If you're interested in contributing to this project or using it independently, consider:   
- Forking the repository.
- Creating a new branch (git checkout -b feature/new-feature).
- Making your changes and committing them (git commit -am 'Add new feature').
- Pushing your changes to the branch (git push origin feature/new-feature).
- Opening a Pull Request.

## License 📜
This project is under the MIT License. See the LICENSE file (if applicable) for more details.
