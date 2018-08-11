# prometheus-armhf

Emerging trends like microservices & containerization on IoT devices like Raspberry Pi, BananaPi, ZeroPi etc., all keep pushing the 
boundaries of what constitutes DevOps Monitoring. We have customers using Prometheus that are monitoring and controlling their IoT 
infrastructure , application and database instances, and containers—providing a consolidated view or single pane of glass solution to 
their DevOps monitoring needs. Dockerworx Ready Solution for Prometheus Stack comprises of ready-to-use Prometheus, Grafana, cAdvisor, 
Grafana, Zipkin & AlertManager all integrated with Slack channel for real-time alerts and management.

 
Prometheus is a systems and service monitoring system. It collects metrics from configured targets at given intervals, evaluates rule expressions, displays the results, and can trigger alerts if some condition is observed to be true.

In case you are Raspberry Pi user and want to try it, check this out !

## Features of Prometheus

Prometheus’s main features are:

a multi-dimensional data model (time series identified by metric name and key/value pairs)
a flexible query language to leverage this dimensionality
no reliance on distributed storage; single server nodes are autonomous
time series collection happens via a pull model over HTTP
pushing time series is supported via an intermediary gateway
targets are discovered via service discovery or static configuration
multiple modes of graphing and dashboarding support
To learn more, refer : https://prometheus.io/docs/introduction/overview/

Under this blog post, we will see how to bring Dockerworx Ready Solution for Prometheus in just 5 minutes. Let’s get started –

## Pre-requisite:

Flash Raspberry Pi 3 with Raspbian OS using SD card
Use the below command to bring up Docker
$curl -sSL https://get.docker.com/ | sh

Verify if Docker is installed or not using the below command:

```
$docker version
```
## Pulling the GITHUB repository:

```
$git clone https://github.com/dockerworx/prometheus-armv7
```

```
$cd prometheus-armv7
```

Run the below command to bring up Prometheus Stack on Raspberry Pi 3:

```
docker run -d –net=host -v /prometheus.yml:/etc/prometheus/prometheus.yml dockerworx/prometheus-armh7
```

Here you go.. Dockerworx Ready Bundle for Prometheus Stack on IoT device is up and running.

Are you looking out to learn more? Connect to us through Slack
