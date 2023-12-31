# SFED

String & File Encode / Decode plus Hashing & Generation of Random Strings

## Installation

```
$ poetry install

$ python setup.py install
```

## Development

This project includes a number of helpers in the `Makefile` to streamline common development tasks.

### Environment Setup

The following demonstrates setting up and working with a development environment:

```
$ poetry shell 

### run hashit cli application

$ sfed --help


### run pytest / coverage

$ make test
```


### Releasing to PyPi

Before releasing to PyPi, you must configure your login credentials:

**~/.pypirc**:

```
[pypi]
username = YOUR_USERNAME
password = YOUR_PASSWORD
```

Then use the included helper function via the `Makefile`:

```
$ make dist

$ make dist-upload
```

## Deployments

### Docker

Included is a basic `Dockerfile` for building and distributing `Hash It`,
and can be built with the included `make` helper:

```
$ make docker

$ docker run -it hashit --help
```
