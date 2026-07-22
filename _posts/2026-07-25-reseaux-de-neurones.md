---
layout: post
title: "Réseaux de neurones : les bases mathématiques"
date: 2026-07-25
author: Stodar
---

Derrière le terme un peu intimidant de "réseau de neurones", il y a une idée mathématique assez simple : combiner beaucoup de fonctions élémentaires pour approximer une fonction complexe.

## Le neurone artificiel

Un neurone reçoit plusieurs entrées `x₁, x₂, ..., xₙ`, les multiplie chacune par un poids `w₁, w₂, ..., wₙ`, additionne le tout avec un biais `b`, puis applique une **fonction d'activation** :

```
y = f(w₁x₁ + w₂x₂ + ... + wₙxₙ + b)
```

La fonction d'activation (ReLU, sigmoïde, tanh...) introduit de la non-linéarité : sans elle, empiler des couches reviendrait juste à faire une seule grande combinaison linéaire, incapable de modéliser des relations complexes.

## Les couches

Un réseau organise ces neurones en couches : une couche d'entrée, une ou plusieurs couches cachées, une couche de sortie. Chaque couche transforme la représentation produite par la précédente. Dans un réseau profond, les premières couches captent des motifs simples (contours, dans le cas d'une image) et les couches suivantes des motifs de plus en plus abstraits.

## L'apprentissage : descente de gradient

Le réseau commence avec des poids aléatoires et ajuste progressivement ces poids pour réduire l'écart entre ses prédictions et les vraies valeurs, mesuré par une **fonction de coût**. La **rétropropagation** calcule comment chaque poids a contribué à l'erreur, et la **descente de gradient** ajuste chaque poids dans la direction qui réduit cette erreur.

## Pourquoi ça marche

Le théorème d'approximation universelle montre qu'un réseau avec suffisamment de neurones peut approximer n'importe quelle fonction continue avec une précision arbitraire. En pratique, l'enjeu n'est pas seulement la capacité théorique du réseau, mais sa capacité à **généraliser** à des données jamais vues, ce qui dépend autant de l'architecture que de la quantité et de la qualité des données d'entraînement.
