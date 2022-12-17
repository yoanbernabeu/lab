# Gestion des Utilisateurs, Groupes et Droits

## Gestion des utilisateurs

### Créer un utilisateur

```bash
adduser nom_utilisateur
```

### Supprimer un utilisateur

```bash
userdel -r nom_utilisateur
```

### Modifier le mot de passe d'un utilisateur

```bash
passwd nom_utilisateur
```

### Modifier le nom d'un utilisateur

```bash
usermod -l nouveau_nom_utilisateur ancien_nom_utilisateur
```

### Modifier le groupe d'un utilisateur

```bash
usermod -g nouveau_nom_groupe nom_utilisateur
```

## Gestion des groupes

### Créer un groupe

```bash
groupadd nom_groupe
```

### Supprimer un groupe

```bash
groupdel nom_groupe
```

### Modifier le nom d'un groupe

```bash
groupmod -n nouveau_nom_groupe ancien_nom_groupe
```

## Gestion des droits

### Les principes de base

Avec les lettres suivantes:

* `r` : lecture
* `w` : écriture
* `x` : exécution

Avec les chiffres suivants:

* `4` : lecture
* `2` : écriture
* `1` : exécution
* `0` : aucun droit
* `7` : lecture + écriture + exécution

Lorsqu'on combine les lettres et les chiffres, on obtient les combinaisons suivantes:

* `rwx` : 4 + 2 + 1 = 7
* `rw-` : 4 + 2 + 0 = 6
* `r-x` : 4 + 0 + 1 = 5
* `r--` : 4 + 0 + 0 = 4
* `-wx` : 0 + 2 + 1 = 3
* `-w-` : 0 + 2 + 0 = 2
* `--x` : 0 + 0 + 1 = 1
* `---` : 0 + 0 + 0 = 0

Lorsqu'on l'on parle de droits, on entend souvent parler de `chmod 777`. Cela signifie que l'on donne tous les droits à l'utilisateur, au groupe et aux autres utilisateurs, voici quelques exemples:

* `chmod 777` : tous les droits
* `chmod 755` : lecture pour tous, écriture et exécution pour l'utilisateur
* `chmod 700` : lecture, écriture et exécution pour l'utilisateur
* `chmod 666` : lecture et écriture pour tous
* `chmod 644` : lecture pour tous, écriture pour l'utilisateur


### Voir les droits d'un fichier

```bash
ls -l nom_fichier
```

### Changer les droits d'un fichier

```bash
chmod 777 nom_fichier
```

### Changer le propriétaire d'un fichier

```bash
chown nom_utilisateur nom_fichier
```

### Changer le groupe d'un fichier

```bash
chgrp nom_groupe nom_fichier
```

### Changer le propriétaire et le groupe d'un fichier

```bash
chown nom_utilisateur:nom_groupe nom_fichier
```