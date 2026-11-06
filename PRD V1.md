# PRD : SPECIFICATIONS DES 5 FONCTIONNALITES PRINCIPALES DU MVP FUTURES
### F01 — AUTHENTIFICATION ET ACCÈS À UN FUTUR

**1. Ce que l'utilisateur fait**

L'utilisateur se connecte à FUTURES à l'aide de son adresse e-mail et de son mot de passe.

Une fois authentifié, il accède à la page d'accueil et peut sélectionner le futur disponible pour commencer son exploration.

Les contenus et fonctionnalités accessibles dépendent de ses autorisations.

**2. Écrans concernés**

- Page de connexion.
- Page d'accueil présentant le futur disponible.
- Interface Explorer après sélection du futur.

**3. Données mobilisées**

| Entité | Utilisation |
|---|---|
| **Utilisateur** | Identifier l'utilisateur connecté, son statut et son organisation. |
| **Organisation** | Identifier l'organisation à laquelle appartient l'utilisateur. |
| **Rôle** | Définir les différents rôles existants dans FUTURES. |
| **Attribution de rôle** | Identifier les rôles attribués à l'utilisateur. |
| **Permission** | Déterminer les actions autorisées selon les rôles. |
| **Futur** | Récupérer le titre, la description, l'illustration et le statut du futur disponible. |

**Précisions techniques :**

- L'authentification est assurée par Supabase Auth.
- Les autorisations d'accès sont contrôlées à partir des données utilisateur, des rôles et des règles de sécurité définies dans Supabase.
- Les comptes et les rôles sont configurés directement dans Supabase pour le MVP. Aucune interface dédiée à leur administration n'est prévue.

**Relations entre les données :**
- Une organisation peut regrouper plusieurs utilisateurs.
- Chaque utilisateur standard appartient à une seule organisation.
- Un utilisateur peut posséder plusieurs attributions de rôle.
- Chaque attribution de rôle associe un utilisateur à un rôle.
- Un rôle peut être attribué à plusieurs utilisateurs.
- Un rôle peut posséder plusieurs permissions.
- Une permission peut être associée à plusieurs rôles.
- Une organisation peut avoir accès à plusieurs futurs.
- Un futur peut être accessible à plusieurs organisations.
Précision : les relations plusieurs-à-plusieurs entre Rôle et Permission, ainsi qu'entre Organisation et Futur, nécessitent des tables d'association dans Supabase.

**4. Règles métier**

- L'utilisateur doit être authentifié pour consulter les contenus protégés.
- Seuls les comptes actifs peuvent accéder à FUTURES.
- Chaque utilisateur standard appartient à une organisation.
- Les autorisations dépendent du rôle attribué et du périmètre d'accès de l'utilisateur.
- Seuls les futurs publiés et autorisés sont accessibles aux collaborateurs.
- Un utilisateur ne peut pas accéder aux contenus ou fonctions pour lesquels il ne dispose pas des autorisations nécessaires.
- Les contrôles d'accès sont appliqués côté serveur et dans Supabase, notamment à travers les politiques RLS.
- La création, la désactivation des comptes et l'attribution des rôles sont réalisées directement dans Supabase durant le MVP.

**5. Priorité**

**Critique — MVP obligatoire.**

**6. Critères d'acceptation**

- Un utilisateur disposant d'un compte actif et autorisé peut se connecter avec ses identifiants.
- Après connexion, il accède à la page d'accueil.
- Il visualise le futur publié auquel il est autorisé à accéder.
- Il peut sélectionner ce futur et ouvrir l'Explorer.
- Un utilisateur non authentifié ne peut pas accéder aux contenus protégés.
- Un utilisateur sans les habilitations nécessaires ne peut pas accéder aux contenus ou fonctions non autorisés, y compris en utilisant directement leur URL.
- Les autorisations appliquées correspondent au rôle de l'utilisateur.
- Un compte désactivé ne peut plus accéder à l'application.

**Objectif SMART associé :** Objectif 3 — Garantir un accès sécurisé à la plateforme (Julien).

<br>



### F02.1 — CONSULTER LE SCÉNARIO FONDATEUR

**1. Ce que l'utilisateur fait**

Depuis l'Explorer, l'utilisateur accède à l'onglet Scénario pour découvrir le récit fondateur du futur sélectionné.

Il prend connaissance du contexte, des principales ruptures envisagées et des caractéristiques du monde fictionnel.

Il peut également consulter au moins trois signaux réels documentés ayant inspiré la construction de ce futur, ainsi que leurs sources.

L'objectif est de permettre à l'utilisateur de comprendre le futur proposé et ses fondements, sans nécessiter une chronologie prospective détaillée.

**2. Écrans concernés**

- Explorer — Onglet Scénario.

**3. Données mobilisées**

| Entité | Utilisation |
|---|---|
| **Futur** | Récupérer le titre, le récit fondateur, les informations de présentation et le statut de publication du futur. |
| **Signal prospectif** | Récupérer les signaux réels associés au futur, leur description, leur date et leurs références documentaires. |

**Précisions techniques :**

- Le scénario fondateur est enregistré dans l'entité Futur. Aucune table Scénario supplémentaire n'est nécessaire.
- Chaque signal prospectif est associé au futur concerné.
- Les signaux sont présentés directement dans l'onglet Scénario, sans développement d'une chronologie.

**Relation entre les données :**
- Un futur peut posséder plusieurs signaux prospectifs.
- Chaque signal prospectif appartient à un seul futur.
- Le scénario fondateur est directement associé à l'entité Futur : aucune entité Scénario distincte n'est nécessaire.
- Précision : dans le MVP, au moins trois signaux prospectifs documentés seront associés au futur publié et présentés directement dans l'onglet Scénario. Cette exigence relève du contenu à livrer, et non d'une cardinalité imposée à tous les futurs.

**4. Règles métier**

- Seuls les utilisateurs autorisés peuvent consulter le scénario d'un futur publié.
- Le scénario fondateur est préparé et validé avant sa publication.
- Le contenu du scénario est stocké et consultable sans génération IA à chaque ouverture.
- Chaque signal prospectif est associé à un futur.
- Chaque signal présenté doit disposer d'une source identifiable et consultable.
- Les signaux correspondent à des informations réelles et documentées. Ils doivent être clairement distingués du récit fictionnel.
- Le premier futur du MVP doit présenter au moins trois signaux documentés.
- La présentation chronologique des signaux et des événements fictionnels relève de F02.2, fonctionnalité optionnelle.

**5. Priorité**

**Critique — MVP obligatoire.**

**6. Critères d'acceptation**

- L'utilisateur peut accéder à l'onglet Scénario depuis l'Explorer.
- Il peut consulter l'intégralité du récit fondateur du futur sélectionné.
- Au moins trois signaux réels documentés sont visibles dans cet onglet.
- Chaque signal présente une description et une référence documentaire identifiable.
- L'utilisateur peut accéder aux sources associées aux trois signaux.
- Le récit fictionnel et les signaux réels sont clairement différenciés.
- Le contenu reste accessible après actualisation de la page, pour un utilisateur autorisé.
- Un utilisateur non autorisé ne peut pas consulter le scénario.
- Un professionnel de la stratégie ou de la prospective peut consulter le scénario et identifier les trois signaux sourcés en 10 minutes maximum lors d'un test.

**Objectif SMART associé :** Objectif 2 — Rendre les scénarios accessibles et crédibles (Claire).

**Objectif SMART également couvert :** Objectif 1 — Faciliter l'exploration des futurs (Thomas).

  <br>

### F02.2 — EXPLORER LA TRAJECTOIRE DU FUTUR

**1. Ce que l'utilisateur fait**

Depuis l'Explorer, l'utilisateur accède à l'onglet Trajectoire pour comprendre comment le monde actuel pourrait progressivement évoluer vers le futur imaginé.

Il parcourt une chronologie composée de deux types d'éléments :

- Des signaux prospectifs réels et documentés, permettant d'identifier les transformations déjà observables.
- Des événements fictionnels, représentant les ruptures et évolutions imaginées dans le scénario.

Cette représentation permet à l'utilisateur de comprendre les étapes possibles du basculement entre le présent et le futur exploré.

**2. Écrans concernés**

- Explorer — Onglet Trajectoire du futur.

**3. Données mobilisées**

| Entité | Utilisation |
|---|---|
| **Futur** | Identifier le futur auquel appartient la trajectoire. |
| **Signal prospectif** | Récupérer les signaux réels documentés, leurs dates et leurs sources. |
| **Événement fictionnel** | Récupérer les événements imaginés, leurs descriptions et leurs dates dans la chronologie. |

**Précisions techniques :**

- Chaque signal prospectif et chaque événement fictionnel est associé à un futur.
- Les signaux documentés peuvent être réutilisés entre l'onglet Scénario et la trajectoire, sans duplication de données.
- La trajectoire peut être construite à partir des dates et informations des signaux et événements, sans nécessiter une table Trajectoire supplémentaire.

**Relation entre les données**
- Un futur peut posséder plusieurs signaux prospectifs.
- Chaque signal prospectif appartient à un seul futur.
- Un futur peut posséder plusieurs événements fictionnels.
- Chaque événement fictionnel appartient à un seul futur.

Précision : les signaux prospectifs sont les mêmes données que celles mobilisées dans F02.1. Leur réutilisation dans la trajectoire ne nécessite pas de duplication ni de table Trajectoire supplémentaire.
L'entité Événement fictionnel et son exploitation dans une chronologie ne sont nécessaires que si la fonctionnalité optionnelle F02.2 est développée.

**4. Règles métier**

- Seuls les utilisateurs autorisés peuvent consulter la trajectoire d'un futur publié.
- Chaque signal prospectif et chaque événement fictionnel doit être associé à un futur.
- Les signaux prospectifs correspondent à des informations réelles et disposent de sources documentaires.
- Les événements fictionnels correspondent à des évolutions imaginées et ne doivent pas être présentés comme des faits.
- Les deux catégories d'éléments doivent être visuellement différenciées.
- Les éléments doivent être affichés dans un ordre chronologique cohérent.
- L'onglet Trajectoire n'est visible que si la fonctionnalité est effectivement développée et disponible.

**5. Priorité**

**Optionnelle — Si le temps le permet / Post-MVP.**

Cette fonctionnalité ne fait pas partie du périmètre obligatoire des six semaines.

Elle ne sera développée que si les fonctionnalités prioritaires sont terminées, testées et stabilisées.

Son absence ne doit pas empêcher le fonctionnement de l'Explorer ou la validation des objectifs SMART du MVP.

**6. Critères d'acceptation**

*Applicables uniquement si la fonctionnalité est développée.*

- L'utilisateur peut accéder à l'onglet Trajectoire depuis l'Explorer.
- Il peut parcourir les événements et signaux selon leur ordre chronologique.
- Les signaux réels et les événements fictionnels sont clairement différenciés.
- Chaque signal documenté dispose d'une source identifiable et consultable.
- Les éléments affichés correspondent au futur sélectionné.
- L'utilisateur peut revenir aux autres onglets sans perdre le futur en cours.
- Si la fonctionnalité n'est pas développée, aucun onglet Trajectoire inactif ou incomplet n'est affiché.

**Objectif SMART associé :** aucun objectif SMART obligatoire du MVP ne dépend de cette fonctionnalité.

<br>



### F03 - CONSULTER LES ARTEFACTS IMMERSIFS

**1. Ce que l'utilisateur fait**
- L'utilisateur consulte la bibliothèque d'artefacts associée au futur sélectionné.
- Il peut ouvrir différents documents fictionnels pour découvrir comment le scénario se manifeste dans la société, les organisations et les métiers.
- Dans le MVP, les artefacts prévus sont des articles, des témoignages écrits et un podcast.

**2. Écrans concernés**
- Explorer — Onglet Artefacts.
- Vue détaillée d'un artefact.
- Lecteur audio pour le podcast.

**3. Données mobilisées**
- Futur :	Identifier le futur auquel appartiennent les artefacts.
- Artefact :	Récupérer le titre, le contenu, le type, le statut de publication et les autres informations de l'artefact.
- Template d'artefact	: Identifier la structure attendue selon le format : article, témoignage ou podcast.
- Média :	Récupérer les illustrations, images principales ou fichiers audio associés aux artefacts.

**Relations entre les données :**
- Un futur peut contenir plusieurs artefacts.
- Chaque artefact appartient à un seul futur.
- Chaque artefact utilise un template.
- Un template peut être utilisé par plusieurs artefacts.
- Un artefact peut comporter plusieurs médias.
- Un média peut être réutilisé par plusieurs artefacts, conformément au modèle cible.
Point technique à préciser lors de la création de la base : la relation Artefact–Média devra être matérialisée par une table d'association si les médias sont effectivement mutualisés entre plusieurs artefacts. Cette table technique n'est pas une nouvelle fonctionnalité produit.

**4. Règles métier**
- Chaque artefact appartient obligatoirement à un futur.
- Chaque artefact utilise un template prédéfini.
- Les champs obligatoires dépendent du template.
- Un article doit comporter au minimum un titre, une image principale et un contenu textuel pour être publié.
- Un témoignage écrit doit comporter les informations requises par son template.
- Un podcast publié doit posséder un fichier audio exploitable.
- Les artefacts doivent être préparés et validés avant publication.
- Seuls les artefacts publiés sont visibles par les collaborateurs.
- Les artefacts déjà publiés sont stockés et consultables sans nouvelle génération IA.
- Le MVP prévoit cinq artefacts pour le premier futur.

**5. Priorité**
Critique — MVP obligatoire.

**6. Critères d'acceptation**
- L'utilisateur accède à la bibliothèque des cinq artefacts du premier futur
- Il peut identifier les différents formats proposés.
- Il peut ouvrir et consulter un article.
- Il peut ouvrir et lire un témoignage écrit.
- Il peut lancer, mettre en pause et reprendre la lecture du podcast.
- Les illustrations et médias associés s'affichent correctement.
- Les artefacts affichés correspondent au futur sélectionné.
- Les artefacts en brouillon ne sont pas accessibles aux collaborateurs.
- La consultation d'un artefact ne déclenche aucun appel de génération IA.

<br>


## F04 - CONSIGNER SES ETONNEMENTS

**1. Ce que l'utilisateur fait**
Pendant l'exploration d'un futur, l'utilisateur peut rédiger une réflexion personnelle dans son carnet d'étonnement.
Il peut enregistrer une note libre ou la rattacher à un élément précis du futur : un artefact, un signal prospectif ou un événement fictionnel.
Il retrouve ensuite ses notes, peut les relire, les modifier ou les supprimer.

**2. Écrans concernés**
- Explorer — Onglet Carnet d'étonnement.
- Interface de création d'une note.
- Interface de consultation et de modification d'une note.

**3. Données mobilisées**
- Utilisateur :	Identifier l'auteur de la note.
- Futur :	Identifier le futur auquel appartient la note.
- Note d'étonnement : 	Enregistrer le contenu de la note, ses dates et ses associations éventuelles.
- Artefact :	Identifier un artefact auquel une note peut être rattachée.
- Signal prospectif :	Identifier un signal auquel une note peut être rattachée.
- Événement fictionnel :	Identifier un événement auquel une note peut être rattachée.

Relations entre les données :
- Un utilisateur peut posséder plusieurs notes d'étonnement.
- Chaque note appartient obligatoirement à un utilisateur.
- Un futur peut posséder plusieurs notes d'étonnement.
- Chaque note appartient obligatoirement à un futur.
- Une note peut être associée à un artefact, un signal ou un événement fictionnel.
- L'association à un contenu précis est facultative.
Précision : aucune table supplémentaire « Contribution » n'est nécessaire.
Dans le modèle cible, l'entité Note d'étonnement possède également une association facultative à Campagne. Cette association n'est pas utilisée dans le MVP.

**4. Règles métier**
- Chaque note possède obligatoirement un auteur et un futur.
- Une note peut être créée sans rattachement à un artefact, un signal ou un événement.
- Une note ne peut être rattachée qu'à un seul type de contenu source à la fois dans le modèle actuel.
- Le contenu associé doit appartenir au même futur que la note.
- Les notes sont personnelles.
- Un utilisateur ne peut consulter, modifier ou supprimer que ses propres notes.
- Les notes sont enregistrées dans Supabase.
- Les notes doivent rester accessibles après déconnexion et reconnexion.
- Les campagnes et les synthèses collectives ne sont pas disponibles dans le MVP.

**5. Priorité**
Critique — MVP obligatoire.

**6. Critères d'acceptation**
- L'utilisateur peut créer une note d'étonnement.
- Il peut enregistrer une note sans la rattacher à un contenu particulier.
- Il peut créer une note associée à un artefact, un signal ou un événement.
- La note est correctement enregistrée dans Supabase.
- Après reconnexion, l'utilisateur retrouve ses notes.
- Il peut modifier une note existante.
- Il peut supprimer une note.
- Le carnet n'affiche que les notes de l'utilisateur connecté.
- Un utilisateur ne peut pas consulter les notes personnelles d'un autre utilisateur, y compris en manipulant directement une requête.

<br>


### F05 - INTERROGER UN FUTUR GRACE A L'AGENT CONVERSATIONNEL IA

1. Ce que l'utilisateur fait
Pendant son exploration, l'utilisateur peut ouvrir un agent conversationnel pour poser des questions sur le futur sélectionné.
Il peut demander des précisions sur le scénario, approfondir les conséquences d'un événement ou explorer les implications possibles du futur sur son environnement professionnel.
Il peut poursuivre la discussion en posant des questions complémentaires.

**2. Écrans concernés**
- Interface de l'agent conversationnel, accessible depuis l'Explorer.
- Zone de saisie des questions.
- Zone d'affichage des réponses et de l'échange en cours.

**3. Données mobilisées**
- Entité du MCD	Utilisation dans la fonctionnalit
- Utilisateur : Identifier l'utilisateur qui interroge l'agent.
- Organisation : Identifier son organisation et son périmètre d'accès.
- Contexte métier : Fournir les informations organisationnelles autorisées nécessaires à la contextualisation des réponses.
- Futur	: Fournir le scénario fondateur et les caractéristiques du monde fictionnel.
- Signal : prospectif	Fournir les éléments réels et documentés qui servent d'ancrage au scénario.
- Événement fictionnel :	Fournir les événements composant la trajectoire du futur.
- Artefact :	Fournir le contenu textuel des artefacts publiés et les informations utiles à leur compréhension.

Cas particulier : Conversation IA et Message
Ces deux entités figurent dans le MCD cible, mais leur mode de stockage définitif n'a pas encore été arrêté.

**Deux approches restent possibles :**
- Conserver les échanges dans des tables de FUTURES, dans Supabase.
- Utiliser les mécanismes de conversation proposés par le fournisseur IA, selon les conditions et paramètres de conservation retenus.
Pour le MVP, l'obligation fonctionnelle consiste à maintenir le contexte nécessaire à l'échange en cours. La conservation permanente de toutes les conversations n'est pas exigée.
Précision : l'API OpenAI est un service externe, pas une table Supabase. De même, le prompt système et les règles de comportement de l'agent relèvent de sa configuration, et non d'une nouvelle entité métier obligatoire.

**4. Règles métier**
- L'utilisateur doit être authentifié et autorisé à consulter le futur concerné.
- L'agent reçoit uniquement les informations autorisées pour cet utilisateur et son organisation.
- L'agent utilise le scénario et les contenus publiés du futur sélectionné.
- Il peut s'appuyer sur le contexte métier autorisé de l'organisation.
- Il distingue les faits réels documentés, les éléments fictionnels et les extrapolations qu'il propose.
- Il peut approfondir les implications du scénario, mais ne modifie pas les contenus publiés.
- Il ne crée pas de nouveaux artefacts dans la bibliothèque.
- Les documents stratégiques confidentiels sont exclus de cette première version.
- Les appels à l'API OpenAI passent par un environnement serveur sécurisé.
- Les clés API ne sont jamais exposées dans le navigateur.
- En cas d'indisponibilité de l'API, les autres fonctionnalités de l'Explorer restent accessibles.
- Le maintien d'un échange ne nécessite pas obligatoirement un historique permanent des conversations.

**5. Priorité**
Critique — MVP obligatoire, notamment pour satisfaire l'exigence d'intégration d'une fonctionnalité IA.

**6. Critères d'acceptation**
- L'utilisateur peut ouvrir l'agent conversationnel depuis l'Explorer.
- Il peut envoyer une question.
- L'agent renvoie une réponse en s'appuyant sur le contexte du futur sélectionné.
- L'utilisateur peut poser une question complémentaire en conservant le contexte de l'échange.
- L'agent peut répondre à une question portant sur un événement ou un artefact publié.
- Lorsqu'il formule une extrapolation, l'agent ne la présente pas comme un fait établi.
- L'agent ne peut pas récupérer de contenus non autorisés.
- Les clés API ne sont pas visibles dans le code exécuté par le navigateur.
- En cas d'erreur de l'API, un message compréhensible est affiché.
  
<br>

