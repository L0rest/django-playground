# Django Playground

> This app is not meant to be used in production, it's just a playground to test Django feature or create POC.


[![Built with Cookiecutter Django](https://img.shields.io/badge/built%20with-Cookiecutter%20Django-ff69b4.svg?logo=cookiecutter)](https://github.com/cookiecutter/cookiecutter-django/)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![python](https://img.shields.io/badge/Python-3.12.5-3776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org)
[![Django](https://img.shields.io/badge/5.0.9-green?logo=django&label=Django&labelColor=grey&color=%23092E20)](https://www.python.org)


License: MIT

## Introduction

### Features

* User Authentication with [allauth](https://github.com/pennersr/django-allauth)
* Bootstrap 5
* Docker
* Sphinx
* Sample App:  **Stock**
* Asynchronous tasks with Celery and RabbitMQ

### Technologies and tools used in this project

### Dependencies
* [Poetry](https://python-poetry.org/) as package manager.
* [Pyenv](https://github.com/pyenv/pyenv) to manage python versions.
* [Pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv) to manage virtual environments.

### Asynchronous tasks
* [Celery](https://docs.celeryproject.org/en/stable/) to run asynchronous tasks.
* [Rabbitmq](https://www.rabbitmq.com/) as message broker.

### Monitoring
* [Flower](https://flower.readthedocs.io/en/latest/) to monitor celery tasks.
* [Prometheus](https://prometheus.io/) to monitor the application. `To be implemented`
* [Grafana](https://grafana.com/) to visualize prometheus metrics. `To be implemented`

### Build and run
* [docker](https://www.docker.com/) to run the project in a container.
* [docker-compose](https://docs.docker.com/compose/) to manage multiple containers.

### Code quality
* [pre-commit](https://pre-commit.com/) to run linters and formatters before commiting.

### Documentation
* [sphinx](https://www.sphinx-doc.org/en/master/) to generate documentation.

## Installation

### 1. Install OS dependencies


#### Ubuntu
```bash
sudo apt-get install -y build-essential curl graphviz graphviz-dev libpq-dev
```

#### MacOS

// TODO

### 2. Create a virtual environment

> It's recommended to use a **virtual environment** to avoid conflicts with other projects.

```bash
pyenv install 3.12.5
pyenv virtualenv 3.12.5 django-playground
pyenv local django-playground-3.12.5
poetry install
```

### 3. Install dependencies

### 4. Setting Up Your Users

A **default superuser** is created with the following credentials

Email : `admin@admin.local`

Password : `admin`

- To create a **normal user account**, just go to Sign Up and fill out the form. Once you submit it, you'll see a "Verify Your E-mail Address" page. Go to your **console** to see a simulated email verification message. Copy the link into your browser. Now the user's email should be verified and ready to go.

- To create a **superuser account**, use this command:

      $ docker compose -f compose.local.yaml run --rm django python manage.py createsuperuser

For convenience, you can keep your normal user logged in on Chrome and your superuser logged in on Firefox (or similar), so that you can see how the site behaves for both kinds of users.


### 5. Start the development server

// TODO

## Development

### Settings

Moved to [settings](http://cookiecutter-django.readthedocs.io/en/latest/settings.html).

See detailed [cookiecutter-django Docker documentation](http://cookiecutter-django.readthedocs.io/en/latest/deployment-with-docker.html).

### Type checks

Running type checks with mypy:

    $ mypy django_playground

### Test coverage

To run the tests, check your test coverage, and generate an HTML coverage report:

    $ coverage run -m pytest
    $ coverage html
    $ open htmlcov/index.html

#### Running tests with pytest

    $ pytest

### Live reloading and Sass CSS compilation

Moved to [Live reloading and SASS compilation](https://cookiecutter-django.readthedocs.io/en/latest/developing-locally.html#sass-compilation-live-reloading).
