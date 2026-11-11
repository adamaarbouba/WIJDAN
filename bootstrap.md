# Bootstrap Guide

Quick instructions for spinning up services locally with Docker.

---

## 1. Initial Setup

Ensure your local environment configuration exists:

```bash
cp .env.example .env
```

Ensure `AIRFLOW_UID` matches your host user ID (run `id -u` on Linux):
```bash
echo "AIRFLOW_UID=$(id -u)" >> .env
```

---

## 2. Running Jupyter for EDA & Experimentation

To start **only** the JupyterLab container with all dependencies (`pandas`, `scikit-learn`, `matplotlib`, `seaborn`, etc.) without starting the rest of the Airflow services:

```bash
docker compose up --build jupyter
```

- Open in browser: **[http://localhost:8888](http://localhost:8888)**
- All changes made in the browser are synced in real time to your local `./notebook/` directory.
- Data is available at `data/student_mental_health.csv` (or `/opt/airflow/data/student_mental_health.csv`).

To run it in the background:
```bash
docker compose up -d --build jupyter
```

To stop it:
```bash
docker compose stop jupyter
```

---

## 3. Running the Full Stack (Airflow + Postgres)

When you are ready to orchestrate DAGs:

```bash
docker compose up -d --build
```

- **Airflow Webserver:** [http://localhost:8080](http://localhost:8080)
- **Default Credentials:** Defined in `.env` (`AIRFLOW_DB_USER` / `AIRFLOW_DB_PASSWORD`)

---

## 4. Teardown & Maintenance

- View container logs:
  ```bash
  docker compose logs -f jupyter
  ```
- Stop all services:
  ```bash
  docker compose down
  ```
- Stop and remove volumes (reset database):
  ```bash
  docker compose down -v
  ```
