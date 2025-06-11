# 🦠 COVID-19 Data Pipeline

This project is a simple end-to-end data pipeline that fetches global COVID-19 statistics daily from a public API and stores it in a PostgreSQL database using Apache Airflow.

---

## 📌 Purpose

As an Associate Data Engineer intern in my learning phase, I built this mini-project to:
- Understand how data pipelines work in a real-world context
- Learn how Apache Airflow schedules and manages DAGs
- Practice database handling using PostgreSQL
- Gain familiarity with Docker-based data engineering setups

---

## ⚙️ Tech Stack

- **Apache Airflow**: For orchestrating and scheduling tasks
- **PostgreSQL**: As the database to store the data
- **Docker**: To containerize the entire setup
- **Python**: For fetching and inserting the data
- **disease.sh API**: Public COVID-19 stats API

---

## 📁 Project Structure

covid-data-pipeline/
│
├── airflow-docker/
│ ├── dags/ # Airflow DAGs
│ ├── scripts/ # Python scripts for data fetching/insertion
│ ├── plugins/ # (optional) custom plugins
│ ├── logs/ # DAG run logs
│ ├── requirements.txt # Python dependencies
│ └── docker-compose.yaml # Docker setup
│
├── screenshots/ # Project screenshots
├── README.md
└── .gitignore

---

---

## 🛠️ How It Works

1. Airflow DAG runs once daily (`@daily`)
2. A Python script fetches COVID-19 stats from `https://disease.sh/v3/covid-19/all`
3. The data is inserted into a PostgreSQL table (`covid_stats`)
4. Logs are stored and monitored via Airflow UI

---

## 📸 Screenshots

| DAG in Airflow UI | PostgreSQL Table | Logs Sample |
|------------------|------------------|-------------|
| ![DAG](./screenshots/dag_running.png) | ![Postgres](./screenshots/data_in_postgres.png) | ![Logs](./screenshots/logs_sample.png) |

---

## ✅ Learnings & Takeaways

- Set up Airflow using Docker
- Created and ran custom Python tasks in Airflow
- Connected to and inserted data into PostgreSQL using Python
- Handled task retries, error logging, and schedule intervals

---

## 🧠 What's Next?

This was a foundational project. As next steps, I plan to:
- Add a data deduplication logic (to avoid inserting the same row daily)
- Add a Streamlit dashboard for visualizing the data (maybe 😉)
- Explore parameterization and templating in Airflow

---

## 🙌 Acknowledgements

- COVID-19 data from [disease.sh](https://disease.sh/)
- Docker + Airflow base from Apache documentation

---

## 🧑‍💻 Author

**Mohamed Hussain S**  
Associate Data Engineer Intern  
[LinkedIn](https://linkedin.com/in/hussainmohhdd) | [GitHub](https://github.com/mohhddhassan)
