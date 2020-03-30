# docker-airflow

An adapted version of [puckel/docker-airflow](https://github.com/puckel/docker-airflow) to specifically for `airflow=1.9` and `python 2.7`.

## Build

    docker build --rm -t ibromley/docker-airflow:1.0 .

## Usage

By default, docker-airflow runs Airflow with **SequentialExecutor** :

    docker run -d -p 8080:8080 ibromley/docker-airflow:1.0 webserver

If you want to run another executor, use the other docker-compose.yml files provided in this repository.

Utilize the **LocalExecutor** :

    docker-compose -f docker-compose-local.yml up -d

Utilize the **CeleryExecutor** :

    docker-compose -f docker-compose-celery.yml up -d

## UI Links

- Airflow: [localhost:8080](http://localhost:8080/)