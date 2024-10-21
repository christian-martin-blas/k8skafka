# Strimzi Kafka Local Installation for Docker Desktop
The purpose of this guide is only to know the steps I followed to install Strimzi Kafka in my Docker Desktop installation.

## Deploy Operator
First I am going to create the namespace and install all the Custom Resource Definitions.

#### 1. Create Kafka Namespace
`kubectl create namespace kafka`

#### 2. Install Kafka Operator
`kubectl create -f 'https://strimzi.io/install/latest?namespace=kafka' -n kafka`

## Deploy Kafka Cluster
#### 1. Deploy Single Kafka Node Cluster
`kubectl apply -f https://strimzi.io/examples/latest/kafka/kraft/kafka-single-node.yaml -n kafka`

#### 2. Check Kafka Cluster Status
You can check if all the pods are deployed and running by executing the following command:
`kubectl get pods -w -n kafka`

