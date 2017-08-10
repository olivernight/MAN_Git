# Présentation de Git

## Définition

Git est un logiciel de <strong>version décentralisé</strong> créé par
Linus Torvald

  - <strong>version</strong>

  > L'objectif est de gérer l'évolution du contenu sur une arborescence de fichier.


  - <strong>décentralisé</strong>

  > Ne repose pas sur un serveur centralisé.
  Cela permet de pouvoir partager du code à n'importe quel moment.
  Pas besoin d'authentification ou de compte. Chacun des utilisateurs a son
  propre historique.

Git gère des <strong>snapshots</strong> (instantanés) en <strong>local</strong>

  - <strong>snapshots</strong>

  > La plus part des gestionnaires de versions tels que SVN enregistre un fichier dans l'état initiale puis ne sauvegarde que les modifications effectuées


![alt text](https://git-scm.com/figures/18333fig0104-tn.png)


  > La plus part des gestionnaires de versions tels que SVN enregistrent un fichier dans son état initial puis ne sauvegarde que les modifications effectuées


![alt text](https://git-scm.com/figures/18333fig0105-tn.png)

  - <strong>local</strong>

  > L'utilisation de Git peut être réaliser de façon  intégrale sur votre poste. Aucune connexion internet n'est nécessaire pour tuiliser Git. <br />
  <strong>Attention</strong> : Il ne faut surtout pas confondre Git, Github, Gitlab, SVN

  |Objet    | Définition                                                        |
  |---------|---------------------------------------------                      |
  |Git      |  Logiciel de gestion de version local                             |
  |Github   |  Site internet communautaire permettant de publier son repository |
  |Gitlab   |  Application web permettant de partager son repository            |
  |SVN      |  Logiciel de gestion de version par différence centralisé         |


## Les différents objets sur Git

|Objet    | Définition                                  |
|---------|---------------------------------------------|
|Blob     |  Contenu d'un fichier                       |
|Tree     |  Liste de blobs                             |
|Commit   |  Message de log + tree + lien Commit Parent |
|Tag      |  Commit + Numéro de version                 |

## Et le travail collaboratif dans tout ça ?!

Il est vrai que dans notre métier nous sommes rarement amener à travailler tout seul dans notre coin sur notre application. De plus, les informaticiens sont réputés pour leur générosité et adorent partager leurs codes avec les autres.

Il existe donc des sites sur internet qui permettent de diffuser/partager nos repository (dépôts). Le plus connu est sans aucun doute Github.

## L'organisation

|Objet    | Définition                                  |
|---------|---------------------------------------------|
|Branche  |  Contenu d'un fichier                       |
|Master   |  Contenu d'un fichier                       |
|Head     |  Contenu d'un fichier                       |


![alt text](https://git-scm.com/figures/18333fig0317-tn.png)
