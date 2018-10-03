The course is designed for ElasticSearch v1.6 and the current ES version is 6.4.2.
Instead of installing ElasticSearch 1.6 and Kibana 4.2 locally we will be running a cluster of 2 nodes of ES and a node of Kibana with Docker Compose.

Head and Marvel plugins are not installed. If you wish to use Head - you can install it as a [Chrome extension](https://chrome.google.com/webstore/detail/elasticsearch-head/ffmkiejjmecolpfloofpjologoblkegm).
Marvel is not required for the purpose of the course and Kibana has built-in monitoring dashboard.
Sense plugin for Kibana is not required as Kibana ships with built-in development console.

Prerequisites: 
- [Docker](https://docs.docker.com/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

To start clone this repository and then run 

```shell
docker-compose up -d && docker-compose logs -f
```

This will start 2 nodes of ElasticSearch and 1 node running Kibana.
Kibana will be available on `localhost:5601` and ElasticSearch on `localhost:9200`

Optionally check the health of ES cluster with 
```shell
curl http://127.0.0.1:9200/_cat/health
```

Open [Kibana Console](http://localhost:5601/app/kibana#/dev_tools/console?_g=()) to execute course exercises. 

Sample documents file is attached for convenience: [1-5.txt](1-5.txt).