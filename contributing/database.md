# Database

## Connect to database
```sh { name=database.connect } 
docker-compose exec db psql -Upostgres
```

## Create alembic migration file

```sh { name=database.migrate }
docker-compose run --rm server python src/manage.py db migrate
```

## Upgrade to latest migration

```sh { name=database.upgrade }
docker-compose run --rm server python src/manage.py db upgrade
```

## Downgrade latest migration

```sh { name=database.downgrade }
docker-compose run --rm server python src/manage.py db downgrade
```
