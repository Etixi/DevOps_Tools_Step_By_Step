<center><h1><u>Intégration Continue Avec Jenkins</u></h1></center>

+ Dans le chapitre précédent, nous avons vu comment le processus de développement est suivi par les développeurs pour créer des logiciels et même maintenir ces logiciels.
+ Ainsi, lorsque les développeurs écrivent du code pour créer des logiciels, ils fusionnent également tout ce code dans un référentiel centralisé ou un système de contrôle de version comme `Github`.
+ Ce code est transféré dans les référentiels plusieurs par jour, et au fil du temps, tout le code est fusionné.
+ Les méthodes traditionnelles de développement de logiciels ne dictent pas la fréquence ou la fréquence à laquelle vous intégrez toutes les sources d'un projet.
+ Les programmeurs peuvent travailler séparément pendant des heures, des jours, voire des semaines sur la même source sans se rendre compte du nombre de conflits (et peut-être de bugs) qu'ils génèrent.


<center><h2><u>L'Intégration est Douloureuse.</u></h2></center>


+ Les équipes agiles produisent du code exploitable et robuste à chaque itération.
+ Tout ce code, s'il est construit et évalué renvoie de nombreux conflits, bugs et erreurs.
+ Les développeurs doivent résoudre ces conflits et problèmes avant de passer à l'itération suivante.
+ Plus les programmeurs partagent du code, plus cela devient problématique.
+ Pour ces raisons les équipes agiles choisissent donc souvent `L'Intégration Continue`.

<center><h2><u>Quelques Terminologies.</u></h2></center>
<br/>

<h3>Code Source</h3>

+ Tout le code que les développeurs écrivent pour créer le logiciel est appelé `Code Source`.

<h3>Le Processus De Construction</h3>

+ Il s'agit d'un processus par lequel le code source est converti en une forme autonome pouvant être exécutée sur un ordinateur.
+ Par exemple, un code source écrit pour développer un logiciel `Windows` une fois construit créera un fichier `.exe ou .msi`.
+ Un autre exemple, si un code `Java` est construit, il peut créer un fichier `.jar, .war, .ear`.
+ Ce logiciel déployable est appelé `Artefact`. 
+ Le code peut être empaqueté et déployé manuellement.
+ Mais il existe des outils de construction qui facilitent la vie des développeurs lorsqu'il s'agit de créer des `artefacts` ou même de les déployer.
+ Ceux-ci sont appelés `Outils d'Automatisation de Construction`.

**Quelques outils de build**

+ `Ant`
+ `Maven`
+ `Gradle`
+ `MsBuild`
+ `Nant`


**Tests Unitaires**

+ `Les tests unitaires` vérifient que chaque unité de code (principalement des fonctions) fonctionne comme prévu.
+ Le développeur, en plus d'écrire du code, écrira les cas de test qui peuvent être exécutés au moment de la construction.
+ Certains cas de tests peuvent être générés automatiquement.
+ L'objectif de tests unitaires est d'isoler une session de code (unité) et de vérifier son exactitude.


<center><h2><u>Qu'est-ce que l'intégration continue</u></h2></center>

+ `L'Intégration Continue (CI)` est le processus d'automatisation de la création et des tests du code chaque fois qu'un membre de l'équipe valide des modifications dans le contrôle de version.
+ `CI` encourage les développeurs à partager leur code et leurs tests unitaires en fusionnant leurs modifications dans un référentiel de version partagé après chaque petite tâche terminée.
+ La validation du code déclenche un système de génération automatisé pour récupérer le dernier code du référentiel partagé et pour créer, tester et valider la branche principale complète (également appelée `tronc ou main`).


<h3>Le Problème</h3>

+ Les développeurs écriront le code et construiront dans un système local.
+ Uen fois que les développeurs ont testé le code et vérifié localement, ils le transfèrent vers un référentiel centralisé comme `github`.
+ De même, tous les développeurs transmettent leur code `VCS` plusieurs par jour.
+ Les développeurs travailleraient dans leurs propres silos ou grottes et continueraient à écrire le code jusqu'à ce qu'ils terminent une tâche particulière ou le projet.
+ Désormais, tout le code que les développeurs ont inséré dans le `VCS`, s'il est construit et testé, renverra de nombreux conflits, erreur à cause de laquelle la construction échouera.

<h3>La Solution</h3>

+ Pour contourner ce problème, chaque fois que le développeur envoie le code au `VCS`, il doit être récupéré, construit et testé par un serveur de `build` en même temps.

![Alt Text](images/image1.jpeg)

+ Ce processus répété plusieurs fois par semaine ou par jour ou quotidiennement une fois est appelé `Intégration Continue`.
+ Le code des développeurs est continuellement intégré, de sorte qu'à tout moment nous disposons d'un logiciel fonctionnel, s'il y a un problème dans le `processus de construction`, les développeurs seront informés par `e-mail` et résoudront le problème.


<center><h2><u>Qu'est-ce que Jenkins</u></h2></center>

+ `Jenkins` est un `serveur d'intégration continue` qui récupérer le dernier code de `VCS`, le construire, le tester et le notifier aux développeurs.
+ `Jenkins` peut faire bien plus de choses en plus d'être simplement un `serveur CI`.
+ Il s'appelait à l'origine `Hudson`, `Oracle Inc.`possède désormais `Hudson`
+ `Jenkins` est un projet open source écrit par `Koshuke Kawagauchi`.
+ `Jenkins` est un serveur d'applications `Web basé sur Java`.
+ Comme condition préalable, nous devons d'abord configurer `Java` sur des machines pour ex&cuter le serveur `Jenkins`.

<center><h2><u>Caractéristiques de Jenkins</u></h2></center>

<br/>

<h3>Open Source</h3>

+ Comme `Jenkins` est open source, il y a de nombreuses contributions partout dans le monde au logiciel `Jenkins`.
+ Il possède toutes les fonctionnalités les plus récentes et les plus intéressantes que les développeurs y intègrent régulièrement.

![Alt Text](images/image2.jpeg)



#### Extensible

+ `Jenkins` est livré avec de nombreux avantages, mais ce n'est tout simplement pas limité à cela, la principale puissance de `Jenkins` est son extensibilité qui peut être obtenue en y installant des `plugins`.
+ La communauté open source `Jenkins` a écrit des tonnes de `plugins`, ces `plugins` peuvent effectuer diverses tâches, comme l'intégration avec des outils ou des serveurs externes.

    + `Plugins VCS` - **git, svn, subversion, etc.**
    + `Plugins de construction` - **MAVEN, ANT, Msbuild, etc.**
    + `Plugins de notification` - **E-mail, chat, sms, etc.**
    + `Plugins cloud` - **Créez des instances cloud, déployez du code sur les services cloud, etc.**
    + `Plugins de test` - **Analyse de code, cas de test unitaire, analyse de code statique, etc.**

+ La liste des `plugins` est très longue, chaque fois nous voulons que `Jenkins` effectue certaines tâches, recherchez simplement ce plugin et la plupart du temps, vous trouverez quelque chose.
+ Par exemple, si vous souhaitez que `Jenkins` déploie `l'artefact Java` sur le serveur `Tomcat`, recherchez le plugin nommé `déployer sur un conteneur`.

![Alt Text](images/image3.jpeg)


# Configuration Jenkins

+ `Jenkins` peut être installé sur `Windows, Linux ou MacOS`.
+ `Jenkins` a juste besoin d'un logiciel `Java` pour fonctionner.
+ Dans ce tutoriel, nous allons installer `Jenkins` sur un serveur `Ubuntu`.
+ Vous pouvez configurer `une machine virtuelle ou une instance cloud`.


![Alt Text](images/image4.jpeg)


#### Installer le client Git et Maven sur le serveur Jenkins

+ Nous intégrerons `Jenkins` à `github` pour télécharger le code source.
+ Nous testons le code source `Java` qui sera construit par `Maven`, nous devons donc également installer `Maven` sur le serveur `Jenkins`.
+ Ce n'est pas une condition obligatoire pour exécuter `Jenkins` si vous n'utilisez pas `git et maven`.

![Alt Text](images/image5.jpeg)


#### Accéder Jenkins

+ `Jenkins` s'exécute sur le port `8080` par défaut.
+ Ouvrez un navigateur et utiliser l'url ci-dessous : http://jenkinsIP:8080
+ `Jenkins` définira un mot de passe aléatoire pour déverrouiller la configuration de `Jenkins`.


![Alt Text](images/image6.jpeg)

+ Le mot de passe serait stocké dans le fichier `/var/lib/jenkins/secrets/initialAdminPassword`.
+ Lisez ce fichier et obtenez le mot de passe. Utilisez ce mot de passe pour déverrouiller `Jenkins`.

![Alt Text](images/image7.jpeg)

+ `Jenkins` vous offre la possibilité d'installer certains `plugins` suggérés au moment de l'installation.
+ Vous pouvez sélectionner des `plugins` individuels ou installer un groupe de plugins suggéré.
+ Sélectionnez le `plugin` suggéré pour le moment.

![Alt Text](images/image8.jpeg)


# Création du premier travail Jenkins

+ `Jenkins` gère toutes les tâches dans ce qu'on appelle des `tâches`.
+ Chaque tâche représente un ensemble d'activités telles que `le processus de construction, le déploiement de logiciels ou l'exécution des scripts`.
+ Nous allons créer un exemple de travail pour mieux comprendre.

  + `Click Create new jobs or New Item => Enter name - "first-jenkins-job" => Select Freestyle project => OK`.

![Alt Text](images/image9.jpeg)


+ Allez dans la section `Build` => Dans la liste déroulante, sélectionnez `shell` => Entrez quelques commandes Linux, `free -m; w` => Enregistrer.

![Alt Text](images/image10.jpeg)

+ Après avoir enregistré le projet, nous atterrissons dans le tableau de bord de travail. 
+ Cliquez sur `Build` maintenant pour exécuter ce projet.

![Alt Text](images/image11.jpeg)

+ Une fois l'exécution terminée, nous pouvons vérifier l'historique des tâches exécutées et en vérifier la sortie.

![Alt Text](images/image12.jpeg)

+ Cliquez sur la boule bleue pour voir le résultat du travail.

![Alt Text](images/image13.jpeg)


+ Nous avons vu dans l'exemple ci-dessus que la mise en place d'un travail `Jenkins` n'est pas une tâche si difficile.
+ Mais vous devez savoir quelles informations sont collectées dans le cadre du travail de `Jenkins`.
+ Dans la tâche suivante, nous créons une véritable tâche de `build`.

# Configurer une tâche build Java avec Maven

+ Noua allons utiliser un code source Java accessible au public depuis github pour tester le travail de `build` : https://github.com/wakalao/game-of-life.git.
+ Ce code source `Java` peut être construit par `Maven`. Il contient également le fichier `pom.xml` dont `Maven` a besoin pour créer le code.
+ Accéder au tableau de bord principal de `Jenkins` => Cliquez sur Nouvel élément => Donnez un nom à votre travail => Freestyle => OK.

![Alt Text](images/image14.jpeg)


#### Gestion du code source

+ Copiez l'`URL` du code source de gameoflife depuis github.
+ Accédez à la section de gestion du code source dans `Jenkins` et sélectionnez sur `Git`.
+ Entrez l'url github du jeu de la vie.

![Alt Text](images/image15.jpeg)


+ Il s'agit d'un référentiel public, donc aucune information d'identification n'est requise et nous sélectionnons la branche principale.


![Alt Text](images/image16.jpeg)

+ Accédez à la section `build` => Dans le menu déroulant, sélectionnez `Invoquer les cibles Maven de premier niveau` => Dans les objectifs, indiquez `installer` => Enregistrer.


![Alt Text](images/image17.jpeg)


+ Cliquez sur `Build Now` => Dans l'historique de construction, cliquez sur le symbole de chargement ou sur la boule clignotante pour voir la sortie de la console d'exécution.

![Alt Text](images/image18.jpeg)

+ Selon le `POM.xml` de ce projet ce travail `maven` particulier effectuera les tâches mentionnées ci-dessous.

    + Téléchargez les dépendances Maven pour créer le travail.
    + Construisez le code source Java.
    + Générez l'artefact
    + Archivez l'artefact
    + Exécutez les cas de tests unitaires dans le code source.

![Alt Text](images/image19.jpeg)

#### Artefact de l'application Web Game Of Life

+ Une fois le processus de construction terminé, vous pouvez trouvez l'artefact de cette tâche dans l'espace de travail de cette tâche.


#### Espace de travail :

+ L'espace de travail est l'endroit où toutes les données du travail sont stockées, par exemple le code source, les artefacts, etc.
+ Chaque travail dans `Jenkins` a son propre espace de travail.

![Alt Text](images/image20.jpeg)

+ Cliquez sur `workspace => gemaoflife-web => target => gameoflife.war`, `gameoflife.war` est l'artefact généré et archivé par le processus de construction de `Maven`.
+ Cette artefact peut être déployé sur le serveur d'applications Web Java comme le serveur `Tomcat ou Jboss`.

![Alt Text](images/image21.jpeg)

# Administration Jenkins

+ Une fois que nous avons eu un petit avant-goût de `Jenkins` et comment exécuter des tâches, nous pouvons comprendre comment administrer `Jenkins`.
+ `Jenkins` offre des fonctionnalités étonnantes et très flexibles, nous pouvons configurer `Jenkins` selon nos besoins.
+ `Jenkins` peut effectuer diverses tâches en plus d'être simplement un serveur `CI`, mais nous devons le configurer selon nos besoins.
+ Dans la section suivante, nous verrons à quel point `Jenkins` est flexible et extensible.
+ Vous pouvez ouvrir les paramètres d'administration de `Jenkins` en cliquant sur `Gérer Jenkins` depuis le tableau de bord principal.

![Alt Text](images/image22.jpeg)

+ Il existe une variété de paramètres avec lesquels vous pouvez bricoler.
+ Nous allons approfondir un par un.
+ **Remarque : Parfois, après avoir apporté une modification à la configuration, vous devez peut-être redémarrer `Jenkins`**.
+ Dans le navigateur, vous pouvez utiliser l'URL ci-dessous pour redémarrer `Jenkins`.


```
http://<JenkinsIP>:8080/restart
```

#### Gérer Les Plugins

+ Les `plugins` sont la fonctionnalité la plus puissante de `Jenkins`.
+ Vous pouvez personnaliser `Jenkins` selon vos besoins en installant et en configurant des `plugins`.
+ Vous pouvez utiliser `Jenkins` pour automatiser presque tout, cela dépend simplement des `plugins` que vous configurez et il existe une grande variété de choix de plugins.
+ Nous avons déjà utilisé certains plugins dans notre travail de construction comme `Git SCM, Invoke top level Maven target etc`.
+ Certains `plugins` sont installés par défaut dans `Jenkins` et vous pouvez ensuite installer n'importe quel plugin selon votre choix et vos besoins.
+ Cliquez sur `Gérer les plugins`.

![Alt Text](images/image23.jpeg)

+ Il y a quatre onglets

+ **1) Mise à Jour**
    + Si un `plugin` est obsolète ou si aucune version de ce plugin n'est disponible, nous pouvons mettre à jour les `plugins` à partir de cet onglet.
    
+ **2) Disponibles**
    + Liste des plugins disponibles à installer. Trouvez votre plugin à partir du filtre, cochez simplement votre plugin préféré et cliquez sur `Installer sans redémarrer`.
    + Si les paramètres ne prennent pas effet, redémarrez le serveur `Jenkins`.
    + Chaque plugin aura une page wiki, cliquez sur le plugin pour lire son wiki.

    ![Alt Text](images/image24.jpeg)

+ **3) Installé**

  + Liste des plugins installés, si vous choisissez de désinstaller un plugin. Mettez une coche et cliquez sur désinstaller.
    ![Alt Text](images/image25.jpeg)
  
+ **4) Avancé**

    + Il arrive parfois que vous soyez assis derrière un serveur proxy et que vous n'ayez pas de connexion Internet directe.
    + Cette fois, vous ne pourrez pas voir la liste des plugins disponibles et vous ne pourrez pas l'installer.
    + Vous pouvez mentionner les paramètres du proxy sur cette page, redémarrer `Jenkins` et vous verrez alors la liste des plugins parmi lesquels choisir.
    + Si vous êtes programmeur `Java` et avez écrit votre plugin, vous pouvez télécharger votre propre plugin sur `Jenkins` au format `.hpi`.
      ![Alt Text](images/image26.jpeg)
  

+ L'option de paramètres sur cette page dépend du nombre de plugins dont vous disposez.
+ De nombreux plugins nécessitent de paramètres de configuration globaux qui peuvent être modifiés depuis cette page.
+ Plus de plugins et plus de paramètres que vous verrez sur cette page.
+ A partir de cette page, nous pouvons modifier quelques paramètres globaux de `Jenkins` comme : 

#### 1) Nombre d'exécuteur testamentaire

+ Nombre de `tâches` pouvant s'exécuter en parallèle dans `Jenkins`.
+ Si vous pouvez disposez du nombre d'exécuteurs 2 et que vous avez lancé 3 tâches en même temps, alors la troisième tâche sera mise en file d'attente.

**Les variables d'environnement et le chemin des outils peuvent également être définis.**

#### 2) Notification par courrier électronique

+ Adresse su serveur `SMTP` et détails du compte pour envoyer des e-mails depuis `Jenkins`.

#### 3) Configurer la sécurité électronique

+ L'ajout, la suppression et la mise à jour de l'utilisateur de son autorisation peuvent être gérés à partir de cette page.

![Alt Text](images/image27.jpeg)



#### Domaine de sécurité

+ Tout d'abord, établissez la méthode d'authentification de l'utilisateur.
+ Pour les installations plus petites et plus informelles, vous pouvez utiliser la propre base de données d'utilisateurs de `Jenkins`.
+ Pour les installations d'entreprise, vous souhaiterez utiliser votre d'entreprise, qui permet aux utilisateurs de se connecter à `Jenkins` avec leur nom d'utilisateur et leur mot de passe habituels.


#### La propre base de données des utilisateurs de Jenkins

+ Il s'agit du schéma d'authentification le plus simple : `Jenkins` gère sa propre base de données d'utilisateurs indépendante.
+ Les gens peuvent créer leur propre compte et vous, en tant qu'administrateur, décidez qui peut faire quoi dans `Jenkins`.

  + 1. Sélectionnez la propre base de données d'utilisateurs de `Jenkins`
  + 2. Cochez la case `Autoriser` les utilisateurs à s'inscrire.
  + 3. Continuez avec `Autorisation` ci-dessous. N'oubliez notamment pas d'appuyer sur le bouton `Enregistrer` en bas de la page.

#### Active Directory sur serveur linux

+ Si `Jenkins` s'exécute sur un serveur `Winbdows`, il est préférable d'installer le plugin `Active Directory`.
+ Sur un hôte `Linux`, vous avez la possibilité d'utiliser le `plug-in Active Directory` ou une authentification basée sur `LDAP`.
+ Pour configurer `LDAP` pour qu'il fonctionne `Active Directory`, fournissez les éléments suivants : 


![Alt Text](images/image28.jpeg)

+ Notez que la valeur correcte du `DN` du gestionnaire peut varier considérablement en fonction de la configuration de votre `Active Directory`.


#### UNIX NIS

+ Pour configurer le système d'information réseau : 

  + Accédez au tableau de bord `Jenkins`, généralement `http://_server_:8080` ou `http://_server_/jenkins:8080`, où le serveur est l'hôte sur lequel `Jenkins` est exécuté
  + Sélectionnez `Gérer Jenkins`, puis configurez la sécurité globale.
  + Cliquez sur `Activer la sécurité`. La page s'agrandira pour offrir un choix de contrôle d'accès.
  + Sélectionnez la base de données des utilisateurs/groupes `Unix#*` Appuyez sur le bouton `Test` (à l'extrême droite).
  + Si succès s'affiche, tout est correctement configuré 
  + Sinon, suivez les instructions pour résoudre le problème et répétez.
  + Si vous n'y parvenez toujours pas, appuyez sur le bouton `Avancé` et spécifiez le nom du service `sshd` et répétez.
  + Continuez avec l'autorisation ci-dessous. N'oubliez notamment pas d'appuyer sur le bouton `Enregistrer` en bas de page.

#### LDAP

+ Votre `Plugin LDAP`. Continuez ensuite avec `Autorisation` ci-dessous. N'oubliez notamment pas d'appuyer sur le bouton `Enregistrer` en bas de page.


#### Autorisation

+ La section `Autorisation` de la page `Configurer` la sécurité globale vous permet de configurer ce que les utilisateurs sont autorisés à faire une fois authentifiés.


#### Sécurité basée sur la matrice

+ La sécurité basée sur la matrice offre le contrôle le plus précis sur les privilèges des utilisateurs.

  + Sélectionnez la sécurité basée sur la matrice comme autorisation.
  + Accordez à l'utilisateur anonyme uniquement un accès global en lecture.
  + Dans la zone de texte sous la matrice, tapez votre nom d'utilisateur (ou le nom d'utilisateur que vous prévoyez d'utiliser lorsque vous vous inscrivez en tant que nouveau `Jenkins` utilisateur) et cliquer sur `Ajouter`.
  + Donnez-vous un accès complet en vérifiant toute la ligne pour votre nom d'utilisateur.
  + Répétez l'opération pour les autres utilisateurs qui méritent un accès complet. La configuration devrait ressembler à l'image ci-dessous :


![Alt Text](images/image29.jpeg)

+ Cliquez sur `Enregistrer` au bas de la page. Vous serez ramené à la première page. `Jenkins` est désormais sécurisé avec succès.
+ Redémarrez `Jenkins` (redémarrage du service `Jenkins` sous `Linux`). Si vous configurez un service comme `NIS, Active Directory ou LDAP`, vous pouvez désormais vous connecter à `Jenkins` en utilisant vos informations d'identification réseau. 
  + Si vous utilisez la propre base de données d'utilisateurs de `Jenkins`, créez un compte utilisateur pour vous-même : 
    + `Cliquez` sur le lien `Connexion` dans la partie supérieure droite de la page 
      + `Choisissez Créer` un compte `Spécifiez` le nom d'utilisateur que vous avez utilisé à l'étape ci-dessus et remplissez le reste.
      + Si tout fonctionne bien, vous êtes maintenant connecté en tant que vous-même avec les autorisations.
      + Si quelque chose ne va pas, suivez ceci pour réinitialiser les paramètres de sécurité.
      

## Configuration Globale Des Outils

+ `Jenkins` s'intègre à une variété d'outils. Dans le travail de `build`, nous avons vu qu'il s'intègre à `git et maven`.
+ De même, vous pouvez installer d'autres outils sur votre système d'exploitation ou les installer à partir de cette page.
+ De plus, nous avons parfois besoin de différentes versions de `Java, Maven ou Git, etc`.
+ Nous pouvons également gérer plusieurs versions des outils à partir de cette page.

![Alt Text](images/image30.jpeg)


1. Sur votre ordinateur maître, accéder à Gérer `Jenkins` > `Gérer les noeuds`.
2. Nouveau noeud --> Entrez le nom du noeud.
3. Sélectionnez `Dump Slave` --> Appuyez sur `OK`.

![Alt Text](images/image31.jpeg)

4. Remplissez les champs suivants : 

  + a. Définissez un certain nombre d'exécuteurs (un ou plusieurs) selon vos besoins.
  
  + b. Définissez une racine `FS` distante, un répertoire personnel pour le maître sur la machine esclave.
    
    + i. Pour un esclave `Windows`, utilisez quelque chose comme : `C:\Jenkins\`.
    + ii. A FAIRE : ajouter des détails.
    
  + c. Sélectionnez le paramètre d'utilisation approprié : 

    + i. Pour un travailleur supplémentaire : Utiliser cet esclave autant que possible.
    + ii. Pour les travaux spécialisés : laissez cette machine uniquement pour les travaux liés.
  
  + d. Méthodes de lancement : 

    + i. Un moyen simple de contrôler un `esclave Windows` consiste à utiliser les `agents esclaves` de lancement via `Java Web Start`(recommandé pour Windows).
    + ii. A FAIRE : ajoutez des étapes pour d'autres méthodes.
    
  + e. Disponibilité --> Gardez cet esclave en ligne autant que possible.

    + i. A FAIRE : ajoutez des détails pour chaque option.
    
  + f. Appuyez sur `OK`.


![Alt Text](images/image32.jpeg)


5. Vous devez maintenant connecter votre machine `esclave au maître` en suivant les étapes suivantes.

+ a. `Ouvrez` un navigateur sur la machine `esclave` et accédez à l'`URL` du serveur maître `Jenkins` (http://youjenkinsmaster:8080).
+ b. Allez dans `Gérer Jenkins` `>` `Gérer les noeuds`, cliquez sur la machine esclave nouvellement crée. Vous devrez vous connecter en tant que personne disposant de l'autorisation esclave `Connecter` si vous avez configuré la sécurité globale.
+ c. Cliquez sur le bouton `Lancer` pour lancer l'agent depuis le navigateur sur l'esclave.

![Alt Text](images/image33.jpeg)


+ Si vous rencontrez un problème de connexion, vous pouvez alors agrandir les fenêtres contextuelles pour voir le `port maître` utilisé et vérifier la configuration de votre réseau `(pare-feu, redirection de port, ...)`.

![Alt Text](images/image34.jpeg)

e. Vous devriez maintenant voir la machine esclave connectée sous les `Noeuds`.

6. Si vous souhaitez que le service s'exécute au démarrage de la machine `esclave`, procédez comme suit (instructions Windows uniquement) :

   + 1. Dans le programme de l'agent esclave exécuté sur votre machine.
   + 2. Cliquez sur `Fichier` `-->` Installer en tant que service Windows.


![Alt Text](images/image35.jpeg)


+ Notez que cette fonctionnalité nécessite `Net Framework 3.5`.

  + 3. Démarrez, tapez `Services` et sélectionnez le programme `Services`.
  + 4. Recherchez `Jenkins Slave` dans la liste, double-cliquez pour l'ouvrir.
  + 5. Sélectionnez `Typede démarrage --> Automatique`.
  + 6. Accédez à l'onglet `Connexion`, modifiez la connexion en tant qu'utilisateur de votre choix (compte utilisateur spécial `Jenkins` recommandé).
  + 7. Assurez-vous que la connexion automatique est définie pour la machine esclave pour le compte utilisateur, puis la `VM` (ou ordinateur physique) doit se connecter et être disponible en cas de besoin.
  

#### Ajout d'un noeud Esclave Linux

+ Configurez d'abord noeud.

![Alt Text](images/image36.jpeg)

## Projet d'intégration continue

+ Nous allons mettre en place un projet qui construira `l'artefact`, le versionnera et téléchargera `l'artefact versionné` dans un référentiel de logiciels.

#### Lien

+ Les `référentiels de logiciels ou les gestionnaires de référentiels` deviennent un élément central des projets d'intégration continue et de livraison continue.
+ Nous l'avons vu dans notre deuxième tâche de construction, chaque fois que nous exécutons la tâche de construction, elle crée un `artefact gameoflife.war`.
+ Cet `artefact` sera remplacé à chaque fois que nous exécuterons le travail.
+ Si nous générons un `artefact` qui ne fonctionne pas ou si nous rencontrons des problèmes, nous devrons peut-être revenir à la version précédente de `l'artefact`.
+ Si nous commençons à gérer les versions des `artefacts` dans `Jenkins`, nous pourrions remplir l'espace disque `Jenkins` très rapidement car ces tâches s'exécutent plusieurs fois par jour.
+ Pour cela, nous devrions disposer d'un mécanisme de gestion des versions et de stockage de notre `artefact` versionné dans un endroit centralisé.

+ Dans ce but précis, nous pouvons utiliser `Nexus Repository Manager`.

![Alt Text](images/image37.jpeg)

+ Il y a d'autres avantages à cela. Il fournit un référentiel hébergé afin que toute personne disposant des informations d'identification appropriées puisse télécharger l'artefact.
+ Par exemple, à partir de nos scripts de déploiement, nous pouvons sélectionner notre artefact depuis `Nexus` et le télécharger vers un emplacement cible comme le serveur `Tomcat`.


#### Configuration Du Projet

```
          Acces Jenkins server from browser
          ---------------------------------
          http://<jenkinsIP>:8080
          ----------------------
```

+ Configuration du plugin `Jenkins`
+ Installer les plugins : 

  + 1. Le plugin `Git`. Récupérez le code source depuis `github`. Intègre `Jenkins` avec `Git`.
  + 2. Le plugin `Zentimestamp ` : 
    + Créez une variable nommée `$BUILD_TIMESTAMP`qui peut être utilisée pour versionner/nommer notre `artefact`.
    + Après avoir installé le plugin, nous devons définir sa valeur depuis la page `Configurer` le système.
    + `Gérer Jenkins` => `Configurer le système` => `Propritétés globales`.


![Alt Text](images/image37jpeg.jpeg)

3. Plugin `Nexus`. Télécharger notre `artefact` versionné dans le référentiel `Nexus`. Intègre `Nexus` avec `Jenkins`.

#### Créer une nouvelle tâche de Build

+ `Nouvel élément` => `Entrez le nom du projet` => `Sélectionnez le projet freestyle`.

![Alt Text](images/image38.jpeg)

+ Sélectionnez `Git` -> `Entrez l'URL du projet git GameOfLife (https://github.com/wakaleo/game-of-life.git`

![Alt Text](images/image39.jpeg)

+ Ajouter une étape de construction -> Invoquer un projet `Maven` de niveau supérieur -> Dans `Objectifs` entrez `Installer`.

![Alt Text](images/image40.jpeg)

+ `Enregistrer -> Construire maintenant`

#### Vérification de la construction

+ Dans le tableau de bord de votre projet => Allez dans l'espace de travail => `gameoflife-web` => `target`.
+ Vous devriez voir `gameoflife.war`.


#### Configuration du Nexus

+ Nous allons configurer le serveur `Nexus` sur `CentOS` dans ce tutoriel.
+ Créez une instance `CentOS vm` ou `cloud` et connectez-vous-y.
+ Suivez les étapes ci-dessous pour configurer `Nexus` :

![Alt Text](images/image41.jpeg)

+ Accessing `Nexus` dashboard
  + From browser hit `URL` `<Nexus server IP>:8080/nexus`.
  + Click login button and enter the credentials. `(admin/admin123)`
  + Create hosted repository named `gol-repo` will all default settings.

![Alt Text](images/image42.jpeg)


#### Configurez le Plugin Nexus pour pousser l'artefact vers le référentiel Nexus

+ Ouvrez le travail de `build Jenkins` => Ajouter une étape de `build` => Télécharger d'artefacts `Nexus`.

![Alt Text](images/image43a.jpg)

+ Si vous exécutez ce travail plusieurs fois, vous verrez à chaque fois que nous obtiendrons un `artefact` avec un nouveau nom.
+ A tout moment, nous pouvons utiliser des versions plus anciennes de l'`artefact` si quelque chose tombe en panne dans une version plus récente.


## Analyse de code statique pour le projet de développement Game of Life

+ Qu'est-ce que `l'analyse de code statique ?`

  + `L'analyse statique du code`(également appelée `analyse statique du coe source`) et généralement effectué dans le cadre d'une révision du code (également appelée `test en boîte blanche`) et est effectuée lors de la phase de mise en oeuvre d'un cycle de développement de sécurité `(SDL)`.
  + `L'analyse de code statique` fait généralement référence à l'exécution d'outils d'analyse de code statique qui tentent de mettre en évidence d'éventuelles vulnérabilités dans le code source <<statique>> (non exécuté) en utilisant des techniques telles que `l'analyse de contamination e l'analyse de flux de données`.

+ Etapes : 

  + 1. Installez le plugin `checkstyle`
  + 2. Dans l'étape de construction `Maven`, mettez à jour les objectifs comme indiqué ci-dessous.
       ![Alt Text](images/image45.jpeg)
  + 3. Cliquez sur `Action de post-construction` et sélectionnez `Publiez les résultats de l'analyse du style de contrôle`.
       ![Alt Text](images/image46.jpeg)
  + 4. Enregistrer le projet et exécutez-le au moins deux fois
  + 5. Accédez au tableau de bord des tâches de développement et consultez le graphique de tendance du style de contrôle.
       ![Alt Text](images/image47t.jpeg)
  + 6. Cliquez sur les avertissements de style de contrôle et voyez l'analyse en détail.
       ![Alt Text](images/image48.jpeg)

## Livraison continue avec Jenkins

+ Nous allons voir maintenant comment se déroule le déploiement de `Jenkins` vers le serveur `Tomcat`.
+ Il s'agira d'un projet de livraison continue à part entière utilisant `Jenkins`.
+ Nous devrons configurer deux serveurs `Tomcat` sur lesquels nous déploierons notre `artefact`.


#### Configuration de Tomcat

+ Connectez-vous en tant qu'utilisateur `root`

![Alt Text](images/image48a.jpg)

+ Donnez à `Tomcat` l'autorisation d'exécuter le script `start & stop`.

![Alt Text](images/image48b.jpg)

#### Ouvrez le navigateur et vérifiez le service Tomcat

+ `http://tomcatIP:8080`

#### Définissez l'utilisateur, le mot de passe et le rôle pour le serveur Tomcat

![Alt Text](images/image48c.jpg)


#### Remplacer le contenu mentionné ci-dessous

![Alt Text](images/image48d.jpg)


#### Configuration du projet

+ Ce projet est un `pipeline de construction complet` qui construire `Java SC`, créera un package `war`, exécutera une analyse de code statique, déploiera le package sur le serveur de préparation `Tomcat` et le déploiera sur le serveur de production `Tomcat`.
+ `Le pipeline` comprend le travail `Jenkins` mentionné ci-dessous travaillant ensemble pour créer `l'intégralité du pipeline de livraison continue`.

+ 1. `Travail de package` - Ce travail extraira le code source du référentiel `git`, utilisera `Maven` pour créer le code, archiver les `artefacts`, déclenchera le `travail d'analyse de code statique et le travail de déploiement intermédiaire`.
+ 2. `Analyse de code statique` - Ce travail extraira le code source du référentiel `git`, utilisez `Maven` pour exécuter une analyse de code de style de contrôle et publier un graphique pour `STA`.
+ 3. `Déployer sur le serveur intermédiaire Tomcat` - Ce travail copiera l'`artefact .war` du travail de package vers le travail de déploiement, déploiera les artefacts sur le serveur `Tomcat` intermédiaire et déclenchera le travail de déploiement `Prod`.
+ 4. `Déployer sur le serveur Prod Tomcat` - Ce travail copiera l'`artefact war` du travail de package vers le travail de déploiement, déploiera les artefacts sur le serveur `Tomcat` de préparation et déclenchera le travail de déploiement `Prod`.

![Alt Text](images/image49.jpeg)


#### Conditions préalable : 

+ 1. `Serveur Jenkins` : le serveur `Jenkins` doit avoir `openjdk 1.7, Git, Maven` (Suivez la documentation de configuration de `Jenkins`).
+ 2. `Plugins` : `git, maven, copier les artefacts, déployer dans un conteneur, vérifier le style, créer un pipeline`.
+ 3. `Serveur Tomcat intermédiaire` : Créer une instance `vm ou ec2` avec `Ubuntu OS` et suivez la documentation de configuration de `Tomcat`.
+ 4. `Prod Tomcat Server` - Créez une instance `vm ou  ec2` avec `Ubuntu OS` et suivez la documentation de configuration de `Tomcat`.


#### Créer des jobs Jenkins

+ 1. `Package CJP` - Créez un nouveau travail avec le nom du package `CJP`, projet `freestyle`. Reportez-vous aux captures d'écran mentionnées ci-dessous pour configurer le travail.

![Alt Text](images/image50.jpeg)

+ 2. `CJP-code-analysis` - Créez un nouveau travail avec le nom `CJP-code-analysis, projet freestyle`.

![Alt Text](images/image51.jpeg)

+ Reportez-vous aux captures d'écran mentionnées ci-dessous pour configurer le travail.

![Alt Text](images/image52.jpeg)

+ 3. `CJP-Deploy-Stage` : Créez un nouveau travail avec le nom `CJP-Deploy-Stage, projet freestyle`. Reportez-vous aux captures d'écran mentionnées ci-dessous pour configurer le travail.

![Alt Text](images/image53jpeg.jpeg)

+ `Deploy-Prod` : Créez un nouveau travail avec le nom `CJP-Deploy-Prod, projet freestyle`. Reportez-vous aux captures d'écran mentionnées ci-dessous pour configurer le travail.

![Alt Text](images/image54.jpeg)


+ Accédez au tableau de bord principal de `Jenkins`.
+ Cliquez sur le symbole `+`.

![Alt Text](images/image55.jpeg)


## Déclencheurs de construction Jenkins

+ Jusqu'à présent, nous avons vu comment exécuter des tâches `Jenkins` manuellement en cliquant sur le bouton `Build Now`.
+ Mais il existe d'autres moyens par lesquels les tâches peuvent être exécutées, appelés `déclencheurs de construction`.

![Alt Text](images/image56t.jpeg)

#### Déclencher la construction à distance

+ Nous pouvons utiliser ce déclencheur si nous voulons exécuter le travail à partir d'un emplacement distant, comme à partir d'un script ou depuis `Github` ou tout autre outil pouvant accéder à l'`URL`.
+ Un exemple typique de cette fonctionnalité serait de déclencher une nouvelle construction à partir du `script hook` du système de contrôle de source, lorsque quelqu'un vient de valider une modification dans le référentiel, ou à partir d'un `script` qui analyse les notifications par courrier électronique de votre contrôle de source.
+ Vous devrez fournir un jeton d'autorisation sous la forme d'une chaîne afin que seuls ceux qui le connaissent puissent déclencher à distance les builds de ce projet.

![Alt Text](images/image57.jpeg)

+ Vous pouvez maintenant utiliser `l'URL` avec le jeton `JENKINS_URL/job/beandeploy/build?token=TOKEN_NAME` pour appeler ce travail à partir de :

  + `CLI` comme la commande `curl`
  + `curl http://username:password@192.168.1.9:8080/job/beandeploy/build?token=electric`
  + Via un script
  + Depuis un navigateur
  + `Github Webhooks`
+ Dans le dépôt `Github`, accédez à `Paramètres => Webhooks => Entrez l'URL Jenkins et le Jeton => Ajouter un Webhook`.
+ Désormais, chaque fois qu'il y a un `commit` dans le dépôt `git`, il déclenchera le travail `Jenkins` en appuyant sur l'URL distante de `Jenkins`.


#### Construisez après la construction d'autres projets.
+ Il s'agit de définir le travail en aval d'un autre travail. Mentionnez le nom du travail en amont, une fois le travail en amont terminé avec succès, notre travail sera déclenché.

![Alt Text](images/image58.jpeg)


#### Construire Périodiquement

+ Si nous souhaitons planifier l'exécution de notre travail, par exemple tous les soirs à 20 heures, nous pouvons utiliser un format `cronjob` pour spécifier l'heure.

![Alt Text](images/image59.jpeg)

+ Ce champ suit la syntaxe de `cron` (avec des différentes mineures).
+ Plus précisément, chaque ligne se compose de 5 champs séparés par des tabulations ou des espaces :

```
MINUTE HOUR DOM MONTH DOW
MINUTE : Minutes dans l'heure (0 à 59)
HOUR : L'heure du jour (0 à 23)
DOM : Le jour du mois (1 à 31)
MONTH : Le mois (1-12)
DOW : Le jour de la semaine (0-7) où 0 et 7 sont dimanche
```

#### Sondage SCM

+ C'est similaire à `cronjob`, mais au lieu d'exécuter le travail à intervalles réguliers, il vérifiera s'il y a un nouveau `commit` dans le dépot `VCS` comme celui de `github`, puis exécutera le travail.


## Intégration Sonarqube Jenkins

![Alt Text](images/image60.jpeg)


#### Documenté Par Karunakar G.

+ `SonarQube` est une plate-forme open source pour l'inspection continue de la qualité du code.
+ Elle rendra compte du code dupliqué, des normes de codage, des tests unitaires, de la couverture du code et de la complexité du code.
+ `SonarQube` peut fournir un endroit central pour visualiser et définir les règles utilisées lors de l'analyse des projets.
+ Ces ensembles de règles sont organisés en profils de qualité. Chaque membre de l'organisation peut voir quelles règles sont appliquées à son projet.
+ Chaque administrateur de projet peut choisir quel profil de qualité est utilisé pour le projet.

<br/>

+ `Plugins` requis
  + Scanner `SonarQube`
  + Processus du scanner `Maven`
  
+ `SonarCode` dans `Jenkins`

  + Extraire le code de `Git`
  + Créer et exécuter des `tests unitaites`
  + Analyse `SonarQube` avec les scanners `sonarqube`.
  + Transférez les rapports de couverture d'analyse `SonarQube` vers le tableau de bord `SonarQube`.
  + Nous pouvons stocker les données `SonarQube` dans `DataBase (MySQL)`.
  + Déployez les applications sur le serveur.
  
+ Cycle de vie de `SonarQube`

![Alt Text](images/image61.jpeg)


####  Condition préalable à l'exercice

+ Pour l'exercice de `SonarQube`, nous avons besoin de deux instances `ec2` avec les détails ci-dessous. Par l'instance `Jenkins`.

  + `OS - Ubuntu 16.10`
  + `Tapez - t2.micro`
  + Clé de sécurité pour `Jenkins (.pem)`
    + Groupe de sécurité pour `Jenkins`
    + Tapez `Custom TCP -> Port:8080->source MyIP`
    + `SSH -> Port22->sourceMyIP`


![Alt Text](images/image62.jpeg)

+ Pour l'instance `SonarQube`

  + Système d'exploitation - `Ubuntu 16.10`
  + Type - `t2.meduim`
  + Clé de sécurité pour `Sonarqube (.pem)`

+ Groupe de sécurité pour `SonarQube`

  + `Type Personnalisé TCP -> Port 9000 -> source MyIP`
  + `Type Personnalisé TCP -> Port 8080 -> source JenkinsSg`
  + `Type Personnalisé TCP -> Port 8080 -> source MyIP`
  + `SSH -> Port 22 -> source MyIP`

![Alt Text](images/image63.jpeg)

#### Procédure d'installation de SonarQube dans Ubuntu 16.10 - Conditions préalables pour configurer SonarQube :

+ Instance `EC2 Ubuntu`
  + `Java-8-oracle`
  + `Sonarqube` version `5.6.6`
  + Serveur `mysql 5.7`

+ Ajout de `Java PPA` à notre référentiel `Ubuntu`.

![Alt Text](images/image64.jpeg)

+ Mise à jour du référentiel `apt`

![Alt Text](images/image65.jpeg)

+ Installation de `Java` sur l'instance `EC2 Ubuntu 16.10`

![Alt Text](images/image66.jpeg)

+ Ici, appuyez sur `OK`

![Alt Text](images/image67.jpeg)

+ Ici, appuyez sur `OK`

![Alt Text](images/image68.jpeg)

+ Ici, nous créons un lien symbolique pour `Java = Java par défaut`

![Alt Text](images/image69.jpeg)

+ Installation du `SonarQube`

![Alt Text](images/image70.jpeg)


+ Ici, nous installons `Unzip`. Décompresser le fichier `Zip SonarQube`.

![Alt Text](images/image71.jpeg)

#### Procédure d'installation de MySQL dans le serveur SonarQube et configuration

+ Installez le serveur `MySQL`

![Alt Text](images/image72.jpeg)

+ Configurez l'adresse de liaison `mysql` avec l'`adresse IP SonarQube Satart` le serveur `MySQL`.

![Alt Text](images/image73.jpeg)

+ Modifiez la configuration du `sonar` dans `sonarserver`

![Alt Text](images/image74.jpeg)


<br/>

```
=> Dans la section Build Projet maven de niveau supérieur
=> Et exécuter le scanner SonerQube
=> Informations d'identification pour les propriétés SonarQube DashBoard et Sonar dans SonarScanner JOB

sonar.projectKey = gameoflife
sonar.projectName = gameoflife
sonar.projectVersion = 1.0
sonar.login = admin
sonar.password = 
sonar.administrateur.sources =
sonar.binaries = gameoflife-web/target/classes/com/wakaleo/gameoflife/webtests/controllers/
sonar.junit.reportsPath = gameoflife-web/target/surefire-reports
sonar.jacoco.reportPath = gameoflife-web/target/jacoco.exec
```

+ Cet aperçu montre les propriétés et les informations d'identification du `SonarQube`.

![Alt Text](images/image75.jpeg)


```
=> Après avoir entré les propriétés du sonar, enregistrez le projet et accédez à Build now,
=> Ci-dessous des instantanés montrant ce processus de construction ainsi que les tests du scanner sonar
=> Après le succès, le travail dans lequel les fichiers et rapports sonartest dans Var/lib/jenkins/workspace, nous devons donc fournir ces fichiers et rapports dans sonarDasboard pour voir le résultat
```

![Alt Text](images/image76.jpeg)

+ Une fois qu'un scanner `SonarQube` a fini d'analyser votre code, le résultat de l'analyse (sources, problèmes, métriques) - le rapport d'analyse - est envoyé au serveur `SonarQube` pour traitement final par `Compute Engine`.
+ Dans ce `SonarDashboard` contient : 

  + Couverture du code
  + Bugs
  + odeurs de code
  + vulnérabilités
  + tests unitaires
  + Duplications

![Alt Text](images/image77.jpeg)

#### Notification de Réussite/Echec
+ Une fois l'analyse effectuée, un rapport est envoyé au serveur `SonarQube` pour être intégré.
+ A la fin de cette intégration, un mécanisme de `webhook standard` vous permet d'avertir n'importe quel système externe de faire ce que vous voulez: déclencher une alarme, mettre à jour un panneau mural et avertir une salle de dimension.


## Artefact

#### Documenté Par Pavan Kumar Ranjit.

+ En tant que premier et unique gestionnaire de référentiel d'artefacts universel sur le marché, `JFrog Artifactory` prend en charge les progiciels créés par n'importe quel langage ou technologie.
+ `Artifactory` est le seul de référentiels prêt pour l'entreprise disponible aujourd'hui, prenant en charge les registres `Docker` sécurisés, en cluster et à haute disponibilité.
+ S'intégrant à tous les principaux outils `CI/CD et DevOps, Artifactory` fournit une solution de bout en bout, automatisée et à toute épreuve pour suivre les artefacts du développement à la production.

#### Qu'est-ce qu'un gestionnaire de référentiel binaire ?

+ Il s'agit d'une passerelle unique par laquelle vous accédez aux artefacts externes et stockez vos propres artefacts de construction.
+ En centralisant la gestion de tous les artefacts binaires, il surmonte la complexité résultant de la diversité des types binaires, de leur position dans le `workflow` et les dépendances entre eux.

#### Les 10 principales raisons pour lesquels vous devriez utiliser un gestionnaire de référentiel binaire.

1. Augmentez la vitesse de construction et les artefacts `proxy` à distance. Eliminez les téléchargements rédondants en mettant automatiquement en cache les artefacts pour toute l'équipe de développement.

<br/>

2. Gérez le cycle de vie des artefacts. Promouvoir les artefacts depuis le développement en passant par l'assurance qualité jusqu'à la production et la distribution.

<br/>

3. Evitez les violations de licence. Recevez des alertes sur des violations potentielles. Contrôlez toutes les licences utilisés dans votre logiciel en gérant les artefacts tiers dans un emplacement central.

<br/>

4. Gardez les versions reproductibles. Intégrez-vous aux principaux serveurs `CI` et gardez les `builds` reproductibles avec des informations de `build` exhaustives pour suivre et protéger tous les artefacts utilisés par vos `builds CI`.

<br/>

5. Appliquez la sécurité du module. Contrôlez l'accès et suivez toutes les modifications apportées aux artefacts. Bloquez les demandes externes indésirables et définissez qui peut créer, supprimer ou écraser des artefacts.

<br/>

6. Consommation du module de contrôle. Définir les règles d'accès pour les utilisateurs et les groupes qui consomment des artefacts.

<br/>

7. Partagez des artefacts entre les équipes. Distribuez facilement les artefacts produits par différentes équipes de votre organisation et partagez-les en tant que dépendances entre les équipes selon vos besoins.

<br/>

8. Nettoyer l'encombrement des artefacts `CI`. Nettoyez automatiquement les artefacts d'intégration et d'instantané produits pendant le processus de création de `CI`.

<br/>

9. Localisez instantanément les artefacts `CI`. NTrouvez facilement des artefacts grâce à des capacités de recherche avancées, notamment la recherche de classes, exécutez des opérations groupées sur l'ensemble de résultats.

<br/>

10. Automatisez pendant que vous `REPOSEZ`. Automatisez et intégrer tous les aspects de la gestion des artefacts au sein de votre organisation à l'aide d'une puissante `API REST`.

### Le référentiel le plus puissant du marché

#### Blocage du téléchargement

+ Nous savons tous qu'il vaut mieux prévenir que guérir. Il en va de même pour vos systèmes logiciels.
+ Supprimer les dépendances potentiellement dangereuses une fois qu'elles sont déjà profondément ancrées dans votre logiciel de production peut nécessiter la recherche d'un composant alternatif, la refactorisation de votre logiciel et l'exécution de plusieurs cycles d'assurance qualité de revenir enfin là où vous étiez.
+ Grâce à l'intégration d'`Artifactory avec Xray`, vous pouvez éviter ce type de scénario en empêchant les artefacts `X-ray` a détectés comme présentant des problèmes ou des vulnérabilités d'être téléchargés à partir de vos référentiels et utilisés an premier lieu.


#### Chef 

+ Le concept `Infrastructure as Code` a été largement adapté par la plupart des services informatiques d'entreprise.
+ `Chef` fournit aux services informatiques et `DevOps` les outils dont ils ont besoin pour gérer les différents environnements dont ils ont besoin pour démarrer.
+ Grâce à la prise en charge des référentiels `Chef Cookbook, Artifactory` apporte une nouvelle dimension à `Infrastructure as Code`.
+ En gérant les packages de configuration via un référentiel binaire, les organisations informatiques et `DevOps` qui travaillent dur sur la gestion de la configuration avec `Chef` disposent de bien plus de fonctionnalités à portée de main.


#### Puppet

+ Le concept `Infrastructure as Code` a été largement adapté par la plupart des services informatiques d'entreprise.
+ `Puppet` fournit aux services informatiques et `DevOps` les outils dont ils ont besoin pour gérer les différents environnements dont ils ont besoin pour démarrer.
+ Grâce à la prise en charge des référentiels `Puppet, Artifactory` apporte une nouvelle dimension à `Infrastructure as Code`.
+ En gérant les packages de configuration via un référentiel binaire, les organisations informatiques et `DevOps` qui travaillent dur sur la gestion de la configuration avec `Puppet` disposent désormais de bien plus de fonctionnalités à portée de main.


#### Docker

+ 