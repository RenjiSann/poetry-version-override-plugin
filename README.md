# Poetry Version Override Plugin

[![CI](https://github.com/RenjiSann/poetry-version-override-plugin/actions/workflows/build.yml/badge.svg)](https://github.com/RenjiSann/poetry-version-override-plugin/actions/workflows/build.yml)

A [Poetry](https://python-poetry.org/) plugin that allows a project
builder to override the project version.  A project version can be
overriden for example during CI process. The version can be overriden
using the environment variable `PROJECT_OVERRIDE_VERSION` or
the `--override-version` switch of the build command.

## Install

Add the plugin to Poetry environment

```sh
$ poetry self add poetry-version-override-plugin
```

or install the plugin using `pip` to the place where `Poetry` is installed.

```sh
$ pip install poetry-version-override-plugin
```

## Usage

Overriding a project version by `PROJECT_OVERRIDE_VERSION` environment variable:

```console
$ PROJECT_OVERRIDE_VERSION=3.2.1 poetry build -f sdist
Overriden project version from 0.8.0 to 3.2.1
Building poetry-version-override-plugin (3.2.1)
  - Building sdist
  - Built poetry_version_override_plugin-3.2.1.tar.gz
```

Overriding a project version by the `--override-version` switch:

```console
$ poetry build -f sdist --override-version=1.2.3
Overriden project version from 0.8.0 to 1.2.3
Building poetry-version-override-plugin (1.2.3)
  - Building sdist
  - Built poetry_version_override_plugin-1.2.3.tar.gz
```
