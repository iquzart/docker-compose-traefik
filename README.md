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
Docker and Docker Compose is required to run the proxy. You may use the [Ansible_Role](https://github.com/iquzart/ansible-role-docker) to setup the infrastructure.


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

cd /opt/containers/traefik 

git clone https://github.com/iquzart/docker-compose-traefik.git .

chmod 600 config/acme/acme.json

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

5. Start sample app (Optional)
```
docker-compose -f sample-app/goapp-compose.yml up -d
```


License
-------

MIT

Author Information
------------------

Muhammed Iqbal <iquzart@hotmail.com>