
---

# Box Office Prediction

This project aims to predict the box office revenue of movies based on various features such as budget, runtime, release date, and popularity. It uses machine learning techniques to create a predictive model and allows users to input data to get a revenue estimate.

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [User Input Prediction](#user-input-prediction)
- [Visualizations](#visualizations)
- [Technologies Used](#technologies-used)
- [Future Enhancements](#future-enhancements)
- [License](#license)

## Overview

This project processes a dataset of movies and extracts useful features such as the movie's release day, month, year, and popularity. It then uses a machine learning model (RandomForestRegressor) to predict the revenue. The project also allows users to input movie details and get a predicted box office revenue as output.

## Project Structure

```
.
├── train.csv               # Dataset containing movie details (you must provide this)
├── box_office_prediction.py # Main Python script for data processing, training, and prediction
├── README.md                # Project documentation
```

## Features

- **Data Cleaning & Preprocessing**: Irrelevant columns are dropped, and release date features are extracted.
- **Machine Learning Model**: Uses `RandomForestRegressor` to predict the box office revenue.
- **User Input Based Prediction**: Collects user input to predict the box office revenue of a movie.
- **Visualizations**: Optional visualizations of budget distributions and movie release counts.
  
## Installation

1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/box-office-prediction.git
    ```
   
2. Navigate to the project directory:
    ```bash
    cd box-office-prediction
    ```
   
3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
   *(Ensure to create a `requirements.txt` file with necessary libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`)*

4. Ensure you have the `train.csv` dataset in the project directory. You can use any relevant dataset with features like `budget`, `runtime`, `release_date`, `popularity`, etc.

## Usage

To run the project, execute the following command in your terminal:

```bash
python box_office_prediction.py
```

### Model Training

The project will:
- Load the dataset (`train.csv`).
- Clean and preprocess the data.
- Train a RandomForest model to predict box office revenue based on available features.

### User Input Prediction

After training, the script will prompt you to input various details about a movie (such as budget, runtime, release day, etc.). Based on these inputs, the model will predict the box office revenue.

### Example:
```bash
--- Predict Box Office Revenue ---
Enter the budget of the movie: 100000000
Enter the runtime (in minutes): 120
Enter the release day (1-31): 15
Enter the release day of the week (0 for Monday, 6 for Sunday): 5
Enter the release month (1-12): 7
Enter the release year: 2015
Enter the movie's popularity score: 80.0

The predicted box office revenue is: $556,789,123.45
```

### Visualizations

The project includes optional data visualizations:
- **Movie Budgets Distribution**
- **Movie Release Counts by Year**

These visualizations will automatically be shown as part of the script execution.

## Technologies Used

- **Python 3.x**
- **Pandas** - for data manipulation.
- **NumPy** - for numerical operations.
- **Matplotlib & Seaborn** - for visualizations.
- **Scikit-learn** - for machine learning model building.

## Future Enhancements

- **Advanced Models**: Implement more sophisticated models like `XGBoost` or `Neural Networks` for better prediction accuracy.
- **Feature Engineering**: Explore additional features such as director, cast, or production company influence on revenue.
- **Web Interface**: Develop a Flask or Django web application for user-friendly input and prediction.
- **Real-time Data**: Integrate APIs to fetch real-time movie data for on-the-fly predictions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
---
