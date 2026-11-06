# Docker Exercises

[`python-app/`](python-app/) is a small Flask example that displays a greeting, the container's hostname, and a visit counter. The counter uses a Redis host named `redis`; if Redis cannot be reached, the page displays a message that the counter is disabled.

## Read the example

| File | What it describes |
| --- | --- |
| [`python-app/app.py`](python-app/app.py) | The HTTP handler and Redis-error fallback |
| [`python-app/Dockerfile`](python-app/Dockerfile) | An image built from `python:2.7-slim`, with the application listening on container port `80` |
| [`python-app/docker-compose.yml`](python-app/docker-compose.yml) | A `web` service using `hydra11/python-app:0.1`, port mapping `4000:80`, and a deployment section requesting five replicas |

The Compose file refers to an existing image; it does not build the adjacent Dockerfile or define a Redis service. These files preserve a historical example and have not been validated here as a complete setup for a current Docker environment.
