# Atm0s Docker Compose

## Usage
Clone this project
```bash
git clone https://github.com/8xFF/atm0s-docker-compose.git 
cd atm0s-docker-compose
```

Start the cluster:
```bash
docker compose up -d
```

After that you'll be able to access console from:
```
http://localhost:8080
```
Gateway URL:
```
http://localhost:3001
```

You can also provide a seed for the cluster by modifying the `env/gateway.env` file before running `docker compose`:
```
SEEDS=0@/ip4/127.0.0.1/udp/10000
```
Each service will have an env file by their name, and a `shared.env` to globally override any local config.
By default, every service nodes will be seeding to the gateway node at localhost port 10000, if you want to customize these configs try updating the env files accordingly.
