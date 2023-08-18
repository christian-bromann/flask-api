# API Server

## Install server with its dependencies

```sh { name=server.install }
docker-compose run --rm server pip install -r requirements-dev.txt --user --upgrade --no-warn-script-location
```

## Start server in its docker container

```sh { name=server.start }
docker-compose up server
```

## Connect to server to lauch commands

```sh { name=server.bash }
docker-compose exec server bash
```

## Start daemon server in its docker container

```sh { name=server.daemon }
docker-compose up -d server
```

## Start server in its docker container

```sh { name=server.stop }
docker-compose stop
```

## Display server logs

```sh { name=server.logs }
tail -f server.log
```

## Upgrade pip dependencies

```sh { name=server.upgrade }
docker-compose run --rm server bash -c "python vendor/bin/pip-upgrade requirements.txt requirements-dev.txt --skip-virtualenv-check"
```