FROM apache/airflow:2.6.1
USER root
RUN apt update && apt install -y default-jdk
COPY env.sh /opt/env.sh
COPY trino /opt/trino
RUN chmod +x /opt/trino
USER airflow
RUN pip install pyspark confluent_kafka