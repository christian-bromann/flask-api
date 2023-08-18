# Test

## Launch tests in their own docker container

```sh { name=test.server }
docker-compose run --rm testserver
```

## Generate test coverage

```sh { name=test.coverage }
docker-compose run --rm testserver bash -c "python -m pytest --cov-report term --cov-report html:coverage --cov-config setup.cfg --cov=src/ test/"
```

## Lint python files with flake8

```sh { name=test.lint }
docker-compose run --rm server bash -c "python -m flake8 ./src ./test"
```

## Check for dependencies security breach with safety

```sh { name=test.safety }
docker-compose run --rm server bash -c "python vendor/bin/safety check"
```
