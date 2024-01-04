# **Script Bash**

## **1. Introduction**

+ Ce didacticiel vous donnera une plate-forme solide sur la façon de créer des `scripts bash et d'automatiser les tâches d'administration systèmes quotidiennes`.
+ Certes, tout ne peut être abordé dans ce chapitre, mais vous serez équipés d'une bonne quantité de connaissances pour créer vos propres scripts et y exceller si vous faites vos projets efforts.
+ Les `Scripts Bash` sont utilisés par de nombreux `administrateurs systèmes et geeks DevOps` pour faire avancer les choses rapidement et efficacement.
+ Il existe de nombreux outils d'automatisations sur le marché comme `Ansible, Puppet, Chef, etc`.
+ Qui sont beaucoup plus sophistiqués mais parfois pour faire avancer les choses rapidement sous `Linux Systèmes`, nous utilisons des `scripts Bash`.
+ De plus,les `scripts` vous feront comprendre ce qu'est l'`automatisation` et vous pourrez alors comprendre rapidement les fonctionnalités utilisés dans la gestion de la configuration des outils comme `Ansible ou Puppet`.


### **a) Que Sont les Scripts**

+ Un `Script Bash` est un fichier brut contenant une série de commandes.
+ Ces commandes sont un mélange de commandes que nous tapierons normalement nous-mêmes sur la ligne de commandes( telles que `ls` ou `cp` par exemple) et des commandes que nous pourrions taper sur la ligne de commande mais que nous ne ferions généralement pas(vous découvrirez au fil des prochaines pages).
+ Un point crucial à retenir cependant est:

  + `Tout ce que vous pouvez exécuter normalement sur la ligne de commande peut être mis dans un script et fera exactement la même chose. De même tout ce que vous pouvez insérer dans un script peut également être exécuté normalement sur la ligne de commande et il fera exactement la même chose`.
  

### **b) Premier Scénario**

+ Comme nous l'avons mentionné précédemment, ce script est un fichier texte normal contenant les commandes.
+ Nous allons ouvrir un éditeur de fichier `vi` et y ajouter quelques commandes.
+ Il est conventionnel de donner aux fichiers qui sont des `scripts Bash` une extension `.sh`(`print.sh` par exemple).


        $ vi print.sh
        1. #!/bin/bash
        2. # Asample Bash script
        3. echo Hello World!


+ Explication:
    + **Ligne 1 :**
        + `#!` est appelé `SHEBANG`,il indique au script d'interpréter le reste des lignes avec un interprète `/bin/bash`.
        + Donc, si nous changeons cela en `/usr/bin/python` alors cela indique au script pour utiliser l'interpréteur `python`.
    + **Ligne 2 :**
        + Cela est un `Un commentaire`. Tout ce qui suit `#` n'est pas executé. C'est pour notre référence seulement. Les commentaires permettent à toutes personnes lisant ce script d'avoir une référence.
    + **Ligne 3 :**
        + `echo` est la commande qui imprimera le message à l'écran. Vous pouvez vous-même taper la ligne de commande et il se comportera exactement de la même manière.

### **Exécuter ou Exécuter un Script ?**

+ Exécuter un `Script Bash` est assez simple. Parfois, vous entendrez les gens dire d'exécuter le script, les deux signifient la même chose, les deux signifient la même chose.
+ Avant de pouvoir exécuter un script, il doit avoir l'autorisation d'exécution d'ensemble.
+ Si vous oubliez d'abord cette autorisation avant d'exécuter le script, vous obtiendrez simplement une erreur message `<<Autorisation refusée>>`.
+ Chaque fois que vous créez un fichier dans le Système Linux par défaut, il n'aura pas une `autorisation d'éxécution`, c'est pour des raisons de sécurité.
+ Vous rendrez votre script exécutable et alors vous pouvez l'exécuter.

<img src= "../images/image1.jpg"/>

+ Sans donner l'autorisation d'execution, nous pouvons également exécuter le script, mais nous forunissosn ensuite un shell et lui demandons d'exécuter toutes les commandes du script sur ce shell.


### **Variables**

+ Stockage temporaire d'informations en mémoire.

**Comment travaillent-ils ?**
+ Une `variable` est un stockage pour une information.
+ Nous pourrions effectuer deux actions pour les variables :
    + Définir une valeur pour une variable.
    + Lire ou utiliser la valeur d'une variable.

+ Pour attribuer une variable, nous utilisons `= signe`, `VariableName=Value`
+ Pour lire/accéder à la valeur de la variable, nous utilisons : `$VariableName`.

<img src= "../images/image2.jpg"/>


**Arguments de ligne de Commande**
+ Lorsque nous exécutons un programme sur la ligne de commande, vous êtes habitué à fournir des arguments après celui-ci pour contrôler son comportement.
+ Par exemple, nous pourrions exécuter la commande `ls -l/tmp`.
+ `-l` et `/tmp` sont tous deux arguments de ligne de commande pour la commande `ls`.
+ Nous pouvons faire la même chose avec nos scripts bash. 
+ Pour ce faire, utilisons les variables `$1` pour représenter le premier argument de ligne de commande, `$2` pour représenter le deuxième argument de ligne de commande et ainsi de suite.
+ Ceux-ci sont automatiquement définis par le système lorsque nous executons notre script, il nous suffit donc de nous y référer.
+ Regardons un exemple.

<img src= "../images/image3.jpg"/>

**Explication**

+ `Ligne 3` - exécutez `cp` avec le premier argument de ligne de commande comme source et le deuxième argument de ligne de commande comme destination.
+ `Ligne 5` - exécutez la commande `echo` pour imprimer un message.
+ `Ligne 6` - Une fois la copie terminée, exécutez la commande `ls` pour la destination juste pour vérifier qu'elle a fonctionné. Nous avons inclus les options `l` pour nous montrer des informations supplémentaires et `h` pour rendre la taille lisible par l'homme afin que nous puissions vérifier qu'elle a été copiée correctement.


**Certaines Variables Systèmes**

+ Le système définit également quelques autres variables que vous pouvez utiliser.

    + `$0` - Le nom du script Bash.
    + `$1 - $9` - Les 9 premiers arguments du script Bash(Comme mentionné ci-dessus).
    + `$#` - Combien d'arguments ont été transmis au script Bash.
    + `$@` - Tous les arguments fournis au script Bash.
    + `$?` - L'état de sortie du processus executé le plus récemment.
    + `$$` - L'ID de processus du script actuel.
    + `$USER` - Le nom de l'utilisateur qui exécute le script.
    + `$HOSTNAME` - Le nom de l'hôte de la machine sur laquelle le script est executé.
    + `$SECONDS` - le nombre de secondes depuis le démarrage du script.
    + `$RANDOM` - Renvoie un nombre aléatoire différent à chaque fois qu'il est mentionné.
    + `$LINENO` - Renvoie le numéro de ligne actuel dans le script Bash.

**Définir Vos Propres Variables**

<img src= "../images/image4.jpg"/>

**Citations**

+ Stocker un seul mot dans une variable fonctionne bien sans guillemets, mais si nous voulons stocker une phrase et également stocker des caractères spéciaux comme `$, %, @ etc`, notre affectation normale de variable ne fonctionnera pas.
  <img src= "../images/image5.jpg"/>

+ Cependant, lorsque nous voulons que les variables stockent des valeurs plus complexes, nous devons utiliser des guillemets.
+ En effet, dans les circonstances normales, `Bash` utilise un espace pour déterminer les éléments distincts.
+ Lorsque nous mettons notre contenu entre guillemets, nous indiquons à `Bash` que le contenu doit être considéré comme un seul élément.
+ Vous pouvez utiliser des guillemets simples `(')` ou des guillemets doubles `(")`.
+ Les guillemets simples traiteront chaque caractère littéralement.
+ Les guillemets doubles, vous permettront d'effectuer une substitution(c'est-à-dire d'inclure des variables dans le réglage de la valeur).

<img src= "../images/image6.jpg"/>

**Remplacement De Commande**
+ La variable définie dans le script part avec elle et meurt à la fin du script.
+ Si nous voulons accessible à tous les scripts de votre shell actuel, nous devons l'exporter.

<img src= "../images/image7.jpg"/>



