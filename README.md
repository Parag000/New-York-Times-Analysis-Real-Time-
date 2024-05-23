# Apache AirFlow Pipelines

The nyt_dag.py script defines 2 Airflow DAG pipelines:
- Real_time_api_pipeline: A pipeline to fetch data from NYT Archive Data real time api, process the data and insert the data into snowflake database NYT_DB.NYT_SCHEMA. This pipeline is scheduled to run every 1st day of month at 12 am.
- Transformation_pipeline: A pipeline to apply transformations and performs analytics. The summarized results are loaded to snowflake database NYT_DB.NYT_RESULTS_SCHEMA. This pipeline is scheduled to run every 1st day of month at 6 am.

To run the piplines start the Airflow though terminal:
astro dev start
To view the pipeline go to Airflow Webserver: http://localhost:8080 on the browser.
