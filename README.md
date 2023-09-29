# weatherapi-data-pipeline-airflow

### Introduction
This project builds an ETL (Extract, Transform, Load) pipeline using the weather API on AWS and orchestrate using Airflow. The pipeline retrieves data from the weather API, transform it to a desired format, and load it into AWS S3.  

### About API
API has information about current weather. [WeatherMap API](https://openweathermap.org/api)

### Architecture
![Architecture Diagram](https://github.com/vponkia/weatherapi-data-pipeline-airflow/blob/main/Data%20Pipeline%20Flow.png)

### Services/Platforms Used
1. **S3(Simple Storage Service):** Amazon S3 is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups, and static website files.

2. **EC2 Instance(Elastic Compute Cloud):** An EC2 instance is a virtual server in Amazon Web Services (AWS) that provides scalable computing capacity in the cloud.

3. **Apache Airflow:** Apache Airflow is an open-source platform designed for orchestrating complex workflows, scheduling tasks, and managing data pipelines. It allows users to define, schedule, and monitor workflows as directed acyclic graphs (DAGs).

4. **SSH Remote extension:** An extension that allows to work on remote development projects by connecting to a remote server using SSH (Secure Shell) directly from within the VS Code editor.

### commands for installation

```
sudo apt update
sudo apt install python3-pip
sudo apt install python3.10-venv
python3 -m venv airflow_venv
sudo pip install pandas
sudo pip install s3fs
sudo pip install apache-airflow
airflow standalone
```

### To configure AWS access key and secret key in VS Code

```
source airflow_venv/bin/activate
sudo apt  install awscli
aws configure
aws sts get-session-token
```

### Project Execution Flow
Extract Data From API -> Transform data using python -> Store to S3 (Manage the flow using Airflow)
