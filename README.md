# Kafka Kraft Playground

## Requirement

* Docker Compose

## Getting Started

```bash
docker compose up -d
```


Create Topics

```bash
docker compose --profile debug run --rm kafka-debug \
    kafka-topics.sh --create \
    --bootstrap-server=kafka1:17005 \
    --replication-factor 3 \
    --partitions 3 \
    --topic test-data
```

Topics List

```bash
docker compose --profile debug run --rm kafka-debug \
    kafka-topics.sh --list \
    --bootstrap-server=kafka1:17005
```
