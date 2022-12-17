# HedgeDoc

## Description

HedgeDoc est un éditeur de notes en temps réel open source qui vous permet de collaborer avec vos amis et vos collègues. Il est conçu pour être facile à utiliser et à configurer, et peut être déployé localement ou dans le cloud.

## Installation

* Création d'un fichier `docker-compose.yml`:

```yaml
version: '3'
services:
  database:
    image: postgres:13.4-alpine
    environment:
      - POSTGRES_USER=hedgedoc
      - POSTGRES_PASSWORD=password
      - POSTGRES_DB=hedgedoc
    volumes:
      - database:/var/lib/postgresql/data
    restart: always
  app:
    # Make sure to use the latest release from https://hedgedoc.org/latest-release
    image: quay.io/hedgedoc/hedgedoc:1.9.6
    environment:
      - CMD_DB_URL=postgres://hedgedoc:password@database:5432/hedgedoc
      - CMD_DOMAIN=localhost
      - CMD_URL_ADDPORT=true
    volumes:
      - uploads:/hedgedoc/public/uploads
    ports:
      - "3000:3000"
    restart: always
    depends_on:
      - database
volumes:
  database:
  uploads:
```

* Lancement du conteneur:

```bash
docker-compose up -d
```

## En savoir plus

* [Documentation officielle](https://docs.hedgedoc.org/)

* [Installation avec Docker](https://docs.hedgedoc.org/setup/docker/)