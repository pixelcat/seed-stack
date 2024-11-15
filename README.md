#    

## Installation instructions

### Copy your ssl certificate to ./container/traefik as:

- traefik.crt
- traefik.key

### Copy env file

```bash
cp .env.example .env
```

Then edit .env and change variables to match your setup

### Configure DNS

Create DNS entries for your setup. For example, let's assume you're using the domain `example.com`. Create the
following DNS entries.

| Hostname              | Record Type | Value                           |
|-----------------------|-------------|---------------------------------|
| seed-stack            | A           | << your seed-stack IP address>> |
| sonarr-internal       | CNAME       | seed-stack                      |
| bazarr-internal       | CNAME       | seed-stack                      |
| deluge-internal       | CNAME       | seed-stack                      |
| flaresolverr-internal | CNAME       | seed-stack                      |
| heimdall-internal     | CNAME       | seed-stack                      |
| hydra2-internal       | CNAME       | seed-stack                      |
| jackett-internal      | CNAME       | seed-stack                      |
| nzbget-internal       | CNAME       | seed-stack                      |
| ombi-internal         | CNAME       | seed-stack                      |
| radarr-internal       | CNAME       | seed-stack                      |
| sonarr-internal       | CNAME       | seed-stack                      |
| tautulli-internal     | CNAME       | seed-stack                      |

## Start the application

```bash
docker-compose up -d
```