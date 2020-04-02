FROM openjdk:8

RUN apt-get update && \
    apt-get install -y \
    jq \
    python-pip

RUN pip install awscli --upgrade