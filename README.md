Aptly for Docker
================

This repo container Docker configurations to deploy and use Aptly. Most
use cases will require you to extend these containers with your own
configuration file overlay.

However, these are also usable as-is, if you just want an environment
in which to play with aptly, for example:

    docker run -t -i mikepurvis/aptly:latest /bin/bash

You are now at a prompt with `aptly`. If you'd like to persist any changes
made past the lifetime of the container, mount the aptly data directory
externally:

    mkdir /tmp/aptly
    docker run -t -i -v /tmp/aptly:/aptly aptly:latest aptly repo create foo
    docker run -t -i -v /tmp/aptly:/aptly aptly:latest aptly repo list
