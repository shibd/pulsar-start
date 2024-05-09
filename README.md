## Run docker directly
docker run -i -e PULSAR_PREFIX_acknowledgmentAtBatchIndexLevelEnabled=true -p 8080:8080 -p 6650:6650 -p 8443:8443 -p 6651:6651 apachepulsar/pulsar:latest /pulsar/bin/pulsar standalone

## Pulsar complete docker compose
https://github.com/apache/pulsar/tree/master/docker-compose/kitchen-sink