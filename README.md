<h1 align="center">Forza metrics proxy</h1>

## Getting Started

### With Docker

Using docker compose:

```yaml
version: "3"
services:
  forza-metrics-proxy:
    image: ghcr.io/jeufore/forza-metrics-proxy:latest
    container_name: forza-metrics-proxy
    ports:
      - 3000:1392
```

or docker run
```bash
docker run -d \
    --name forza-metrics-proxy \
    -p 3000:1392
    ghcr.io/jeufore/forza-metrics-proxy:latest
```

### For the development

```bash
# install dependencies project
npm i

# start project
npm start
```

## .env
| Parameter             | Example value                                 | Description                               |
|-----------------------|-----------------------------------------------|-------------------------------------------|
| INFLUXDB_URL          | "http://influx:3892"                          | InfluxDb url                              |
| INFLUXDB_TOKEN        | "dkezjfkenzfjeznfjn2874nlfzef"                | InfluxDb token                            |
| INFLUXDB_ORG          | "admin_org"                                   | InfluxDb org                              |
| INFLUXDB_BUCKET       | "speedtest_bucket"                            | InfluxDb bucket                           |
| FLUSH_BATCH_SIZE      | 1000                                          | Size flushing batch size                  |
| UDP_PORT              | 3000                                          | UDP server port                           |
<br/>