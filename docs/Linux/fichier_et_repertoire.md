# Gestion des fichiers et repertoires

## Gestion des fichiers

### Créer un fichier

```bash
touch nom_du_fichier
```

### Supprimer un fichier

```bash
rm nom_du_fichier
```

### Copier un fichier

```bash
cp nom_du_fichier nom_du_fichier_copie
```

### Déplacer un fichier

```bash
mv nom_du_fichier nom_du_fichier_deplace
```

### Renommer un fichier

```bash
mv nom_du_fichier nom_du_fichier_renomme
```

### Afficher le contenu d'un fichier

```bash
cat nom_du_fichier
```

### Afficher le contenu d'un fichier en temps réel

```bash
tail -f nom_du_fichier
```

## Chercher un fichier

### Rechercher un fichier par son nom

```bash
find / -name "nom_du_fichier"
```

### Rechercher un fichier par son contenu

```bash
grep -rnw '/path/to/somewhere/' -e "pattern"
```

## Gestion des repertoires

### Créer un repertoire

```bash
mkdir nom_du_repertoire
```

### Supprimer un repertoire

```bash
rmdir nom_du_repertoire
```

### Copier un repertoire

```bash
cp -r nom_du_repertoire nom_du_repertoire_copie
```

### Déplacer un repertoire

```bash
mv nom_du_repertoire nom_du_repertoire_deplace
```

### Renommer un repertoire

```bash
mv nom_du_repertoire nom_du_repertoire_renomme
```

### Afficher le contenu d'un repertoire

```bash
ls nom_du_repertoire
```

### Afficher le contenu d'un repertoire en temps réel

```bash
watch -n 1 ls nom_du_repertoire
```

### Afficher le contenu d'un repertoire en détail

```bash
ls -l nom_du_repertoire
```
