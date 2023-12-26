# Zoomcamp

## Setup

In order to stick with the standard way of managing python projects, we opted for the usage of [poetry](https://python-poetry.org/).
See [FAQ](#faq) for common issues.

After having pull the project, open poetry shell by typing 

```bash
poetry shell
``` 

then you can install all the required dependencies for this project by running

```bash
poetry install
```

Poetry will install the packages listed in pyproject.toml file and their dependencies. 

### FAQ

There are many things that could cause issues with installing or running the virtual environement. A few of the most common ones and their solutions will be listed here. If none of these suggestions solve your problem, google the error and document your solution here so future collaborators don't need to.

- Problem : couldn't run docker inside virtual env 

```permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json": dial unix /var/run/docker.sock: connect: permission denied```

Solution : 

Run : 

```sudo usermod -aG docker ${USER}```

```sudo chmod 666 /var/run/docker.sock```
