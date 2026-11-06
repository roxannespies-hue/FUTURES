### 1. Contexte et Problème

Dans un environnement marqué par des transformations technologiques, économiques, sociétales et environnementales, les organisations doivent anticiper les ruptures susceptibles de remettre en question leurs activités, leurs métiers et leurs orientations stratégiques.

Pour éclairer ces réflexions, les professionnels de la stratégie, de la prospective et de l'innovation s'appuient notamment sur des études de tendances, des signaux émergents, des scénarios prospectifs et des ateliers collaboratifs.

Cependant, la difficulté ne réside pas uniquement dans la construction de scénarios, mais aussi dans leur appropriation par les collaborateurs et dans l'exploitation des réflexions qu'ils suscitent.

Trois problématiques principales émergent des recherches exploratoires :

1. **Des futurs difficiles à appréhender concrètement.** Les scénarios de rupture peuvent rester abstraits pour des collaborateurs peu familiers de la prospective. Il leur est alors difficile de se représenter les conséquences possibles sur leur métier, leurs pratiques ou leur environnement professionnel.
2. **Des démarches d'exploration parfois complexes et ponctuelles.** Les exercices prospectifs mobilisent différents supports et outils, souvent dispersés. Leur appropriation nécessite du temps et les échanges peuvent se concentrer sur quelques ateliers, limitant les possibilités d'exploration individuelle et de participation de profils variés.
3. **Une capitalisation des réflexions difficile.** Les réactions et questionnements formulés pendant les démarches prospectives peuvent être dispersés entre plusieurs supports. Leur collecte, leur consolidation et leur restitution demandent un travail supplémentaire, avec un risque de perdre certaines perspectives singulières ou divergentes.

**Le problème central est donc la difficulté à transformer des scénarios prospectifs de rupture en une réflexion collective accessible, approfondie et exploitable pour les organisations.**

Ces constats constituent des pistes issues de la recherche secondaire et de l'analyse des pratiques existantes. Leur importance et leur fréquence auprès des utilisateurs cibles restent à confirmer par des entretiens et des observations terrain.

<br>

### 2. Proposition de valeur

FUTURES permet aux professionnels de la stratégie, de la prospective et de l’innovation d’impliquer davantage les collaborateurs dans l’exploration de scénarios de rupture, grâce à une plateforme immersive et réutilisable qui rend les futurs concrets, stimule les questionnements métier et permet de capitaliser sur les réflexions pour enrichir la réflexion stratégique.

<br>

### 3.Cibles et Persona

- Claire - Cible principale / porteuse du besoin : professionnelle de la stratégie et de la prospective.
- Thomas - Utilisateur final principal : collaborateur non spécialiste de la prospective.
- Julien - Utilisateur support : administrateur de la plateforme. (secondaire)

<img width="632" height="675" alt="image (8)" src="https://github.com/user-attachments/assets/fd3588e5-9bf9-439e-babd-326a5cf032a6" />

<img width="639" height="767" alt="image (7)" src="https://github.com/user-attachments/assets/08ce532e-8fda-4389-8217-92a538684d07" />

<img width="629" height="741" alt="image (6)" src="https://github.com/user-attachments/assets/ba0da05d-ddcd-4377-82b6-ae7733165f67" />



<br>

### 4. Objectifs SMART

Les objectifs du MVP de FUTURES sont définis à partir des critères de réussite des trois personas : Claire, Thomas et Julien.

Ils visent à vérifier la capacité des utilisateurs à accomplir les actions essentielles du produit à l'issue des six semaines de développement.

#### Objectif 1 — Faciliter l'exploration des futurs (Thomas)

Permettre à au moins **4 collaborateurs sur 5**, non spécialistes de la prospective, d'explorer un scénario de rupture, de consulter au moins deux artefacts et de consigner une réflexion personnelle dans leur carnet d'étonnement, **en moins de 15 minutes et sans assistance**, lors des tests réalisés à l'issue des six semaines.

**Résultat attendu :** les collaborateurs parviennent à explorer un futur et à exprimer un questionnement sans accompagnement préalable.

**Indicateurs de réussite :**
- Au moins 80 % des participants terminent le parcours.
- Durée du parcours inférieure ou égale à 15 minutes.
- Aucune assistance nécessaire pour accomplir les actions demandées.

**Fonctionnalités du PRD associées :** F01, F02.1, F03 et F04.

#### Objectif 2 — Rendre les scénarios accessibles et crédibles (Claire)

Permettre à un professionnel de la stratégie ou de la prospective de consulter le scénario fondateur d'un futur et d'identifier **au moins trois signaux réels documentés, accompagnés de leurs sources, directement dans l'onglet Scénario**, en moins de 10 minutes, sur la version livrée à l'issue des six semaines.

**Résultat attendu :** les professionnels de la prospective peuvent consulter un scénario structuré et vérifier ses principaux fondements documentaires, sans avoir besoin d'une chronologie prospective dédiée.

**Indicateurs de réussite :**
- Consultation du scénario fondateur.
- Identification d'au moins trois signaux réels documentés.
- Accès aux sources correspondant à chacun des trois signaux.
- Parcours effectué en 10 minutes maximum.

**Fonctionnalité du PRD associée :** F02.1 — Consulter le scénario fondateur.

#### Objectif 3 — Garantir un accès sécurisé à la plateforme (Julien)

Permettre, à l'issue des six semaines, de vérifier que **100 % des scénarios de contrôle d'accès définis pour le MVP** sont réussis : un utilisateur actif et autorisé peut se connecter et consulter le futur disponible, tandis qu'un utilisateur non authentifié ou ne disposant pas des habilitations nécessaires se voit refuser l'accès aux contenus et fonctions protégés.

**Résultat attendu :** l'authentification et les autorisations fonctionnent conformément aux rôles et aux règles de sécurité définis, sans nécessiter une interface dédiée d'administration des comptes.

**Indicateurs de réussite :**
- Connexion réussie pour un utilisateur actif disposant des autorisations nécessaires.
- Accès au futur autorisé après authentification.
- Refus d'accès aux contenus protégés pour un utilisateur non authentifié.
- Refus d'accès aux contenus ou fonctions non autorisés, y compris par accès direct à leur URL.
- Réussite de l'ensemble des scénarios de contrôle d'accès documentés pour le MVP.

**Fonctionnalité du PRD associée :** F01 — Authentification et accès à un futur.

  <br>

### 5. Périmètre

Le MVP de FUTURES vise à proposer une première expérience fonctionnelle d'exploration prospective, permettant à un collaborateur de découvrir un scénario de rupture, d'explorer des contenus fictionnels, de consigner ses réflexions personnelles et d'approfondir ses questionnements grâce à un agent conversationnel IA.

Cette première version est volontairement limitée à **un seul futur**, afin de concentrer les six semaines de développement sur la qualité de l'expérience, la cohérence des contenus et la fiabilité des fonctionnalités essentielles.

**5.1. Fonctionnalités incluses dans le MVP** 

| Bloc fonctionnel | Périmètre retenu |
| --- | --- |
| **Authentification et accès (F01)** | Connexion des utilisateurs via Supabase Auth, reconnaissance des rôles et contrôle des autorisations d'accès aux contenus et fonctions protégés. |
| **Accueil et sélection du futur (F01)** | Page d'accueil présentant le premier futur disponible et donnant accès à son exploration. |
| **Exploration du scénario (F02.1)** | Consultation du scénario fondateur présentant le contexte, les ruptures et les caractéristiques du monde futur. Présentation d'au moins trois signaux réels documentés, accompagnés de leurs sources, directement dans l'onglet Scénario. |
| **Artefacts immersifs (F03)** | Consultation de cinq artefacts fictionnels préparés en amont, répartis entre articles, témoignages écrits et podcast. |
| **Carnet d'étonnement (F04)** | Création, consultation, modification et suppression de notes personnelles associées au futur exploré. Possibilité de consigner des réflexions libres, sans rattachement obligatoire à un contenu particulier. |
| **Agent conversationnel IA (F05)** | Intégration d'un agent via l'API OpenAI permettant d'interroger le scénario et les contenus publiés du premier futur. Contextualisation limitée aux informations autorisées et au corpus disponible. |
| **Gestion minimale des comptes et des rôles** | Préparation et gestion des comptes directement dans Supabase, sans développement d'une interface dédiée. Vérification des autorisations selon les rôles définis. |
| **Gestion des contenus** | Préparation, validation et enregistrement des contenus du premier futur dans Supabase. Aucune interface complète de création ou de publication éditoriale n'est exigée pour le MVP. |
| **Actualisation en temps réel** | Intégration ciblée de Supabase Realtime sur un cas d'usage simple, afin de satisfaire les exigences techniques du projet sans développer de fonctionnalités collaboratives avancées. |

  <br>

**5.2. Fonctionnalité optionnelle — Si le temps le permet**

| Bloc fonctionnel | Périmètre envisagé |
| --- | --- |
| **Trajectoire prospective (F02.2)** | Visualisation d'une chronologie présentant les signaux réels documentés et les événements fictionnels qui conduisent au futur exploré. Les éléments réels et fictionnels sont clairement différenciés. |

La trajectoire prospective constitue un enrichissement de l'expérience immersive, mais n'est pas indispensable à la première démonstration de valeur de FUTURES.

Sa réalisation implique un travail supplémentaire de recherche documentaire, de construction narrative, de conception d'interface et de développement.

Elle sera développée uniquement si les fonctionnalités obligatoires du MVP sont terminées, testées et stabilisées. Dans le cas contraire, elle sera reportée à une version ultérieure.

  <br>

**5.3. Fonctionnalités exclues du MVP**

| Bloc fonctionnel | Évolution envisagée |
| --- | --- |
| **Catalogue de plusieurs futurs** | Enrichissement progressif du catalogue avec de nouveaux scénarios de rupture. |
| **Campagnes prospectives** | Création de campagnes avec une question centrale, des participants et un ou plusieurs futurs associés. |
| **Synthèses collectives** | Analyse des notes d'étonnement associées aux campagnes, identification des thèmes récurrents et des divergences. |
| **Studio de création avancé** | Création guidée de futurs et génération assistée de scénarios et d'artefacts. |
| **Génération multimédia automatisée** | Intégration des services IA permettant de produire automatiquement articles, illustrations et podcasts depuis l'application. |
| **Administration des utilisateurs avancée** | Interface dédiée à la création et à la désactivation des comptes, à l'attribution des rôles et à la gestion des habilitations. |
| **Gestion éditoriale avancée** | Interface permettant de créer, modifier, valider et publier les scénarios, les signaux, les événements et les artefacts. |
| **Gestion multi-organisation avancée** | Administration de plusieurs organisations et de leurs contenus contextualisés. |
| **Administration et suivi avancés** | Tableaux de bord, indicateurs d'utilisation, supervision détaillée des générations et des coûts IA. |
| **Exports et restitutions** | Export des synthèses et résultats des campagnes, notamment au format PDF. |
| **Intégrations d'entreprise** | Authentification SSO, connexions aux systèmes internes et traitement de documents stratégiques sensibles. |
  <br>

**5.4. Principes de limitation du périmètre** 

Pour garantir une livraison cohérente dans le délai prévu :

- Un seul futur sera disponible.
- L'Explorer comprendra trois onglets obligatoires : Scénario, Artefacts et Carnet d'étonnement.
- Les trois signaux réels documentés seront accessibles depuis l'onglet Scénario, sans nécessiter une chronologie dédiée.
- L'agent conversationnel IA sera intégré à l'Explorer, avec un périmètre limité au premier futur et à ses contenus validés.
- Les cinq artefacts seront préparés en amont et stockés dans l'application, sans génération automatique à chaque consultation.
- La gestion des utilisateurs, des rôles et des contenus s'appuiera principalement sur les outils d'administration de Supabase, sans développement d'un back-office complet.
- Les fonctionnalités de collaboration avancée et de restitution collective seront reportées.
- Les développements techniques seront priorisés selon leur contribution aux objectifs SMART et aux exigences obligatoires de la Checklist Qualité Produit.

**Le MVP doit avant tout démontrer la capacité de FUTURES à rendre un scénario prospectif concret, accessible et explorable, tout en permettant aux utilisateurs de formaliser leurs étonnements et d'approfondir leurs questionnements grâce à l'intelligence artificielle.**

<br>

### 6. Grille de sélection de la stack d’outils

<img width="677" height="348" alt="image (3)" src="https://github.com/user-attachments/assets/718b466a-5395-41ae-badb-9c749f4aa7e6" />


Outil complémentaire : Claude Cowork. Il peut être utilisé pour la documentation et certaines automatisations de travail, mais ne constitue pas une dépendance technique de FUTURES.

**Grille d'évaluation selon les six critères**

Les évaluations sont établies pour le contexte de FUTURES : une première application développée individuellement, puis potentiellement déployée dans un environnement professionnel.

<img width="648" height="816" alt="image (4)" src="https://github.com/user-attachments/assets/b63157d2-422a-4810-a597-9b6538f2854b" />
<img width="659" height="580" alt="image (2)" src="https://github.com/user-attachments/assets/016cb4ff-a47d-421e-aeba-2278bcdeeef4" />


**Le cas spécifique de Claude cowork :** 

<img width="631" height="511" alt="image (5)" src="https://github.com/user-attachments/assets/bf1c8adb-96ed-4aa1-badf-ac2210412704" />


<br>

### 7. Matrice des risques

La réalisation du MVP de FUTURES repose sur plusieurs outils de développement assisté par IA, des services externes et une architecture intégrant notamment Supabase, Lovable et l'API OpenAI.

Dans un délai de développement de six semaines, les principaux risques concernent la maîtrise du périmètre, les intégrations techniques, la sécurité des données et la livraison des fonctionnalités obligatoires.

La matrice suivante évalue chaque risque selon sa **probabilité estimée**, son **impact potentiel** et les mesures permettant d'en réduire les conséquences.

| Risque | Probabilité | Impact | Mitigation |
| --- | --- | --- | --- |
| **R1 — Dérive du périmètre fonctionnel.** L'ajout de fonctionnalités ou la complexification des parcours retarde la livraison du MVP. | Élevée | Élevé | Figer le périmètre dans le PRD, maintenir une liste des fonctionnalités post-MVP et soumettre chaque ajout à un arbitrage de priorité. |
| **R2 — Difficultés d'intégration de l'agent IA.** L'API OpenAI, la contextualisation du scénario ou la gestion des erreurs nécessitent davantage de développement que prévu. | Moyenne | Élevé | Tester un premier appel API dès le début du développement, limiter l'agent à un futur et à un corpus validé, puis enrichir progressivement ses capacités. |
| **R3 — Erreurs de gestion des accès ou de sécurisation des données.** Des règles Supabase mal configurées permettent des accès non autorisés aux notes ou aux fonctions administratives. | Moyenne | Élevé | Activer les politiques RLS sur les tables concernées, tester les accès avec plusieurs comptes de rôles différents et réaliser un audit de sécurité avec Claude Code avant livraison. |
| **R4 — Difficultés d'interconnexion entre les outils.** Des problèmes de synchronisation entre Lovable, GitHub, VS Code, Supabase et Vercel ralentissent le développement. | Moyenne | Moyen | Configurer et tester la chaîne complète dès le démarrage, définir GitHub comme référentiel du code et effectuer régulièrement des déploiements de vérification. |
| **R5 — Non-respect des exigences de livraison.** Certaines obligations techniques ou documentaires sont découvertes ou traitées trop tard. | Moyenne | Élevé | Associer chaque point de la checklist qualité à un livrable, planifier les preuves attendues par module et vérifier leur avancement chaque semaine. |

Les risques présentant un impact élevé seront traités en priorité, notamment ceux liés à la sécurité des données, à l'intégration IA et au respect du périmètre.

Trois principes guideront leur maîtrise :

- **Anticiper les dépendances techniques :** vérifier rapidement les connexions entre les différents services avant de construire les fonctionnalités complexes.
- **Développer de manière incrémentale :** livrer et tester chaque bloc fonctionnel avant de passer au suivant.
- **Sécuriser la livraison :** conserver un périmètre MVP stable et documenter progressivement les preuves techniques et fonctionnelles attendues.

Les probabilités et impacts présentés constituent des estimations initiales. Ils seront réévalués pendant le développement en fonction des difficultés effectivement rencontrées.

<img width="652" height="465" alt="image (1)" src="https://github.com/user-attachments/assets/7a76f305-3f84-4ede-9d0f-9c9b763ee0fe" />


<br>

### 8. Planning et jalons

Le développement du MVP de FUTURES s'inscrit dans un programme de six semaines, organisé autour des modules du bootcamp Vibe Coding de Lion.

Le planning suit une progression allant du cadrage produit à la conception des interfaces, puis à la structuration de la base de données, à l'intégration de l'intelligence artificielle et au déploiement sécurisé.

Chaque semaine est associée à des livrables vérifiables, permettant de suivre l'avancement du développement et de constituer progressivement les éléments attendus pour la certification.

**8.1. Planning prévisionnel**

| Période | Module de formation | Travaux prévus pour FUTURES | Jalons et livrables |
| --- | --- | --- | --- |
| **Préparation — M0** | Préparation et configuration | Etude de l’envionnement lié au projet personnel (ex : tendance, concurrence…)  | Environnement configuré et installation des logiciels de travail. Lecture de l’on-boarding.   |
| **Semaine 1 — M1** | Cadrage, stratégie et choix de stack | Finalisation de la note de cadrage, des personas, des objectifs SMART, de la proposition de valeur, de la grille de sélection de stack, du périmètre MVP et du PRD. | Note de cadrage complète, PRD documenté, matrice des risques et périmètre fonctionnel validé. |
| **Semaine 2 — M2** | Front-end et expérience utilisateur | Création du design system et d'au moins trois maquettes dans Stitch. Développement des premiers écrans dans Lovable, structuration de la navigation et préparation de leur connexion aux données. | Maquettes et premiers parcours navigables, audit de contraste WCAG AA.  |
| **Semaine 3 — M3** | Architecture de données et back-end | Traduction du MCD en schéma relationnel Supabase, création des tables nécessaires au MVP, configuration de Supabase Auth, des permissions et des politiques RLS. Connexion des écrans développés à la base. | Base Supabase opérationnelle, au moins trois tables reliées, diagramme entité-relation documenté, authentification et premiers parcours connectés. |
| **Semaine 4 — M4** | Intelligence métier et automatisation | Intégration d'un agent conversationnel via l'API OpenAI, limité au premier futur et à ses contenus validés. Création d'une automatisation de veille prospective avec Claude Cowork. | Agent IA fonctionnel, connexion API sécurisée, workflow Claude Cowork exécuté et documenté. |
| **Semaine 5 — M5** | Dashboards de données et déploiement sécurisé | Finalisation des fonctionnalités essentielles, intégration ciblée de Supabase Realtime, configuration du déploiement Vercel, vérification des habilitations et audit de sécurité avec Claude Code. | Application déployée en HTTPS avec domaine personnalisé, actualisation des données en temps réel, audit de sécurité documenté et corrections prioritaires. |
| **Semaine 6 — M6** | Finalisation et préparation de la soutenance | Tests des parcours utilisateurs, correction des anomalies restantes, stabilisation du MVP, finalisation de la documentation et préparation de la démonstration. | MVP stabilisé, dépôt GitHub avec au moins 15 commits lisibles, README complet, documentation utilisateur, Checklist Qualité Produit, rapport d'audit et présentation finale. |

**8.2. Jalons de contrôle**

Trois jalons principaux permettront de vérifier la progression du développement.

**Jalon 1 - Fondations fonctionnelles et techniques (fin de semaine 3)**

**Objectif :** disposer d'une première application navigable, connectée à une base de données sécurisée.

Livrables attendus :

- Note de cadrage et PRD finalisés.
- Trois maquettes d'interfaces au minium  conçues et archivées.
- Structure de navigation de FUTURES développée.
- Schéma relationnel Supabase documenté.
- Authentification et premières politiques RLS opérationnelles.
- Premiers écrans connectés aux données.

**Jalon 2 - Expérience immersive et intelligence artificielle (fin de semaine 4)**

**Objectif :** rendre opérationnels les principaux parcours d'exploration et l'interaction avec l'agent IA.

Livrables attendus :

- Premier futur accessible dans l'Explorer.
- Scénario, trajectoire et artefacts consultables.
- Carnet d'étonnement permettant d'enregistrer et de retrouver des notes.
- Agent conversationnel connecté à l'API OpenAI.
- Workflow Claude Cowork de veille prospective fonctionnel et documenté.

**Jalon 3 - MVP déployé et vérifié (fin de semaine 6)**

**Objectif :** disposer d'une application stable, accessible en ligne et accompagnée des livrables nécessaires à son évaluation.

Livrables attendus :

- Application déployée sur Vercel, accessible en HTTPS avec domaine personnalisé.
- Fonctionnalité Supabase Realtime opérationnelle.
- Contrôles d'accès et politiques de sécurité vérifiés.
- Audit de sécurité réalisé avec Claude Code et rapport archivé.
- Parcours utilisateurs testés et anomalies bloquantes corrigées.
- Dépôt GitHub documenté, avec historique de commits conforme aux attentes.
- Checklist Qualité Produit complétée avec les preuves correspondantes.
- Documentation utilisateur et support de présentation finalisés.
