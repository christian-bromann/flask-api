# Format

## Run black on every file

```sh { name=format.black }
docker-compose run --rm server bash -c "python vendor/bin/black src/ test/ --exclude vendor/"
```

## Sort imports

```sh { name=format.isort }
docker-compose run --rm server bash -c "python vendor/bin/isort -rc src/ test/ --skip vendor/ --skip src/models/__init__.py"
```