# docker-compose-services

A curated collection of reusable Docker Compose service definition snippets, organized by topic.
Each YAML file contains a single service block that can be copied into your own `docker-compose.yml`.

## Usage

Copy the desired service snippet(s) into the `services:` section of your `docker-compose.yml` and adjust environment variables, ports, and volumes as needed.

```yaml
services:
  # paste service definition here
```

Replace every `CHANGEME` placeholder with a strong secret before running in production.

---

## Services

### 🤖 AI / Machine Learning — [`services/ai/`](services/ai/)

| File | Description |
|---|---|
| [ollama.yml](services/ai/ollama.yml) | Ollama LLM server with optional GPU support |
| [ollama-init.yml](services/ai/ollama-init.yml) | One-shot init container to pre-pull Ollama models |
| [open-webui.yml](services/ai/open-webui.yml) | Open WebUI chat interface for Ollama |
| [localai.yml](services/ai/localai.yml) | LocalAI — self-hosted OpenAI-compatible API |
| [litellm.yml](services/ai/litellm.yml) | LiteLLM proxy — unified API gateway for 100+ LLM providers |
| [anythingllm.yml](services/ai/anythingllm.yml) | AnythingLLM — all-in-one AI document chat and agent platform |
| [flowise.yml](services/ai/flowise.yml) | Flowise — drag-and-drop LLM workflow builder |
| [comfyui.yml](services/ai/comfyui.yml) | ComfyUI — node-based Stable Diffusion UI (GPU) |

### 🗄️ Databases — [`services/databases/`](services/databases/)

| File | Description |
|---|---|
| [postgresql.yml](services/databases/postgresql.yml) | PostgreSQL 16 relational database |
| [mysql.yml](services/databases/mysql.yml) | MySQL 8 relational database |
| [mariadb.yml](services/databases/mariadb.yml) | MariaDB 11 relational database |
| [mongodb.yml](services/databases/mongodb.yml) | MongoDB 7 document database |
| [redis.yml](services/databases/redis.yml) | Redis 7 in-memory key/value store |
| [elasticsearch.yml](services/databases/elasticsearch.yml) | Elasticsearch 8 search and analytics engine |
| [cassandra.yml](services/databases/cassandra.yml) | Apache Cassandra 5 wide-column NoSQL database |
| [memcached.yml](services/databases/memcached.yml) | Memcached distributed memory caching |
| [influxdb.yml](services/databases/influxdb.yml) | InfluxDB 2 time-series database |
| [neo4j.yml](services/databases/neo4j.yml) | Neo4j 5 graph database |
| [clickhouse.yml](services/databases/clickhouse.yml) | ClickHouse columnar OLAP database |
| [cockroachdb.yml](services/databases/cockroachdb.yml) | CockroachDB distributed SQL database |
| [meilisearch.yml](services/databases/meilisearch.yml) | Meilisearch fast full-text search engine |

### 📨 Messaging — [`services/messaging/`](services/messaging/)

| File | Description |
|---|---|
| [rabbitmq.yml](services/messaging/rabbitmq.yml) | RabbitMQ message broker with management UI |
| [zookeeper.yml](services/messaging/zookeeper.yml) | Apache ZooKeeper (required by Kafka) |
| [kafka.yml](services/messaging/kafka.yml) | Apache Kafka distributed event streaming |
| [nats.yml](services/messaging/nats.yml) | NATS messaging system with JetStream |
| [mosquitto.yml](services/messaging/mosquitto.yml) | Eclipse Mosquitto MQTT broker |
| [emqx.yml](services/messaging/emqx.yml) | EMQX high-performance MQTT broker |
| [activemq.yml](services/messaging/activemq.yml) | Apache ActiveMQ Artemis message broker |
| [redpanda.yml](services/messaging/redpanda.yml) | Redpanda Kafka-compatible streaming platform |

### 🔀 Proxy / Web Servers — [`services/proxy/`](services/proxy/)

| File | Description |
|---|---|
| [nginx.yml](services/proxy/nginx.yml) | Nginx web server and reverse proxy |
| [traefik.yml](services/proxy/traefik.yml) | Traefik v3 edge router with Docker provider |
| [caddy.yml](services/proxy/caddy.yml) | Caddy web server with automatic HTTPS |
| [haproxy.yml](services/proxy/haproxy.yml) | HAProxy TCP/HTTP load balancer |

### 📊 Monitoring — [`services/monitoring/`](services/monitoring/)

| File | Description |
|---|---|
| [prometheus.yml](services/monitoring/prometheus.yml) | Prometheus metrics collection |
| [grafana.yml](services/monitoring/grafana.yml) | Grafana metrics visualization dashboard |
| [node-exporter.yml](services/monitoring/node-exporter.yml) | Prometheus Node Exporter for host metrics |
| [cadvisor.yml](services/monitoring/cadvisor.yml) | cAdvisor container resource usage metrics |
| [alertmanager.yml](services/monitoring/alertmanager.yml) | Prometheus Alertmanager for alert routing |
| [loki.yml](services/monitoring/loki.yml) | Grafana Loki log aggregation system |
| [promtail.yml](services/monitoring/promtail.yml) | Promtail log shipping agent for Loki |
| [uptime-kuma.yml](services/monitoring/uptime-kuma.yml) | Uptime Kuma self-hosted uptime monitoring |
| [jaeger.yml](services/monitoring/jaeger.yml) | Jaeger distributed tracing system |
| [zipkin.yml](services/monitoring/zipkin.yml) | Zipkin distributed tracing system |

### 💾 Storage — [`services/storage/`](services/storage/)

| File | Description |
|---|---|
| [minio.yml](services/storage/minio.yml) | MinIO S3-compatible object storage |
| [nextcloud.yml](services/storage/nextcloud.yml) | Nextcloud self-hosted file sync and share |
| [filebrowser.yml](services/storage/filebrowser.yml) | File Browser web-based file manager |
| [seafile.yml](services/storage/seafile.yml) | Seafile self-hosted cloud storage and collaboration |

### 🛠️ Dev Tools — [`services/devtools/`](services/devtools/)

| File | Description |
|---|---|
| [gitea.yml](services/devtools/gitea.yml) | Gitea self-hosted Git service |
| [vault.yml](services/devtools/vault.yml) | HashiCorp Vault secrets management (dev mode) |
| [portainer.yml](services/devtools/portainer.yml) | Portainer Docker management UI |
| [sonarqube.yml](services/devtools/sonarqube.yml) | SonarQube code quality and security analysis |
| [code-server.yml](services/devtools/code-server.yml) | VS Code in the browser via code-server |
| [jenkins.yml](services/devtools/jenkins.yml) | Jenkins automation server (LTS) |
| [nexus.yml](services/devtools/nexus.yml) | Sonatype Nexus Repository Manager |
| [n8n.yml](services/devtools/n8n.yml) | n8n workflow automation platform |
| [woodpecker-server.yml](services/devtools/woodpecker-server.yml) | Woodpecker CI server |
| [woodpecker-agent.yml](services/devtools/woodpecker-agent.yml) | Woodpecker CI agent |

### 🔒 Security / Auth — [`services/security/`](services/security/)

| File | Description |
|---|---|
| [keycloak.yml](services/security/keycloak.yml) | Keycloak identity and access management (IAM) |
| [authelia.yml](services/security/authelia.yml) | Authelia authentication and authorization server |
| [authentik-server.yml](services/security/authentik-server.yml) | Authentik IdP server |
| [authentik-worker.yml](services/security/authentik-worker.yml) | Authentik background worker |
| [vaultwarden.yml](services/security/vaultwarden.yml) | Vaultwarden — self-hosted Bitwarden-compatible server |
| [crowdsec.yml](services/security/crowdsec.yml) | CrowdSec collaborative security engine |

### 🎬 Media — [`services/media/`](services/media/)

| File | Description |
|---|---|
| [jellyfin.yml](services/media/jellyfin.yml) | Jellyfin free media server |
| [plex.yml](services/media/plex.yml) | Plex Media Server |
| [sonarr.yml](services/media/sonarr.yml) | Sonarr TV series manager |
| [radarr.yml](services/media/radarr.yml) | Radarr movie manager |
| [prowlarr.yml](services/media/prowlarr.yml) | Prowlarr indexer manager for *arr apps |
| [overseerr.yml](services/media/overseerr.yml) | Overseerr media request management |
| [bazarr.yml](services/media/bazarr.yml) | Bazarr subtitle manager for Sonarr/Radarr |

### 🌐 Networking — [`services/networking/`](services/networking/)

| File | Description |
|---|---|
| [pihole.yml](services/networking/pihole.yml) | Pi-hole network-wide ad and DNS blocker |
| [adguard-home.yml](services/networking/adguard-home.yml) | AdGuard Home network-level ad blocker and DNS |
| [wg-easy.yml](services/networking/wg-easy.yml) | WG-Easy — WireGuard VPN with web UI |
| [unifi-controller.yml](services/networking/unifi-controller.yml) | Ubiquiti UniFi Network Application |

### 📋 Logging — [`services/logging/`](services/logging/)

| File | Description |
|---|---|
| [fluentd.yml](services/logging/fluentd.yml) | Fluentd unified log collector |
| [logstash.yml](services/logging/logstash.yml) | Logstash log processing pipeline (ELK stack) |
| [kibana.yml](services/logging/kibana.yml) | Kibana log visualization (ELK stack) |
| [vector.yml](services/logging/vector.yml) | Vector high-performance observability data pipeline |

### 🚀 CI/CD — [`services/ci-cd/`](services/ci-cd/)

| File | Description |
|---|---|
| [gitlab.yml](services/ci-cd/gitlab.yml) | GitLab Community Edition — self-hosted DevOps platform |
| [gitlab-runner.yml](services/ci-cd/gitlab-runner.yml) | GitLab Runner for CI/CD pipelines |
| [drone-server.yml](services/ci-cd/drone-server.yml) | Drone CI server |
| [drone-runner.yml](services/ci-cd/drone-runner.yml) | Drone CI Docker runner |
| [concourse-web.yml](services/ci-cd/concourse-web.yml) | Concourse CI web server |

---

## Contributing

Feel free to open a PR adding new service definitions. Place each service in the appropriate topic directory and follow the existing file format.
