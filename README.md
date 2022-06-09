# airflow

## start
### 1. docker
```
docker-compose up
```
### 2. edit or add script in ./dags
```
kst = pendulum.timezone("Asia/Seoul")

with DAG(
    dag_id='first_sample_dag',
    start_date=datetime(2022, 6, 9, tzinfo=kst),
    # schedule_interval="47 * * * *"            # when you scheduling
    schedule_interval=None                      # when no scheduling

) as dag:
```

* when you wanna setting schedule
    ```
    # schedule_interval="47 * * * *"            # when you scheduling
    ```

* when you wanna unsetting schedule
    ```
    schedule_interval=None                      # when no scheduling
    ```

### 3. check localhost:8080
