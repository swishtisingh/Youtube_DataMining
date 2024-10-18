# YouTube Data Mining 

<!DOCTYPE html>
<html lang="en">

<body>
    <div>
        <img src="[https://i.pinimg.com/originals/37/4a/9c/374a9ce6182b7a8aafd8c6ea6b698ff3.gif](https://www.google.com/url?sa=i&url=https%3A%2F%2Ftechnologyadvice.com%2Fblog%2Finformation-technology%2Fwhat-is-data-mining%2F&psig=AOvVaw19BKeEu0CcfY_-Xg3PqDvw&ust=1729358946786000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCIC92aC6mIkDFQAAAAAdAAAAABAR)" alt="Banner Image" class="banner">
    </div>
</body>
</html>

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
- [Modeling Techniques](#modeling_techniques)
- [Future Work](#future_work)
- [Contributing](#contributing)
- [Author](#author)
- [License](#license)

## Motivation
With billions of videos uploaded to YouTube, there's immense potential for extracting valuable insights by analyzing video metadata. This project aims to:

- Identify clusters of videos based on shared metadata attributes, such as views, likes, and duration.
- Detect anomalous videos that exhibit unusual patterns, such as rapid growth in views or highly disproportionate engagement metrics.
  
Such insights can be valuable for content creators, advertisers, data scientists, and even YouTube itself, helping to better understand trends, audience preferences, and content behavior.

## Features

1. ### Data Collection:
- **API Integration:** The project uses YouTube's API to fetch video metadata, including video titles, descriptions, view counts, likes, dislikes, comments, and more.
- **Comprehensive Dataset:** Data is collected on multiple features, which is then compiled into a structured format for analysis.
  
2.  ### Preprocessing:
- **Data Cleaning:** Handling missing data, filtering out irrelevant features, and removing duplicates.
- **Normalization:** Normalizing numerical features to bring them into a comparable range.
- **Handling Missing Values:** Imputation techniques are applied to address missing data where necessary.

3. ### Dimensionality Reduction:
- **Principal Component Analysis (PCA):** PCA is applied to reduce the dimensionality of the dataset while retaining as much of the variance as possible, making the dataset more manageable for clustering.

4. ### Clustering:
- **K-means Clustering:** A classic unsupervised learning algorithm that groups videos based on similar metadata characteristics.
- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise):** An algorithm particularly useful for identifying clusters of varying shapes and sizes, along with outliers.
- **Silhouette Score:** Used to evaluate the quality of the clustering and select the optimal algorithm.
  
5. ### Anomaly Detection:
- **DBSCAN for Outliers:** Videos that do not belong to any cluster are flagged as outliers.
- **Isolation Forest:** Another anomaly detection method used to identify videos that deviate significantly from common patterns.

## Technologies
The project is built using the following technologies:

- **Programming Language:** Python
  
- **Libraries:**
    - `pandas`, `numpy` for data manipulation and analysis
    - `scikit-learn` for machine learning algorithms (clustering, anomaly detection, PCA)
    - `matplotlib`, `seaborn` for data visualization
    - `Streamlit` for building an interactive web app
    - `Google API Client` for YouTube API integration
      
- **Jupyter Notebook:** Used for experimenting with models and visualizing the results.
  
- **Streamlit:** For interactive exploration and visualization of video clusters and anomalies.

## Data_Flow

1. **Data Collection:** The data is fetched from YouTube's API, which includes metadata such as video titles, views, likes, comments, etc.
   
2. **Preprocessing:** Data is cleaned and preprocessed to remove noise and ensure it's ready for modeling.
   
3. **Clustering:** Videos are grouped into clusters based on similar characteristics using K-means and DBSCAN.
   
4. **Anomaly Detection:** Outlier detection methods such as DBSCAN and Isolation Forest identify videos that deviate significantly from others.
   
5. **Results Visualization:** Data is visualized and explored using graphs and plots via a Streamlit app.

## Installation

To get started with the project, follow the steps below:
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/idokapel/youtube-data-mining.git
   ```
3. Navigate to the project directory:
   ```bash
   cd youtube-data-mining
   ```
5. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Running_the_project
To run the analysis on the YouTube dataset:
1. **Set your YouTube API key** in the configuration file.
2. **Run the YouTube data crawler:**
```bash
python youtube_crawler.py
```

This will fetch the metadata from YouTube and save it into a dataset.

3. **Analyze the data using Jupyter Notebook:** Open `final_project.ipynb` and run the cells to perform clustering, anomaly detection, and data visualization.

### Running_the_Streamlit_App
For an interactive web application, follow these steps:

1. Ensure the virtual environment is activated.
2. Run the Streamlit application:
```bash
streamlit run app.py
```
3. Open your web browser and navigate to the local address displayed in the terminal to interact with the app.

## Modeling_Techniques

### Clustering Algorithms:

- **K-means:** Efficient for clustering videos into predefined numbers of groups based on metadata attributes. Ideal when clusters are spherical and evenly distributed.
  
- **DBSCAN:** Density-based clustering method, capable of discovering clusters with irregular shapes and identifying noise (outliers).

### Anomaly Detection Algorithms:

- **DBSCAN:** Finds anomalies as part of the clustering process by marking low-density points as outliers.
  
- **Isolation Forest:** Detects anomalies by isolating data points that differ significantly from the rest of the dataset.

## Future_Work

- **Enhance Data Collection:** Incorporate more diverse video features, such as sentiment analysis from comments or audio-visual data.
  
- **Expand Algorithms:** Test other clustering algorithms like Hierarchical Clustering and Gaussian Mixture Models for comparison.
  
- **Time-Series Analysis:** Add temporal components to detect anomalies or trends over time.
  
- **Advanced Visualizations:** Build interactive visualizations for cluster and anomaly exploration.

## Contributing

Contributions to this project are highly encouraged! Whether you're improving the documentation, fixing bugs, or adding new features, your input is invaluable.

1. Fork the repository on GitHub.
2. Create a branch for your feature or fix:
```bash
git checkout -b feature-branch
```
3. Commit your changes:
``` bash
git commit -m "Add some feature"
```
4. Push to the branch:
```bash
git push origin feature-branch
```
5. Open a Pull Request and describe your changes.

## Author
### Srishti Singh
Data Scientist and Machine Learning Enthusiast
Feel free to connect with me on [LinkedIn.](https://www.linkedin.com/in/srishti-singh-921aa52aa/)

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

### Happy Coding!





