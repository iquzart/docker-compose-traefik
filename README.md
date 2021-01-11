Traefik Proxy
-------------

Traefik proxy docker compose


Features
--------
```
    1. Basic Authentication
    2. HTTPS Redirection
    3. IP Whitelist
    4. Letsencrypt
    5. TLS 1.2 and 1.3
    6. Access logs to file
```

Requirements
------------
Docker and Docker Compose is required to run the proxy. You may user my ansible role to setup the infrastructure.


Deploy Traefik
--------------

1. Create docker network proxy
```
$ docker network create proxy
```

2. Create directories for containers and Clone the repository
```
{

mkdir -p /opt/containers/traefik

git clone github.com/iquzart/docker-compose-traefik .

}
```

3. Update below files 
```
.env
docker-compose.yml
config/traefik.yml
config/dynamic/middleware.yml
```

4. Start Traefik
```
docker-compose up -d
```


License
-------

MIT

Author Information
------------------

Muhammed Iqbal <iquzart@hotmail.com>