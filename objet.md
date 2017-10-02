# Les différents objets & états sur Git
<hr />

|Objet    | Définition                                    |
|---------|---------------------------------------------    |
|Blob     |  Contenu d'un fichier                         |
|Tree     |  Liste de blobs                               |
|Commit   |  Message de log + tree + lien Commit Parent       |
|Tag      |  Commit + Numéro de version                     |
|Branche  |  Pointeur sur un commit. Ceci nous permets de récupérer un ensemble de commit. Le but des branches est de vous permettre de travailler sur des modifications sans pour autant impacter le travail des autres. Cela permet notamment de cloisonner les développements, travailler sur des correctifs tout en maitrisant limitant les impacts. |                               
|Master   |  Lorsque l'on créé un nouveau repository, deux branches par défaut sont créés. L'une d'entre elle est la branche master. Etant donné que cette branche existe dans tous les repository, par convention, c'est celle qui doit contenir le code le plus propre possible |
|HEAD     |  A l'image de master, HEAD est lui aussi un pointeur créé lors de la création de notre repository. C'est l'endroit sur lequelle je me trouve actuellement. Toutes les modifications effectuées seront donc faite à partir de ce point.|

<center><img src="https://git-scm.com/figures/18333fig0317-tn.png" /></center>

|Etat     | Définition                                                               |
|---------|---------------------------------------------                             |
|Non indexé | Nouveau fichier dans le répertoire                                     |
|Validé   |  Les données ont été sauvegardées dans notre base de données locale      |
|Modifié  |  Liste de blobs                                                          |
|Indexé   |  Message de log + tree + lien Commit Parent                              |
