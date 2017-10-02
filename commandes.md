#J':heart: la ligne de commande
<hr />

<i>Pré-requis : Installation de Git sur votre environnement.</i>
## Initialisation d'un repository
```bash
cd /my/personal/directory
git init
```

## Clone d'un repository distant

```bash
cd /my/personal/directory
git clone https://github.com/olivernight/MAN_Git.git
```

## Indexation d'un nouveau fichier

```bash
# Pour un fichier
touch mytralala.txt
git add mytralala.txt

# Pour tous les fichiers du répertoire courant
touch mytralala2.txt
touch mytralala3.txt
git add .
```

## Création d'un commit

```bash
# Création d'un commit. L'option -m permet de saisir un commentaire.
git commit -m "Création de mon premier commit"
```

## Création d'une nouvelle branche

```bash
# Création de maNouvelleBranche puis replacement de HEAD
git branch maNouvelleBranche
git checkout maNouvelleBranche

# All in one
git checkout -b branch1

# Création d'une nouvelle branche mBranche à partir du commit C2
# et positionne HEAD dessus.
git checkout -b maBranche C2
```

## Tag

```bash
# Création un tag T1 pour pointer sur le commit C2
git tag T1 C1

# Il est possible d'utiliser le tag plutôt qu'un hash de commit
git checkout -b maBranche T1
```

## Merge

```bash
# Création d'un nouveau commit C de fusion de la branche maNouvelleBranche
# vers la branche master.
# Le dernier commit de la branche ne changera pas.
git merge maNouvelleBranche

# Création d'un nouveau commit C de fusion de la branche maNouvelleBranche vers
# la branche master.
# Le dernier commit de la branche sera C.
git checkout maNouvelleBranche
git merge master
```

## Parcours des commits parents
```bash
# Il est possible de remonter la chaine de commit sans pour autant saisir un numéro
# de hash.
# L'idée est de dire par exemple : "Je veux récupérer le 3e commit parent"
# Pour ce faire, il existe deux fonctions : ~ et ^
# ~ permet de remonter sur le commit parent. Il peut être coupler avec
# un nombre n pour remonter de n noeuds.
git branch test HEAD~3

# Lorsque nous avons plusieurs parents, il existe l'oéprateur ^ qui permet
# de choisir le chemin que l'on souhaite prendre. ^ peut être coupler avec un
# entier n pour choisir le nieme plus vieux parent.
# Les opérateurs peuvent être couplés entre eux
git branch test HEAD~3^2~

```

## Rebase
```bash
# Déplacement de la branche
git rebase maNouvelleBranche

# Rebase interractif
git rebase -i HEAD~4
```

## Cherry-pick
```bash
# Création de nouveaux commits à partir d'une liste de commits existant
# passée en paramètre
git cherry-pick C5 C2 C3
```

## Remote / origin
Lorsque l'on travaille avec un repo distant (en utilisant la commande clone ou remote)
Git donne un nom par défaur au serveur le nom origin

```bash
# Récupération du contenu d'une branche distante en local sans pour autant modifier
# mon répertoire courant
git fetch brancheDistante

# Récupération du contenu d'une branche distante en local et tente de
# fusionner avec la branche locale
git pull brancheDistante
```
