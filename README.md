# Data Engineering Project

This is my data engineering demo project, which consists of the following:

- Data Source: DuckDB dataset serves as the foundation
- API Layer: Go service exposes endpoints for raw data access
- Transformation: dbt handles the data modeling and transformations
- Orchestration: Dagster manages the entire pipeline execution
- Analytics: Python and R provide reports and visualizations

AI (Claude) is used in this project only for these purposes:

- Writing documentations (docstrings, README, etc)
- Writing unit tests
- Generating a Makefile
- Code review with the following prompt:

> Please review this code and provide suggestions for improvement. Identify common issues such as code smells, anti-patterns, potential bugs, performance bottlenecks, and security vulnerabilities. Prioratize readability and maintainability. Do not provide code, but offer general recommendations to improve the overall quality of the code.

## Workflow

Here's how the components interact:

1. Dagster triggers the overall pipeline
2. Raw data is validated/prepared
3. Go API is started and running
4. dbt models are run to transform the data
5. Analytics scripts generate reports/visualizations
6. Logs are collected throughout the process

## Project Structure

```
./
├── README.md                   # You are here
├── data/
│   ├── raw/                    # Original DuckDB dataset
│   └── transformed/            # Output from dbt transformations
├── api/                        # Go API service
├── dbt/                        # dbt project
├── dagster/                    # Dagster project
├── analytics/
│   ├── python/                 # Python notebooks/scripts
│   └── r/                      # R reports/scripts
└── logs/                       # Centralized logging directory
```

## TODO

- Use Docker
