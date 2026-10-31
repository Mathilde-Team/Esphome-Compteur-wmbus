# Journal des versions

Format : [Keep a Changelog](https://keepachangelog.com/fr/1.1.0/). Les numéros suivent [SemVer](https://semver.org/lang/fr/), et la version de `pyproject.toml` est égale au tag.

## [Non publié]

- CI et publication : repli GitHub autorisé, publication manuelle sur un tag
  déjà livré dans main, vérification d’ascendance et archives du tag exact.


### Modifié
- **Licence** (#65) : passage en **GPL-3.0-or-later**. `LICENSE` remplacé par le texte officiel de la GPLv3, `license = "GPL-3.0-or-later"` dans `pyproject.toml`, en-têtes SPDX dans `scripts/` et `tests/`. Origine du code externe vérifiée et documentée dans le README (composant SzczepanLeon sans fichier de licence en amont, drivers dérivés de wmbusmeters) ; historique git vérifié : aucun contributeur externe hors organisation.

### Corrigé
- **Débit estimé** (#46) : ajout de `device_class: volume_flow_rate` sur le capteur du compteur et sur ceux des voisins. Le champ « Débit d'eau » du tableau de bord Énergie de Home Assistant ne signale plus « Classe d'appareil inattendue ».

## [0.1.0] - 2026-10-22

Première version publiée sous forme de release GitHub.

### Ajouté
- **Workflow de release** (#54) : `.github/workflows/release.yml` publie une release GitHub au push d'un tag `vX.Y.Z` sur `main` (tag = version de `pyproject.toml`, notes tirées de la section `## [X.Y.Z]` de ce journal, archive des sources jointe).
