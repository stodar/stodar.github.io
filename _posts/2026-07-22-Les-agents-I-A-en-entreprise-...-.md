# Au-delà de l'intelligence, un nouveau défi de gouvernance

## Introduction

L'intelligence artificielle connaît une évolution spectaculaire. Après les assistants conversationnels capables de répondre à des questions ou de générer du contenu, une nouvelle génération d'outils s'impose progressivement dans les entreprises : les agents intelligents. Contrairement aux chatbots traditionnels, ces agents ne se limitent plus à fournir des réponses. Ils sont capables de prendre des initiatives, d'interagir avec plusieurs applications, d'exécuter des actions et même de collaborer avec d'autres agents pour accomplir des objectifs complexes.

Cette évolution ouvre des perspectives considérables. Un agent peut aujourd'hui rédiger un rapport, analyser des millions de lignes de données, corriger automatiquement du code ou encore assister les équipes d'exploitation dans la résolution d'incidents. Pour beaucoup d'organisations, cette automatisation représente une opportunité majeure d'améliorer la productivité et d'accélérer les processus métiers.

Pourtant, derrière cette promesse se cache une question beaucoup plus importante que le choix du modèle d'intelligence artificielle lui-même : comment intégrer ces nouveaux acteurs numériques dans un système d'information sans compromettre sa sécurité, sa gouvernance et sa conformité ?

## Comprendre ce qu'est réellement un agent IA

Le terme agent IA est aujourd'hui utilisé pour désigner des outils extrêmement différents. Certains développent du code, d'autres répondent aux courriels ou produisent des analyses financières. Cette diversité explique pourquoi il est difficile de définir une stratégie unique de déploiement.

En réalité, la nature d'un agent ne dépend pas du fournisseur qui le commercialise ni du modèle de langage qu'il utilise. Elle dépend essentiellement de trois caractéristiques fondamentales :

- les informations auxquelles il peut accéder ;
- les actions qu'il est autorisé à exécuter ;
- les ressources externes avec lesquelles il peut communiquer.

Ces trois dimensions déterminent directement les risques associés à son utilisation et les mécanismes de sécurité qu'il sera nécessaire de mettre en œuvre.

| Critère | Question principale | Impact sur l'architecture |
|---|---|---|
| Plan de données | À quelles données l'agent accède-t-il ? | Détermine son emplacement de déploiement |
| Plan d'exécution | Quelles actions peut-il réaliser ? | Détermine les permissions IAM |
| Communication externe | Quelles informations quittent l'entreprise ? | Détermine les mécanismes de contrôle réseau |

Cette approche permet de dépasser la simple vision marketing des agents IA pour les considérer comme de véritables composants du système d'information.

## Une classification pensée pour les entreprises

Lorsqu'on observe les usages réels en entreprise, quatre grandes familles d'agents apparaissent naturellement.

Les premiers sont les **agents bureautiques**, principalement utilisés pour assister les collaborateurs dans leurs tâches quotidiennes. Ils manipulent des documents, des courriels, des calendriers ou encore des outils collaboratifs. Leur principal enjeu consiste à protéger les informations confidentielles échangées avec les modèles d'intelligence artificielle.

À l'opposé, les **agents de développement** interviennent directement dans le cycle logiciel. Ils disposent souvent de privilèges élevés leur permettant de compiler un projet, d'exécuter des scripts ou de modifier un dépôt Git. Cette capacité d'action nécessite un environnement d'exécution fortement isolé afin d'éviter qu'une erreur ou une attaque ne compromette l'infrastructure de développement.

Les **agents de données** représentent probablement la catégorie la plus prometteuse. Leur rôle consiste à transformer les immenses volumes d'informations disponibles dans les entrepôts de données en indicateurs exploitables par les métiers. Leur puissance est considérable, mais elle impose également des mécanismes rigoureux de contrôle des accès, d'anonymisation et de limitation des requêtes.

Enfin, les **agents d'exploitation**, parfois appelés agents SRE, assistent les équipes responsables des infrastructures. Ils analysent les journaux techniques, détectent les anomalies et peuvent même proposer des actions correctives. Toutefois, toute intervention susceptible de modifier un environnement de production doit rester soumise à une validation humaine.

Le tableau suivant résume les principales caractéristiques de ces différentes catégories.

| Type d'agent | Données manipulées | Actions principales | Niveau de risque |
|---|---|---|---|
| Agent bureautique | Documents, courriels, agendas | Assistance utilisateur | Faible à moyen |
| Agent de développement | Code source | Compilation, tests, génération de code | Élevé |
| Agent de données | Bases de données, Data Warehouse | Analyse, requêtes SQL, reporting | Très élevé |
| Agent SRE | Journaux, métriques, traces | Diagnostic et opérations d'exploitation | Critique |

## La sécurité ne repose pas sur l'intelligence de l'agent

L'une des erreurs les plus fréquentes consiste à penser qu'un agent sera sécurisé parce qu'il a reçu des instructions précises dans son prompt. En pratique, un modèle peut toujours être confronté à des situations imprévues ou à des tentatives de manipulation.

La véritable sécurité repose donc sur des mécanismes techniques indépendants du modèle lui-même. Les permissions doivent être limitées au strict nécessaire, les identités clairement définies et toutes les actions enregistrées dans des journaux d'audit.

Autrement dit, un agent ne doit jamais être considéré comme un utilisateur humain. Il doit disposer d'une identité propre, de privilèges spécifiques et d'un périmètre d'action parfaitement maîtrisé.

...

## Conclusion

Les agents d'intelligence artificielle représentent bien davantage qu'une évolution des assistants numériques traditionnels. Ils introduisent une nouvelle catégorie d'acteurs capables d'interagir de manière autonome avec les applications, les données et les infrastructures de l'entreprise.

Leur adoption ne dépendra pas uniquement de la qualité des modèles d'IA, mais surtout de la capacité des organisations à construire une architecture robuste, fondée sur une gouvernance claire, une gestion rigoureuse des identités et une observabilité complète de toutes les interactions.

À mesure que les agents collaboreront entre eux et deviendront des composants permanents du système d'information, ils devront être administrés avec le même niveau d'exigence que les applications critiques. L'enjeu ne sera plus seulement de créer des agents toujours plus intelligents, mais de bâtir un environnement où leur autonomie s'exerce dans un cadre sécurisé, transparent et maîtrisé.
