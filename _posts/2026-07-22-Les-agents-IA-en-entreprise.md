# Les agents IA en entreprise : au-delà de l'intelligence, un nouveau défi de gouvernance

> *Les agents IA promettent de transformer profondément les entreprises. Mais leur véritable défi n'est pas leur intelligence : c'est la manière dont ils sont intégrés, gouvernés et sécurisés au sein du système d'information.*

---

# Introduction

L'intelligence artificielle connaît une évolution spectaculaire. Après l'arrivée des assistants conversationnels capables de générer du texte, d'écrire du code ou de répondre à des questions complexes, une nouvelle génération d'outils fait son apparition : **les agents intelligents**.

Contrairement aux assistants classiques, ces agents ne se limitent plus à fournir une réponse. Ils sont capables d'exécuter des tâches, d'interagir avec plusieurs applications, de prendre des décisions dans un cadre défini et parfois même de collaborer avec d'autres agents pour atteindre un objectif.

Cette évolution marque une rupture importante dans la manière dont les entreprises envisagent l'automatisation. Là où les logiciels traditionnels exécutaient des règles prédéfinies, les agents IA introduisent une forme d'autonomie capable de s'adapter au contexte.

Aujourd'hui, un agent peut assister un développeur dans la création d'une application, analyser plusieurs millions de lignes de données en quelques secondes, produire un rapport financier ou encore diagnostiquer une panne sur une infrastructure informatique.

Mais cette puissance soulève immédiatement une question essentielle :

> **Comment intégrer ces nouveaux collaborateurs numériques dans le système d'information sans compromettre la sécurité, la gouvernance et la conformité de l'entreprise ?**

Pendant longtemps, les discussions autour de l'IA se sont concentrées sur les performances des modèles de langage. Désormais, le véritable enjeu se situe ailleurs. Les entreprises doivent apprendre à considérer les agents IA comme de nouveaux composants de leur architecture informatique, disposant de droits, d'identités, de responsabilités et d'un périmètre d'action clairement défini.

---

# Les agents IA : un terme unique pour des réalités très différentes

Le terme **agent IA** est devenu omniprésent. Pourtant, il désigne des outils extrêmement variés.

Pour certains, un agent est simplement un assistant capable de rédiger un document ou de répondre à un courrier électronique. Pour d'autres, il s'agit d'un développeur virtuel capable d'écrire du code ou encore d'un analyste qui interroge des bases de données complexes.

Cette diversité explique pourquoi de nombreuses entreprises rencontrent des difficultés lorsqu'elles souhaitent déployer leurs premiers agents.

L'erreur consiste souvent à croire que tous les agents peuvent être administrés de la même manière.

En réalité, un agent qui manipule des documents bureautiques n'a absolument pas les mêmes contraintes qu'un agent autorisé à modifier une infrastructure Kubernetes ou à exécuter des commandes sur un serveur Linux.

La véritable différence ne réside donc pas dans leur intelligence.

Elle réside dans trois caractéristiques fondamentales.

- Les données auxquelles ils peuvent accéder.
- Les actions qu'ils sont autorisés à réaliser.
- Les ressources avec lesquelles ils communiquent.

Ces trois dimensions déterminent directement les risques associés à leur utilisation.

---

# Les trois piliers qui définissent un agent IA

Avant même de parler de modèles d'intelligence artificielle, il est nécessaire de comprendre la nature technique d'un agent.

Chaque agent peut être décrit selon trois plans complémentaires.

| Élément | Question principale | Impact |
|----------|--------------------|--------|
| **Plan de données** | Quelles informations l'agent consulte-t-il ? | Détermine son emplacement de déploiement |
| **Plan d'exécution** | Quelles actions peut-il effectuer ? | Détermine les permissions nécessaires |
| **Plan de communication** | Quelles informations quittent le système ? | Détermine les contrôles réseau |

Cette approche est beaucoup plus pertinente qu'une classification basée sur le fournisseur ou le modèle de langage utilisé.

Deux agents utilisant exactement le même LLM peuvent présenter des niveaux de risque totalement différents selon leurs permissions.

Autrement dit, ce n'est pas l'intelligence qui détermine le niveau de sécurité nécessaire, mais le périmètre d'action accordé à l'agent.

---

# Une classification pensée pour les entreprises

Lorsqu'on analyse les usages réels observés dans les entreprises, quatre grandes catégories d'agents apparaissent naturellement.

## Les agents bureautiques

Les agents bureautiques sont les plus répandus.

Ils assistent les collaborateurs dans leurs activités quotidiennes : rédaction de documents, gestion des courriels, préparation de comptes rendus, recherche d'informations ou organisation de réunions.

Ils manipulent principalement des informations bureautiques.

Leur principal risque n'est pas l'exécution de commandes dangereuses mais la fuite d'informations confidentielles vers un fournisseur externe de modèles IA.

Dans ce contexte, la priorité consiste à protéger les données échangées avec le modèle et à garantir que chaque utilisateur ne puisse accéder qu'aux documents qui lui sont réellement autorisés.

---

## Les agents de développement

Les agents de développement interviennent directement dans le cycle de production logicielle.

Ils génèrent du code, exécutent des tests, analysent des projets existants et peuvent lancer des commandes système.

Leur capacité d'action est beaucoup plus importante que celle d'un simple assistant bureautique.

Une mauvaise commande peut supprimer un dépôt Git, modifier une configuration critique ou exposer des informations sensibles.

Pour cette raison, ces agents doivent fonctionner dans un environnement isolé, généralement sous forme de conteneur ou de machine virtuelle, afin d'éviter qu'ils n'héritent directement des privilèges du poste de travail du développeur.

---

## Les agents de données

Les agents de données représentent probablement la famille la plus prometteuse.

Ils permettent aux métiers de dialoguer directement avec les plateformes analytiques en langage naturel.

Au lieu d'écrire une requête SQL complexe, un utilisateur peut simplement demander :

> « Affiche-moi l'évolution des ventes des douze derniers mois par région. »

L'agent construit alors automatiquement la requête nécessaire.

Cette simplicité cache cependant des risques importants.

Une requête mal optimisée peut saturer une base de données transactionnelle.

Une mauvaise gestion des permissions peut également permettre l'accès à des informations confidentielles.

Pour cette raison, les architectures modernes privilégient l'utilisation d'entrepôts de données, de couches sémantiques et de mécanismes de contrôle des accès au niveau des lignes et des colonnes.

---

## Les agents d'exploitation (SRE)

Les agents SRE accompagnent les équipes responsables des infrastructures.

Ils analysent les journaux, surveillent les métriques, détectent les anomalies et proposent des actions correctives.

Contrairement aux autres catégories, leur danger ne provient pas des données qu'ils consultent mais des actions qu'ils peuvent exécuter.

Redémarrer un cluster Kubernetes, modifier une configuration réseau ou restaurer une base de données sont autant d'opérations qui peuvent avoir un impact direct sur la production.

Ces agents doivent donc être soumis à un contrôle particulièrement strict.

Le diagnostic peut être largement automatisé.

En revanche, toute modification ayant un impact sur la production doit rester validée par un opérateur humain.

---

# Comparaison des principales catégories d'agents

| Type d'agent | Données manipulées | Actions principales | Niveau de risque |
|--------------|-------------------|---------------------|------------------|
| Agent bureautique | Documents, courriels, agendas | Assistance utilisateur | Faible |
| Agent de développement | Code source | Génération de code, exécution de scripts | Élevé |
| Agent de données | Bases de données, Data Warehouse | Analyse et génération de requêtes | Très élevé |
| Agent SRE | Journaux, métriques, infrastructures | Diagnostic et opérations système | Critique |

---

# Pourquoi les permissions sont plus importantes que les prompts

Une erreur fréquente consiste à croire qu'un agent est sécurisé parce qu'on lui demande explicitement :

> « Ne modifie jamais la production. »

ou encore :

> « Demande toujours confirmation avant d'exécuter une commande. »

Ces instructions constituent de simples recommandations.

Elles ne remplacent jamais un véritable mécanisme de contrôle des accès.

La sécurité d'un agent ne doit pas dépendre de son comportement supposé mais des limitations imposées par l'infrastructure.

Autrement dit, si un agent ne doit pas modifier une base de données, il ne doit tout simplement pas posséder les permissions nécessaires pour le faire.

Les règles de sécurité doivent être appliquées au niveau des identités, des permissions IAM et des politiques réseau, et non uniquement dans le prompt.

---

# Une nouvelle problématique : la collaboration entre agents

L'évolution actuelle montre que les agents ne travailleront bientôt plus seuls.

Un assistant commercial pourra demander à un agent de données de produire des indicateurs de vente.

Ce dernier pourra ensuite solliciter un agent analytique chargé de construire des visualisations.

Enfin, un agent bureautique rédigera automatiquement le rapport destiné à la direction.

Cette collaboration ouvre des perspectives considérables.

Elle impose également une nouvelle exigence : conserver l'identité de l'utilisateur tout au long de la chaîne d'exécution.

Chaque agent doit agir **au nom de l'utilisateur**, sans jamais contourner les mécanismes de contrôle des accès existants.

La traçabilité devient alors un élément fondamental de la gouvernance.

---

# L'observabilité : le véritable fondement de la confiance

Dans les architectures modernes, il ne suffit plus de savoir qu'un agent a exécuté une tâche.

Les équipes doivent être capables de répondre à plusieurs questions :

- Quel utilisateur est à l'origine de la demande ?
- Quel agent a été sollicité ?
- Quels outils ont été utilisés ?
- Quelles données ont été consultées ?
- Quelles actions ont été réalisées ?
- Quel a été le coût de cette exécution ?

Cette capacité d'observation transforme les outils de supervision traditionnels en véritables plateformes de gouvernance des agents IA.

Sans observabilité, il devient impossible d'accorder des permissions avec confiance.

---

# Les agents IA annoncent une nouvelle génération d'architectures

Pendant plusieurs décennies, les systèmes d'information ont été conçus autour de deux grandes catégories d'acteurs : les utilisateurs et les applications.

Les agents IA introduisent une troisième catégorie.

Ils possèdent une identité.

Ils disposent d'autorisations.

Ils exécutent des actions.

Ils collaborent avec d'autres systèmes.

Ils prennent parfois des initiatives.

Cette évolution oblige les entreprises à repenser entièrement leur manière de concevoir les architectures informatiques.

Les agents devront progressivement être administrés comme de véritables collaborateurs numériques, avec des identités dédiées, des permissions limitées, des journaux d'audit complets et des environnements d'exécution isolés.

---

# Conclusion

Les agents d'intelligence artificielle ne représentent pas simplement une amélioration des assistants numériques que nous connaissions jusqu'à présent.

Ils constituent une nouvelle génération de composants capables d'interagir de manière autonome avec les applications, les données et les infrastructures de l'entreprise.

Le succès de leur adoption dépendra moins de la puissance des modèles de langage que de la qualité de leur intégration dans le système d'information.

Les organisations qui réussiront cette transformation seront celles qui considéreront les agents non pas comme de simples outils, mais comme de véritables identités numériques disposant d'un rôle clairement défini, d'un périmètre d'action limité et d'une gouvernance rigoureuse.

L'avenir de l'intelligence artificielle en entreprise ne se jouera donc pas uniquement sur la performance des modèles.

Il reposera avant tout sur notre capacité à construire des architectures où l'autonomie des agents s'accompagne d'un niveau de sécurité, de transparence et de contrôle équivalent à celui exigé pour les systèmes les plus critiques.