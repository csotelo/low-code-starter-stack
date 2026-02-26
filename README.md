# Low-Code Starter Stack

## Purpose
This project is a personal starter blueprint designed to facilitate the rapid deployment of a low-code automation. It bridges the gap between **n8n** (automation), **NoSQL/Relational databases**, and **S3-compatible storage**, providing a robust foundation for projects.

## Technical Information
The stack is built on a **Twelve-Factor App** methodology, utilizing Docker Compose for container orchestration on **Debian 13**. It features strict service dependency management through health checks.

### Core Stack:
* **Automation:** n8n (Queue Mode)
* **Databases:** PostgreSQL 16, MongoDB 4.4, Redis (Broker/Cache)
* **AI/Vector Search:** Qdrant
* **Storage:** MinIO (S3 Compatible)
* **Observability:** Dozzle (Log Viewer)

## URL Access & References
Once the stack is running ("docker-compose up -d"), you can access the following interfaces:

| Service | Local URL | Default Credentials |
| :--- | :--- | :--- |
| **n8n** | http://localhost:5678 | Configured in .env |
| **MinIO Console** | http://localhost:9001 | admin / supersecretminio |
| **Dozzle (Logs)** | http://localhost:8888 | No Auth |
| **Mongo Express** | http://localhost:8081 | admin / admin |
| **Redis Commander** | http://localhost:8082 | No Auth |
| **Qdrant Dashboard**| http://localhost:6333/dashboard | No Auth |

## Backup Strategy
Automated daily backups are handled by the "db_backup" service. 
* **Frequency:** Daily at 03:00.
* **Retention:** 7 days.
* **Target:** MinIO "backups" bucket.

## License
Apache License 2.0 - See LICENSE file for details.