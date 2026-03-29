# CLAUDE.md — olibruet.github.io

## Qu'est-ce que ce repo ?

Site GitHub Pages personnel d'Olivier Bruet : **https://olibruet.github.io**
Pages HTML statiques publiées directement depuis la branche `main`.

## Structure

```
index.html                  # Page d'accueil avec liens vers les sections
sport-health/               # Plans d'entraînement, exercices, santé, tutos
scolarite/                  # Fiches scolaires (CM1, 5ème…)
```

## Conventions

- **Langue** : contenu en français
- **Format** : fichiers HTML autonomes (CSS inline, pas de framework)
- **Publication** : push sur `main` → GitHub Pages déploie automatiquement
- **Style HTML** : pages self-contained avec styles intégrés dans `<style>`, responsive, police système (`-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`)
- **Nommage** : kebab-case pour les fichiers et dossiers

## Workflow de publication

Utiliser le skill `/publish-gh` pour publier de nouvelles pages.
Chaque page HTML doit être autonome (pas de dépendance CSS/JS externe sauf CDN publics).

## Points d'attention

- Ne pas publier de données sensibles (ce repo est **public**)
- Mettre à jour `index.html` quand on ajoute une nouvelle section ou page importante
