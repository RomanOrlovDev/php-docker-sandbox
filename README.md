# A boilerplate to run Docker containers for PHP development

It includes Nginx, Xdebug, Composer, Git and PHP by itself.

PHP container runs as rootless. You can check it in docker-compose.yml, find the line:

`user: ${MY_UID}:${MY_GID}`

Hence, in order for container valid build you need to export those variable in terminal where `docker compose up` runs:

```
export MY_UID="$(id -u)" MY_GID="$(id -g)"
```

Afterwards all is ready to run docker compose:
```
docker compose up
```

Check if it works:
```
curl localhost:8811
```