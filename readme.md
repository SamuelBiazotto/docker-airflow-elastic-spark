# Requirements
- Docker version: 20
- Docker-compose version: 1.29

# Introduction 
- This project contains a docker runing a Apache Spark Cluster with JupyterLab, an Elastic stack with Kibana, and Apache Airflow

- For Elastic use localhost:5601
    - ES01 in port 9200

- For JupyterLab use localhost:8888
    - master in 8080
    - workers in 8081 ans 8082

- For Airflow use localhost:9090
    - user: airflow
    - passwor: airflow

- Redis in port 6379

- Postgres in port 5432

- Flower in localhost:5555

# Start

º Remember to give permission to folder and files with *sudo chmod -R 777* 
º Need incresse memory for elastic search with the command: *sysctl -w vm.max_map_count=262144*
º To see if the command works execute: *sysctl vm.max_map_count*


1. First run *sudo ./build.sh* to download some dependencies (may take some time)

2. Second run *sudo docker-compose up airflow-init* to download and start airflow dependencies 

3. Third run *sudo docker-compose up* to download an set elastic and kibana dependencies and start all services.



# Links

[Airflow](http://airflow.apache.org/)<br>
[Elastic](https://www.elastic.co/pt/elastic-stack)<br>
[Kibana](https://www.elastic.co/pt/what-is/kibana)<br>
[Spark](https://spark.apache.org/)<br>
[Jupyter](https://jupyter.org/)<br>
[Docker](https://www.docker.com/)<br>
[Docker Compose](https://docs.docker.com/compose/)<br>
[Spark Clusterization](https://towardsdatascience.com/apache-spark-cluster-on-docker-ft-a-juyterlab-interface-418383c95445)<br><br>


# Thanks To
* **André Perez** - To amazing tutorial of Spark Clusterization (The images in docs was made by him)
