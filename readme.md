This repository contains a [remoteRotator](github.com/dh1tw/remoteRotator) example playground which
is online available at [demo.rotator.shackbus.org](demo.rotator.shackbus.org).

The playground uses [docker-compose](https://docs.docker.com/compose/) to orchestrate 6 remoteRotator instances
and a [nats-server](https://nats.io) which serves as the communication backend.

![screenshot rotator demo1](/images/rotator-demo1.png)

## Description

### Instances

#### remoteRotator rotator instances:
All instances use the *dummy* rotator implementation.

- [2m 2x10el](/rotator-demo1/config/vhf.toml) (Azimuth + Elevation)
- [UHF Group]((/rotator-demo1/config/uhf.toml)) (Azimuth + Elevation limited to 30°-170°)
- [Tribander]((/rotator-demo1/config/tribander.toml)) (Azimuth)
- [WARC Yagi]((/rotator-demo1/config/warc.toml)) (Azimuth - Stop @170°)
- [40m 3L]((/rotator-demo1/config/40m.toml)) (Azimuth - limited to 45°-270°)

#### Other
- remoteRotator web (aggregator)
- nats-server

## How to execute

It's pretty easy to run you own demo instance locally if you have
[docker]() installed on your machine.

Depending on your OS and CPU's architecture you might have to adjust in the [docker-compose.yml](/rotator-demo1/docker-compose.yml) the arguments
- arch
- os
- [release](github.com/dh1tw/remoteRotator/releases)

Then just run
``` bash
$ docker-compose up --build
```
