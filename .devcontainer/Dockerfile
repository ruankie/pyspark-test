FROM python:3.7-slim

COPY ./requirements.txt /requirements.txt

# python packages and git
RUN apt update && \
    apt install --no-install-recommends -y build-essential gcc && \
    apt install -y git && \
    apt clean && rm -rf /var/lib/apt/lists/* && \
    pip3 install --no-cache-dir -r /requirements.txt

# java setup
RUN apt install curl mlocate default-jdk -y

# spark
RUN wget https://dlcdn.apache.org/spark/spark-3.2.1/spark-3.2.1-bin-hadoop3.2.tgz && \
    tar xvf spark-3.2.1-bin-hadoop3.2.tgz && \
    mv spark-3.2.1-bin-hadoop3.2/ /opt/spark

ENV SPARK_HOME="/opt/spark"
ENV PATH="${PATH}:${SPARK_HOME}/bin:${SPARK_HOME}/sbin"

RUN start-master.sh


EXPOSE 8080
