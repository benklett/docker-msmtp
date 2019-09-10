# Docker Image Packaging for msmtp

[![Travis](https://img.shields.io/travis/alvistack/docker-msmtp.svg)](https://travis-ci.org/alvistack/docker-msmtp)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-msmtp.svg)](https://github.com/alvistack/docker-msmtp/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-msmtp.svg)](https://github.com/alvistack/docker-msmtp/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/msmtp.svg)](https://hub.docker.com/r/alvistack/msmtp/)

msmtp is an SMTP client.

Learn more about msmtp: <https://marlam.de/msmtp/>

## Supported Tags and Respective `Dockerfile` Links

  - [`latest` (master/Dockerfile)](https://github.com/alvistack/docker-msmtp/blob/master/Dockerfile)
  - [`1.8` (1.8/Dockerfile)](https://github.com/alvistack/docker-msmtp/blob/1.8/Dockerfile)

## Overview

This Docker container makes it easy to get an instance of msmtp up and running.

### Quick Start

Start msmtp:

    # Pull latest image
    docker pull alvistack/msmtp

    # Run as detach
    docker run \
        -itd \
        --name msmtp \
        --publish 25:25 \
        alvistack/msmtp

    # Run with custom /usr/local/etc/msmtprc
    docker run \
        -itd \
        --name msmtp \
        --publish 25:25 \
        --volume /usr/local/etc/msmtprc:/usr/local/etc/msmtprc \
        alvistack/msmtp

**Success**. msmtp is now available on port `25`.

## Versioning

The `latest` tag matches the most recent version of this repository. Thus using `alvistack/msmtp:latest` or `alvistack/msmtp` will ensure you are running the most up to date version of this image.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
