# ⚙️ n8n Repocloud Deployment (Autoscaling + Queue Mode)

This repository demonstrates how to deploy **production-ready n8n workflows** on Railway or Repocloud using queue mode, autoscaling workers, and a reliable backend setup.

---

## 🚀 Overview

n8n Cloud works well for simple use cases, but as workflows scale, teams often face:

- Execution limits  
- Failed jobs during spikes  
- Lack of proper autoscaling  
- Limited observability  

This setup solves those issues by moving to a **self-hosted, autoscaled architecture**.

---

## 🧩 What this solves

- Reliable execution of high-volume workflows  
- Horizontal scaling using worker queues  
- Reduced downtime and failed jobs  
- Better control over infrastructure and performance  

---

## 🏗 Architecture

**Core components:**

- **n8n (main instance)** – handles orchestration  
- **Worker instances** – process jobs in queue mode  
- **Redis** – job queue  
- **Postgres** – workflow + execution data  
- **S3-compatible storage** – binary data  
- **Repocloud autoscaling** – dynamic scaling based on load  
- **Railway autoscaling** – dynamic scaling based on load  
---

## ⚙️ Key Features

- Queue-based execution (Redis)
- Autoscaling worker configuration
- Retry & error handling strategies
- Environment-based configuration
- Health checks & monitoring setup
- Scalable architecture for production workloads

---

## 📂 Repository Structure

```bash
.
├── docker/
│   ├── docker-compose.queue.yml
│   ├── docker-compose.worker.yml
│   └── .env.example
├── repocloud/
│   ├── autoscale-config-example.md
│   └── deployment-notes.md
├── redis/
│   └── queue-mode-explained.md
├── postgres/
│   └── database-setup.md
├── monitoring/
│   ├── logging-strategy.md
│   └── retry-strategy.md
└── screenshots/
    └── architecture-diagram.png
