# batch-data-pipeline-airflow-postgres


**One-line:** A small reproducible ETL pipeline that extracts CSV data, transforms it with Pandas, and loads results into Postgres — orchestrated by Apache Airflow inside Docker.


## What you get
- `docker-compose.yml` to run Airflow (webserver + scheduler) and Postgres locally.
- `dags/batch_etl_dag.py` — Airflow DAG that defines `extract -> transform -> load` tasks.
- `scripts/etl.py` — Python code (Pandas) with the ETL logic.
- `data/sample/sales.csv` — small sample dataset so the pipeline runs out-of-the-box.
- `tests/test_transform.py` — pytest unit tests for the transform function.
- `requirements.txt` — packages used by tests/local scripts.


## Prerequisites
- Docker and Docker Compose installed (Desktop or Engine). Tested with Docker Compose v2.
- (Optional) Python 3.10+ and pip if you want to run tests locally.


## Quick start (recommended)
1. Clone the repo.
2. Start services:


```bash
# start Postgres and Airflow containers
docker compose up -d
