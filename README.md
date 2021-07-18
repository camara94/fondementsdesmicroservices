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