from airflow import DAG
from airflow.operators.python import PythonOperator
from datetime import datetime

def print_hello():
    print("Hello from Airflow DAG!")

with DAG(
    dag_id='sample_hello_dag',
    start_date=datetime(2023, 1, 1),
    schedule_interval='@daily',
    catchup=False,
    tags=['example'],
) as dag:
    hello_task = PythonOperator(
        task_id='print_hello',
        python_callable=print_hello,
    )
