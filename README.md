``` bash
# Run container
docker-compose up --build -d
```

``` yaml
# To add in project containers
labels:
    - traefik.enable=true
    - traefik.http.routers.mail-yes-trade.rule=Host(`mail.yes-trade.wip`)
    - traefik.http.services.mail-yes-trade.loadbalancer.server.port=1080
```