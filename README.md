# Docker-Shared-Services

### To run Flask:

```
docker-compose -f docker-compose.yaml -f docker-compose.flask.yaml up -d

```

#### The resullt should like this:

```
docker ps
CONTAINER ID   IMAGE                                  COMMAND                  CREATED          STATUS                    PORTS                                       NAMES
1bb1c06be09a   docker-shared-services_proxy_flask     "nginx -g 'daemon of…"   23 seconds ago   Up 3 seconds              0.0.0.0:80->80/tcp, :::80->80/tcp           docker-shared-services-proxy_flask-1
e5a9e30040a0   docker-shared-services_backend_flask   "/bin/sh -c 'flask r…"   23 seconds ago   Up 4 seconds              0.0.0.0:5000->5000/tcp, :::5000->5000/tcp   docker-shared-services-backend_flask-1
db8e6b521ad2   mariadb:10.6.4-focal                   "docker-entrypoint.s…"   24 seconds ago   Up 22 seconds (healthy)   3306/tcp, 33060/tcp                         docker-shared-services-db-1
```

### To run ASP.NET

```
docker-compose -f docker-compose.yaml -f docker-compose.asp.yaml up -d
```