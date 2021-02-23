This repository contains a [remoteRotator](github.com/dh1tw/remoteRotator) example playground which
is online available at [demo.rotator.shackbus.org](demo.rotator.shackbus.org).

The playground uses [docker-compose](https://docs.docker.com/compose/) to orchestrate 5 remoteRotator instances
+ a [nats-server](https://nats.io).

![screenshot rotator demo1](/images/rotator-demo1.png)

## Description

### Instances

#### remoteRotator rotator instances:
All instances use the "dummy" rotator implementation.

- 2m 2x10el (Azimuth + Elevation)
- UHF Group (Azimuth + Elevation limited to 30°-170°)
- Tribander (Azimuth)
- WARC Yagi (Azimuth - Stop @170°)
- 40m 3L (Azimuth - limited to 45°-270°)

#### Other
- remoteRotator web (aggregator)
- nats-server