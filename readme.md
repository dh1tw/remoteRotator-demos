# remoteRotator Playground

This repository contains the sources to the [remoteRotator](github.com/dh1tw/remoteRotator) playground at [demo.rotator.shackbus.org](demo.rotator.shackbus.org).

The playground uses [docker-compose](https://docs.docker.com/compose/) to orchestrate 6 remoteRotator instances.

![screenshot rotator demo1](/images/rotator-demo1.png)

## Description

### Instances

#### remoteRotator rotator instances:
All instances use the *dummy* rotator implementation.

- [2m 2x10el](/rotator-demo1/config/vhf.toml) (Azimuth + Elevation)
- [UHF Group](/rotator-demo1/config/uhf.toml) (Azimuth + Elevation limited to 30°-170°)
- [Tribander](/rotator-demo1/config/tribander.toml) (Azimuth)
- [WARC Yagi](/rotator-demo1/config/warc.toml) (Azimuth - Stop @170°)
- [40m 3L](/rotator-demo1/config/40m.toml) (Azimuth - limited to 45°-270°)

#### Other
- remoteRotator web (aggregator)
- nats-server (communication backend)

## How to execute

It's pretty easy to run you own demo instance locally if you have
[docker](https://www.docker.com/products/docker-desktop) installed on your machine.

Depending on your OS and CPU's architecture you might have to adjust in the [docker-compose.yml](/rotator-demo1/docker-compose.yml) the arguments
- arch
- os
- [release](github.com/dh1tw/remoteRotator/releases)

Then just run
``` bash
$ docker-compose up --build
```
