# Portainer

## Description

Portainer est un outil de gestion de conteneurs Docker qui offre une interface utilisateur graphique conviviale pour gérer et surveiller vos conteneurs Docker. Il est facile à utiliser et permet de gérer de manière efficace vos conteneurs, images et réseaux Docker.

Avec Portainer, vous pouvez déployer, arrêter et supprimer des conteneurs, gérer les images Docker et les réseaux, ainsi que visualiser les journaux de conteneurs et surveiller l'état de vos conteneurs en temps réel.

## Installation

```bash
docker volume create portainer_data
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```

## Plus d'informations

- [Portainer](https://www.portainer.io/)