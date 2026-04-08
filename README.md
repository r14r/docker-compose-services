# docker-compose-services

A curated collection of reusable Docker Compose service definition snippets, organized by topic.
Each YAML file contains a single service block that can be copied into your own `docker-compose.yml`.

## Usage

Copy the desired service snippet(s) into the `services:` section of your `docker-compose.yml` and adjust environment variables, ports, and volumes as needed.

```yaml
services:
  # paste service definition here
```

---

## Services

### 🤖 AI / Machine Learning — [`services/ai/`](services/ai/)

| File | Description |
|---|---|
| [ollama.yml](services/ai/ollama.yml) | Ollama LLM server with optional GPU support |
| [ollama-init.yml](services/ai/ollama-init.yml) | One-shot init container to pre-pull Ollama models |
| [open-webui.yml](services/ai/open-webui.yml) | Open WebUI chat interface for Ollama |
| [localai.yml](services/ai/localai.yml) | LocalAI — self-hosted OpenAI-compatible API |

### 🗄️ Databases — [`services/databases/`](services/databases/)

| File | Description |
|---|---|
| [postgresql.yml](services/databases/postgresql.yml) | PostgreSQL 16 relational database |
| [mysql.yml](services/databases/mysql.yml) | MySQL 8 relational database |
| [mariadb.yml](services/databases/mariadb.yml) | MariaDB 11 relational database |
| [mongodb.yml](services/databases/mongodb.yml) | MongoDB 7 document database |
| [redis.yml](services/databases/redis.yml) | Redis 7 in-memory key/value store |
| [elasticsearch.yml](services/databases/elasticsearch.yml) | Elasticsearch 8 search and analytics engine |

### 📨 Messaging — [`services/messaging/`](services/messaging/)

| File | Description |
|---|---|
| [rabbitmq.yml](services/messaging/rabbitmq.yml) | RabbitMQ message broker with management UI |
| [zookeeper.yml](services/messaging/zookeeper.yml) | Apache ZooKeeper (required by Kafka) |
| [kafka.yml](services/messaging/kafka.yml) | Apache Kafka distributed event streaming |
| [nats.yml](services/messaging/nats.yml) | NATS messaging system with JetStream |

### 🔀 Proxy / Web Servers — [`services/proxy/`](services/proxy/)

| File | Description |
|---|---|
| [nginx.yml](services/proxy/nginx.yml) | Nginx web server and reverse proxy |
| [traefik.yml](services/proxy/traefik.yml) | Traefik v3 edge router with Docker provider |
| [caddy.yml](services/proxy/caddy.yml) | Caddy web server with automatic HTTPS |

### 📊 Monitoring — [`services/monitoring/`](services/monitoring/)

| File | Description |
|---|---|
| [prometheus.yml](services/monitoring/prometheus.yml) | Prometheus metrics collection |
| [grafana.yml](services/monitoring/grafana.yml) | Grafana metrics visualization dashboard |
| [node-exporter.yml](services/monitoring/node-exporter.yml) | Prometheus Node Exporter for host metrics |
| [cadvisor.yml](services/monitoring/cadvisor.yml) | cAdvisor container resource usage metrics |
| [alertmanager.yml](services/monitoring/alertmanager.yml) | Prometheus Alertmanager for alert routing |

### 💾 Storage — [`services/storage/`](services/storage/)

| File | Description |
|---|---|
| [minio.yml](services/storage/minio.yml) | MinIO S3-compatible object storage |
| [nextcloud.yml](services/storage/nextcloud.yml) | Nextcloud self-hosted file sync and share |

### 🛠️ Dev Tools — [`services/devtools/`](services/devtools/)

| File | Description |
|---|---|
| [gitea.yml](services/devtools/gitea.yml) | Gitea self-hosted Git service |
| [vault.yml](services/devtools/vault.yml) | HashiCorp Vault secrets management (dev mode) |
| [portainer.yml](services/devtools/portainer.yml) | Portainer Docker management UI |

---

## Contributing

Feel free to open a PR adding new service definitions. Place each service in the appropriate topic directory and follow the existing file format.
