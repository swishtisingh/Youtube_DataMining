# YouTube Data Mining 

## Overview
The YouTube Data Mining Project applies advanced data mining techniques and machine learning algorithms to analyze YouTube video metadata. By leveraging clustering and anomaly detection, this project uncovers patterns in video characteristics and detects anomalies that deviate from common trends. The insights derived from this project can help in understanding user engagement, video trends, and outliers in the vast amount of content hosted on YouTube.

## Table of Contents

- [Motivation](#motivation)
- [Features](#features)
- [Technologies](#technologies)
- [Data Flow](#data_flow)
- [Installation](#installation)
- [Usage](#usage)
    - [Running the Project](#running_the_project)
    - [Running the Streamlit App](#running_the_streamlit_app)
- [Modeling Techniques](#modeling_technologies)
- [Future Work](#future_work)
- [Contributing](#contributing)
- [Author](#author)
- [License](#license)

## Motivation
The vast amount of videos available on YouTube presents a unique opportunity to explore and analyze video metadata for insights. By identifying clusters of similar videos and detecting anomalies, we aim to uncover the underlying structures within the dataset that could inform future analyses and applications.

## Features
- **Data Collection**: Utilizes YouTube's API to fetch and compile video metadata into a comprehensive dataset.
- **Preprocessing**: Involves cleaning and preparing the data for machine learning tasks, including normalization and handling missing values.
- **Dimensionality Reduction**: Uses Principal Component Analysis (PCA) to reduce the complexity of the dataset while retaining essential information.
- **Clustering**: Implements the K-means and DBSCAN algorithms, selecting the optimal method via silhouette score, to cluster videos into groups based on their metadata characteristics.
- **Anomaly Detection**: Applies algorithms such as DBSCAN and Isolation Forest to identify videos that significantly deviate from common patterns.

## Installation
1. Clone this repository to your local machine: git clone https://github.com/idokapel/youtube-data-mining.git
2. Navigate to the project directory: cd youtube-data-mining
3. Install the required Python packages: pip install -r requirements.txt

## Usage
### To run the project and analyze the YouTube dataset:
- Ensure you have a valid YouTube API key and set it in the configuration.
- Run [youtube_crawler.py](youtube_crawler.py)
- Run [final_project.ipynb](final_project.ipynb)

### To run the Streamlit app:
- Navigate to the project directory
- Ensure you have activated the project's virtual environment
- Run the Streamlit application by executing the following command in your terminal or command prompt:
streamlit run app.py



