# Les Fondements Des Microservices

En tant que responsable d'un site web, vous devez vous assurer qu'il est parfaitement optimisé pour les moteurs de recherche. Grâce à cette formation de Youssef Jlidi, les crawlers et analyseurs de logs n'auront plus de secrets pour vous. Après avoir abordé les bases et les principes des sites Internet, des moteurs de recherche et du SEO, vous procéderez à la mise en place de crawlers, qui simulent le passage de robots dans la structure de votre site, et d'analyseurs de logs, et vont observer le comportement du moteur de recherche Google dans vos pages web. Cela vous permettra d'effectuer des analyses et d'améliorer votre stratégie de communication sur Internet.

## Programme De La Formation
### Aperçu Historique Des Microservices
![apercus](images/historiquems.png)
### Concepts Clés Des Microservices
![concept](images/conceptcles.png)
### Concepts Avancés
![conceptavance](images/conceptsavance.png)
### Choix En Matière D'Architecture
![choix](images/choix.png)

## Etablir Les Prérequis
### Managers
Que vous soyez managers ou decideurs dans le cycle de vie d'une équipe de développement logiciel, nous allons dans cette formation:
![manager](images/managers.png)

### Architectes
Si vous êtes architectes cette formation constituera un excellent point de depart et vous permettra d'acquerir des bases solide  pour prendre des décisions:
![architectes](images/architectes.png)
### Développeurs
Si vous êtes développeurs, cette formation vous donnera de très bonnes bases pour expliquer pourquoi vous codez comme vous le faits:
![developpeurs](images/developpeurs.png)

Pour suivre cette formation:
* il faut simplement avoir envie d'apprendre 
* connaître les base du développement logiciel
* en tant que développeur ou architectes, vous devez connaître la composition et la décomposition logiciel
* vous devez comprendre les principes de la communication à distance via le protocole **HTTP** et **HTTPS** afin de cerner certaines des complexités des architectures **microservices**

## Explorer L'Historique Des Architectures Basées Sur Les Services
### Architeture Monolithique
Avec les architectures monolithique, il faut créer un artefact constitué en trois (3) couches en générales(Présentation, Processus métier, Accèss aux données), souvent chaque couche se décompose en des sous couches par exemple pour la couche **accès aux données**(Façade, traitement, Entrée-sortie), cela permet de separer le problème et de décomposer le code en composant fonctionnel. Autre que ces problème avec les applications monolithiques il ya un problème de couplage fort, leurs conceptions prennent assez de temps et le test peut paraître parfois trop penible.
![monolitque](images/monolitique.png)

### Architecture De Service
Puis nous avons aussi l'avènement des architectures de service notamment des architectures orientées services(SOA) qui permettent de décomposer  les applications en plus petits modules mais génerent des nouveaux problèmes la technologie de service web repose sur le protocole SOAP ce qui provoque de nouveaux problèmes, chaque réponse est 200(OK) ou 500(Erreur interne) en plus le problème de couche d'agregation car les transformation du XML et les opérations logiques étaient rajoutées aux **Bus SOA** cela crée un nouveau niveau de couplage cependant la **SOA** s'était imposée à un moment donnée de l'histoire.
![servicesoa](images/archservice1.png)
![servicesoa](images/archservice2.png)
  

### Microservices
Les microservices offrent un Framework plus agile qui peut être étendu dans un environnement Cloud Natif beaucoup plus facilement que les applications  monolithique  ou SOA.
Ce modèle convient mieux aux développeur web et aux développeurs des services web car ils reposent sur le protocole **HTTP**
![microservice](images/microservice.png)

## Microservices
### Définition
Les microservices constituent la décomposition d'un problème logiciel en plus petits problèmes, plus facile à comprendre et à résoudre, mais ils servent aussi à faire en sorte que l'architecture au niveau des composants fonctionne de la même manière que les bonnes pratiques de développment avec la modularisation du code. Face un problème logiciel, nous savons qu'il faut décomposer le problème en plus petits problèmes pour résoudre chacun de ces problèmes de façon modulaire et découplé. Les microservices reprennent ce problèmes et l'appliquent à l'ensemble du système. 
![microservices](images/microservice2.png)
Les microservices utilisent l'interopérabilité héterogene basée sur l'adaptation au protocole pour gerer les comminucations ainsi:
![microservices](images/microservice3.png)
![microservices](images/microservice4.png)

## Distinguer Microservice Et Cloud Natif
### Architecture Cloud Natif
Les architectures Cloud Natifs réposent sur la méthodologie de création d'application à 12 facteurs.
Les architectures cloud natifs incluent des modèles pour créer des systèmes s'exécutant dans une infrastructure cloud.
#### Infrastructure Cloud 
les infrastructure cloud peuvent être:
![infrastructure](images/infrastructurecloud.png)
Le cloud computing est un modèle de système distribuer à l'echelle mondiale qui maximise la disponibilité, évolutivité et distribution. Nous pouvons créer des systèmes cloud s'exécutant dans un seul data center et prevoir de les étendre.
Les microservices s'intègrent très bien trop souvent dans une architecture cloud natif car ils constituent une transition très fluide vers une application à 12 facteurs. ils sont deux facteurs très différents.
Nous pouvons créer des applications cloud monolithique et des application microservices incapables de migrer dans le cloud. Trop souvent les gens confondent les deux modèles.
Mais malgré leurs différences ces deux modèles vont souvent de pairs
### Applications De Microservices Cloud Natives
![mservice](images/mservice.png)

## Différencier Les Services
Avec les microservices toutes les comminucations entre les services fonctionnent avec le REST à l'aide du protocole HTTP, il y a d'autre méthode base sur  la notion d'évènement, mais les appels intra-service répose tous sur  le REST.
![rest](images/restmicroservice.png)
### Service
Avec les microservices, un service fonctionne sur un domaine bien défini, les opérations sont définis sur  le domaine et non sur les objets métiers. 
![service](images/service.png)
Dans une architecture de microservice il faut fornir des services de très bon niveaux, souvent ses services exposent des opérations GRUD spécifique à un domaine sur l'objet de domaine, mais ce domaine peut couvrir plusieurs domaines.
![domaine](images/domaine.png)
### Blocage De Conception De Service
![blocage](images/blocage.png)

## Aborder La Danse De La Communication
![communication](images/communication.png)
### Interopérabilité Hétérogène Basée Sur L'Adaptation Aux Protocoles
![interoperabilite](images/interoperabilite.png)

### Avantages
![avantage](images/avantage.png)
### Problème
![probleme](images/probleme.png)
### Solution 
Chaque service doit maintenir un certain niveau de passivité dans ces API pour éviter les defaillances dans ces systèmes, un service pouvant appeler n'import lequel de ces services, il n'y a pas de delimitation claire qui vous appelle, nous devons avoir une solide stratégie de gestion de version de API passive pour que les système d'appelles ne tombent pas en panne lors de la publication d'une nouvelle version d'API.
![api](images/gestionversion.png)

## Examiner La Distribution Et L'Evolutivité
![distr](images/distr.png)
### Besoins Liés A Internet Du Point De Vue De L'Entreprise
![besoin](images/besoin1.png)
### Avantage
* évolutivité 
* distribution
* scalabilité

## Anticiper Les Danger De La Latence  Et L'Engorgement
### La Latence
La latence peut devenir intolérable dans une architectiure microservice
![latence](images/latence.png)

### Appels Circulaire
Les appels circulaire peuvent devenir problématiques.
![appelcirculaire](images/appelcirculaire.png)
Avant de passer à une architecture nous devons penser aux problèmes de latence.
## Définir Le Context Délimité
### Modèle De Conception
![modeleconception](images/modeleconception.png)
![delimiter](images/delimiter.png)

## Observer Les Limites Des Domaines De Données
### Limites Trasactionnelles
![limitetransactionnelle](images/limitetransactionnelle.png)
![msservice](images/basemicroservices.png)
Si vous travaillez sur une couche d'API
![coucheapi](images/coucheapi.png)

## Découvrir Les Pertes Des Transactions Atomiques
![proprietet](images/proprieteacidet.png)
![atomique](images/atomique.png)
![coherente](images/coherente.png)
![isolee](images/isolee.png)
![durable](images/durable.png)

Dans une architecture monolithique ces opérations bien respectés par contre dans une architecture microservice, ces opérations sont presque inexistantes à la place: 
![cherchons](images/cherchons.png)

Mais il y a des moment où nous avons réellement besoins des transactions ACID par exemple pour les applications bançaire où les débits et les crédits doivent se produire dans une seule transaction bancaire.
![transactionbancaire](images/transactionbancaire.png)

## Etudier La Couche API
La couche API est un proxi agréger toutes nos offres de service
![coucheapi2](images/coucheapi2.png)
![coucheapi3](images/coucheapi3.png)

## Aborder Les Communication Asynchrones
![comasync1](images/comasync1.png)
![comasync2](images/comasync2.png)
![comasync3](images/comasync3.png)
## Enregistrer Et Tracer Dans Une Architecture De Microservices
![tracer](images/tracer.png)
![journaliser](images/journaliser.png)
Le traçage consiste à créer un jeton unique appeler trace à utiliser cette trace dans tous les évènements de journalisation interne cette pile d'appelle en intégrant cette valeur à tous les résultats de journalisation et  de minitage pour tous les services concernés pour faciliter la journalisation.
![tracage](images/tracage.png)
## Comprendre L'Importance De La Livraison Livraison Continue 
### Livraison Continue
![livraisoncontinue](images/livraisoncontinue.png)
### CI/CD
![cicd](images/cicd.png)
#### CD Hors Production
![cd](images/cd.png)

#### CD Production
Une fois l'artefact valider, il sera deployer automatiquement
![deployer](images/cda.png)
![la](images/livraisoncontinueta.png)
## Connaître Quelques Architectures Hybrides Viables
### Architecture Hybride De Service
![archhy](images/archhybride.png)
#### Architecture N-tiers Hybrides
Dans le modèle hiérarchique n-tiers, nous pouvons définir différentes classes de services:
* le service de données est une classe commune qui expose la logique des données spécifique au domaine au monde exterieur
* le service des processus métier constitue une autre classe commune qui définie precisement des processus métiers de haut niveau
* nous pouvons également definir des services de passerelles qui créent des abstractions vers des dépendances externes
* et enfin nous pouvons definir des services edges qui exposent nos données et nos processus métiers aux monde exterieurs 
* une fois que nous avons une taxonomie claire, nous pouvons definir des règles sur ce que les services peuvent consommer, etudier les risques liés aux appels circulaires et interdire qu'un service appel aun autre service de donnée sans être impliqué dans un processus métier. La consommation de service de passerelle intervient aussi via les même processus métier et non entre eux.
![ntierhybride](images/ntierhybride.png)

### Architecture De Services
![architecturedeservice](images/architecturedeservice.png)
![architecturedeservice](images/architecturedeservice2.png)

## Parcourir Les Considérations Relatives A La Conception
Pour concevoir une architecture microservice voici quelques points essentiels à tenir compte:
![point1](images/point1.png)
![point2](images/point2.png)
* Concernant le code nous devons envisager de tirer parti de la conception piloter le domaine
* nous devons effectuer une véritable analyse de l'ensemble du système et utiliser ces connaissances pour développer nos services
* nous devons reflichir à la création de nos services et à la fonction qu'ils vont exécuter
* nous devons également penser si nous allons exploiter des services de données dédiers ou intégrer les données dans les processus métiers
* devrions-nous intégrer les services ensembles pour obtenir les transactions avec leur propriétés ACID là où cela est requis ou devrions-nous élaborer des stratégie basée sur la cohérence eventuelle des données

### Conception Des Mécanismes Pour Contrôler La Latence
![mecanisme](images/conceptiondemecanisme.png)
Beaucoup de développeur n'aime entendre la standardisation, mais les équipes qui réussent le mieux avec les architectures de microservices ont opté pour la standardisation.
La standardisation permet de deplacer les ressources plus facilement en fonction de l'évolution des besoins métiers, de plus au depart concevons nos systèmes de manière asynchrône. Essyons de créer chaque service avec des opérations asynchrônes jusqu'à ce qu'il soit aprouvé que nous en avons besoins des opérations synchrônes.

## Discerner Les Compromis
### Payer La &lt;&lt;Distribution Tax &gt;&gt; Offre Plusieurs Avantages
![distributionTax](images/distributiontax.png)
Prenons le cas d'amaazone qui opère à l'echelle mondiale et qui clairement ateint une pic d'activité à la veille de la fête de paque il serait quasiment impossible pour elle de gerer son système dans le cadre d'un deployement monolithique. Elle gere la **distribution tax** modèle hautement disponible qui constitue un avantage evident pour operer à l'echelle mondiale.
### Problèmes Liés A La Complexité
![complexite](images/complexite.png)
### Pratiques De Développement Polyglotte
![polyglotte](images/polyglotte.png)
Le développement polyglotte s'accompagne avec une complication de la gestion des service en production.

## Voir Les Avantages Des Services De Pointe
![servicepointe](images/servicepoint.png)
### Services Edges Sortants
![servicesedgesortant](images/serviceedgesortant.png)
![edge](images/edge2.png)
### Services Edges Entrantes / De Traduction
![serviceedgeentrante](images/serviceedgeentrant.png)
![edge](images/edge.png)

#### Avantages D'un service Edge
![avanatege](images/avantageedge.png)