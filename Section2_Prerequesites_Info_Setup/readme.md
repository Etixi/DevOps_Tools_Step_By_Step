## **Résumé**
<hr>

|PLAN|
|----|
|8. Informations préalables aux outils|
|9. Chocolatey pour Windows|
|10. Homebrew pour MacOS|
|11. Installation de logiciels|
|12. Outils requis pour Ubuntu 20|
|13. Inscriptions|
|14. Configuration AWS|
|15. Sortie|


## **8. Informations préalables aux outils**


+ <h3><b>N°1 : Les outils dans votre ordinateur</b></h3>
+ <h3><b>N°2 : Paramétrage des comptes</h3></b>
+ <h3><b>N°3 : Configuration AWS</h3></b>

### **Lancement du projet**
<hr>

+ **[Dépôt Github](https://github.com/Etixi/vprofile-project.git)**

### **Outils**
<hr>

|Outils Partie 1|Outils Partie 2|
|---------------|---------------|
|Oracle VM VirtualBox|JDK8/11|
|Git Bash|MAVEN|
|Vagrant|INTELLIJ/ECLIPSE|
|Chocolatey/Brew|Sublime Text Editor|
|VS Code|AWS CLI|


### **S'inscrire**
<hr>

+ ***Github***
+ ***Achat de domaine(GoDaddy)***
+ ***DockerHub***
+ ***SonarCloud***

### **AWS**
<hr>

+ ***Compte gratuit***
+ ***IAM avec MFA***
+ ***Alarme de facturation***
+ ***Configuration du certificat***

###**9. Chocolatey pour Windows**

+ ***Le premier outil que nous allons installer est `chocolatey`.***

+ ***`chocolatey` est un outil sous Windows pour installer des logiciels via une ligne de commande comme:***

    + `choco install notepad++`.
        + Ce sera la commande pour installer `notepad++`.

+ ***Et ce n'est pas un outil obligatoire. Vous pouvez simplement rechercher un logiciel sur Internet, le télécharger et l'installer également. Mais c'est juste pour vous faciliter la vie. Vous ouvrez donc PowerShell ou une invite de commande, exécutez la commande et installez le logiciel.***

+ ***Alors cherchez simplement du `chocolatey`. C'est pour les fenêtres. Si vous utilisez `Mac OS`, j'ai un autre outil pour vous, un `homebrew`, que je vais vous montrer dans un minute.***

+ ***`Chocolatey` sera donc notre outil pour installer tous les autres outils. Et nous devons d’abord installer `Chocolatey`. Et nous allons exécuter cette commande sur `PowerShell`. Lorsque nous exécutons cette commande dans `PowerShell`, elle installera Chocolaty.***

+ ***Et puis nous pouvons utiliser la commande: `chocolate install` pour installer tous les autres outils. Alors laissez-moi d'abord ouvrir PowerShell. Vous devez ouvrir `PowerShell en tant qu'administrateur`.***

+ ***Alors faites un clic droit et exécutez en tant qu'administrateur. Nous devons exécuter quelques commandes pour vérifier si nous pouvons installer `Chocolatey`, vous devez exécuter cette politique d'exécution commande: `Get-ExecutionPolicy`.***

+ ***Si cela renvoie restreint, nous devons alors exécuter cette commande : `Set-ExecutionPolicy`. Donc, il lit Tout signé pour moi.***

+ ***Mais si vous avez reçu une restriction, vous feriez mieux d'exécuter commande: `Set-ExecutionPolicy`.***

+ ***Donc si vous nous donnez la commande pour installer `VirtualBox`. Vous pouvez donc simplement installer `VirtualBox`. Il installera `VirtualBox` ou tout autre logiciel que vous recherchez comme `IntelliJ`.***


        ************* OPEN YOUR POWERSHELL ******************

        ###**vérifions si nous pouvons installer Chocolatey**
        PS C:\WINDOWS\system32> Get-ExecutionPolicy
        ###**En cas de restriction executer la commande suivante**
        PS C:\WINDOWS\system32> Set-ExecutionPolicy AllSigned
        ###**Installation de chocolatey**
        PS C:\WINDOWS\system32> Set-ExecutionPolicy Bypass -Scope Process -Force; iwr https://community.chocolatey.org/install.ps1 -UseBasicParsing | iex


+ https://chocolatey.org/install

+ https://community.chocolatey.org/packages


### **Homebrew pour MacOS**
            
            ******************** Open Your Terminal and paste ******************
            /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
            echo 'eval "${/opt/homebrew/bin/brew shellenv}"' >> /users/etienne/.zprofile
            eval "${/opt/homebrew/bin/brew shellenv}"
            brew


### **11. Installation de logiciels**

#### **Outils Windows**
+ ***Installez `chocolatey` à partir des instructions données dans le lien ci-dessous.***

    + https://chocolatey.org/docs/installation

            ### ************* OPEN YOUR POWERSHELL AND EXECUTE******************

            choco install virtualbox --version=7.0.8 -y
            choco install vagrant --version=2.3.4 -y
            choco install git -y
            choco install corretto11jdk -y
            choco install maven -y
            choco install awscli -y
            choco install intellijidea-community -y
            choco install vscode -y
            choco install sublimetext3.app -y


### **12. Outils requis pour Ubuntu 20**


#### **Conditions préalables aux outils pour Ubuntu 20**

+ **Install Virtualbox**

        $ sudo apt update

        $ sudo apt install virtualbox

#### **Install Vagrant**

        $ curl -O https://releases.hashicorp.com/vagrant/2.2.9/vagrant_2.2.9_x86_64.deb

        $ sudo apt install ./vagrant_2.2.9_x86_64.deb


#### **Install Git**

        $ apt install git

#### **Install jdk8**

        $ sudo apt-get install openjdk-8-jdk

#### **Install Maven**

        $ sudo apt-get install maven

#### **Install awscli**

        $ sudo apt-get install awscli

#### **Install Intellij community**

        $ sudo snap install intellij-idea-community --classic

#### **Install Sublime Text**

        $ sudo apt update

        $ sudo apt install dirmngr gnupg apt-transport-https ca-certificates software-properties-common

        $ curl -fsSL https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -

        $ sudo add-apt-repository "deb https://download.sublimetext.com/ apt/stable/"

        $ sudo apt install sublime-text


### **Signups**


+ ***Github***

    + ***https://github.com/Etixi***

+ ***Achat de domaine(GODADDY)***

    + ***https://dashboard.godaddy.com/venture?ventureId=2d801ba4-06c4-451e-bb76-76af0e7d9dd2***

+ ***DOCKERHUB***

    + ***https://hub.docker.com/***

+ **SONARCLOUD**

    + ***https://sonarcloud.io/projects***



