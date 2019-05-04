![GitHub tag](https://img.shields.io/github/tag/STAMP-project/camp.svg)
[![Build Status](https://travis-ci.org/STAMP-project/camp.svg?branch=master)](https://travis-ci.org/STAMP-project/camp)
[![Test Coverage](https://img.shields.io/codacy/coverage/916007abcf574c8eadbde9ef5b720a5a.svg)](https://www.codacy.com/app/fchauvel/camp?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=STAMP-project/camp&amp;utm_campaign=Badge_Coverage)
[![Code Grade](https://img.shields.io/codacy/grade/916007abcf574c8eadbde9ef5b720a5a.svg)](https://www.codacy.com/app/SINTEF-9012/camp?utm_source=github.com&utm_medium=referral&utm_content=STAMP-project/camp&utm_campaign=Badge_Grade)


# CAMP &mdash; Amplify your Configuration Tests

CAMP (Configuration AMPlification) takes as input a sample testing
configuration and generates automatically a number of diverse
configurations. The generation is guided by predefined features and
constraints, and utilizes a set of reusable pieces. The current
version of CAMP is focused on the Docker environment, and the input
and output configurations are specified as Dockerfiles or
docker-compose files.

Check out the documentation on the [CAMP Companion website](https://stamp-project.github.io/camp)!

## Running CAMP on your project
To set CAMP on your project. There are two prerequisites:

*   Your project should be dockerised.

*   New configuration of the project can be achieved by:

    *   By substituting the FROM statement of a Dockerimage file
    *   By substituting an image of a docker-compose file
    *   Or by doing substitution in any file you `ADD` in your Dockerfile

Further, we need to identify variation points of your configuration,
e.g., java versions. We fill out feature.yml with this information. We
also need to define building rules which are used to build new docker
files. This information is filled in images.yml file. This allows
generating various docker files which are various possible
configuration of your application. If we need to generate various
docker-compose file, we need to fill in compose.yml. However, this is
optional.
