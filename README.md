# s00r1 Repo

Ce dépôt héberge la source APT de s00r1, destinée aux appareils iOS
jailbreakés. Il permet d'installer facilement divers tweaks et paquets
via Cydia, Sileo ou Zebra.

## Ajouter la source

- **Cydia** : `https://repo.s00r1.com`
- **Sileo** : `sileo://source/https://repo.s00r1.com`
- **Zebra** : `zbra://source/https://repo.s00r1.com`

Ajoutez simplement cette adresse comme nouvelle source dans votre
gestionnaire de paquets.

## Mise à jour des fichiers `Packages` et `Release`

Si vous maintenez ce dépôt, exécutez les commandes suivantes dans le
répertoire racine pour régénérer les index :

```bash
apt-ftparchive packages ./debs > Packages
gzip -kfc Packages > Packages.gz
bzip2 -kfc Packages > Packages.bz2
xz -c Packages > Packages.xz
apt-ftparchive release . > Release
```

Cela actualisera les fichiers utilisés par les gestionnaires de paquets.
