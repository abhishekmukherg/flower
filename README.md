# Docker container for flower

This is just a simple docker container for [flower](https://flower.readthedocs.org/)

Tags available are currently:

    * `0.8.2`, `latest` 

## Usage

This docker container starts with flower exposed at port 5555. You must supply your own broker via command line arguments, for example, assume you're using rabbitmq in a linked container named `rabbitmq`:

```bash
docker run --rm --link rabbitmq -p 5555:5555 linkinpark342/flower --broker amqp://guest:guest@rabbitmq:5672//
```
