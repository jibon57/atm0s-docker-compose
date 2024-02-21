# Atm0s Docker Compose

## Usage
Clone this project
```bash
git clone https://github.com/luongngocminh/atm0s-docker-compose.git 
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

You can also provide a seed by modifying the `env/shared.env` file before running `docker compose`:
```env
SEEDS=0@/ip4/127.0.0.1/udp/4000/ip4/127.0.0.1/tcp/4000
```