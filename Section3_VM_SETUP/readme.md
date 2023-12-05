### **Virtualisation**

+ `La Virtualisation` n'est pas une nouveauté dans l'industrie informatique.
+ La `Virtualisation` a pris un essor considérable grâce à `VMWare`, car elle a résolu le problème de l'exécution de plusieurs systèmes d'exploitation et applications sur un ordinateur physique.
+ Mais ce n'est que la pointe de l'iceberg, `VMWare` et d'autres fournisseurs de virtualisation ont offert d'excellentes fonctionnalités telles que le `clustering de machines physiques virtualisées, la mise en commun des ressources de calcul, la mise en commun du stockage, la haute disponibilité, la migration en direct des machines virtuelles et bien plus encore`.
+ Dans ce chapitre, nous comprendrons la `virtualisation`, ses avantages et comment l'utiliser pour nos opérations `DevOps` quotidiennes.


#### **1. La vie sans virtualisation**

+ Dans l'industrie du logiciel, nous créons et livrons des logiciels ou, comme on dit aujourd'hui, des applications.
+ L'application gère les entreprises ou vice versa. Si l'application ne fonctionne pas ou présente des performances insuffisantes. l'entreprise en souffrira.


+ Les applications s'exécutent sur des serveurs. Nous déployons une application par serveur car nous souhaitons que nos applications soient isolées.
+ Par exemple, si nous avons besoin d'une application `Web`, d'une application de base de données et quelques applications backend.
+ Nous pourrions finir par avoir plusieurs systèmes physiques exécutant chacun une seule instance de cette application.


<img src="https://binarymist.files.wordpress.com/2012/01/bare-metal_hypervisor.png"/>


+ Ainsi, chaque fois que nous avons besoin d'exécuter une nouvelle application, nous achetons des serveurs, installons le système d'exploitation et configurons notre application sur celui-ci.
+ Et la plupart du temps, personne ne connaissait les exigences de performance de la nouvelle application ! Cela signifiait que le service devriat faire des suppositions lors du choix du modèle et de la taille des serveurs à acheter.
+ En conséquence, le service informatique a fait la seule chose raisonnable : il a acheté de gros serveurs et dotés d'une grande résilience.
+ Après tout, la dernière chose que quiconque voulait- y compris l'entreprise- était des serveurs sous-alimentés.

+ La plupart du temps, les ressources informatiques de ces serveurs physiques seront sous-utilisées jusqu'à 5 à 10% de leur capacité potentielle. Un gaspillage tragique du capital et des ressources de l'entreprise.


#### **2. Entrez le VMWare**
+ Au milieu de tout cela, `VMare`, `Inc.` a donné au monde la `machine virtuelle (VM)`.
+ Et presque du jour au lendemain, le monde est devenu bien meilleur !
+ Enfin, nous disposions d'une technologie qui nous permettrait d'executer plusieurs applications métier sur un seul serveur en toute sécurité. 

#### **3. La machine virtuelle**
+ Un système informatique virtuel est appelé `machine virtuelle (VM)`: un conteneur logiciel étroitement contenant un système d'exploitation et une application.
+ Chaque `VM` autonome et complètement indépendante.
+ Placer plusieurs machines virtuelles sur un seul ordinateur permet à plusieurs systèmes d'exploitation et applications de s'exécuter sur un seul serveur physique, ou `hôte`.


#### **4. Propriété clés des machines virtuelles**

+ Comme généralement, nous installons le système d'exploitation sur le serveur physique, puis installons nos applications dessus.
+ En configurant `Hypervisor` sur le serveur physique, nous pouvons créer plusieurs `VM`, chacune avec son propre système d'exploitation.

<img src="https://binarymist.files.wordpress.com/2012/01/bare-metal_hypervisor.png"/>


+ Il existe deux types d'hyperviseurs:

    + **Type 1**
  
        + Les hyperviseurs s'exécutent directement sur le matériel du système.
        + Ils sont souvent appelés hyperviseurs `natifs` ou `bare métal`.
        + Ils sont installés sur un ordinateur physique comme système d'exploitation.
        + Ainsi, au lieu d'installer le système d'exploitation, nous installons `Hypervisor` pour réaliser la `virtualisation`.
        + Exemple :
            + Microsoft Hyper-V
            + VMware ESX/ESXI.
            + Xen Hypervisors.
        + Ces hyperviseurs sont utilisés sur des machines virtuelles de niveau production offrant d'excellentes performances.
          + Les `hyperviseurs de type 1` peuvent être regroupés (clusters) et gérés de manière centralisée par un logiciel comme `VMware Vcenter pour Esxi`.
          
    + **Type 2**
  
        + Les `Hyperviseurs de Type 2` s'exécutent sur un système d'exploitation hôte.
        + Dans ce genre, nous installons un hyperviseur sur les `OS` comme `Linux ou Windows`.
        + Exemple :
            + Vmware server/workstation/player
            + Oracle Virtualbox
        
<img src= "https://microkerneldude.files.wordpress.com/2012/01/type1-vs-2.png"/>


#### **5. Votre choix d'hyperviseur**

+ Les hyperviseurs de type 1 sont excellentes et vous offrent des fonctionnalités étonnantes telles que le `clustering de machines physiques virtualisées, la mise en commun des ressources de calcul, la mise en commun du stockage,la haute disponibilité, la migration en direct de la machine virtuelle et bien plus encore`.
+ Il est généralement utilisé pour virtualiser des centres de données entiers ou un pool de serveurs. Ceci est géré par des logiciels très coûteux comme `VMware Vcenter`.
+ Comme ces didacticiels se concentrent sur les outils `DevOps`, nous n'entrerons pas dans les hyperviseurs de `type 1`.
+ Nous allons nous concentrer sur les `hyperviseurs de type 2` comme `Oracle Virualbox` que nous pouvons installer sur nos ordinateurs portables/de bureau et utiliser les machines virtuelles.
+ Nous devons exécuter plusieurs machines virtuelles sur notre système pour tester/exécuter nos outils et scripts.
+ Nous devons également configurer des logiciels d'application Web sur plusieurs systèmes d'exploitation et nous le ferons en utilisant `Oracle virtualbox Hypervisor`.


#### **6. Quelques terminologies**

+ Lorsqu'il s'agit de virtualisation (et également pour comprendre les chapitres suivants de cette documentation), il est utile de se familiariser avec un peu de terminologie cruciale, en particulier avec les termes suivants:

    + **Systèmes D'exploitation Hôte (OS Hôte)**
        + Il s'agit du système d'exploitation de l'ordinateur physique sur lequel `Virtualbox` est installé. Il existe des versions de virtualBox pour les hôtes `WXindows, Mac OS X, Linux et Solaris`.

    + **Système D'exploitation Invité (OS invité)**
        + Il s'agit du système d'exploitation qui s'exécutent à l'intérieur de la machine virtuelle.

<img src= "images/téléchargement.jpg"/>