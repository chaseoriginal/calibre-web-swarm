# calibre-web-swarm

Web UI for Calibre library.

## Stack

- **Host**: ore-dock-110-1
- **Stack**: `calibre-web-swarm`
- **Image**: lscr.io/linuxserver/calibre-web:latest
- **Config**: named volume `calibre-web-swarm.config`
- **Library**: shares `calibre-swarm.config` named volume with calibre-swarm

## Ports

| Port | Published | Protocol |
|------|----------|----------|
| 8083 | 8083 | TCP |

## Deploy

```bash
ssh ore-dock-110-1
cd /data/compose/calibre-web-swarm
set -a && source .env && docker stack deploy -c docker-compose.yml --with-registry-auth calibre-web-swarm && set +a
```
