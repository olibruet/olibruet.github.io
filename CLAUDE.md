# Pages publiques

Site : https://olibruet.github.io — HTML statique publié depuis `main`.

## Périmètre autorisé

Seules ces cinq pages, leur sommaire `index.html` et ce fichier d’instructions doivent être conservés dans ce dépôt :

- `maison/solaire/dashboard-production.html` — dashboard solaire.
- `sport-health/plans/custom/2026_semi_casteljaloux_3s.html` — plan semi.
- `sport-health/plans/custom/2026_10km_izon_caisse_3s.html` — plan 10 km Izon.
- `sport-health/entrainements/exercices/renfo_2026_semi.html` — renforcement.
- `sport-health/plans/custom/2026_piscine_cross-training.html` — natation.

Les fiches scolaires, études familiales, pages médicales, études de vacances et autres documents restent dans leurs dépôts privés. Ne pas les republier sans demande explicite.

## Confidentialité — règle bloquante

**Aucune donnée personnelle ou sensible ne doit être introduite dans un commit ni publiée. Toute détection ou tout doute bloque le commit et le push jusqu’à correction.**

- Interdits : identité et domicile du foyer, contacts et dates de naissance, informations fiscales et bancaires, données médicales personnelles, secrets et identifiants d’installation. Vérifier le contenu, les commentaires, données embarquées, noms de fichiers, messages de commit et identités auteur/committer.
- La présence d’une page dans la liste autorisée ne constitue aucune exemption à cette règle. Relire humainement chaque fichier destiné à la publication.
- Les hooks de confidentialité sont obligatoires. Leur programme et le contexte privé restent dans le dépôt privé voisin. Installation depuis ce dépôt : `python3 ../maison/scripts/publication/public_guard.py --install .`.
- Avant commit : `python3 ../maison/scripts/publication/public_guard.py --repo . --staged`. Le contrôle porte sur tous les fichiers de l’index, en entier, y compris les fichiers inchangés. Les hooks contrôlent également les messages et les commits sortants.
- Ne jamais contourner un blocage avec `--no-verify`, des hooks désactivés ou une exemption ajoutée pour faire passer des données sensibles. Corriger le contenu, ou corriger et vérifier un faux positif réel avant de reprendre.
- Une nouvelle copie du dépôt nécessite la réinstallation des hooks. S’ils sont absents ou indisponibles, ne pas commiter ni publier.
- La détection automatique complète la relecture ; elle ne garantit pas l’anonymat. Une page déjà présente qui contient des informations sensibles bloque tous les commits tant qu’elle n’est pas anonymisée.

## Publication

- Conserver les chemins existants afin de préserver les liens.
- Régénérer `index.html` avec `~/bin/generate-gh-index` après ajout ou retrait autorisé.
- Vérifier le diff avant publication et limiter les fichiers ajoutés aux chemins autorisés.
- Ne jamais publier de secrets, identifiants d’installation, coordonnées ou mentions nominatives du foyer.
- Utiliser une identité technique générique pour les commits publics, sans modifier la configuration Git globale.

## Sources sportives publiques

Les versions sportives sont générées depuis les sources relues `../maison/docs/publication/sport/`, avec `python3 ../maison/scripts/publication/build_sport_pages.py --out .`. Ne jamais recopier directement les documents personnels du dépôt sportif privé. Préserver les programmes et les exercices, sans ajouter de journal individuel, identifiant de séance ou compte rendu médical. Le dashboard énergétique reste le contenu technique choisi par le propriétaire, sans secret ni identifiant d’installation.
