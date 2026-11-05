PRD : SPECIFICATIONS DES 5 FONCTIONNALITES PRINCIPALES DU MVP FUTURES
F01 - AUTHENTIFICATION ET ACCES A UN FUTUR

1. Ce que l'utilisateur fait
L'utilisateur se connecte à FUTURES avec ses identifiants personnels.
Après authentification, il accède à la page d'accueil et visualise les futurs auxquels il est autorisé à accéder.
Dans le cadre du MVP, un seul futur est disponible. L'utilisateur peut le sélectionner pour entrer dans l'espace Explorer.
2. Écrans concernés
•	Page de connexion.
•	Page d'accueil présentant le futur disponible.
•	Interface Explorer après sélection du futur.
3. Données mobilisées
Entité du MCD	Utilisation dans la fonctionnalité
Utilisateur	Identifier l'utilisateur connecté, son statut et son organisation de rattachement.
Organisation	Identifier l'organisation de l'utilisateur et son périmètre d'accès.
Rôle	Déterminer les rôles existants : Collaborateur, Responsable habilité, Administrateur d'organisation et Super Administrateur.
Attribution de rôle	Identifier le ou les rôles attribués à l'utilisateur.
Permission	Déterminer les actions autorisées en fonction des rôles attribués.
Futur	Récupérer les informations du futur à afficher : titre, description, illustration et statut de publication.
Relations techniques à prévoir :
•	Utilisateur est relié à Organisation par un identifiant d'organisation.
•	Attribution de rôle relie un utilisateur à un rôle.
•	Les rôles sont reliés aux permissions via une association rôle–permission.
•	L'accès d'une organisation à un futur repose sur la relation Organisation–Futur définie dans le MCD cible. Cette relation plusieurs-à-plusieurs nécessitera une table d'association lors de sa traduction dans Supabase.
Précision : Supabase Auth assure l'authentification technique. L'entité Utilisateur conserve les informations métier du compte et référence l'identité authentifiée. Il n'est pas nécessaire de créer une seconde gestion des mots de passe.
4. Règles métier
•	L'utilisateur doit être authentifié pour accéder aux espaces protégés de FUTURES.
•	Chaque utilisateur standard appartient à une seule organisation.
•	Un utilisateur disposant du rôle global Super Administrateur peut ne pas être rattaché à une organisation.
•	Les rôles sont attribués aux utilisateurs via l'entité Attribution de rôle.
•	Les droits d'accès sont déterminés par les rôles, les permissions et le périmètre organisationnel.
•	Seuls les futurs publiés et autorisés sont accessibles aux collaborateurs.
•	Un utilisateur ne peut pas modifier ses propres habilitations.
•	Les contrôles d'accès doivent être appliqués côté serveur et dans Supabase, et pas uniquement dans les interfaces.
5. Priorité
Critique — MVP obligatoire.
6. Critères d'acceptation
•	Un utilisateur possédant un compte actif peut se connecter avec ses identifiants.
•	Après connexion, il accède à la page d'accueil.
•	Il visualise le futur publié auquel son organisation a accès.
•	Il peut sélectionner ce futur et accéder à l'Explorer.
•	Un utilisateur non authentifié ne peut pas consulter les contenus protégés.
•	Un utilisateur non autorisé ne peut pas accéder à un futur, même en utilisant directement son URL.
•	Les rôles attribués sont correctement pris en compte dans les autorisations.








F02 - EXPLORER LE SCENARIO ET SA TRAJECTOIRE PROSPECTIVE

1. Ce que l'utilisateur fait
Depuis l'Explorer, l'utilisateur découvre le scénario fondateur d'un futur.
Il peut consulter les caractéristiques du monde fictionnel, comprendre les principales ruptures envisagées et parcourir une chronologie reliant les signaux réels du présent aux événements imaginés.
L'utilisateur peut ainsi comprendre comment le monde fictionnel présenté aurait pu émerger.
2. Écrans concernés
•	Explorer — Onglet Scénario.
•	Explorer — Onglet Trajectoire du futur.
3. Données mobilisées
Entité du MCD	Utilisation dans la fonctionnalité
Futur	Récupérer le scénario fondateur, ses informations de présentation et son statut de publication.
Signal prospectif	Afficher les signaux réels documentés associés au futur.
Événement fictionnel	Afficher les événements imaginés qui composent la trajectoire du futur.
Relations entre les données :
•	Un futur peut posséder plusieurs signaux prospectifs.
•	Chaque signal prospectif appartient à un futur.
•	Un futur peut posséder plusieurs événements fictionnels.
•	Chaque événement fictionnel appartient à un futur.
Le scénario fondateur est porté par l'entité Futur dans le modèle retenu. Aucune table supplémentaire n'est créée uniquement pour afficher le scénario.
4. Règles métier
•	Chaque signal et chaque événement fictionnel est obligatoirement rattaché à un futur.
•	Les signaux prospectifs correspondent à des faits ou tendances réels et documentés.
•	Chaque signal publié doit disposer d'une source identifiable.
•	Les événements fictionnels représentent des hypothèses d'évolution et ne doivent pas être présentés comme des faits réels.
•	La distinction entre informations documentées et fictionnelles doit être clairement visible.
•	Les éléments de la trajectoire doivent pouvoir être présentés dans un ordre chronologique cohérent.
•	Les collaborateurs ne consultent que les contenus publiés du futur auquel ils ont accès.
•	Un futur en préparation peut ne pas encore posséder de signaux ou d'événements. Ses conditions de publication sont définies séparément.
5. Priorité
Critique — MVP obligatoire.
6. Critères d'acceptation
•	L'utilisateur peut consulter le scénario fondateur du futur.
•	Il peut accéder à la trajectoire depuis l'Explorer.
•	Les signaux réels et les événements fictionnels sont visuellement différenciés.
•	Il peut identifier la source et la date documentaire des signaux lorsque ces informations sont disponibles.
•	Les liens de source renseignés peuvent être ouverts.
•	Les événements apparaissent selon l'ordre chronologique prévu.
•	L'utilisateur peut passer du scénario à la trajectoire sans perdre le futur sélectionné.
•	Aucun contenu non publié n'est accessible à un collaborateur standard.















F03 - CONSULTER LES ARTEFACTS IMMERSIFS

1. Ce que l'utilisateur fait
L'utilisateur consulte la bibliothèque d'artefacts associée au futur sélectionné.
Il peut ouvrir différents documents fictionnels pour découvrir comment le scénario se manifeste dans la société, les organisations et les métiers.
Dans le MVP, les artefacts prévus sont des articles, des témoignages écrits et un podcast.
2. Écrans concernés
•	Explorer — Onglet Artefacts.
•	Vue détaillée d'un artefact.
•	Lecteur audio pour le podcast.
3. Données mobilisées
Entité du MCD	Utilisation dans la fonctionnalité
Futur	Identifier le futur auquel appartiennent les artefacts.
Artefact	Récupérer le titre, le contenu, le type, le statut de publication et les autres informations de l'artefact.
Template d'artefact	Identifier la structure attendue selon le format : article, témoignage ou podcast.
Média	Récupérer les illustrations, images principales ou fichiers audio associés aux artefacts.
Relations entre les données :
•	Un futur peut contenir plusieurs artefacts.
•	Chaque artefact appartient à un seul futur.
•	Chaque artefact utilise un template.
•	Un template peut être utilisé par plusieurs artefacts.
•	Un artefact peut comporter plusieurs médias.
•	Un média peut être réutilisé par plusieurs artefacts, conformément au modèle cible.
Point technique à préciser lors de la création de la base : la relation Artefact–Média devra être matérialisée par une table d'association si les médias sont effectivement mutualisés entre plusieurs artefacts. Cette table technique n'est pas une nouvelle fonctionnalité produit.
4. Règles métier
•	Chaque artefact appartient obligatoirement à un futur.
•	Chaque artefact utilise un template prédéfini.
•	Les champs obligatoires dépendent du template.
•	Un article doit comporter au minimum un titre, une image principale et un contenu textuel pour être publié.
•	Un témoignage écrit doit comporter les informations requises par son template.
•	Un podcast publié doit posséder un fichier audio exploitable.
•	Les artefacts doivent être préparés et validés avant publication.
•	Seuls les artefacts publiés sont visibles par les collaborateurs.
•	Les artefacts déjà publiés sont stockés et consultables sans nouvelle génération IA.
•	Le MVP prévoit cinq artefacts pour le premier futur.
5. Priorité
Critique — MVP obligatoire.
6. Critères d'acceptation
•	L'utilisateur accède à la bibliothèque des cinq artefacts du premier futur.
•	Il peut identifier les différents formats proposés.
•	Il peut ouvrir et consulter un article.
•	Il peut ouvrir et lire un témoignage écrit.
•	Il peut lancer, mettre en pause et reprendre la lecture du podcast.
•	Les illustrations et médias associés s'affichent correctement.
•	Les artefacts affichés correspondent au futur sélectionné.
•	Les artefacts en brouillon ne sont pas accessibles aux collaborateurs.
•	La consultation d'un artefact ne déclenche aucun appel de génération IA.









F04 - CONSIGNER SES ETONNEMENTS
1. Ce que l'utilisateur fait
Pendant l'exploration d'un futur, l'utilisateur peut rédiger une réflexion personnelle dans son carnet d'étonnement.
Il peut enregistrer une note libre ou la rattacher à un élément précis du futur : un artefact, un signal prospectif ou un événement fictionnel.
Il retrouve ensuite ses notes, peut les relire, les modifier ou les supprimer.
2. Écrans concernés
•	Explorer — Onglet Carnet d'étonnement.
•	Interface de création d'une note.
•	Interface de consultation et de modification d'une note.
3. Données mobilisées
Entité du MCD	Utilisation dans la fonctionnalité
Utilisateur	Identifier l'auteur de la note.
Futur	Identifier le futur auquel appartient la note.
Note d'étonnement	Enregistrer le contenu de la note, ses dates et ses associations éventuelles.
Artefact	Identifier un artefact auquel une note peut être rattachée.
Signal prospectif	Identifier un signal auquel une note peut être rattachée.
Événement fictionnel	Identifier un événement auquel une note peut être rattachée.
Relations entre les données :
•	Un utilisateur peut posséder plusieurs notes d'étonnement.
•	Chaque note appartient obligatoirement à un utilisateur.
•	Un futur peut posséder plusieurs notes d'étonnement.
•	Chaque note appartient obligatoirement à un futur.
•	Une note peut être associée à un artefact, un signal ou un événement fictionnel.
•	L'association à un contenu précis est facultative.
Précision : aucune table supplémentaire « Contribution » n'est nécessaire.
Dans le modèle cible, l'entité Note d'étonnement possède également une association facultative à Campagne. Cette association n'est pas utilisée dans le MVP.
4. Règles métier
•	Chaque note possède obligatoirement un auteur et un futur.
•	Une note peut être créée sans rattachement à un artefact, un signal ou un événement.
•	Une note ne peut être rattachée qu'à un seul type de contenu source à la fois dans le modèle actuel.
•	Le contenu associé doit appartenir au même futur que la note.
•	Les notes sont personnelles.
•	Un utilisateur ne peut consulter, modifier ou supprimer que ses propres notes.
•	Les notes sont enregistrées dans Supabase.
•	Les notes doivent rester accessibles après déconnexion et reconnexion.
•	Les campagnes et les synthèses collectives ne sont pas disponibles dans le MVP.
5. Priorité
Critique — MVP obligatoire.
6. Critères d'acceptation
•	L'utilisateur peut créer une note d'étonnement.
•	Il peut enregistrer une note sans la rattacher à un contenu particulier.
•	Il peut créer une note associée à un artefact, un signal ou un événement.
•	La note est correctement enregistrée dans Supabase.
•	Après reconnexion, l'utilisateur retrouve ses notes.
•	Il peut modifier une note existante.
•	Il peut supprimer une note.
•	Le carnet n'affiche que les notes de l'utilisateur connecté.
•	Un utilisateur ne peut pas consulter les notes personnelles d'un autre utilisateur, y compris en manipulant directement une requête.








F05 - INTERROGER UN FUTUR GRACE A L'AGENT CONVERSATIONNEL IA
1. Ce que l'utilisateur fait
Pendant son exploration, l'utilisateur peut ouvrir un agent conversationnel pour poser des questions sur le futur sélectionné.
Il peut demander des précisions sur le scénario, approfondir les conséquences d'un événement ou explorer les implications possibles du futur sur son environnement professionnel.
Il peut poursuivre la discussion en posant des questions complémentaires.
2. Écrans concernés
•	Interface de l'agent conversationnel, accessible depuis l'Explorer.
•	Zone de saisie des questions.
•	Zone d'affichage des réponses et de l'échange en cours.
3. Données mobilisées
Entité du MCD	Utilisation dans la fonctionnalité
Utilisateur	Identifier l'utilisateur qui interroge l'agent.
Organisation	Identifier son organisation et son périmètre d'accès.
Contexte métier	Fournir les informations organisationnelles autorisées nécessaires à la contextualisation des réponses.
Futur	Fournir le scénario fondateur et les caractéristiques du monde fictionnel.
Signal prospectif	Fournir les éléments réels et documentés qui servent d'ancrage au scénario.
Événement fictionnel	Fournir les événements composant la trajectoire du futur.
Artefact	Fournir le contenu textuel des artefacts publiés et les informations utiles à leur compréhension.
Cas particulier : Conversation IA et Message
Ces deux entités figurent dans le MCD cible, mais leur mode de stockage définitif n'a pas encore été arrêté.
Deux approches restent possibles :
•	Conserver les échanges dans des tables de FUTURES, dans Supabase.
•	Utiliser les mécanismes de conversation proposés par le fournisseur IA, selon les conditions et paramètres de conservation retenus.
Pour le MVP, l'obligation fonctionnelle consiste à maintenir le contexte nécessaire à l'échange en cours. La conservation permanente de toutes les conversations n'est pas exigée.
Précision : l'API OpenAI est un service externe, pas une table Supabase. De même, le prompt système et les règles de comportement de l'agent relèvent de sa configuration, et non d'une nouvelle entité métier obligatoire.
4. Règles métier
•	L'utilisateur doit être authentifié et autorisé à consulter le futur concerné.
•	L'agent reçoit uniquement les informations autorisées pour cet utilisateur et son organisation.
•	L'agent utilise le scénario et les contenus publiés du futur sélectionné.
•	Il peut s'appuyer sur le contexte métier autorisé de l'organisation.
•	Il distingue les faits réels documentés, les éléments fictionnels et les extrapolations qu'il propose.
•	Il peut approfondir les implications du scénario, mais ne modifie pas les contenus publiés.
•	Il ne crée pas de nouveaux artefacts dans la bibliothèque.
•	Les documents stratégiques confidentiels sont exclus de cette première version.
•	Les appels à l'API OpenAI passent par un environnement serveur sécurisé.
•	Les clés API ne sont jamais exposées dans le navigateur.
•	En cas d'indisponibilité de l'API, les autres fonctionnalités de l'Explorer restent accessibles.
•	Le maintien d'un échange ne nécessite pas obligatoirement un historique permanent des conversations.
5. Priorité
Critique — MVP obligatoire, notamment pour satisfaire l'exigence d'intégration d'une fonctionnalité IA.
6. Critères d'acceptation
•	L'utilisateur peut ouvrir l'agent conversationnel depuis l'Explorer.
•	Il peut envoyer une question.
•	L'agent renvoie une réponse en s'appuyant sur le contexte du futur sélectionné.
•	L'utilisateur peut poser une question complémentaire en conservant le contexte de l'échange.
•	L'agent peut répondre à une question portant sur un événement ou un artefact publié.
•	Lorsqu'il formule une extrapolation, l'agent ne la présente pas comme un fait établi.
•	L'agent ne peut pas récupérer de contenus non autorisés.
•	Les clés API ne sont pas visibles dans le code exécuté par le navigateur.
•	En cas d'erreur de l'API, un message compréhensible est affiché.

