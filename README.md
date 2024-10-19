# Movie Data Analysis with Kafka and Spark

## Overview

This project implements a real-time data processing pipeline that reads movie rating data from Kafka, processes it using Apache Spark, and writes the results to a MySQL database. It is designed for analyzing movie ratings and generating insights based on user demographics, genre popularity, and average ratings over the years.

## Features

- Consumes JSON movie rating data from a Kafka topic.
- Processes and analyzes the data using PySpark.
- Outputs the processed data to the console for real-time monitoring.
- Saves aggregated results to a MySQL database.

## Technologies Used

- Python
- Apache Kafka
- Apache Spark
- MySQL
- PySpark

## Requirements

Before you begin, ensure you have the following installed on your machine:

- Python 3.x
- Java Development Kit (JDK) 8 or higher
- Apache Kafka
- Apache Spark
- MySQL server
- `pyspark` and `confluent-kafka` Python packages

## Dataset Information

This project uses the **MovieLens 1M Dataset**, which contains 1 million movie ratings from users. Each entry includes the following attributes:

- **Rating**: The rating given by the user (1 to 5).
- **Year_x**: The year the movie was released.
- **UserID**: The unique identifier for each user.
- **Gender**: The gender of the user (M or F).
- **Age**: The age group of the user.
- **Occupation**: The occupation code of the user.
- **Zip-code**: The user's zip code.
- **id**: A unique identifier for the movie.
- **name**: The title of the movie.
- **date**: The release date of the movie.
- **genre**: The genre of the movie.

### Sample Data Format

The application expects the following JSON format for movie ratings:

```json
{
  "Rating": 5,
  "Year_x": 2000,
  "UserID": 1,
  "Gender": "F",
  "Age": 1,
  "Occupation": 10,
  "Zip-code": "48067",
  "id": 1193,
  "name": "One Flew Over the Cuckoo's Nest",
  "date": "1975",
  "genre": "Drama"
}
