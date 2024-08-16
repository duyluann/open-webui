# Open WebUI Setup
[Open WebUI](https://docs.openwebui.com/) is an extensible, feature-rich, and user-friendly self-hosted WebUI designed to operate entirely offline. It supports various LLM runners, including Ollama and OpenAI-compatible APIs.

This repository provides a simple setup for running the Open WebUI using Docker Compose.

## Prerequisites

Before you start, ensure that you have the following installed on your machine:

- Docker
- Docker Compose

## Getting Started

1. Clone the Repository
```bash
git clone https://github.com/duyl97/open-webui.git
cd open-webui
```

2. Copy Environment File
Before starting the services, you need to create a .env file by copying the provided .env.example file:

```bash
cp .env.example .env
```

Make sure to update the .env file with any necessary environment-specific configurations.

3. Run Docker Compose
To start the Open WebUI, run:

```bash
docker-compose up -d
```

This command will build and start all the services defined in the docker-compose.yml file.

4. Access the WebUI
Once the services are up and running, open your browser and navigate to:

```bash
http://localhost:3000
```

## Configuration

If you need to customize the setup (e.g., environment variables, port numbers), modify the .env file or the `docker-compose.yml` file.

## Create a Pipe function to connect with Azure OpenAI models

Use the shared function [Azure OpenAI](https://openwebui.com/f/nomppy/azure).

## Stopping the Services

To stop the running services, use:

```bash
docker-compose down -v
```

This will stop and remove the containers.

## Troubleshooting

If you encounter any issues, ensure that Docker and Docker Compose are installed correctly and running. For further issues, please check the logs:

```bash
docker-compose logs
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
