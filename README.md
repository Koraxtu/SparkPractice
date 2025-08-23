# Spark + PySpark in Docker with VSCode & Jupyter

Run a local Spark cluster (master + workers) with a Jupyter server for PySpark
notebooks. Edit notebooks in VSCode while the compute runs in containers.

> Works on Docker Desktop (WSL2 on Windows), macOS, and Linux.

Python 3.12 REQUIRED,
---

## TLDR (Quick Start)

```bash
# 1) Add data source
In data/ folder, add a CSV/Parquet/JSON data source
SQL databases can be added as a source via JDBC

# 2) Start cluster + Jupyter
docker compose up -d

# 3) Open Jupyter
#    Token is set in compose (JUPYTER_TOKEN=dev)
#    Or connect VSCode → Jupyter: Existing server → http://localhost:8888/?token=dev

# 4) Test your config
Run the first 2 Jupyter cells.
If the first one fails, most likely, the containers did not start up correctly.
If the second cell fails, most likely, your environment is not configured correctly for Python 3.12 
You may have to restart your pc after correcting the environment to ensure everything works.