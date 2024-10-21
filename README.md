# Strimzi Kafka Local Installation for Docker Desktop
The purpose of this guide is only to know the steps I followed to install Strimzi Kafka in my Docker Desktop installation.

## Deploy Operator
First I am going to create the namespace and install all the Custom Resource Definitions.

#### 1. Create Kafka Namespace
`kubectl create namespace kafka`

#### 2. Install Kafka Operator
`kubectl create -f 'https://strimzi.io/install/latest?namespace=kafka' -n kafka`


