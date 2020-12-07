## Karma Bot for Discord

## Install

This project uses [pipenv](https://pipenv.readthedocs.io/en/latest/) and requires Python 3.6. Karma Bot is installed in the following way:

```bash
pip install pipenv  # if you don't have it already
pipenv install
```

## Use

```bash
pipenv run python -m karma.bot -t <discord-bot-token>
```

## Test

```bash
pipenv run pytest
```

## Build the docker container

1. You can build the docker container and push to a registry if you'd like
1. Run the following:
```bash
docker build -t <registry>/discord-karma:1.0.0
docker push <registry>/discord-karma:1.0.0
```

## Run on Kubernetes

1. Open the [deployment.yaml](./deployment.yaml) and add your TOKEN at the specific line, if you built the container like above, change the location.
1. Run the following to run it on Kubernetes
```bash
kubectl apply -f deployment.yaml
```