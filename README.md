# Zeppelin + Grafana Docker

This repository contains the necessary material to spin up a dockerized
[Spark](https://spark.apache.org) cluster, on top of which lies a
dockerized [Zeppelin](https://zeppelin.apache.org) instance,
providing a convenient notebook interface.
The `docker-compose.yml` file also spins up a
[Grafana](https://grafana.com) instance,
as well as a [Graphite](https://graphiteapp.org) instance
relying on a
[Carbon](https://github.com/graphite-project/carbon) backend.

## How to

To **start the service**, use `[sudo] docker-compose up -d`

(the option `-d` spins the containers in *detached* mode, giving the prompt
back once the containers have been instantiated).

To **stop the service**, use `[sudo] docker-compose down`.

By default, the spark cluster involves the Spark Master and a single Spark Worker.
To scale up the number of workers, use the option `--scale`.
For example, to have 2 workers, use `sudo docker-compose up -d --scale spark-worker=2`.
