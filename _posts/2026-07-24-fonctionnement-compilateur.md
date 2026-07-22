---
layout: post
title: "Que fait vraiment un compilateur ?"
date: 2026-07-24
author: Stodar
---

Écrire du code et obtenir un programme exécutable semble presque magique. En réalité, un compilateur suit une série d'étapes bien définies, chacune transformant le code sous une forme un peu plus proche de ce que la machine peut comprendre.

## 1. Analyse lexicale

Le code source, une simple suite de caractères, est découpé en **tokens** : mots-clés, identifiants, opérateurs, nombres. `x = a + 1;` devient une liste comme `[IDENT x] [EGAL] [IDENT a] [PLUS] [NOMBRE 1] [POINT-VIRGULE]`.

## 2. Analyse syntaxique

Les tokens sont organisés en un **arbre syntaxique abstrait (AST)**, qui représente la structure grammaticale du programme : quelle expression appartient à quelle instruction, quel opérateur s'applique à quels opérandes.

## 3. Analyse sémantique

Le compilateur vérifie que le programme a du sens : les types sont-ils cohérents, les variables sont-elles déclarées avant d'être utilisées, les fonctions sont-elles appelées avec le bon nombre d'arguments. C'est à cette étape que sont détectées la plupart des erreurs de type.

## 4. Génération de code intermédiaire

Beaucoup de compilateurs (GCC, LLVM) traduisent d'abord l'AST vers une représentation intermédiaire indépendante du matériel. Cela permet d'appliquer des optimisations générales avant de se soucier du processeur cible.

## 5. Optimisation

Élimination de code mort, propagation de constantes, déroulement de boucles : le compilateur réécrit le programme pour qu'il fasse la même chose, mais plus vite ou avec moins de mémoire.

## 6. Génération de code machine

Enfin, le code est traduit dans le jeu d'instructions du processeur cible (x86, ARM...), avec allocation des registres et prise en compte des spécificités matérielles.

## Compilé vs interprété

Un langage interprété (Python, JavaScript côté navigateur classique) saute une partie de ces étapes et exécute une représentation intermédiaire directement, instruction par instruction, ce qui explique une bonne partie de l'écart de performance avec des langages compilés comme C ou Rust.
