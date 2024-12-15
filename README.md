# Netflix EDA PySpark
Exploratory Data Analysis (EDA) on Netflix datasets using PySpark. This project is part of the **CE408 - Cloud Computing Assignment** by **M. Ahabb Sheraz**.


## Overview
This project demonstrates using PySpark to conduct an exploratory data analysis on the Netflix dataset. The analysis includes visualizations and insights derived from the dataset.

### Features:
- Data preprocessing with PySpark.
- Analysis of Netflix titles by genre, release year, and more.



## Dataset
The dataset used for this analysis is publicly available on [Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows) and contains information about Netflix titles, such as:
- Title
- Genre
- Release Year
- Country
- Duration
- Ratings

The dataset file is stored locally and mounted into the Docker container for processing.


## Requirements

### Software Requirements:
- Docker and Docker Compose
- Python 3.x (for local testing, if required)


## Setup Instructions

### Using Docker
1. Clone the repository:
   ```bash
   git clone https://github.com/AhabbscienceStudioPak/Netflix_EDA_PySpark.git
   cd Netflix_EDA_PySpark
   ```

2. Start the Spark cluster:
   ```bash
   docker-compose up -d
   ```

3. Verify that the services are running:
   - Spark Master: [http://localhost:9090](http://localhost:9090)

### Running the Script
1. Copy the dataset to the `spark-master` container:
   ```bash
   docker cp -L netflix_titles_eda.py spark-master:/opt/bitnami/spark/netflix_eda.py
   ```

2. Submit the PySpark job:
   ```bash
   docker exec spark-master spark-submit --master spark://spark-master:7077 /opt/bitnami/spark/netflix_eda.py
   ```

3. Check the console output for analysis results and visualizations.



## Project Files

### Repository Structure:
```
Netflix_EDA_PySpark/
|
├── data/
│   └── netflix_titles.csv            # Netflix dataset
│
├── netflix_titles_eda.py            # PySpark script for EDA
├── docker-compose.yaml              # Docker Compose configuration
├── Dockerfile                       # Custom Spark image with dependencies
└── README.md                        # Project documentation
```


## Results
https://github.com/user-attachments/assets/bcbefa2e-f280-4ffb-8e7a-4f7b084a6e4b


