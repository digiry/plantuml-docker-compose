# plantuml-docker-compose

This docker compose uses the public plantuml/plantuml-server docker image.

The local plantuml server can render a plantuml markdown in PlantUML VSCode extension(`jebbs.plantuml`)

The following link tells how to configure the PlantUML extension on local.

[Configure plantuml extension in VSCode](./configure_plantuml_extension_vscode.md)

<br>

## Prerequisites

First, make a `docker-compose.override.yml` using `docker-compose.override.yml.sample`.

You can change the port of the server.  
The default port is `8080`.

```yaml
services:
  plantuml-server:
    # You can change the Port number.
    ports:
      - 8080:8080
```

You can see the overrode Compose file with the following command.

```bash
docker compose config
```

<br>

## Run

```bash
docker compose up -d
```

