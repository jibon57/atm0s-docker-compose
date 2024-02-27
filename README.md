# Atm0s Docker Compose

## Usage
Clone this project
```bash
git clone https://github.com/8xFF/atm0s-docker-compose.git 
cd atm0s-docker-compose
```

Start a cluster:
```bash
docker compose --profile cluster up -d
```

By default the cluster profile won't include the connector server, to start a cluster with connector:
```bash
docker compose --profile cluster --profile connector up -d
```

Start a single server:
```bash
docker compose --profile <server> up -d
```

You can also provide a seed for the cluster by modifying the `env/gateway.env` file before running `docker compose`:
```
SEEDS=0@/ip4/127.0.0.1/udp/4000/ip4/127.0.0.1/tcp/4000
```
Each service will have an env file by their name, and a `shared.env` to globally override any local config.
By default, every service nodes will be seeding to the gateway node at localhost port 4000, if you want to customize these configs try updating the env files accordingly.
