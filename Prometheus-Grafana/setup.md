
# Prometheus-Grafana Setup

This setup demonstrates how to monitor an Apache web server using Prometheus and Grafana, all orchestrated with Docker Compose.

## Overview

1. **Prometheus**: Used for scraping and storing metrics from the Apache web server.
2. **Grafana**: Provides a visualization layer for the metrics collected by Prometheus.
3. **Apache Web Server**: Acts as the target for Prometheus to scrape metrics.

## Steps to Set Up

1. **Clone the Repository**:
   Ensure you have the project cloned locally.

2. **Configure Prometheus**:
   - The `prometheus.yml` file is pre-configured to scrape metrics from the Apache web server running on `web_server:80`.
   - Prometheus will scrape metrics every 15 seconds as defined in the `scrape_interval`.

3. **Run Docker Compose**:
   Use the following command to start all services:
   ```bash
   docker-compose up -d

4. **Access the Services**:

   Prometheus: http://localhost:9090
   Grafana: http://localhost:3000
   Apache Web Server: http://localhost:80
   
5. **Visualize Metrics in Grafana**:

   Log in to Grafana (default credentials: admin/admin).
   Add Prometheus as a data source.
   Import or create dashboards to visualize Apache metrics.


## Adding some ScreenShot of the practical



