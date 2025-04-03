# Notes on "Austin Green Energy Predictor"

## Overview
This GitHub repository contains a machine learning model that predicts renewable energy output (in MWh) from wind and solar farms in Texas based on weather data. The project was developed as a capstone project for the UT Austin Data Analytics & Visualization Bootcamp.

## Key Components

### Project Objective
- Forecast power generation from renewable energy sources using weather data
- Predict MWh output for Hackberry Wind Farm and Webberville Solar Farm
- Use time and weather factors (temperature, wind speed, cloud coverage) as predictors

### Data Sources
1. **Energy Output Data**:
   - Provided by Austin Energy
   - Hourly power generation data from 2017 through July 2020
   - Two renewable energy farms:
     - Hackberry Wind Farm (165,600 kW capacity, 72 turbines)
     - Webberville Solar Farm (35,000 kW capacity, 127,278 PV panels)

2. **Weather Data**:
   - Collected using Local Historical Weather Online API
   - Hourly weather parameters including temperature, humidity, cloud coverage
   - Matched to the locations of each renewable energy farm
   - Same time frame as energy output data (2017-2020)

### Database
- MongoDB Atlas database hosted on AWS
- Two collections: wind data and solar data
- Data accessed using PyMongo driver

### Machine Learning Models
1. **Multiple Linear Regression**:
   - Solar model achieved ~60% accuracy
   - Wind model achieved ~30% accuracy
   - Captured general shape but struggled with precise value predictions

2. **Neural Network**:
   - Better at handling complex relationships in the data
   - Three layers with 20-30 neurons per layer
   - Relu activation function to ensure continuous, non-negative output
   - Solar model: ~10% mean absolute error (1.5 MWh)
   - Wind model: ~15% mean absolute error (25 MWh)
   - Better at predicting output patterns and timing

### Technologies Used
- **Languages/Frameworks**: Python, HTML, Flask, CSS, JavaScript
- **Database**: MongoDB, PyMongo
- **Data Visualization**: Matplotlib, Seaborn, Plotly, hvPlot
- **Machine Learning**: Scikit-Learn, TensorFlow
- **Deployment**: Heroku, Pickle Module

### Project Structure
- Dashboard: Web interface for viewing predictions
- Database: Data storage and management
- Resources: Raw data and reference materials
- Solar/Wind: Model-specific code and analysis
- Static/Templates: Web application files

## Reference
GitHub Repository: Duvey314/austin-green-energy-predictor
URL: https://github.com/Duvey314/austin-green-energy-predictor
Live Demo: https://austin-green-energy-predictor.herokuapp.com/
