<center><u><h1>Ansible</h1></u></center>

+ `Ansible` est un outil d'automatisation open source très puissante.
+ Il entre dans la catégorie des outils de gestion de configuration comme `Puppet, Chef, Salstack, etc`.
+ C'est le plus simple parmi tous les outils de gestion de configuration en termes d'approche facile à lire et à écrire et d'architecture `sans maître/sans serveur.
+ Etant simple à utiliser, il peut gérer les tâches les plus complexes en matière d'orchestration, où vous exécutez des tâches d'automatisation en chaîne et dans l'ordre sur plusieurs serveurs et appareils différents


<center><u><h2>Gestion de Configuration</h2></u></center>

+ En termes simples, les outils qui gèrent la configuration des infrastructures informatiques telles que le système d'exploitation, les périphériques réseau, les applications, les logiciels et les services de cloud sont appelés `outils de gestion de configuration`.
+ La configuration de l'infrastructure informatique, comme les modifications des logiciels et du système d'exploitation, se produit de temps en temps.
+ Nous les ajoutons, les supprimons et les mettons à jour pour de bon.
+ Effectuer de telles modifications sur des centaines de serveurs et d'appareils prend beaucoup de temps et est sujet aux erreurs si vous le faites manuellement.
+ Ces outils vous aident à gérer et automatiser tous ces changements en toute simplicité et depuis un endroit centralisé.

<center><u><h3>Certaines Fonctionnalités</h3></u></center>

<h4>1) Configuration Centralisée</h4>

+ La configuration des différents serveurs et appareils est gérée à partir d'un serveur central.
+ Comme si vous gérez des serveurs `Web`, des serveurs de base de données ou des consommateurs, toutes leurs configurations telles que les logiciels, les correctifs, les fichiers de configuration, etc. peuvent être configurées sur le serveur central.
+ Lorsque le nœud souhaite mettre à jour les dernières modifications, il peut les récupérer depuis le serveur ou les transmettre au nœud depuis le serveur.

<h4>2)Mise en vigueur</h4>

+ L'application de la configuration peut être la fonctionnalité la plus importante d'un outil de gestion de configuration.
+ En s'exécutant régulièrement et en s'assurant que la machine est configurée dans l'état souhaité, les outils de gestion de configuration empêchent la désynchronisation de la configuration.
+ La dérive de configuration peut se produire de différentes manières : `mises à jour, de packages, débogage en direct, collègues "utiles", etc`.
+ Quelle qu'en soit la cause, être capable de dire en toute confiance : "C'est ainsi que cette machine est configurée" est un excellent moyen pour raccourcir le temps de résolution des incidents et réduire les surprises.

<h4>3)Abstraction</h4>
+ Les administrateurs systèmes maintiennent des environnements complètement homogènes.
+ Même si vous êtes une boutique entièrement `Linux`, vous avez probablement plusieurs distributions que vous prenez en charge, ou au moins plusieurs versions d'une distribution.
+ Avec les outils de gestion de configuration, de nombreuses implémentations d'une configuration spécifiques au système d'exploitation sont résumées pour vous.
+ Le même fichier de configuration peut être utilisé pour gérer, par exemple, l'installation d' `Apache HTTPD` sur les systèmes `Red Hat` et `Ubuntu`.

<h4>4) Contrôle De Version Convivial.</h4>
+ Bien entendu, la meilleure façon de permettre la coopération est de tout avoir dans un système de version.
+ Tous les outils repertoriés ci-dessous utilisent une forme de texte pour la configuration.
+ Cela signifie que vous pouvez profiter des avantages de votre système de contrôle de version.

<h4>5) Replication</h4>
+ La gestion de la configuration facilite la `réplication` des environnements avec exactement les mêmes logiciels et configurations.
+ Cela vous permet de créer efficacement un écosystème à plusieurs étapes, avec des serveurs de production, de développement et de test.


<h4>6) Quelques Outils De Gestion De Configuration</h4>

+ `Puppet`
+ `Chef`
+ `Ansible`
+ `Slastack`
+ `CFEngine`


<center><u><h2>Quelques Terminologies</h2></u></center>

<h4>1)Gestion Du Changement</h4>

+ Il s'agit d'un processus lorsqu'une configuration spécifique de la machine ou du logiciel est modifiée.
+ Ce processus `CM` typique dans l'industrie informatique par un processus d'approbation du client ou de la direction supérieure, nous parlons bien sûr de systèmes de production.
+ Un seul changement sur 1, 10, ou 100 serveurs doit être effectués de manière très précise et efficace.
+ Par exemple, mettre à niveau un progiciel présentant un bug sur des centaines de serveurs ou redémarrer un service tel qu'un service `Web` pour prendre en compte toute nouvelle modification.

<h4>2)Approvisionnement</h4>


+ En général, le `provisionnement` signifie `fournir` ou rendre quelque chose disponible dans l'infrastructure informatique.
+ Par exemple, `provisionner un serveur Web` signifie installer et configurer des logiciels de service `Web` et leur configuration sur un système d'exploitation.
+ `Provisionner une instance cloud` signifie créer une machine virtuelle cloud.

<center><img src = "images/image1.jpeg"/></center>

<h4>3)Orchestration</h4>

+ `L'automatisation` consiste à regrouper une liste de tâches et à les exécuter de haut en bas via un script, généralement comme l'installation d'un serveur `Web` via un script.
+ Alors que `l'orchestration` est le processus par lequel nous regroupons plusieurs tâches automatisées et les exécutons dans un ordre.
+ Par exemple, si nous orchestrons la configuration d'une application `Web` à plusieurs niveaux, nous devons configurer tous les services tels que les bases de données, les services `Web`, l'équilibrage à charge et la surveillance dans un ordre afin qu'ils soient validés lorsque toute la configuration est en cours d'exécution.
+ Tout d'abord, nous allons configurer le service de base de données afin que lorsque le service `Web` est configuré, il soit connecté à la base de données et validés.
+ Ensuite, nous pouvons configurer `LoadBalancer` et y ajouter des services `Web`.
+ La surveillance serait mise en place à la toute fin.
+ Désormais, les services de surveillance renverront les bons résultats de l'équilibreur de charge, du service `Web` et du service de base de données.
+ Ce processus est appelé `orchestration`, mais sans s'y limiter, et est effectué pour divers autres processus d'infrastructure informatique tels que le `cloud computing, la configuration du réseau, etc`.



<center><img src = "images/image2.jpeg"/></center>


+ Le mot `orchestration` vient du mot `Orchestra` où différents instruments sont joués dans un ordre approprié pour générer la belle mélodie.
+ Tout est question d'ordre, sinon vous n'obtenez pas de musique, tout ce que vous obtenez est du son et probablement pas si bon.

<center><img src = "images/image3.jpeg"/></center>

+ De même, `l'orchestration informatique` consiste à automatiser les tâches dans un ordre approprié.

<center><img src = "images/image4.jpeg"/></center>


<h4>4) Comportement Idempotent</h4>

+ Les outils de gestion de configuration assurent le suivi de l'état des ressources afin d'éviter de répéter des tâches exécutées auparavant.
+ Si un package était déjà installé, l'outil ne tentera pas de l'installer à nouveau.
+ L'objectif est qu'après chaque exécution de provisionnement, le système atteigne (ou conserve) l'état souhaité, même si vous l'exécute plusieurs fois.
+ C'est ce qui caractérise ces outils comme ayant un comportement idempotent.
+ Un autre exemple serait que si nous essayons de transmettre un fichier à plusieurs serveurs ont déjà le même fichier avec le même conteneu, il ne va pas écraser le fichier, il l'ignorera simplement et le transmettra à leurs serveurs là où il se trouve une inadéquation.


<center><u><h2>Introduction à Ansible</h2></u></center>

+ `Ansible` peut contrôler un grand nombre de serveurs et facilite les tâches d'administration et d'exploitation.
+ `Ansible` peut effectuer une gestion de configuration simple et une orchestration complexe, il possède toutes les fonctionnalités des outils de configuration et il est très facile à apprendre et à mettre en œuvre.
+ Il communique via les canaux `SSH` normaux afin de récupérer des informations sur des machines distantes, d'émettre des commandes et de copier des fichiers.
+ Pour notre `Windows` il utilise `winrm`.

<center><img src = "images/image5.jpeg"/></center>

+ Puisqu'il utilise `SSH` pour `Linux et winrm` pour `Windows`, il n'est pas nécessaire de configurer quoi que ce soit du côté de l'agent, car `ssh` est fourni par défaut sur les serveurs `Linux` et donc comme `winrm` sur le serveurs `Windows`.


<center><u><h2>Installation d'Ansible</h2></u></center>

+ `Ansible` gère par défaut les machines via le protocole `SSH`.
+ Une fois `Ansible` installé, il n'ajoutera pas de base de données et il n'y aura aucun daemons à démarrer ou à continuer d'exécuter.
+ Il vous suffit de l'installer sur une seule machine (qui pourrait facilement être un ordinateur portable) et il peut gérer tout une flotte de machines distantes à partir de ce point central.


<h4>1) Dernière version de yum</h4>

+ Les `RPM` sont disponibles auprès de `yum` pour les distributions `EPEL 6, 7` et `Fedora` actuellement prises en charge 

+ `Ansible` lui-même peut gérer les systèmes d'exploitation antérieurs contenant `Python 2.6 ou supérieur` (donc également `EL 6`).
+ Les utilisateurs de `Fedora` peuvent installer `Ansible` directement, mais si vous utilisez `RHEL` ou `CentOS` et l'avez pas déjà fait, configurez `EPEL`.


<center><img src = "images/image6.jpeg"/></center>


<h4>2) Dernière version Via Apt (Ubuntu)</h4>

+ Les versions `Ubuntu` sont disponibles dans un `PPA` ici. (`Windows` n'est pas pris en charge pour la machine de contrôle).
+ Pour configurer le `PPA` sur votre machine et installer `ansible`, exécutez ces commandes:

<center><img src = "images/image7.jpeg"/></center>

<h4>3) Quelques Notes Rapides :</h4>

+ La machine sur laquelle `ansible` est installé est appelée `Control Machine`.
+ `Ansible` est écrit en langage `Python`.
+ Vous devez disposer de python `2.6/2.7` pour installer `ansible` sur la machine de contrôle.
+ `Windows` n'est pas pris en charge pour la machine de contrôle.
+ `Ansible` peut automatiser les tâches sur les machines `Linux et Windows`


<center><u><h2>Inventaire/Inventory</h2></u></center>


+ L'inventaire est un fichier texte dans lequel vous les informations sur l'hôte que vous souhaitez gérer avec `ansible`.
+ L'emplacement par défaut du fichier d'inventaire est `etc/ansible/hosts`.
+ Vous pouvez spécifier un autre fichier d'inventaire à l'aide de l'option `-i <paths>` sur la ligne de commande.
+ Pour cet exercice, nous avons besoin de deux serveurs `Linux`, vous pouvez faire tourner deux instances `centosvm ou ec2` pour vous entrainer.

<h4>1) Hôtes et Groupes</h4>

+ Créez le fichier nommé `inventor-dev` (le nom peut être n'importe quoi) et ajoutez l'entrée mentionnée ci-dessous.
<center><img src = "images/image8.jpeg"/></center>

**Explication**

+ `web1` et `db1` sont les noms que nous avons donnés aux hôtes.
+ `ansible_ssh_host` est la variable et sa valeur est `l'addresse IP` du serveur.
+ La variable `ansible_ssh_user` contient le nom de l'utilisateur.
+ `ansible_ssh_password` contient le mot de passe.
+ `[webserver] & [dbservers]` est le nom du groupe qui peut contenir `n` nombre d'hôtes. Les noms de groupe sont mis entre crochets `[]`.


+ **Remarque**

