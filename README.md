# Phishing URL Detection Web Application

## Project Overview

This project is a Python-based web application designed to detect phishing URLs using a machine learning model. It provides a user-friendly interface to upload datasets, train a Gradient Boosting Classifier (GBC) model, and make predictions on new URLs.

## Features

* **Data Upload:** Ability to upload CSV files containing legitimate and phishing URLs for model training.
* **Model Training:** Train a Gradient Boosting Classifier model using the provided datasets.
* **URL Prediction:** Input a URL to get an instant prediction on whether it is malicious (phishing) or legitimate.
* **Interactive Web Interface:** A web-based user interface for easy interaction, likely built with Flask or Django.

## Technologies Used

* **Python:** The core programming language for the application and machine learning logic.
* * **Flask:** A lightweight micro-web framework for Python. Used for building the web interface and handling requests.
* **scikit-learn:** A comprehensive machine learning library for Python, used for the Gradient Boosting Classifier model.
* **Pandas:** A powerful data manipulation and analysis library for Python.
* **HTML, CSS, JavaScript:** For structuring, styling, and adding interactivity to the web interface.

## Project Structure

.
├── .idea/                 # PyCharm/IntelliJ IDEA IDE configuration files (ignored by Git)
├── venv/                  # Python Virtual Environment (ignored by Git)
├── pycache/           # Python compiled bytecode files (ignored by Git)
├── data/                  # Directory for storing various datasets or data-related files
│   ├── legitmateurls.csv  # Dataset of legitimate URLs used for training
│   └── phishing.csv       # Dataset of known phishing URLs used for training
├── static/                # Static web assets like CSS, JavaScript files, and images
│   ├── css/
│   ├── js/
│   └── images/
├── templates/             # HTML template files rendered by the web application
├── views/                 # (Optional, if used) Python modules containing web view functions
├── app.py                 # The main application file, likely the entry point for the web server
├── convert.py             # A module or script for data conversion or transformation tasks
├── DataAnalysis.py        # A module or script dedicated to data analysis and preprocessing logic
├── feature.py             # A module for feature engineering or common utility functions
├── gbc_malicious.pkl      # A serialized (pickled) pre-trained Gradient Boosting Classifier model
├── requirements.txt       # A text file listing all required Python packages and their versions
├── test_input.txt         # Sample input data for testing purposes
├── upload_dataset.html    # (Likely) An HTML file related to the dataset upload interface
└── ...                    # Other project-specific files or directories


## Installation Guide

Follow these steps to set up and run the project on your local machine:

1.  **Clone the Repository:**
    
    ```bash
    git clone [https://github.com/Mohammadalam-codes/MaliciousURLDetection.git](https://github.com/Mohammadalam-codes/MaliciousURLDetection.git)
    ```

2.  **Create and Activate a Python Virtual Environment:**
    Using a virtual environment is highly recommended to manage project dependencies without interfering with your system-wide Python installation.
    ```bash
    python -m venv venv
    ```
    * **On Windows:**
        ```bash
        venv\Scripts\activate
        ```
    * **On macOS/Linux:**
        ```bash
        source venv/bin/activate
        ```

3.  **Install Dependencies:**
    Once your virtual environment is active, install all the required Python packages listed in `requirements.txt`:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1.  **Run the Application:**
    From the project's root directory (where `app.py` is located) and with your virtual environment activated, run the main application file:
    ```bash
    python app.py
    ```
    *(If your main application file is named differently, adjust `app.py` accordingly.)*

2.  **Access the Web Interface:**
    After running the application, your terminal will usually display a URL where the application is hosted (e.g., `http://127.0.0.1:5000/` for Flask). Open this URL in your web browser.

3.  **Interact with the Application:**
    Use the web interface to:
    * Upload your `legitmateurls.csv` and `phishing.csv` datasets (if the application supports dynamic training via the UI).
    * Enter individual URLs to get real-time phishing detection predictions.

## Data

The project utilizes the following datasets for training and evaluation of the machine learning model:
* `legitmateurls.csv`: Contains a collection of URLs identified as legitimate (non-phishing).
* `phishing.csv`: Contains a collection of URLs identified as phishing.

These datasets are integral for the machine learning model's performance in distinguishing between benign and malicious URLs.

## Contribution

Contributions to this project are welcome! If you find a bug, have a suggestion for improvement, or would like to add new features, please feel free to:
1.  Fork this repository.
2.  Create a new branch (`git checkout -b feature/YourFeatureName`).
3.  Make your changes and commit them (`git commit -m 'Add new feature X'`).
4.  Push to your branch (`git push origin feature/YourFeatureName`).
5.  Open a Pull Request.

Please ensure your code adheres to existing style guidelines and includes appropriate tests.

## License

This project is licensed under the [MIT License](LICENSE).
