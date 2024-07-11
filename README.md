# Futur-Tech Monitoring Zabbix for Ollama

A Zabbix template to monitor an Ollama instance. It checks the Ollama port response and uses the API to verify model count and status.

## Template Items

- **Ollama: API port**: Ensures the Ollama API port is responsive.
- **Ollama: models available raw**: Retrieves raw data of available models from the API.
- **Ollama: models available count**: Counts the number of available models.
- **Ollama: models running raw**: Retrieves raw data of running models from the API.
- **Ollama: models running count**: Counts the number of running models.

## Discovery Rules

- **Ollama: models available discovery**: Discovers available models.

## Item Prototypes

- **Ollama: model {#MODEL.FAMILY}/{#MODEL.NAME} is running**: Detects if a specific model is running.
- **Ollama: model {#MODEL.FAMILY}/{#MODEL.NAME}**: Fetches data for a specific model.

## Triggers

- **Ollama API port is down**: Alerts if the Ollama API port is not responding.
