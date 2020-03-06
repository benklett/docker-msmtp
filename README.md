# Docker Image Packaging for msmtp

[![Travis](https://img.shields.io/travis/alvistack/docker-msmtp.svg)](https://travis-ci.org/alvistack/docker-msmtp)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-msmtp.svg)](https://github.com/alvistack/docker-msmtp/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-msmtp.svg)](https://github.com/alvistack/docker-msmtp/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/msmtp.svg)](https://hub.docker.com/r/alvistack/msmtp/)

msmtp is an SMTP client.

Learn more about msmtp: <https://marlam.de/msmtp/>

## Supported Tags and Respective `Dockerfile` Links

  - [`1.8`, `latest`](https://github.com/alvistack/docker-msmtp/blob/master/molecule/1.8/Dockerfile.j2)

## Overview

This Docker container makes it easy to get an instance of msmtp up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Minimized `Dockerfile` for meta data definition
  - Provision by Ansible and Molecule Docker driver in single layer
  - Handle `ENTRYPOINT` with [tini](https://github.com/krallin/tini)

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

### `alvistack/msmtmp:latest`

The `latest` tag matches the most recent [GitHub Release](https://github.com/alvistack/docker-msmtp/releases) of this repository. Thus using `alvistack/msmtp:latest` or `alvistack/msmtp` will ensure you are running the most up to date stable version of this image.

### `alvistack/msmtmp:<version>`

The version tags are rolling release rebuild by [Travis](https://travis-ci.org/alvistack/docker-msmtp) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
