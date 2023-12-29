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


