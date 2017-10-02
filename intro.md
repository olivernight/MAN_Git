# Introduction
<hr />
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


## Petit rappel sur les différents termes de votre quotidien

  |Objet    | Définition                                                        |
  |---------|---------------------------------------------                      |
  |Git      |  Logiciel de gestion de version local                             |
  |Github   |  Site internet communautaire permettant de publier son repository |
  |Gitlab   |  Application web permettant de partager son repository            |
  |SVN      |  Logiciel de gestion de version par différence centralisé         |
