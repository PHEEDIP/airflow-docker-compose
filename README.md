# Apache Airflow with Docker Compose

![Airflow Logo](https://upload.wikimedia.org/wikipedia/commons/d/de/AirflowLogo.png)

Welcome to the Apache Airflow Docker Compose project! This repository contains everything you need to deploy Apache Airflow using Docker Compose, making it easy to orchestrate complex workflows in a containerized environment.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Directory Structure](#directory-structure)
  - [Environment Variables](#environment-variables)
- [Usage](#usage)
  - [Running Airflow](#running-airflow)
  - [Accessing the Web Interface](#accessing-the-web-interface)
  - [Connecting to the Airflow CLI](#connecting-to-the-airflow-cli)
  - [Stopping Airflow](#stopping-airflow)
- [Configuration](#configuration)
  - [Modifying the Docker Compose File](#modifying-the-docker-compose-file)
  - [Customizing Airflow Configuration](#customizing-airflow-configuration)
- [Common Issues & Troubleshooting](#common-issues--troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project provides a Docker Compose setup for running Apache Airflow with essential components like PostgreSQL for the metadata database, Redis for Celery backend, and Flower for monitoring. This setup is ideal for development and small-scale production deployments.

**Apache Airflow** is an open-source tool to programmatically author, schedule, and monitor workflows. Using Docker Compose simplifies setting up the Airflow environment by managing the services through containers.

![Architecture Diagram](https://airflow.apache.org/docs/apache-airflow/stable/_images/arch-diagram.png)

## Features

- **Dockerized Environment:** Run Airflow and its components in isolated Docker containers.
- **Scalable Architecture:** Easily scale your worker nodes using Celery Executor.
- **Preconfigured Database:** Includes PostgreSQL for reliable metadata management.
- **Monitoring:** Integrate Flower for real-time monitoring of Celery tasks.
- **Extensible:** Customize the Airflow configuration as per your requirements.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Docker:** [Install Docker](https://docs.docker.com/get-docker/)
- **Docker Compose:** [Install Docker Compose](https://docs.docker.com/compose/install/)
- **Git:** [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

### Installation

Clone the repository to your local machine:

```bash
git clone https://github.com/PHEEDIP/airflow-docker-compose.git
cd airflow-docker-compose
docker compose up airflow-init

after finish

```bash
docker compose up

Login at web ui http://localhost:8080.
user/password : airflow / airflow