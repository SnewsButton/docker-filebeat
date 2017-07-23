# Docker-Filebeat

Structural inspiration derived from [deviantony/docker-elk](https://github.com/deviantony/docker-elk).

`version`: 5.5.0

Image used is the offical Elastic Filebeat image.

** Important: ** The Docker-Filebeat only looks within its own container, in order to ship foreign logs, they must be mounted into the container. This is done through `docker-compose.yml`.
## Requirements

1. Install Docker version 1.10.0+
2. Install Docker Compose version 1.6.0+
3. Clone this repository

## Initial Setup

To start filebeat, run the following command:

```$ docker-compose up```

## Configuration

**Note:** Configuration is not loaded dynamically, the Filebeat container must be restarted to see changes.

The configuraion file for filebeat is located in `./filebeat/congfig/filebeat.yml`.

As this repo works well with devianthony's docker-elk repo, the default port for logstash is 5000. 

For a list of possible configuration options, visit [here](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-configuration-details.html).
