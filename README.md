# API-Ingestion-Pipeline-for-Hospitality-Intelligence
This project is a data engineering pipeline that ingests real-time data from external APIs, processes it, and stores it in a structured database.

The goal is to simulate the data backbone of an AI Concierge system, where external data (like weather and events) is continuously collected and made available for downstream analytics and recommendations.


#Objectives
Extract data from a real-world API (weather data)
Transform unstructured JSON into structured format
Load data into a relational database (MySQL)
Build a modular ETL pipeline
Prepare data for future analytics and AI use cases


#Architecture
API (Weather Data)
        ↓
Extract (requests)
        ↓
Transform (Python)
        ↓
Load (MySQL)
        ↓
Schedule (Cron Job / Orchestrator)


#Project Stucture

api-ingestion-pipeline/
│
├── app/
│   ├── extract.py       # API calls
│   ├── transform.py     # Data cleaning & structuring
│   ├── load.py          # Database insertion
│   └── pipeline.py      # Orchestration
│
├── config/
│   └── db_config.py     # Database connection settings
│
├── .env                 # Environment variables (API keys, DB creds)
├── requirements.txt
└── README.md



#Technologies Used

- Python  
- requests (API calls)  
- MySQL (data storage)  
- python-dotenv (environment management)  
- Cron (task scheduling)  
- Prefect (workflow orchestration)



 # Data Source

Weather data is fetched from:

- [OpenWeather API](https://openweathermap.org/api)



  *Database Schema

  | Column         | Type      | Description         |
| -------------- | --------- | ------------------- |
| id             | INT       | Primary key         |
| city           | VARCHAR   | City name           |
| temperature    | FLOAT     | Temperature (°C)    |
| weather        | VARCHAR   | Weather description |
| ingestion_time | TIMESTAMP | Time of ingestion   |




#Database
<img width="1429" height="617" alt="image" src="https://github.com/user-attachments/assets/7a48da11-bdd7-4bac-8d1c-fbea71f7a487" />



#Workflow Architecture

<img width="980" height="886" alt="image" src="https://github.com/user-attachments/assets/5572082c-1efd-4199-a79a-ba51b9d800fc" />



#Key Learnings
Understanding API-based data ingestion
Structuring ETL pipelines
Managing Python project imports
Connecting Python to relational databases
Handling real-world debugging issues



#Project Context

This project is part of a larger system:

AI Concierge Platform

Where real-time data (weather, events, locations) will power intelligent recommendations for users.



#Author

Mercy Andrew



