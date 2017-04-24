[![](https://images.microbadger.com/badges/image/sgtsquiggs/organizr.svg)](https://microbadger.com/images/sgtsquiggs/organizr)

# organizr

This image is derived from [sgtsquiggs/alpine.nginx](https://hub.docker.com/r/sgtsquiggs/alpine.nginx/).

[organizr](https://github.com/causefx/Organizr) - HTPC/Homelab Services Organizer, Written in PHP

## Usage
```
docker run \
    --name=organizr \
    -v <path to data>:/config \
    -e PGID=<gid> -e PUID=<uid> \
    -p 80:80 \
    sgtsquiggs/organizr
```

## Parameters
* `-p 80:80` external port 80 mapping to internal port 80
* `-v <path>:/config` where configuation files are stored.
* `-e PGID=<gid>` for Group ID (see below)
* `-e PUID=<uid>` for User ID (see below)

## User and Group ID
Set these to match the user/group ID of shared data volumes. Files written to these volumes will match the
provided uid/gid.

## Acknowledgements

* [linuxserver/organizr](https://github.com/linuxserver/docker-organizr)
