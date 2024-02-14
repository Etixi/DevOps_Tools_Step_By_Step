# Scripts Python


## Introduction A Python

+ `Python` est un langage de script de haut niveau, `interprété, interactif et orienté objet`.
+ `Python` est conçu pou être hautement lisible.

#### Alors Pourquoi y a t-il un didacticiel dans ce Livre

+ Lorsque nous écrivons un `script bash` pour effectuer `l'automatisation` nous avons lentement augmenté la complexité de notre code.
+ Notre code est devenu de plus en plus complexe. De plus, nous n'avons aucune autre fonctionnalité dans le `script bash` en dehors de la simple automatisation des tâches `Linux`.
+ `Python` est l'un des langages de programmation les plus simples du marché.
+ Etant simple, cela nous offre de nombreuses fonctionnalités et bibliothèques qui étendent la puissance de `Python`.
+ `Pyhon` est très extensible. Nous pouvons utiliser `Python` pour exécuter l'automatisation `Linux`, l'automatisation `Windows`, l'automatisation `Cloud` et plusieurs autres. Il est de nature très polyvalent.


#### Python est Interprété

+ `Python` est traité au moment de l'exécution par l'interpréteur. Vous n'avez pas besoin de compiler votre programme avant de l'exécuter. Ceci est similaire à `PERL et PHP`.


#### Python est Interactif

+ Vous pouvez en fait vous asseoir devant une invite `Python` et interagir avec l'interpréteur directement pour écrire vos programmes.

#### Python est Orienté Objet

+ `Python` prend en charge le style ou la technique de programmation orientée objet qui encapsule le code dans les objets.

#### Python est un Langage Pour les Débutants

+ `Python` est un excellent langage pour les programmeurs débutants et prend en charge le développement d'un large éventail d'applications, du simple traitement de texte aux navigateurs `WWW` en passant par les jeux.


## Installation de Python

#### Installation de Windows

+ Voici les étapes pour installer `Python` sur une machine `Windows`.

    + Ouvre votre navigateur Web et accéder à [python](http://www.python.org/download/).
    + Suivez le lien vers le fichier `python-XYZ.msi` du programme d'installation de `Windows` où `XYZ` est la version que vous devez installer.
    + Pour utiliser ce programme d'installation `python-XYZ.msi`, le système `Windows` doit prendre en charge `Microsoft Installer 2.0`.
    + Enregistrez le fichier d'installation sur votre ordinateur local, puis exécutez-le pour savoir si votre ordinateur prend en charge `MSI`.
    + Exécutez le fichier téléchargez.
    + Cela fait apparaitre l'installation de `Python`, qui est vraiment simple à utiliser.
    + Acceptez simplement les paramètres par défaut, attendez que l'installation soit terminée.
    + Après installation, nous devons configurer `Python` dans le `PATH` dans la variable d'environnement système.

#### Installer Linux

+ Le système `Linux` est livré par défaut avec `Python` installé, il n'est donc pas nécessaire de prendre des mesures pour le système `Linux`.


## Syntaxe de Base

<br/>

#### Programmation Interactive Python

+ Ouvre le `shell Linux` => Tapez `Python` et appuyez sur `Entrée`, cela vous déposera dans le `shell/interpréteur python`.

![Alt Text](images/image1.jpeg)

+ Tapez le texte suivant à l'invite `Python` et appuyez `Entrée`.

![Alt Text](images/image2.jpeg)

<br/>

<h4>Script Python</h4>

+ Créez un fichier nommé `hello.py`, `py` signifie print et est une extension du fichier `python`.
+ Ajoutez le contenu mentionné ci-dessous et enregistrez le fichier.

![Alt Text](images/image3.jpeg)

+ **Ligne 1 :** `#!` est le `charset shebang` comme nous le savons grâce aux `scripts bash`, le chemin de l'interprète est `/usr/bin/python`.
  + Vous pouvez trouver le chemin de l'interpréteur `Python` dans votre système `Linux` en indiquant `quel python`.
  + L'appel de l'interpréteur avec un paramètre de script démarre l'exécution du script et se poursuit jusqu'à ce qu'il soit terminé.
  + Une fois le script terminé, l'interpréteur n'est plus actif.
+ **Ligne 2 :** `print` est la commande `python` qui imprime les messages.


#### Exécution du Script Python

+ Maintenant, essayez d'exécuter ce programme comme suit : 

  + Exécution du script `Python` : 

![Alt Text](images/image4.jpeg)

#### Lignes et retrait

+ Les instructions du programme `Python` sont écrites les unes au-dessus des autres, comme le montre l'exemple suivant : 

![Alt Text](images/image5.jpeg)

+ Le programme de 3 lignes ci-dessus est correct et s'exécutera pour produire le résultat attendu.
+ Le programme ci-dessous générera une erreur de syntaxe à cause du caractère espace inséré au début de la deuxième ligne.

![Alt Text](images/image6.jpeg)

+ `Python` évalue de la deuxième instruction d'impression comme un bloc de code à l'intérieur instruction d'impression.
+ Ainsi, sa deuxième impression de réflexion est sous la première déclaration d'impression, mais c'est une déclaration distincte.
+ `Python` ne fournit aucune accolade pour indiquer des blocs de code pour les définitions de classes et de fonctions ou contrôle de flux.
+ Les blocs de code sont indiqués par une indentation de ligne, qui est strictement appliquée.

#### Citation en python

+ Nous pouvons utiliser des guillemets en `Python` pour entourer `le texte/les chaînes`.
+ Il existe trois types de citations en `python`.

  + **Guillemet simple ('')'**
    + Tout ce qui se trouve entre guillemets est considéré comme une chaîne littérale et ne sera pas évalué par `python`.
  + **Guillemets doubles ("")**
    + Peuvent être utilisés lorsque vous avez une variable dans la chaîne qui doit être évalué
+ ``






