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

  + **Guillemet simple (')**
    + Tout ce qui se trouve entre guillemets est considéré comme une chaîne littérale et ne sera pas évalué par `python`.
  + **Guillemets doubles ("")**
    + Peuvent être utilisés lorsque vous avez une variable dans la chaîne qui doit être évalué par python en utilisant le formatage de chaîne `(%)`
  +  **Triple(""or"")**
    + Ceci est utilisé pour écrire une chaîne multiligne ou également appelée chaîne de paragraphe.
  + Par exemple :
    ![Alt Text](images/image7.jpeg)

#### Commentaires en Python
+ Un signe `dièse(#)` est un symbole de commentaire en python. `Python` ignore tout le texte après `#` et ne l'évalue pas.
+ Tous les caractères après le `#` et jusqu'à la fin de la ligne physique font partie du commentaire et l'interpréteur `Python` les ignore.

![Alt Text](images/image8.jpeg)

+ Ceci produit le résultat suivant : `Hello, Python!`

![Alt Text](images/image9.jpeg)


#### Commentaire Multiligne

+ Nous pouvons utiliser une chaîne de paragraphe pour créer un commentaire multiligne. 
+ Tout ce qui se trouve dans la chaîne de paragraphe serait ignoré par `Python`.

![Alt Text](images/image10.jpeg)

## Types de variables

+ Les `variables` sont un stockage temporaire des données en mémoire. Il existe différents types de données.
+ En attribuant différents types de données aux variables, vous pouvez stocker des entiers, des décimales ou des caractères dans ces variables.

#### Affectation de variables
+ Nous n'avons pas besoin de définir les types de variables en python comme les autres langages de programmation.
+ La déclaration de variable se produit automatiquement lorsque nous attribuons une valeur à une variable.
+ Le signe égal `(=)` est utilisé pout attribuer des valeurs aux variables. L'opérande à gauche de l'opérateur `=` est le nom de la variable et l'opérande à droite de l'opérateur `=` est la valeur stocké dans la variable.
+ Par exemple : 

![Alt Text](images/image11.jpeg)

+ Ici, 86, 86.11 et imran sont des valeurs attribuées respectivement aux noms de variables `mynumber, myfloatnumber et myname`.
+ Exécutez le script ci-dessus et vérifiez le résultat.

#### Affectation multiple

+ `Python` vous permet d'attribuer une seule valeur à plusieurs variables simultanément. Par exemple : 

```
              x=y=z=86
```

+ Ici, un objet entier est créé avec la valeur 86 et les trois variables affectées au même emplacement mémoire.
+ Vous pouvez également affecter plusieurs objets à plusieurs variables. Par exemple : 

```
          x,y,z = 86, 11 "imran".
```

+ Ici, les deux objets entiers avec les valeurs 86 et 11 sont affectés respectivement aux variables `x` et `y`, et un objet chaîne avec la valeur `"imran"` est affecté à la variable `z`.


## Types de données Python

+ Les données stockées en mémoire peuvent être de plusieurs types. 
+ Par exemple, l'âge d'une personne est stocké sous forme de valeur numérique et son adresse est stockée sous forme de caractères alphanumériques.
+ `Python` dispose de différents `types de données standards` qui sont utilisés pour définir les opérations possibles sur celles-ci et la méthode de stockage pour chacune d'elles.

#### Python propose 5 types de données standard

+ Numbers
+ String
+ List
+ Tuple
+ Dictionary

+ Si vous utilisez `bash` pour les `scripts`, vous devez sans aucun doute beaucoup utiliser de conditions.
+ En fonction d'une condition, vous décidez si vous devez ou non exécuter certaines commandes sur le système.
+ Une instruction `if` de base dit effectivement que si un test particulier est vrai, alors effectuez un ensemble d'actions donné.
+ Si ce n'est pas vrai, n'effectuez pas ces actions. Si suit le format ci-dessous :

#### Nombre Python

+ Les nombres Python sont de type entier, flottant, long et complexe comme indiqué ci-dessous.

![Alt Text](images/image12.jpeg)

#### Chaînes Python

+ Les chaînes Python sont de simples données texte entourées de guillemets simples ou doubles.

```
          stringvar = 'sample string'
          strvar2 = 'string#2'
```

+ Python autorise des paires de guillemets simples ou doubles.

```
          stringvar = "sample string"
          strval2 = "string#2"
```

![Alt Text](images/image13.jpeg)

+ Le découpage de chaîne peut également être effectué et stocké dans une variable, `slice` signifie un sous-ensemble ou  une paire de la chaîne.

![Alt Text](images/image14.jpeg)


+ Des sous-ensembles de chaînes peuvent être créés par l'opérateur `slice([] et [:])` avec des index commençant à 0 au debut de la chaîne et progressant de `-1` à la fin.
+ Le signe `plus (+)` est l'opérateur de concaténation de chaînes et l'astérisque `(*)` est l'opérateur de répétition. Par exemple :

![Alt Text](images/image15.jpeg)

+ Cela produira le résultat suivant :


![Alt Text](images/image16.jpeg)

#### Listes Python

+ Les `listes` connaissent également un tableau de Python. Il peut stocker plusieurs valeurs de types de données différents dans une variable.
+ Une liste contient des élements séparés par des virgules et placés entre crochets `([])`.
+ C'est similaire aux tableaux en `C` mais la différence entre eux que tous les éléments appartenant à une liste peuvent être de types de données différents.
+ Les valeurs stockées dans une liste sont accessibles à l'aide de l'opérateur `slice([]) et [:])` avec des index commençant à 0 au début de la liste et allant jusqu'à la fin `-1`.
+ Le signe plus `(+)` est l'opérateur de concaténation de liste et l'astérisque `(*)` est l'opérateur de répétition. Par exemple :

![Alt Text](images/image17.jpeg)

+ Cela produit le résultat suivant :

![Alt Text](images/image17a.jpeg)

#### Tuples Python

+ Le `tuple` est un autre type de tableau qui ressemble exactement à une liste, mais les `tuples` sont `immuables`, ce qui signifie que vous ne pouvez pas modifier un tuple tout comme vous ne pouvez pas modifier le contenu d'un `cd-rom`.
+ Un `tuple` est constitué d'un certain nombre de valeurs séparées par des virgules. Les tuples sont placés entre parenthèses `()`.
+ Les tuples peuvent être considérés comme des listes en lecture seule. Par exemple :

![Alt Text](images/image18.jpeg)

+ Cela produit le résultat suivant : 

![Alt Text](images/image18a.jpeg)

+ Le code suivant n'est pas valide avec le tuple, car nous avons tenté de mettre à jour un tuple, ce qui n'est pas autorisé.
+ Un cas similaire est possible avec les listes : 

![Alt Text](images/image19.jpeg)

#### Dictionnaire Python

+ Dans les données du dictionnaire, elles sont stockées sous forme de paire de clé-valeur, contrairement à une liste ou à un tuple où nous n'avons que des valeurs.
+ Vous pouvez penser qu'il s'agit d'un dictionnaire anglais normal où le mot dans la clé et sa signification sont sa valeur.
+ Les dictionnaires de Python sont une sorte de type de table de hachage. Une clé de dictionnaire peut être presque n'importe quel type `Python`, mais il s'agit généralement de combres ou de chaînes.
+ Les valeurs en revanche, peuvent être n'importe quel objet `Python` arbitraire. Les dictionnaires sont entourés d'accolades `({})` et les valeurs peuvent être attribuées et accessibles à l'aide d'accolades `([])`. Par exemple : 

![Alt Text](images/image20.jpeg)

+ Cela produit le résultat suivant : 

![Alt Text](images/image20a.jpeg)

## Opérateurs Python

+ Les opérateurs sont les constructions qui peuvent manipuler la valeur des opérandes.
+ Considérons l'expression `4 + 5 = 9`. Ici, 4 et 5 sont appelés `opérande` et + est appelé `opérateur`.

#### Types d'opérateurs
+ Le langage Python prend en charge les types d'opérateurs suivants.

1. Opérateurs arithmétiques

2. Opérateurs de comparaison (relationnels)

3. Opérateurs d'affectation

4. Opérateurs logiques

5. Opérateur au niveau du bit

6. Opérateur d'appartenance

7. Opérateurs d'identité

+ Opérateurs arithmétiques Python

  + `+ : Addition` - ajoute des valeurs de chaque côté de l'opérateur.
    + `x + y = 110`
  + `- : soustraction` - soustrait l'opérande de droite de l'opérande de gauche.
    + `x - y = -10`
  + `* : Multiplication` - multiplie les valeurs de chaque côté de l'opérateur.
    + `x * y = 200`
  + `/ : Division` - divise l'opérande de gauche par l'opérande de droite.
    + `x / y = 2`
  + `% : Module` - divise l'opérande de gauche par l'opérande de droite et renvoie le reste.
    + `x % y = 0`
  + `** : Exposant` - effectue un calcul exponentiel (puissance) sur les opérateurs.
    + `x ** y = 10 à la puissance 20`

#### Opérateurs de comparaison python

+ Ces opérateurs comparent les valeurs de chaque côté et décident de la relation entre elles.
+ Ils sont également appelés opérateurs relationnels.

![Alt Text](images/image21.jpeg)

+ Une fois exécuté, il renvoie la sortie ci-dessous : 

![Alt Text](images/image21a.jpeg)

#### Opérateurs logiques python

+ Il existe les opérateurs logiques suivants pris en charge par le langage python.
  + Si la variable `a` contient 40 et la variable `b` contient 50, alors : 
    + Si les deux opérandes sont vrais, la condition devient vraie, `(a et b)` est vrai.
    + Si l'un des deux opérandes est différent de zéro, la condition devient vraie, `(a ou b)` est vrai.
    + `Non(a et b)` est faux.
  
#### Opérateurs d'adhésion python.

+ Les opérateurs d'appartenance de `Python` testent l'appartenance à une séquence, telle que des chaînes, des listes ou des tuples.
+ Il existe deux opérateurs d'appartenance comme expliqué ci-dessous : 
  + prend la valeur `true` s'il trouve une variable dans la `séquence` spécifié et `false` dans le cas contraire.

![Alt Text](images/image22.jpeg)

+ Une fois exécuté, le résultat ci-dessous donne : 

![Alt Text](images/image22a.jpeg)

## Prise de décision

+ La `prise de décision` est présente dans chaque langage de programmation.
+ Sur la base d'un scénario de test, le programme décide d'exécuter ou non des instructions/commandes.
+ En python, nous utilisons les mots-clés `if, elif et else` pour prendre des décisions.


#### L'instruction If - Syntaxe

![Alt Text](images/image23.jpeg)

+ Si le scénario de test est vrai, le code du bloc `if` est exécuté.
+ Si l'expression textuelle est fausse, la ou les instructions ne sont pas exécutées.
+ Comme nous l'avons vu précédemment dans la section indentation, pour créer un bloc de code sous toute instruction, nous indentons le code ou lui donnons des espaces.
+ Par exemple, l'instruction `print` se trouve sous le bloc `if`.

```
if True:
  print "Indented three spaces"
```

+ En python, 0 est interprété comme `False` et toute valeur non nulle est `True`.


![Alt Text](images/image24.jpeg)

+ L'instruction `if/else` évalue le scénario de test et exécutera le corps de `if` uniquement lorsque la condition de test est vraie.
+ Si la condition est fausse, le corps est exécuté.


![Alt Text](images/image25.jpeg)

+ Si la condition est fausse, sinon le bloc est exécuté, mais que se passe-t-il si nous voulons évaluer quelques conditions supplémentaires et ensuite décider de l'exécution. 
+ Nous pouvons utiliser `elif` pour mettre plus de conditions dans notre processus de prise de décision, sa forme abrégée `else if`. Si la condition `if` est fausse, il vérifie la condition du prochain bloc `elif` et ainsi de suite.
+ Si toutes les conditions sont fausses, le corps de `else` est exécuté. Le bloc `if` ne peut avoir qu'un seul bloc `else`. Mais il peut avoir plusieurs blocs `elif`.

![Alt Text](images/image26.jpeg)

## Boucles Python

+ Les boucles sont utilisées lorsque vous souhaitez répéter un bloc pendant un nombre de fois fixe ou jusqu'à ce qu'une condition ne soit pas satisfaite. Python nous fournit deux boucles.

#### Boucle While

+ Répétez le bloc de code jusqu'à ce que la condition `while` soit vraie.

![Alt Text](images/image27.jpeg)

#### Boucle for

+ répétez le bloc de code plusieurs fois.

![Alt Text](images/image27a.jpeg)

+ Les `boucles for` sont traditionnellement utilisées lorsque vous disposez d'un bloc de code que vous souhaitez répéter un nombre fixe de fois.
+ L'instruction `Python for` parcourt les membres d'une séquence dans l'ordre, exécutant le bloc à chaque fois.
+ Comparez l'instruction `for` avec la `boucle while`, utilisée lorsqu'une condition doit être vérifiée à chaque itération ou pour répéter un bloc de code pour toujours. Par exemple : 

![Alt Text](images/image28.jpeg)

#### Boucle While Infinie
+ Exemple : `Boucle while` de 1 à l'infini, donc exécutée pour toujours.

![Alt Text](images/image29.jpeg)

#### Boucles While

+ Dans la `boucle while`, le scénario de test est d'abord évalué, si scénario de test est vrai, le corps de la boucle `while` est exécuté et répété jusqu'à ce que le scénario de test soit évalué comme faux.
+ Après chaque itération, le cas de test est évalué. Python interprète toute valeur non nulle comme `True`. `None` et 0 sont interprétés comme faux.

![Alt Text](images/image30.jpeg)

#### Les boucles for

+ La `boucle for` peut parcourir toutes les séquences comme une liste, un tuple pu une chaîne qui sont indexées.
+ Chaque élément de ces types de donnés est indexé et peut être itéré. Ce processus d'itération sur une séquence est appelé `traversée ou traversée dans la nature`.

![Alt Text](images/image31.jpeg)

+ Ici, la variable1 est la variable qui prend la valeur de l'élément à l'intérieur de la séquence à chaque itération.
+ La boucle continue jusqu'à ce que nous atteignions le dernier élément de la séquence. Le corps de la `bucle for` est séparé du reste du code par indentation.

![Alt Text](images/image32.jpeg)

#### Break and continue

+ L'utilisation des `boucles for et while` en Python vous permet d'automatiser et de répéter des tâches de manière efficace.
+ Mais parfois, vous souhaitez intercepter ou modifier le flux ou sortie de la boucle pendant son exécution. 
+ En `Python`, les instructions `break et continue` peuvent modifier le déroulement d'une boucle normale. 
+ Les instructions `break et continue` sont utilisées dans ce cas.

#### Instruction Break De Python

+ L'instruction `break` vous offre la possibilité de sortir d'une boucle lorsqu'une condition externe est déclenchée.
+ Cette condition externe peut être un bloc `if` qui est évalué à vrai quelque part dans l'itération et utilise le mot-clé `break` pour sortir de la boucle.

![Alt Text](images/image33.jpeg)
![Alt Text](images/image33a.jpeg)

#### Instruction continue Python

+ L'instruction `continue` est utilisée pour ignorer le reste du code dans une boucle pour l'itération en cours uniquement.
+ La boucle ne se termine pas mais `continue` avec l'itération suivante :


#### Organigramme de continue

![Alt Text](images/image34.jpeg)
![Alt Text](images/image35a.jpeg)

## Méthodes/fonctions intégrées

+ `Python` dispose de nombreuses fonctions intégrées qui étendent ses capacités. Vous trouverez ci-dessus quelques-unes des méthodes intégrées utiles sur tous les types de données.
+ Consultez la documentation `Python` pour la liste de toutes les méthodes et leurs utilisations.

#### Fonctions de chaîne

+ `capitalize` : met en majuscule la première lettre de la chaîne.

![Alt Text](images/image35.jpeg)

+ `find` : détermine si `str` apparaît dans une chîne ou dans une sous-chaîne.

![Alt Text](images/image36.jpeg)

+ `join` : fusionne (concatène) les représentations sous forme de chaîne des éléments de la séquence `seq` en une chaîne, avec une chaîne de séparation.

![Alt Text](images/image37.jpeg)

+ `rstrip` : supprime tous les espaces de fin de chaîne.

![Alt Text](images/image38.jpeg)

+ `split` : divise la chaîne en fonction du délimiteur `str` (espace s'il n'est pas fourni) et renvoie la liste des sous-chaînes; divisé en au plus nombre de sous-chaînes si donné.

![Alt Text](images/image39.jpeg)

#### Fonctions des listes

+ `append` : ajoute un élément à la fin de la liste.

![Alt Text](images/image40.jpeg)

+ `extend` : combiner deux listes ensemble.

![Alt Text](images/image41.jpeg)

+ `insert` : insère un élément dans la valeur d'index spécifiée.

![Alt Text](images/image42.jpeg)

+ `pop` : supprime l'élément de la liste à une valeur d'index spécifié, la valeur par défaut est le dernier élément.

![Alt Text](images/image43.jpeg)

#### Fonctions du dictionnaire

+ Mettre à jour les élements du dictionnaire

![Alt Text](images/image44.jpeg)

+ Supprimer des éléments du dictionnaire

![Alt Text](images/image45.jpeg)


## Fonctions Python

+ Une `fonction` est un bloc de code organisé et réutilisable utilisé pour effectuer une action unique.
+ Les fonctions offrent une meilleure modularité à votre application et un haut degré de réutilisation du code.
+ Nous avons déjà utilisé certaines fonctions intégrées comme `range(), len(), type(), etc`.
+ Nous allons maintenant apprendre à écrire nos propres fonctions.

#### Règle de fonctions
+ Le bloc fonctionnel commence par le mot-clé `def` suivi du nom de la fonction et des parenthèses. Syntaxe : 

![Alt Text](images/image46.jpeg)

+ Si des arguments doivent être transmis à la fonction, ils doivent être définis sous parenthèses : 

![Alt Text](images/image47.jpeg)


+ Le bloc de code commence par deux points `:`. Syntaxe : 

![Alt Text](images/image48.jpeg)

+ Le mot clé `return` dans le bloc de code quitte la fonction et peut renvoyer une valeur, si aucune valeur n'est renvoyée, la valeur de retour par défaut est `None`. Syntaxe :

![Alt Text](images/image49.jpeg)

![Alt Text](images/image49a.jpeg)


#### Arguments de fonction
+ Vous pouvez appeler une fonction en utilisant les types d'arguments formels suivants : 

  + Arguments obligatoires
  + Arguments de mots clés
  + Arguments par défaut
  + Arguments de longueur variable
  
#### Arguments requis

+ Les arguments obligatoires sont les arguments transmis à une fonction dans l'ordre de position correct.
+ Ici, le nombre d'arguments dans l'appel de fonction doit correspondre exactement à la définition de la fonction.
+ Pour appeler la fonction `printime()`, vous devez impérativement passer un argument, sinon cela donne une erreur de syntaxe comme suit : 

![Alt Text](images/image50.jpeg)

#### Arguments de mots clés

+ Les `arguments de mots clés` sont liés aux appels de fonction.
+ Lorsque vous utilisez des arguments de mots clés dans un appel de fonction, l'appelant identifie les arguments par le nom du paramètre.
+ Cela vous permet d'ignorer des arguments ou de les placer dans le désordre car l'interpréteur `Python` est capable d'utiliser les mots-clés à la fonction `printime()` des manières suivantes.

![Alt Text](images/image51.jpeg)

+ Lorsque le code ci-dessus est exécuté, il produit le résultat suivant : 

```
output : My string
```

+ L'exemple suivant donne une image plus claire. Notez que l'ordre des paramètres n'a pas d'importance.

![Alt Text](images/image52.jpeg)

+ Lorsque le code ci-dessus est exécuté, il produit le résultat suivant :

```
name : miki
age : 50
```

#### Arguments par défaut

+ Un `argument par défaut` est un argument qui prend une valeur par défaut si aucune valeur n'est fournie dans l'appel de fonction pour cet argument.
+ L'exemple suivant donne une idée sur les arguments par défaut, il affiche l'âge par défaut s'il n'est pas transmis : 

![Alt Text](images/image53.jpeg)

+ Lorsque le code ci-dessus est exécuté, il produit le résultat suivant : 

```
Name: miki
Age: 50
Name: miki
Age: 35
```


#### Arguments de longueur variable

+ Vous devrez peut-être traiter une fonction pour plus d'arguments que ce que vous avez spécifié lors de la définition de la fonction.
+ Ces arguments sont appelés arguments de longueur variable et ne sont pas nommés dans la définition de la fonction, contrairement aux arguments obligatoires et par défaut.
+ La syntaxe d'une fonction avec des arguments variables autres que les mots-clés est la suivante : 

![Alt Text](images/image54.jpeg)

+ Un astérisque `(*)` est placé avant le nom de la variable qui contient les valeurs de tous les arguments de variable non mot-clé. 
+ Ce tuple reste vide si aucun argument supplémentaire n'est spécifié lors de l'appel de la fonction. Voici un exemple simple :

![Alt Text](images/image55.jpeg)

+ Lorsque le code ci-dessus est exécuté, il produit le résultat suivant :

![Alt Text](images/image55a.jpeg)

#### La déclaration de retour

+ L'instruction `return[expression]` quitte une fonction, en renvoyant éventuellement une expression à l'appelant.
+ Une instruction `return` sans argument est identique à `return None`. Tous les exemples ci-dessus me renvoient aucune valeur. 
+ Vous pouvez aussi renvoyer une valeur de la fonction comme suit :

![Alt Text](images/image56.jpeg)

#### Moduler Python

+ Les modules en Python sont simplement des fichiers Python avec l'extension `.py`, qui implémente un ensemble de fonctions.
+ Les modules sont importés depuis d'autres modules à l'aide de la commande import.
+ Nous utilisons des modules pour décomposer les gros programmes en petits fichiers gérables et organisés.
+ De plus, les modules permettent la réutilisabilité du code.
+ Nous pouvons définir nos fonctions les plus utilisées dans un module et l'importer, au lieu de copier leurs définitions dans les différents programmes.
+ L'exemple de nom de script est `Operations.py`.

![Alt Text](images/image57.jpeg)

#### Importer mon module

+ Importer un module et appeler des méthodes à l'intérieur.
+ Récupère tous les éléments du module, mais doit faire référence à [module].

![Alt Text](images/image58.jpeg)

#### La déclaration from ... import

+ L'instruction `from` de python vous permet d'importer des attributs spécifiques d'un module dans l'espace de noms actuel.
+ Le `from ... import` a la syntaxe suivante :

```
from Modname Import Name1[, Name2[, ...NameN]]

Example : from myomodule import x
```

+ Importe `x` depuis `mymodule` directement dans cet espace de noms.

![Alt Text](images/image59.jpeg)


+ **Remarque :** Cette instruction n'importe pas l'intégralité du module dans l'espace de noms actuel; il introduit simplement l'élément `fibonacci` du module `fib` dans la table des symboles globales du module d'importation.


#### L'instruction `from ... import * :`

+ Il est également possible d'importer tous les noms d'un module dans l'espace de noms actuel en utilisant l'instruction d'importation suivante :

#### From Modname Import*

+ Cela fournit un moyen simple d'importer tous les éléments d'un module dans l'espace de noms actuel.

![Alt Text](images/image60.jpeg)

#### La fonction Dir()

+ La fonction intégrée `dir()` renvoie une liste triée de chaines contenant les noms définis par un module.
+ La liste contient les noms de tous les modules, variables et fonctions définis dans un module. Voici un exemple simple :

![Alt Text](images/image61.jpeg)

+ Lorsque le code ci-dessus est exécuté, il produit le résultat suivant : 

![Alt Text](images/image61a.jpeg)

+ Ici, la variable de chaîne spéciale `__name__` est le nom du module et `__file__` est le nom du fichier à partir duquel le module a été chargé.

#### Python pour les tâches du système d'exploitation

+ `Python` est très largement utilisé comme langage de script pour automatiser les tâches quotidiennes d'administration système ou même une orchestration à grande échelle de plusieurs systèmes.
+ Le `module OS` en `Python` fournit un moyen d'utiliser les fonctionnalités dépendantes du système d'exploitation.
+ Les fonctions fournies par le `module OS` vous permettent d'interfacer avec le système d'exploitation sous-jacent sur lequel `Python` s'exécute (Windows, Mac ou Linux).
+ Vous pouvez trouver des informations importantes sur votre emplacement ou sur le processus.
+ Avant de commencer, assurez-vous d'avoir importé le module du système d'exploitation `import os`.


![Alt Text](images/image62.jpeg)

## Fabric pour l'automatisation

+ Comme le dit le `README` : 

  + `Fabric` est une bibliothèque `Python (2.5-2.7)` est outil de ligne de commande permettant de rationaliser l'utilisation de `SSH` pour le déploiement d'applications ou les tâches d'administration de systèmes.
  + Plus précisément, `Fabric` est : un outil qui vous permet d'exécuter des fonctions `Python` arbitraire via la ligne de commande; Une bibliothèque de sous-programmes (construite au-dessus d'une bibliothèque de niveau inférieur) pour rendre l'exécution des commandes shell sur `SSH` facile et `Pythonique`.
  + Naturellement, la plupart des utilisateurs combinent ces deux choses, en utilisant `Fabric` pour écrire et exécuter des fonctions ou des tâches `Python` afin d'automatiser les interactions avec les serveurs distants.
  
#### Installation de Fabric

+ Le module `Fabric` n'est pas intégré à `Python` mais peut être installé avec le gestionnaire de packages Python comme `pip`.
+ `Pip` est un système de gestion de packages utilisé pour installer et gérer des packages logiciels écrits en `Python`. Nous devons d'abord installer `pip`.


#### Dois-je installer pip?

+ `pip` est déjà installé si vous utilisez les binaires `Python 2>=2.7.9 ou Python 3>= 3.4` et téléchargés depuis `python.org`, mais vous devrez mettre à niveau `pip`.


#### Installation avec get-pip.py

+ Pour installer `pip`, téléchargez en toute sécurité : https://bootstrap.pypa.io/get-pip.py
+ Ensuite, exécutez ce qui suit : 

![Alt Text](images/image63.jpeg)


#### Fabfile ou Fabscripts

+ `Fabric` chargera `fabfile.py` et exécutera les fonctions que nous y avons définies.
+ Créez un script python nommé `fabfile.py` et définissez-y des fonctions. Par exemple : 

![Alt Text](images/image64.jpeg)

+ Les commandes `Fab` sont exécutées à partir du `shell bash`, lorsque la commande `fab` est exécutée, elle recherche le script `fabfile.py` localement et appelle la fonction qu'il contient.

#### Arguments de tâche

+ Il est souvent utile de transmettre des paramètres d'exécution à vos tâches, comme vous le feriez lors d'une programmation `Python` classique.

![Alt Text](images/image65.jpeg)


#### Fonctions Fabric

+ `Fabric` fournit un ensemble de commandes dans l'`API Fabric` qui sont simples mais puissantes.
+ Avec `Fabric`, vous pouvez utiliser des appels `Fabric` simples comme

![Alt Text](images/image66.jpeg)

+ Pour tester les fonctions `run, sudo, get, put et reboot`, vous aurez besoin d'un système `Linux distant`.
+ Il peut s'agir d'une instance de `machine virtuelle ou de cloud`.

![Alt Text](images/image67.jpeg)

#### Appels de fonctions Fab

+ Lorsque nous appelons des fonctions `fab` à partir du `shell`, nous pouvons ou non avoir besoin de transmettre certains arguments en fonction de ce qui s'exécute dans la fonction `fab`.
+ Par exemple, si j'appelle une méthode locale, elle s'exécute simplement les tâches/commandes du système d'exploitation, mais si j'appelle la méthode `run ou sudo`, elle a besoin de l'adresse `IP` et des informations d'identification du serveur distant pour créer une session `SSH`.
+ Si nous devons transmettre l'adresse IP du serveur distant et l'utilisateur passe, nous utilisons la syntaxe ci-dessous.

![Alt Text](images/image68.jpeg)

+ Ces informations sur le serveur distant peuvent également être ajoutées au fichier `fab` en utilisant les variables `env.hosts, env.user et env.password` que nous verrons dans l'exemple suivant.

![Alt Text](images/image69.jpeg)

#### Aides Fab

+ Le gestionnaire de contexte `cd` permet de conserver l'état du repertoire (c'est-à-dire où le bloc de commentaires suivant doit être exécuté).
+ Cela revient à exécuter la commande `cd` pendant une session `SSH` et à exécuter diverses commandes différentes. Exemples d'utilisation :

![Alt Text](images/image70.jpeg)

+ Le gestionnaire de contexte `lcd (cd local)` fonctionne de manière très similaire à celui-ci dessus (cd); cependant, cela n'affecte que l'état du système local.
+ Exemples d'utilisation :

![Alt Text](images/image71.jpeg)

+ Consultez la documentation `Fab` pour plus d'aides : https://docs.fabfile.org/en/1.13/api/core/context_managers.html


#### Exemple de fabfile pour automatiser la configuration d'apache

+ Dans ce fichier fabuleux, nous écrirons des fonctions pour pour configurer `Apache` et nettoyer la configuration d'`Apache` sur une machine distante.
+ Nous utiliserons les variables `env.hosts, env.user, env.password` pour définir les informations du serveur distant.
+ `env.hosts` est une liste et nous pouvons ajouter `n` nombre d'adresses `IP/noms d'hôte` dans la liste séparés par une virgule.

![Alt Text](images/image72.jpeg)


+ A partir du script ci-dessus, nous avons vu qu'au départ, lors de la configuration, nous n'avions donné qu'une seule méthode `Fabric` dans une fonction.
+ Mais lors du démontage/nettoyage d'`Apache`, nous avons donné toute la méthode de fabric requise en une seule fonction.
+ Les deux approches fonctionnent bien, mais si j'ai une fonction distincte pour démarrer ou installer `Apache` ou configurer une règle de pare-feu, je peux également les appeler individuellement à partir du `shell bash`.
+ C'est très pratique si je viens de démarrer `Apache` sur un tableau d'hôtes distants. J'ai déjà une fonction distincte définie pour cela.
+ De cette façon, nous pouvons également réutiliser ce code pour d'autres tâches.

#### Exemple de fichier fabfile pour automatiser la configuration de tomcat

![Alt Text](images/image73.jpeg)


## Boto pour AWS

+ `Boto` est une bibliothèque `Python` qui fournit une interface pour interagir avec les services AWS.

#### Installation

![Alt Text](images/image74.jpeg)

#### Configuration

+ Nous devons configurer l'authentification `AWS`, afin de pouvoir nous authentifier auprès des services `AWS`.
+ Pour ce faire, un utilisateur `IAM` doit être créé avec un accès par programmation.
+ Créez un fichier `~/.boto` avec la syntaxe ci-dessous :

```
[Credentials]
aws_access_key_id = YOURACCESSKEY
aws_secret_access_key = YOURSECRETKEY
```

![Alt Text](images/image75.jpeg)

+ ... liste des clés dans le `bucket`

#### Supprimer un compartiment

+ La suppression d'un `bucket` peut être effectuée à l'aide de la méthode `delete_bucket`. Par exemple :

![Alt Text](images/image76.jpeg)

#### Lancement d'instances

+ Pour lancer une instance et y avoir accès, vous devez d'abord configurer un groupe de sécurité et une paire de clés.
+ Maintenant, disons que vous disposez déjà d'une paire de clés, que vous souhaitez un type d'instance spécifique et que votre groupe de sécurité est entièrement configuré.
+ Dans ce cas, nous pouvons utiliser les arguments de mots-clés pour y parvenir : 

![Alt Text](images/image77.jpeg)

#### Travailler avec des instantanés

+ Les `instantanés` vous permettent de créer des instantanés à un moment donné d'un volume `EBS` pour une récupération future.
+ Les `instantanés` vous permettent de créer des sauvegardes incrémentielles et peuvent également être utilisés pour instancier plusieurs nouveaux volumes.
+ Les instantanés peuvent également être utilisés pour déplacer des `volumes EBS` entre les zones de disponibilité ou pour effectuer des sauvegardes sur `S3`.
+ Créer un instantané est simple :

![Alt Text](images/image78.jpeg)

+ Une fois que vous avez un instantané, vous pouvez créer un nouveau volume à partir de celui-ci.
+ Les volumes sont créés paresseusement à partir d'instantanés, ce qui signifie que vous pouvez commencer à utiliser à un tel volume immédiatement :

![Alt Text](images/image79.jpeg)

#### Un exemple de script de création de table Dynamo DB

+ `DynamoDB` est le service de base de données `AWS NOSQL`.
+ `Amazon DynamoDB` est un service de base de données `NoSQL` entièrement géré qui offre des performances rapides et prévisibles avec une évolutivité transparente.
+ `DynamoDB` vous permet de vous décharger des charges administratives liées à l'exploitation et à la mise à l'échelle d'une base de données distribuée, de sorte que vous n'ayez pas à vous soucier de l'approvisionnement matériel, de l'installation et de la configuration, de la réplication, des correctifs logiciels ou de la mise à l'échelle du cluster.

![Alt Text](images/image80.jpeg)


#### Resumé

+ `Python` est un langage interprété, hautement extensible et livré avec de nombreux avantages.
+ `Python` est très facile à lire et à écrire par rapport à tout autre langage de programmation.
+ `Les nombres, les chaînes, la liste, les tuples et le dictionnaire` sont des types de données Python. `Python` est livré avec de nombreuses méthodes qui peuvent être appliquées à ces types de données pour manipuler ou présenter les données de différentes manières.
+ `La prise de décision (if/elif/else) et les boucles (for & while)` en python ont une syntaxe très simple et les blocs de code à l'intérieur sont principalement indentés de deux ou trois espaces.
+ Les fonctions Python sont utilisés lorsque nous souhaitons regrouper du code et le rendre accessible à n'importe quel autre code `Python`. Nous pouvons également utiliser ces fonctions comme modules et les importer dans d'autres scripts Python. Cela nous donne une structure très modulaire pour notre code complexe.
+ La bibliothèque `OS Python` est utilisée pour exécuter des commandes systèmes à partir de scripts Python tels que `cd, mkdir, chmod, cp, mv, etc`. Il existe également d'autres bibliothèques pour les tâches système telles que les sous-processus et les commandes.
+ `Fabric` est une bibliothèque `Python` utilisée pour exécuter des commandes systèmes sur un système local et distant. La plupart du code Python nous est retiré, nous appelons simplement des fonctions `Fabric` pour automatiser les tâches `Linux` sur le système local et distant.
+ `Boto` est une bibliothèque système Python permettant d'appeler, d'exploiter et de gérer les services `AWS` à partir de Python.


#### Conclusion
+ Etant de nature si polyvalente, gérer un énorme code Python devient difficile.
+ Lorsqu'il s'agit de partager notre code avec nos coéquipiers ou d'autres équipes, c'est un gros problème.
+ Tout le monde a son propre style de codage et la plupart d'entre nous, lorsque nous effectuons l'automatisation, ne suivons aucune bonne pratique, ce qui rend le code difficile à lire et à comprendre.
+ C'est la raison pour laquelle le monde évolue ou s'oriente vers des outils de gestion de configuration pour l'automatisation.
+ Les différences seront discutées dans le chapitre `Ansible`.


#### Quelques liens importants

+ Pour pratiquer Python avec des exercices
  + https://www.codeacademy.com/learn/python
+ Erreurs de publications et questions
  + https://stackoverflow.com/
+ Documentation Fabric
  + https://docs.fabric.io/
+ Documentation Boto
  + https://boto3.readthedocs.io/en/latest/
