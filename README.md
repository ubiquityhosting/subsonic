# docker-subsonic

## Description
A Dockerfile for [Subsonic](http://www.subsonic.org/) version 5.3.

## Ports

### 443
WebUI port.

## Data
Uses the default /var/subsonic folder for data.

## User
Add the environmental variable SUBSONIC_USER to change the user the subsonic process runs as.
SUBSONIC_USER_UID specifies the UID of the user, and is optional.

## Example
docker run -d -e SUBSONIC_USER=subsonic -v '/var/subsonic:/var/subsonic' -v '/var/music:/mnt/music' -p 443:443 --name subsonic ubiquityhosting/subsonic
