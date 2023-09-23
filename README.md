# Simple ELK Stack Configuration for Generating Logs with Docker

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Generating Logs](#generating-logs)
- [Viewing Logs](#viewing-logs)
- [Customization](#customization)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project aims to provide a simple configuration for setting up an ELK (Elasticsearch, Logstash, Kibana) stack using Docker. The ELK stack is a powerful combination of tools used for searching, analyzing, and visualizing log data in real-time.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Installation

1. Clone this repository to your local machine:

```
git clone https://github.com/yourusername/elk-stack-docker.git
cd elk-stack-docker
```

## Usage

To start the ELK stack, run:

```
docker-compose up -d
```

To stop the ELK stack, run:

```
docker-compose down
```

## Configuration

The default configuration is suitable for most use cases. However, if you need to customize the ELK stack, you can edit the respective configuration files located in the `config` directory.

- `config/logstash/logstash.conf`: Logstash configuration file.
- `config/elasticsearch/elasticsearch.yml`: Elasticsearch configuration file.
- `config/kibana/kibana.yml`: Kibana configuration file.

## Generating Logs

To generate sample logs, you can use the provided Docker container with a simple Python script. 

1. Build the logging container:

```
docker build -t log-generator ./log-generator
```

2. Start the container:

```
docker run --rm --name log-generator log-generator
```

This will generate random logs and send them to Logstash.

## Viewing Logs

Open your web browser and go to [http://localhost:5601](http://localhost:5601) to access the Kibana dashboard. You can start exploring and visualizing your logs.

## Customization

If you have specific log sources or formats, you may need to customize Logstash configuration (`config/logstash/logstash.conf`). Refer to the [Logstash documentation](https://www.elastic.co/guide/en/logstash/current/index.html) for more details.

## Troubleshooting

If you encounter any issues, please refer to the [troubleshooting section](https://github.com/yourusername/elk-stack-docker#troubleshooting) in the project's GitHub repository.

## Contributing

If you'd like to contribute to this project, please fork the repository, make your changes, and submit a pull request.

## License

This project is Not licensed  - Feel free to use .