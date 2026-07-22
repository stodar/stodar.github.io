# Mon Blog

Blog Jekyll minimal prêt pour GitHub Pages, avec commentaires Giscus.

## Structure

```
_config.yml          → réglages du site (titre, URL, etc.)
_posts/               → tes articles (un fichier .md par article)
_layouts/post.html    → mise en page d'un article + zone de commentaires
_includes/giscus.html → widget de commentaires (à configurer, voir plus bas)
index.md              → page d'accueil
```

## Écrire un article

Crée un fichier dans `_posts/` nommé `AAAA-MM-JJ-titre.md` avec cet en-tête :

```yaml
---
layout: post
title: "Titre de l'article"
date: 2026-07-22
---

Contenu en Markdown ici.
```

## Tester en local (optionnel)

```
bundle install
bundle exec jekyll serve
```

Le site sera visible sur http://localhost:4000
