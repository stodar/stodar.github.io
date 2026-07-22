---
layout: post
title: "Comprendre la complexité algorithmique (notation Big O)"
date: 2026-07-23
author: Stodar
---

Quand on compare deux algorithmes, le temps d'exécution en secondes ne veut pas dire grand-chose : il dépend de la machine, du langage, de l'implémentation. Ce qui compte vraiment, c'est **comment le temps d'exécution évolue quand la taille des données augmente**. C'est exactement ce que mesure la notation Big O.

## Les classes de complexité les plus courantes

- **O(1)** — temps constant : accéder à un élément d'un tableau par son index.
- **O(log n)** — logarithmique : recherche dichotomique dans un tableau trié.
- **O(n)** — linéaire : parcourir une liste une fois.
- **O(n log n)** — la plupart des tris efficaces (tri fusion, tri rapide en moyenne).
- **O(n²)** — boucles imbriquées, comme un tri à bulles naïf.
- **O(2ⁿ)** — exponentiel : certains algorithmes récursifs non optimisés, comme le calcul naïf de Fibonacci.

## Pourquoi ça compte en pratique

Un algorithme en O(n²) sur 100 éléments fait 10 000 opérations. Sur 100 000 éléments, il en fait 10 milliards. Un algorithme en O(n log n) sur la même donnée fait environ 1,7 million d'opérations. La différence n'est pas cosmétique : c'est ce qui sépare un programme qui répond en une seconde d'un programme qui ne termine jamais.

## Un exemple concret : recherche dans un tableau trié

Une recherche linéaire vérifie chaque élément un par un : O(n). Une recherche dichotomique divise l'espace de recherche en deux à chaque étape : O(log n). Sur un million d'éléments, ça représente environ 20 comparaisons au lieu d'un million.

## Ce qu'il faut retenir

La notation Big O décrit le pire cas (ou le cas moyen, selon le contexte) de croissance du coût en fonction de la taille de l'entrée, indépendamment du matériel. C'est l'outil de base pour choisir une structure de données ou un algorithme avant même d'écrire une ligne de code.
