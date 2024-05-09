## How to run

Env:
- Ubuntu 20.04

1. Start a pulsar cluster with proxy
```shell
sudo su
mkdir -p ./data/zookeeper ./data/bookkeeper
chown -R 10000 data
docker compose up -d
```

2. Download pulsar-client
```text
wget https://archive.apache.org/dist/pulsar/pulsar-2.10.5/apache-pulsar-2.10.5-bin.tar.gz
tar -xvf apache-pulsar-2.10.5-bin.tar.gz
```

3. Send a message to a topic that doesn't exist
```shell
./apache-pulsar-2.10.5/bin/pulsar-client produce persistent://public/default/test-topic --messages "hello"
```

4. Show metadata
```shell
./apache-pulsar-2.10.5/bin/pulsar-admin topics get-partitioned-topic-metadata persistent://public/default/test-topic

OutPut:
{
  "partitions" : 1
}
```
