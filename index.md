# Présentation de Git

## Définition

Git est un logiciel de gestion de <strong>version décentralisé</strong> créé par
Linus Torvald <br/>

  - <strong>version</strong><br/><br/>

  > L'objectif est de gérer l'évolution du contenu sur une arborescence de fichier. C'est le même fonctionnement qu'une base de données.


  - <strong>décentralisé</strong>

  > Ne repose pas sur un serveur centralisé.
  Cela permet de pouvoir partager du code à n'importe quel moment.
  Pas besoin d'authentification ou de compte. Chacun des utilisateurs a son
  propre historique.

Git gère des <strong>snapshots</strong> (instantanés) en <strong>local</strong>

  - <strong>snapshots</strong>

  > La plus part des gestionnaires de versions tels que SVN enregistre un fichier dans l'état initiale puis ne sauvegarde que les modifications effectuées


<center><img src="https://git-scm.com/figures/18333fig0104-tn.png" /></center>


  > A l'inverse, Git stocke la dernière version indexée. Le terme snapshots est utilisé pour dire que l'on sauvegarde une image de notre code à un instant T (commit).A l'inverse des autres, Git enregistre l'intégralité de nos fichiers. Lorsque nous créons un nouveau commit et si le fichier n'a pas été modifié, Git n'enregistre pas à nouveau le fichier mais stocke un pointeur vers la dernière version du fichier.

<center><img src="https://git-scm.com/figures/18333fig0105-tn.png" />
</center>


  - <strong>local</strong>

  > L'utilisation de Git peut être réaliser de façon  intégrale sur votre poste. Aucune connexion internet n'est nécessaire pour utiliser Git. <br />
  <strong>Attention</strong> : Il ne faut surtout pas confondre Git, Github, Gitlab, SVN



  |Objet    | Définition                                                        |
  |---------|---------------------------------------------                      |
  |Git      |  Logiciel de gestion de version local                             |
  |Github   |  Site internet communautaire permettant de publier son repository |
  |Gitlab   |  Application web permettant de partager son repository            |
  |SVN      |  Logiciel de gestion de version par différence centralisé         |

## Et le travail collaboratif dans tout ça ?!

  Comme vous avez pu le constater, pour l'instant nous n'avons jamais travailler en dehors notre propre machine. Je ne me suis jamais connecté à un serveur distant ni demandais du code à une autre personne. Il est très important de comprendre que la gestion de version à travers Git se fait en local avant tout.

  Mais il est vrai que dans notre métier nous sommes rarement amener à travailler tout seul dans notre coin sur notre application. De plus, les informaticiens sont réputés pour leur générosité et adorent partager leurs codes avec les autres.

  Il existe donc des sites sur internet qui permettent de diffuser/partager nos repository (dépôts). Le plus connu est sans aucun doute Github.

  L'idée est de diffuser l'ensemble des snapshots afin que n'importe qui puisse reprendre le projet pour contribuer à l'amélioration du projet en cours (clone).


## Les différents objets & états sur Git

|Objet    | Définition                                    |
|---------|---------------------------------------------    |
|Blob     |  Contenu d'un fichier                         |
|Tree     |  Liste de blobs                               |
|Commit   |  Message de log + tree + lien Commit Parent       |
|Tag      |  Commit + Numéro de version                     |
|Branche  |  Pointeur sur un commit. Ceci nous permets de récupérer un ensemble de commit. On utilise souvent les branches pour isoler des évolutions afin de ne pas impacter le reste de notre code. |                               
|Master   |  Lorsque l'on créé un nouveau repository, deux branches par défaut sont créés. L'une d'entre elle est la branche master. Etant donné que cette branche existe dans tous les repository, par convention, c'est celle qui doit contenir le code le plus propre possible |
|HEAD     |  A l'image de master, HEAD est lui aussi un pointeur créé lors de la création de notre repository. C'est l'endroit sur lequelle je me trouve actuellement. Toutes les modifications effectuées seront donc faite à partir de ce point.|

<center>![alt text](https://git-scm.com/figures/18333fig0317-tn.png)</center>

|Etat     | Définition                                                               |
|---------|---------------------------------------------                             |
|Non indexé | Nouveau fichier dans le répertoire                                     |
|Validé   |  Les données ont été sauvegardées dans notre base de données locale      |
|Modifié  |  Liste de blobs                                                          |
|Indexé   |  Message de log + tree + lien Commit Parent                              |


## Démarrer son repository

Pré-requis : Installation de Git sur votre environnement.

### Initialisation d'un repository
```sh
cd /my/personal/directory
git init
```

### Clone d'un repository distant

```sh
cd /my/personal/directory
git clone https://github.com/olivernight/MAN_Git.git
```

### Indexation d'un nouveau fichier

```sh
# Pour un fichier
touch mytralala.txt
git add mytralala.txt

# Pour tous les fichiers du répertoire courant
touch mytralala2.txt
touch mytralala3.txt
git add .
```

### Création d'un commit

```sh
git commit -m "Création de mon premier commit"
```

### Création d'une nouvelle branche

```sh
# Création de maNouvelleBranche puis replacement de HEAD
git branch maNouvelleBranche
git checkout  maNouvelleBranche

# All in one
git checkout -b branch1
```

### Merge

```shell
# Création d'un nouveau commit C de fusion de la branche maNouvelleBranche vers la branche master.
# Le dernier commit de la branche ne changera pas.
git merge maNouvelleBranche

# Création d'un nouveau commit C de fusion de la branche maNouvelleBranche vers la branche master.
# Le dernier commit de la branche sera C.
git checkout maNouvelleBranche
git merge master
```
### Rebase

```sh
# Déplacement de la branche
# Le dernier commit de la branche ne changera pas.
git merge maNouvelleBranche
```
