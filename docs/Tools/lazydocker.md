# Lazydocker

## Description

Lazydocker est un outil en ligne de commande qui fournit une interface utilisateur pour les outils de conteneurisation et de gestion de conteneurs Docker.

## Installation

Pour Ubuntu 22.04:

```bash
LAZYDOCKER_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazydocker/releases/latest" | grep -Po '"tag_name": "v\K[0-9.]+')

curl -Lo lazydocker.tar.gz "https://github.com/jesseduffield/lazydocker/releases/latest/download/lazydocker_${LAZYDOCKER_VERSION}_Linux_x86_64.tar.gz"

mkdir lazydocker-temp
tar xf lazydocker.tar.gz -C lazydocker-temp

sudo mv lazydocker-temp/lazydocker /usr/local/bin

rm -rf lazydocker.tar.gz
rm -rf lazydocker-temp
```

## Utilisation

Pour lancer l'interface utilisateur, exécutez simplement la commande `lazydocker` dans un terminal.

## Sources

- [Lazydocker](https://github.com/jesseduffield/lazydocker)