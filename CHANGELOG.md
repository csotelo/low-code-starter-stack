# Changelog

## [0.2.0] - 2026-02-26

### Added
- Expanded Docker Compose with **Qdrant**, **MinIO**, **Dozzle**, and **MongoDB**.
- Integrated **Mongo Express** and **Redis Commander** for database management.
- Added **tiredofit/db-backup** for automated daily S3 backups to MinIO.
- Implemented **mcuadros/ofelia** as a sidecar scheduler for workflow versioning.
- Established strict service health check dependencies for **n8n** startup.
- Updated ".env" structure to include S3 and NoSQL credentials.
- Applied **Apache 2.0** License to the project.

## [0.1.0] - 2026-02-23

### Added
- Initial Docker Compose blueprint for **n8n**, **Postgres**, and **Redis**.
- Version control strategy for workflows using local volume mapping.
- ".gitignore" to protect environment secrets.