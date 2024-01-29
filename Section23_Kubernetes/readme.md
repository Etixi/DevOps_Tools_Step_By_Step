# Presentation De Kubernetes

+ Nous avons vu jusqu'à présent dans le chapitre `Docker` que nous pouvons créer et exécuter des conteneurs sur l'hôte `Docker`.
+ C'est tellement cool, c'est léger, rapide et livrable, mais qu'en est-il de la production.
+ Pouvons-nous exécuter nos applications sur ces conteneurs légers ou, plus spécifiquement, vous demander d'exécuter tous ces conteneurs sur un seul hôte ?
+ La réponse est qu'il n'est pas prudent de mettre tous ses œufs dans le même panier.
+ Nous avons donc besoin d'un `cluster d'hôtes Docker`, qui peut être géré par une application externe.
+ Quelque chose qui puisse planifier des `conteneurs` pour nous sur l'hôte le mieux approprié du `cluster`.
+ Il devrait également détecter un `conteneur` défaillant et résoudre le problème pour nous.
+ Nous recherchons donc un `outil d'orchestration Docker`.

![Alt Text](C:\DevOps_Tools_Step_By_Step\Section23_Kubernetes\images\image1.jpeg)

+ Nous disposons de peu `d'outils d'orchestration Docker et de services cloud` sur le marché, comme indiqué ci-dessous.

    + `Amazon ECS` : `Amazon EC2 Container Service (ECS)` prend en charge les `conteneurs Docker` et vous permet d'exécuter des applications sur un `cluster` géré d'instances `Amazon EC2`.
    + `Azure Container Service (ACS)` : `ACS` vous permet de créer un `cluster de machine virtuelles` qui agissent en tant qu'hôtes de conteneurs ainsi que de `machines maîtres` utilisées pour gérer vos `conteneurs` d'applications.
    + `Cloud Foundry's Diego` : `Diego` est un système de gestion de conteneurs qui combine un planificateur, un exécuteur et un gestionnaire de santé. Il s'agit d'une réécriture `Cloud Foundry`.
    + `CoreOS Fleet` - `Fleet` est un outil de gestion de conteneurs qui vous permet de déployer des conteneurs `Docker` sur des hôtes d'un cluster ainsi que de distribuer sur un cluster
    + `Docker Swarm` : `Docker Swarm` fournit unr fonctionnalité de `clustering` native pour les `conteneurs Docker`, qui vous permet de transformer un groupe de moteurs `Docker` en un seul moteur `Docker virtuel`.
    + `Google Container Engine` - `Google Container Engine`, basé sur `Kubernetes`, vous permet d'exécuter des `conteneurs Docker` sur la plate-forme `Google Cloud`. Il planifie les conteneurs dans le `cluster` et les gère en fonction des exigences définies par l'utilisateur.
    + `Kubernetes` - `Kubernetes` est un système d'orchestration pour les conteneurs `Docker` Il gère la planification et gère les charges de travail en fonction de paramètres définis par l'utilisateur.
    + `Mesosphère Marathon` - `Marathon` est un `framework d'orchestration de conteneurs pour Apache Mesos` conçu pour lancer des applications de longue durée. Il offre des fonctionnalités clés pour exécuter dans un environnement en cluster.

# Pourquoi Kubernetes ?

+ Parmi eux, nous nous sur `Kubernetes` dans ce didacticiel pour les raisons mentionnées ci-dessous.
  + `Kubernetes` est le propre projet de `Google` qu'ils ont utilisé pour gérer les `conteneurs` des 10 dernières années. Ainsi, une vaste expérience en matière d'applications et un modèle mature sont des élements que nous recherchons pour les productions.
  + `Kubernetes` est classé parmi les `meilleurs outils d'orchestration de conteneurs` du marché selon une enquête.
  + Il prend en charge d'autre plate-formes de `conteneurs` en dehors de `Docker` comme `RKT`.
  + `Kubernetes` est un projet `open source`, distinct des autres projets **pilotés par les fournisseurs** comme `Swarm, Msos, CloudFoundry`. `Docker swarm` est également open source mais il est étroitement intégré à d'autres outils `Docker`.
  + Il peut prendre en charge un grand nombre d'applications. C'est un sujet de discussion au sein de la communauté `Kubernetes` depuis le printemps, lorsqu'elle a annoncé que l'outil pouvait exécuter plus de `1000 noeuds`.
  + Cela ne veut pas dire que les autres outils d'orchestration ne sont pas que `kubernetes`, mais nous voulions simplement essayer d'abord les meilleurs d'entre eux, puis nous pourrons en essayer d'autres d'il y a des lacunes avec `Kubernetes`.
  
# Qu'est-ce que Kubernetes ?

+ `Ansible` peut contrôler un grand nombre de serveurs et facilite les tâches d'administrations et d'exploration.
+ `Ansible` peut effectuer une gestion de configuration simple et une orchestration complexe, il possède toutes les fonctionnalités des outils de configuration et il est très facile à apprendre et à mettre en oeuvre.
+ Il communique via les `canaux SSH` normaux afin de récupérer des informations sur des machines distantes, d'émettre des commandes et de copier des fichiers. Pour les noeud `Windows`, il utilise `winrm`.

![Alt Text](C:\DevOps_Tools_Step_By_Step\Section23_Kubernetes\images\image2.jpeg)

### **Selon La documentation Kubernetes**

+ `Kubernetes` est une `plate-forme open source` permettant `d'automatiser ,la mise en échelle et les opérations de conteneurs d'applications sur des clusters d'hôtes`, fournissant une infrastructure centrée sur les conteneurs.

+ Avec `Kubernetes`, vous pouvez répondre rapidement et efficacement à la demande des clients:

  + `Déployez` vos applications de manière rapide et prévisible.
  + Faites évoluer vos applications à la volée.
  + Déployez de nouvelles fonctionnalités en toute transparence.
  + Limitez l'utilisation du matériel aux ressources requises uniquement.
  
+ L'objectif de `Kubernetes` est de favoriser un écosystème de composants et d'outils qui allègent le fardeau d'applications dans les `cloud publics et privés`.

+ Kubernetes est:

  + `Portable` : public, privé, hybride, multi-cloud.
  + `Extensible` : modulaire, enfichable, hookable, composable.
  + `Auto-réparation` : placement automatique, redémarrage automatique, replication automatique, mise à l'échelle automatique.
  + `Google` a lancé le projet `Kubernetes` en 2014. `Kubernetes` s'appuie sur une décennie et demie d'expérience de `Google` dans l'exécution de charges de travail de production à grande échelle, combiné aux meilleures idées et pratiques de la communauté.
  
# Que peut faire Kubernetes ?
+ Au minimum, `Kubernetes` peut planifier et exécuter des conteneurs d'applications sur des `clusters de machines physiques ou virtuelles`.
+ `Kubernetes` fournit l'infrastructure nécessaire pour créer un environnement de développement véritablement centré sur les conteneurs.
+ `Kubernetes` répond à un certain nombre de besoins courants des applications exécutées en production, telles que : 
  + `Colocalisation des processus d'assistance`, facilitant les applications composites et préservant le modèle d'une application par conteneur.
  + Montage de systèmes de stockage.
  + Distribution de secrets.
  + Vérification de l'état des applications
  + Replication instances d'application
  + Utilisation de la mise à l'échelle automatique des pods horizontaux.
  + Dénomination et découverte 
  + Equilibrage des charges
  + Mise à jour progressive.
  + Surveillance des ressources
  + Accès et ingestion de journaux
  + Débogage d'applications
  + Fournir une authentification et une autorisation
  
# Architecture Kubernetes

+ `Kubernetes` est une pile de services qui fonctionnent ensemble pour gérer tous les hôtes, le cluster `Kubernetes` est ainsi que nous appelons ensemble `AKA K8`.
+ Tous ces services ou composants sont présentés ci-dessous.

  + `POD` : un `pod` est un groupe d'un ou plusieurs conteneurs (tels que des conteneurs `Docker`), le stockage partagé pour ces conteneurs et des options sur la façon d'exécuter les conteneurs. Les `pods` sont toujours colocalisés et co-programmés, et exécutés dans un contexte partagé. Un `pod` modélise un `hôte logique` spécifique à une application. Il contient un ou plusieurs conteneurs d'applications relativement étroitement couplés - dans un monde pré-conteneur, lis se seraient exécutés sur la même machine physique ou virtuelle.
  + `SERVICE` : Les pods `kuberenetes` sont mortels. Il naissent et lorsqu'ils meurent, ils ne ressuscitent pas. Les `ReplicationControllers` en particulier créent et détruisent de manière dynamique (par exemple lors d'une mise à l'échelle vers le haut ou vers le bas ou lors de mises à jour progressive). Bien que chaque `pods` ait sa propre `addresse IP`, même ces addresses IP ne peuvent pas être fiables pour être stables dans le temps. Cela conduit à un problème. Le `service` sera au-dessus du `POD` et aura une adresse IP stable, c'est comme un `équilibreur de charge` donc peu importe les `noeuds` que vous avez sous l'équilibreur de charge et quelle est leur adresse IP, l'équilibreur de charge pourra y accéder. C'est similaire pour le `service` dans `Kubernetes`.



  
# Architecture du Noeud Maître
+ `etcd` : Il s'agit d'un magasin clé-valeur open source developpé par `CoreOS`. `Kubernetes` utilise `etcd` pour stocker les données de configuration accessibles par tous les noeuds (sbires et maître) du cluster. Des exemples de données stockées par `Kubernetes` dans `etcd` sont les tâches planifiées, es détails et l'état du `pod/service` crées et déployés, les espaces de noms et les informations de réplication etc.
+ `KubeApiServer` : Le serveur `API Kubernetes` valide également généralement le magasin de données de configuration dans `etcd` et les détails du conteneur déployé qui sont en accord. Il fournit également une interface `RESTFUL` pour faciliter la communication.
+ `Serveur Kube-Schedule` : le déploiement ` des pods et des services` configurés sur les noeuds est effectués par le composant planificateur. Il est responsable de l'attribution des tâches aux niveaux du cluster. Le planificateur dispose également des informations concernant les ressources sur les membres du cluster. Comme ceux requis pour l'exécution du service configuré et est donc en mesure de décider où déployer un service spécifique.
+ `Kube-Controller-Manager` : Il est généralement responsable de la gestion des fonctions au niveau du `cluster` telles que le `contrôleur de réplication`. Chaque fois que l'état souhaité du cluster change, il est écrit dans `etcd` puis le gestionnaire de contrôleur tente de faire apparaître le `cluster` dans l'état souhaité. Un contrôleur utilise `apiserver` pour surveiller l'état partagé du cluster et apporte des modifications correctives à l'état actuel pour qu'il corresponde à celui souhaité. Un exemple est `Replication Controller` qui prend en charge les `PODS` dans le système, si un `POD` échoue, il le remplace par un nouveau `POD`.


# Architectures des Noeuds de serviteurs.
+ `Docker` : L'une des exigences de base des neouds est `Docker`.`Docker` est responsable de l'extraction et de l'exécution du conteneur à partir des images `Docker`.
+ `Kube-proxy` : chaque noeud du cluster exécute un simple proxy réseau. L'utilisation d'un noeud proxy dans le cluster achemine la requête vers le conteneur approprié dans le noeud.
+ `kubelet` : Il s'agit d'un processus agent qui s'exécute suer chaque noeud. Il est responsable de la gestion `des pods et leurs conteneurs`. Il traite les spécifications des pods qui snt définies au format `YAML ou JSON`. `Kubelet` prend les spécifications des pods et vérifie si les pods fonctionnent correctement ou non.
+ `Flannel` : Il s'agit d'un réseau superposé qui fonctionne sur l'attribution d'une plage d'adresses de sous-réseau. Il est utilisé pour attribuer des `adresses IP` à chaque `pod` exécuté et pour établir les communications de pod à pod et de pod à services.


# Configuration de Kubernetes

+ Kubernetes peut être configuré sur une seule machine `Linux` ou nous pouvons avoir `le maître et les noeuds` sur une machine séparée.
+ Comme vous l'auriez deviné, un cluster à noeud unique est idéal pour l'apprentissage et les tests, mais un cluster `Kubernetes` de qualité de production est nécessaire pour gérer des applications et des conteneurs à grande échelle. Nous verrons les deux manières de mettre en place un `cluster Kubernetes`. La configuration manuelle de tous les composants `Kubernetes` est une tâche très fastidieuse, mais il existe peu d'outils sur le marché capable d'automatiser le déploiement du cluster `Kubernetes` pour nous.
  + `Minikube` : `Minikube` configure un cluster à noeud unique sur une machine virtuelle exécuté sur `viurtualbox`. Nous pouvons créer et également géré le cluster `Kubernetes avec minikube`.
  + `Kops` : `Kops` met en place un cluster kubernetes multi-neuds de qualité de production sur le cloud `AWS`, actuellement il ne prend en charge que le fournisseur `AWS`.

# Configuration du Minikube Localement

