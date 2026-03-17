![Monitoring Stack](./ss/monitoring-stack.png)
# Monitoring Stack

Monitoring Stack (Kubernetes + Prometheus + Grafana)

A production-style DevOps project demonstrating Kubernetes monitoring using Prometheus for metrics collection and Grafana for visualization.

# Project Overview

Monitoring is a critical component of modern DevOps and production systems.

This project sets up a complete monitoring stack inside a Kubernetes cluster where:

      Prometheus collects metrics from the cluster
      Grafana visualizes metrics using dashboards

# Architecture

User (Browser)<br>
      ↓<br>
Node Exporter (metrics source)<br>
      ↓<br>
Prometheus (collection)<br>
      ↓<br>
Grafana (visualization)<br>

User (Browser)<br>
      ↓<br>
Grafana (Visualization Layer)<br>
      ↓<br>
Prometheus (Metrics Collection)<br>
      ↓<br>
Kubernetes Cluster (Pods & Nodes)

Project Structure
devops-monitoring-stack/<br>
 ├── monitoring/<br>
 │    ├── prometheus.yaml<br>
 │    └── grafana.yaml<br>
 └── README.md

# Tools Used

Container Orchestration

      • Kubernetes

Monitoring & Metrics Collection

      • Prometheus

Visualization Dashboard

      • Grafana

Local Kubernetes Cluster

      • Minikube


# Monitoring Workflow

      • Prometheus scrapes metrics from Kubernetes workloads
      • Metrics are stored in the Prometheus database as time-series data
      • Grafana reads metrics from Prometheus
      • Dashboards visualize system performance


# Metrics Monitored

Examples include:

      • CPU usage
      • Memory usage
      • Pod status
      • Node health
      • Cluster performance

# Deployment Workflow

Start Cluster

      minikube start
      kubectl get nodes

Deploy Prometheus

      kubectl apply -f prometheus.yaml

Deploy Grafana
      
      kubectl apply -f grafana.yaml

Verify Resources
      
      kubectl get pods
      kubectl get services

Access Services
      
      minikube service prometheus
      minikube service grafana

# Grafana Setup

Default credentials:

      Username: admin
      Password: admin

Add Prometheus Data Source

      URL: http://prometheus:9090

# Dashboard Setup

Import dashboard using ID:

      1860

# Cleanup

      minikube delete

# What This Project Demonstrates

      • Kubernetes monitoring fundamentals
      • Metrics collection using Prometheus
      • Visualization using Grafana
      • Observability in DevOps

# Future Improvements

      • Add Alertmanager for alerts
      • Configure Slack/Email notifications
      • Monitor application-level metrics
      • Deploy on cloud Kubernetes (EKS/GKE)

Screenshots

Start Cluster

![Start Cluster](<./ss/>)

Deploy Prometheus

![Deploy Prometheus](<./ss/>)

Deploy Grafana

![Deploy Grafana](<./ss/>)

Verify Resources

![Verify Resources](<./ss/>)

Access Services

![Access Services](<./ss/>)

Grafana Setup

![Grafana Setup](<./ss/>)

Dashboard Setup

![Dashboard Setup](<./ss/>)

Cleanup

![Cleanup](<./ss/>)
