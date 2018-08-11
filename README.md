# Running Prometheus Docker container for monitoring Microservices on Raspberry Pi

Emerging trends like microservices & containerization on IoT devices like Raspberry Pi, BananaPi, ZeroPi etc., all keep pushing the 
boundaries of what constitutes DevOps Monitoring. We have customers using Prometheus that are monitoring and controlling their IoT 
infrastructure , application and database instances, and containers—providing a consolidated view or single pane of glass solution to 
their DevOps monitoring needs. Dockerworx Ready Solution for Prometheus Stack comprises of ready-to-use Prometheus, Grafana, cAdvisor, 
Grafana, Zipkin & AlertManager all integrated with Slack channel for real-time alerts and management.

## What’s unique about Prometheus?
 
Prometheus is a self-hosted set of tools which collectively provide metrics storage, aggregation, visualization and alerting. Usually most of the available monitoring tools are push based, i.e. agents on the monitored servers talk to a central server (or set of servers) and send out their metrics. Prometheus is little different on this aspect – It is a pull based server which expects monitored servers to provide a web interface from which it can scrape data. This is a unique characteristic of Prometheus.

The main features of Prometheus can be summed below:

Decentralized architecture
Scalable data collection
Powerful Query language (leverages the data model for meaningful alerting (including easy silencing) and graphing (for dashboards and for ad-hoc exploration).
A multi-dimensional data model.( data can be sliced and diced at will, along dimensions like instance, service, endpoint, and method)
No reliance on distributed storage; single server nodes are autonomous.
Time series collection happens via a pull model over HTTP.
Pushing time series is supported via an intermediary gateway.
Targets are discovered via service discovery or static configuration.
Multiple modes of graphing and dashboard support.
You can deep dive more into its architecture at https://prometheus.io/docs/introduction/overview/#architecture.

Under this blog post, we will see how to bring Dockerworx Ready Solution for Prometheus in just 5 minutes. Let’s get started –

## Pre-requisite:

## Hardware:

- Raspberry Pi 3 ( You can order it from Amazon in case you are in India for $35)
- Micro-SD card reader ( I got it from here )
- Any Windows or Linux Desktop or Laptop
- HDMI cable ( I used the HDMI cable of my plasma TV)
- Internet Connectivity(Wifi/Broadband/Tethering using Mobile) – to download Docker 1.12.1 package
- Keyboard & mouse connected to Pi’s USB ports


## Software:

- SD-Formatter – to format microSD card
- Win32 disk imager(in case you have Windows OS running on your laptop) – to burn Raspbian Jessie ISO into microSD card

## Steps:

Format the microSD card using SD Formatter. Insert the microSD card into your Pi box. Now connect the HDMI cable  from one end of Pi’s HDMI slot to your TV or display unit and mobile charger(recommended 5.1V@1.5A).

## Installing Docker

Use the below command to bring up Docker

```
$curl -sSL https://get.docker.com/ | sh
```

## Verify if Docker is installed or not using the below command:

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
