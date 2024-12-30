# freezing-shared
Shared classes for Freezing Saddles
==============================================

This has some shared classes that multiple other Freezing Saddles projects use, outside the data models in [freezingsaddles/freezing-model](https://github.com/freezingsaddles/freezing-model). See [Eliminate redundant code for register_athlete_team #66](https://github.com/freezingsaddles/freezing-web/issues/66) for the first issue to tackle here.

Usage
-----
This is intended for use with the other
[Freezing Saddles projects](https://github.com/freezingsaddles/) projects
including [freezing-web](https://github.com/freezingsaddles/freezing-web) and [freezing-sync](https://github.com/freezingsaddles/freezing-sync).


### Coding standards
The `freezing-sync` code is intended to be [PEP-8](https://www.python.org/dev/peps/pep-0008/) compliant. Code formatting is done with [black](https://black.readthedocs.io/en/stable/) and [isort](https://pycqa.github.io/isort/) and can be linted with [flake8](http://flake8.pycqa.org/en/latest/). See the [.flake8](.flake8) file and install the `dev` dependencies to get these tools (`pip install -e '.[dev]''`).

Developing
----------
This project uses [setuptools](https://setuptools.readthedocs.io/en/latest/) for packaging with a modern [pyproject.toml](https://setuptools.pypa.io/en/latest/userguide/pyproject_config.html) configuration. To get started, create a virtual environment and install the dependencies:

    python3 -m venv .venv
    source .venv/bin/activate
    pip install -e '.[lint]'  # install with linters for development

### Cloning all the Freezing Saddles repositories
If you are working with multiple Freezing Saddles repositories, you can clone them all with the following script:

```
# Clone all the freezingsaddles repositories
mkdir -p freezingsaddles
cd freezingsaddles
for part in beanstalkd compose infra model nq sync shared teams web; do
  [ -d freezing-$part ] || git clone https://github.com/freezingsaddles/freezing-$part.git
done
```

### Linting
This project uses [flake8](http://flake8.pycqa.org/en/latest/) for linting. To run the linter:

    flake8 freezing

This project uses black for code formatting. To format the code:

    black freezing

This project uses isort for sorting imports. To sort the imports:

    isort freezing


# Legal

This software is a community-driven effort, and as such the contributions are owned by the individual contributors:

Copyright 2019 Hans Lillelid <br>
Copyright 2020 Merlin Hughes <br>
Copyright 2020 Richard Bullington-McGuire <br>

This software is licensed under the [Apache 2.0 license](LICENSE).
