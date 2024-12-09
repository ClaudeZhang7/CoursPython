---
title: "Cours sur le langage de programmation Python"
css: styles.css
---

# Python pour les Nuls (Oui toi la)

Je suggère que **Python** a été au préalable installé ainsi que son **gestionnaire de paquet (pip)**, pip est le gestionnaire qui permet de gérer les librairies/paquets.

Dans le cas contraire vous pouvez le télécharger sur le site [Python.org](https://www.python.org/downloads/).

Pour Python, je vous suggère d'utiliser **un éditeur de code (IDE)** tels que :

* **Visual Studio  Code**
* **Jupyter Notebook**

## Hello World !

Le premier programme consistera à afficher le message **Hello World**, pour ce faire on utile une fonction de python appelé **print()** qui permet d'afficher des valeurs.

```python
print("Hello World !")
>>> Hello World !
```

## Les types

Ils existent plusieurs types, on va dans cette première partie parler des types de base.

| Nom du type   | Description   | Exemple   | Syntaxe
|-------------|-------------|-------------|-------------|
| int   | Nombre entier   | -644 |          entier = -644       |
| float   | Nombre à virgule   | 3.5 |      flottant = 3.5      |
| str   | Chaine de caractère   | "Hello" | chaine = "msg"      |
| bool   | Valeur logique  | True (Vrai) ou False (False) | vrai = True |
| list   | Collection de valeurs | [1,2,"ok"]  | liste =[1,2,"ok"]  |

**Les chaines de caractères doivent être déclaré dans des guillemets simple ou double !**

Les **booléans (bool)** sont utilisés au sein d'une condition afin de vérifier si tel ou tel élément est exacte, nous verrons un exemple plus tard.

Les **listes sont une collection de valeurs**, il faut imaginer une boite ou à l'intérieur on a mis nos données, la également, nous verrons un exemple plus tard.

Le type d'une variable peu être vérifier à travers la fonction **type** en fournissant une valeur au paramètre.

**Exemple :**

```python
type(True)
>>> bool
type(5)
>>> int
type([1,2,3])
>>> list
```

## Les variables

une variable est un nom qui va **stocker une valeur**.

Une variable est caractérisée par :

* **un nom** (choisi par le programmeur)
* **un type** (le type est déduit automatiquement par le compilateur si il n'est pas spécifié)
* **une adresse mémoire** (correspond à un endroit ou est stocké notre variable)

**Exemple :**

```python
# on crée une variable var à laquelle on lui affecte la valeur 18
var = 18
print(5 + var)
>>> 23
```

L'affectation d'une valeur à une variable se fait par **l'opérateur =**.

Une variable peu être combiner avec d'autre variable ou valeur afin d'y faire une **Opération arithmétique** ou bien  de faire ce qu'on appel une **concaténation** (pour les chaînes de caractères).

Une même variable **peu être affecté à elle même** afin d'y faire une opération arithmétique (vous l'utiliserez souvent pour les boucles while).

```python
somme = 0
cinq = 5 
deux = 2
somme = somme + cinq + deux

print(somme)
>>> 7
```

## Opération arithmétique :

| **Opération**       | **Symbole** | **Exemple**         | **Résultat**        |
|----------------------|-------------|---------------------|---------------------|
| Addition             | `+`         | `5 + 3`            | `8`                |
| Soustraction         | `-`         | `10 - 4`           | `6`                |
| Multiplication       | `*`         | `7 * 2`            | `14`               |
| Division             | `/`         | `9 / 2`            | `4.5`              |
| Division entière     | `//`        | `9 // 2`           | `4`                |
| Modulo (reste)       | `%`         | `9 % 2`            | `1`                |
| Puissance            | `**`        | `3 ** 2`           | `9`                |

La division entière permet de diviser deux nombres et de garder uniquement la partie entière du résultat, en ignorant la partie décimale.

La **division entière ne fait pas d'arrondi**, c'est à dire que même si 140 / 3 équivaut à 46.6, la division entière ne sera pas 47 mais bien 46 !

Par exemple :

```python
140 // 3 
>>> 46
```

L'opérateur Modulo `(%)` permet de **récupérer le reste d'une division entière**, par exemple 11 % 2 affichera 1.

## Concaténation

La concaténation est un procédé permettant de **fusionner/coller des chaînes de caractères entre elles**, la concaténation est représenté par **l'opérateur `+`**.

```python
hello = "hello "
world = "world"
print( hello + world)
>>> hello world
```

Les chaines de caractères peuvent aussi être combiner avec **l'opérateur** `*` afin d'afficher la chaîne de caractère `x` fois.

```python 
print("hello " *2)
>>> hello hello
```

## Exerçons voyons !

Dans cette section, je vais vous donner 3 exercices simples :

* **1.1 Faites la somme de deux valeurs en passant par des variables**
* **1.2 Afficher le message Hello World 3 fois**
* **1.3 Calculer le modulo de 7 par 2 (7 % 2) et de 6 par 2, n'hésitez pas a faire plusieurs tests avec modulo 2 !** 

### Réponses

**1.1 Faites la somme de deux valeurs en passant par des variables**

```python
cinq = 5
sept = 7
print(cinq + sept)
>>> 12
```

**1.2 Afficher le message Hello World 3 fois**

```python
print("Hello World " * 3)
>>> Hello World Hello World Hello World

# Il est également possible d'afficher Hello World sur plusieurs lignes
print("Hello World \n" * 3)
>>> Hello World
>>> Hello World
>>> Hello World
```

`\n` est un caractère dit **échappement** qui permet de faire un **saut/retour de ligne**, il existe beaucoup de caractère d'échappement cependant ce n'est pas l'objectif de ce cours.

**1.3 Calculer le modulo de 7 par 2 (7 % 2) et de 6 par 2**

```python
print(7 % 2)
>>> 1
print(6 % 2)
>>> 0
```

L'objectif de cet exercice était de vous faire comprendre qu'en faisant une valeur modulo 2, on **pouvait déterminer si une valeur est pair ou impair selon le reste**. Par exemple si le reste est 1, la valeur est impair et si la valeur est 0 la valeur est pair.

## Les conditions

Les conditions permettent de vérifier que tel ou tel valeur est Vrai ou Faux. Admettons que je fasse un virement de mon compte à un autre, je souhaite vérifier que la valeur envoyé n'est pas négative dans le cas contraire cela devra engendrait un bug.

**Syntaxe d'une condition :**

```python
if (condition):
    print("condition valide")
    # bloc d'instructions ...
```

Comme vous pouvez le voir ci-dessus, il y a une distance, print n'est pas mis tout à gauche comme auparavant. C'est ce qu'on appel **l'indentation**.

L'indentation permet de faire comprendre au compilateur que ce bloc d'instructions appartient à notre condition, on peu donc le traduire par : `print("condition valide")` ne sera affiché que si on passe par cette condition.

L'indentation est très important, car ils permettent de définir un bloc d'instructions pour un **mot clé donné (if est un mot clé)**.

L'indentation est utilisé lorsqu'on déclare : des conditions, des boucles, des fonctions, etc...

Il est possible de définir plusieurs conditions en même temps ainsi que de définir une condition par défaut.

**Syntaxe :**

```python
cinq = 5
if (cinq > 6):
    print("5 est plus grand que 6")
elif (cinq < 6):
    print("5 est plus petit que 6")
else :
    print("5 est égal à 6")
```

Le mot clé `elif` est utilisé à la suite d'une condition if, elif permet de rajouter des conditions supplémentaires dans le cas ou la/les précédentes sont fausses. On peu avoir autant de bloc elif qu'on souhaite.

Le mot clé `else` est une condition par défaut qui s'éxécute seulement lorsque toutes les conditions précédentes sont fausses.

En ayant compris ça d'après vous qu'affichera le code ci-dessus ?

Enfin les conditions sont effectués à travers plusieurs opérateurs :

* **Les opérateurs de comparaison**
* **Les opérateurs logiques**
* **Les opérateurs d'appartenance**

### Liste d'opérateurs de comparaison

| **Opérateur** | **Description**           | **Exemple**          | **Résultat**  |
|---------------|---------------------------|-----------------------|---------------|
| `==`          | Égal à                   | `5 == 5`             | `True`        |
| `!=`          | Différent de             | `5 != 3`             | `True`        |
| `<`           | Inférieur à              | `3 < 5`              | `True`        |
| `>`           | Supérieur à              | `5 > 3`              | `True`        |
| `<=`          | Inférieur ou égal à      | `3 <= 3`             | `True`        |
| `>=`          | Supérieur ou égal à      | `5 >= 3`             | `True`        |

### Liste d'opérateurs logiques

| **Opérateur** | **Description**         | **Exemple**                     | **Résultat**  |
|---------------|-------------------------|----------------------------------|---------------|
| `and`         | ET logique              | `(5 > 3) and (3 > 1)`           | `True`        |
| `or`          | OU logique             | `(5 > 3) or (3 < 1)`            | `True`        |
| `not`         | Négation logique        | `not (5 > 3)`                   | `False`       |

### Liste d'opérateurs d'appartenance

| **Opérateur** | **Description**         | **Exemple**                  | **Résultat**  |
|---------------|-------------------------|------------------------------|---------------|
| `in`          | Appartient à            | `"a" in "abc"`               | `True`        |
| `not in`      | N'appartient pas à      | `"d" not in "abc"`           | `True`        |

**Résumé :**

* **Les opérateurs de comparaison compare seulement 2 élément**
* **Les opérateurs logiques permettent de rajouter plusieurs conditions (and et or)**
* **les opérateurs d'appartenance permettent de savoir si un élément appartient à une collection de valeur utilisé souvent pour les listes et les str.**

### Exercices

**2.1** Nous avons 2 variables pos et neg, je souhaite qu'on affiche les valeurs des variables positifs dans le cas contraire on effectuera la valeur absolue de la valeur négatif.

```python
pos = 5
neg = -6

# ... à vous de jouer
```

**2.2** Déterminer quels sont les variables pair et impair ci-dessous en utilisant une condition.

```python
six = 6
trois = 3
deux = 2

# ... à vous de jouer
```

**2.3** Améliorer le code suivant, je souhaite n'avoir **qu'une seule instruction conditionnelle (un seul if et un seul else)** :

```python
if 7 > 5 :
    if 8 > 6 :
        print("Vrai")
    else :
        print("Faux")
else :
    print("Faux")
```

### Réponses

**2.1**

```python
pos = 5
neg = -6

if pos > 0 :
    print(pos)
else :
    pos = pos * -1

if neg > 0 :
    print(neg)
else :
    neg = neg * -1
```

Il est également possible d'utiliser des conditions au sein d'une affectation.

```python
negatif = -7
positif = negatif if negatif > 0 else negatif * -1
print(positif)
>>> 7
```

Il faut le lire de cette manière : on affecte la variable negatif à la variable positif si negatif est supérieur à 0, sinon on affecte la valeur negatif * -1 à positif

## Les Listes

Les listes sont une collection de valeurs qui permettent de stocker plusieurs valeurs en une variable.

Imaginons que, j'ai choisi 5 produits sur amazon, chaque produit peu avoir un prix différent ce qui fais qu'a un moment donné, amazon devra effectuer la somme de ses produits afin de me faire payer la totalité du panier.

Nous aurons donc une liste correspondant aux valeurs de chaque produit.

```python
panier = [10,11,15,17,18]
```

Une liste peu être déclarer comme vide ou bien en la déclarant avec des valeurs par défaut comme ci-dessus. La déclaration d'une liste/tableau se fait en utilisant les crochets `[]`.

### Créer une Liste

```python
# crée une liste vide
t = []
# crée une liste avec des valeurs par défaut
t1 = [1,2,3,4,5]
```

### Accéder aux éléments d'une liste

On accède a une valeur d'une liste en donnant l'indice (position) de l'élément qu'on souhaite récupérer. La position d'une liste commence toujours à 0 !

```python
t = [1,5,6,8]
# récupére la première valeur du tableau
print(t[0])
>>> 1
# récupère la dernière position du tableau
print([3])
>>> 8
```

### Modifier les éléments d'une liste

On peu modifier les éléments d'une liste en accédant à l'élément de la liste puis en lui affectant une nouvelle valeur.

```python
t = [10,20,40]
t[2] = 30

print(t)
>>> [10,20,30]
```

### Fonctions utiles pour les listes

| **Méthode**        | **Description**                                              | **Exemple**                          |
|---------------------|--------------------------------------------------------------|--------------------------------------|
| `append(x)`         | Ajoute un élément `x` à la fin de la liste                  | `nombres.append(10)`                |
| `insert(i, x)`      | Insère un élément `x` à l'indice `i`                        | `nombres.insert(1, 20)`             |
| `remove(x)`         | Supprime la première occurrence de `x`                     | `nombres.remove(5)`                 |
| `pop(i)`            | Supprime et retourne l'élément à l'indice `i` (par défaut le dernier) | `nombres.pop(2)`                   |
| `index(x)`          | Retourne l'indice de la première occurrence de `x`         | `nombres.index(20)`                 |
| `len(liste)`        | Retourne le nombre d'éléments dans la liste                | `len(nombres)`                      |

## Les Boucles (while, for)

Les boucles permettent d'exécuter un bloc de code plusieurs fois.

Les boucles sont utilisés pour la pluspart des cas avec des listes puisqu'ils permettent de parcourir les éléments de la liste sans le faire à la main.

### Les boucles while

La boucle while s'éxécute tant que la condition est vrai.

**Syntaxe :**

```python
while (condition):
    ... bloc d'instructions
```

Si on souhaite afficher les nombres de 0 à 10 par exemple.

```python
i = 0
while i <= 10:
    print(i)
    i = i+1
```

Il faut **incrémenter (augmenter) la valeur i** puisque dans le cas contraire, on ne pourrait jamais sortir de la boucle. Il faut donc se rappeler que au sein d'une boucle while, il faut toujours incrémenter afin de sortir de la boucle dans le cas contraire on serait dans une boucle infinie.

La variable `i` **peu prendre n'importe quel autre nom** mais lorsqu'on effectue une **itération (parcours) sur une boucle** la norme veut qu'on l'appel i, mais vous pouvez lui donner n'importe quel nom.

On peu également arreter la boucle immédiatement avec le mot clé `break` que ce soit pour une boucle `while` ou `for`.

```python
i = 0
while True :

    print(i)
    if i == 10 :
        break
    i = i + 1
```

### Les boucles for

Les boucles for sont utilisés pour faciliter l'utilisation des listes.

**Syntaxe :**

```python
t = [1,2,3,4]

# val contient les valeurs de la liste t une par une
for val in t :
    print(val)
# Affichera
>>> 1
>>> 2
>>> 3
>>> 4
```

Les boucles for peuvent aussi être utilisés de la même manière que les boucles while en répétant un bloc d'instruction `x` fois en utilisant la fonction `range()`.

La fonction **range(start, stop, step)** peu prendre plusieurs paramètres optionnel et une obligatoire :

* **start (optionnel) : point de départ de la séquence, par défaut, elle est a 0**
* **stop (obligatoire) : La fin de la séquence (exclu).**
* **step (optionnel) : Le pas entre chaque nombre. Par défaut, c'est 1.**

Exemple :

```python

for i in range(10):
    print(i)
# affiche les valeurs de 0 à 9

for i in range(10,15):
    print(i)
# affiche les valeurs de 10 à 14

for i in range(0,20,2):
    print(i)
# affiche les valeurs 0,2,4,6 ... ,18
```

Avec cette syntaxe, nous pouvons créer une liste en une ligne ayant plusieurs valeurs selon la fonction `range`. 

Ce procédé s'appel la **compréhension** qui est le fait de créer une liste conscise et stylé, je ne vous demande pas de savoir ça pour l'instant, je prèfere que vous en restez avec les synaxes ci-dessus.

```python
# t contient une liste de 0 à 9
t = [i for i in range(10)]
```

### Exercices

Pour l'instant, je vous interdis d'utiliser les compréhension pour les exercices.

**3.1 Créer un tableau ayant les valeurs de 10 à 17 en passant par une boucle.**

```python
t = []

# ... a vous de jouer
```

**3.2 Effectuer la somme du tableau ci-dessous en utilisant la syntaxe avec la boucle while et la boucle for.**

```python
tab = [1,9,99,66,55]

# ... à vous de jouer
```

**3.3 Créer deux listes : l'une qui contient les valeurs pairs et une autre les valeurs impairs sur l'intervalle 0 à 27.**

```python
listePair = []
listeImpair = []

# ... a vous de jouer
```

**3.4 Remplacer la boucle for ci-dessous par la boucle while.**

```python
for i in range(10,40,3):
    print(i)
```

### Réponses

Si vous avez réussi tout les exercices sans soucis jusqu'a présent, vous possédez des bases assez solide permettant de comprendre tout le reste de la programmation, il faudra seulement passer par la connaissance de la syntaxe ainsi que de sa logique.

**3.1 Créer un tableau ayant les valeurs de 10 à 17 en passant par une boucle.**

```python
t = []
for i in range(10,18):
    t.append(i)
```

**3.2 Effectuer la somme du tableau ci-dessous en utilisant la syntaxe avec la boucle while et la boucle for.**

**Syntaxe avec la boucle while :**

```python
somme = 0
i = 0
tab = [1,9,99,66,55]

while i < len(tab):
    somme = somme + tab[i]
    i = i + 1
print(somme)
>>> 230
```

**Syntaxe avec la boucle for:**

```python
somme = 0
tab = [1,9,99,66,55]

for i in tab :
    somme = somme + i
print(somme)
>>> 230
```

**3.3 Créer deux listes : l'une qui contient les valeurs pairs et une autre les valeurs impairs sur l'intervalle 0 à 27.**

```python
listePair = []
listeImpair = []

for i in range(27):
    if i % 2 == 0 :
        listePair.append(i)
    else :
        listeImpair.append(i)
```


**3.4 Remplacer la boucle for ci-dessous par la boucle while.**

```python
i = 10 
while i < 40 :
    print(i)
    i = i+3
```

## Les dictionnaires

Les **dictionnaires** sont un type particulier avec un système de **clé-valeur**, **chaque clé est unique et est associé à une valeur**. Pour faire simple **pour accéder à la valeur d'un dictionnaire, on passe par sa clé**.

Les dictionnaires regroupe des valeurs selon une clé donné ça permet de savoir quel valeur correspond a quel clé. Par exemple un chat a un nom, un poid, un age.

### Créer un dictionnaire

Il existe 2 procédé pour créer un dictionnaire, comme pour les listes on peu en créer par défaut en spécifiant des valeurs et également créer un dictionnaire vide.

```python

# création d'un dictionnaire vide
dico = {}

# dictionnaire avec des valeurs par défauts
dico = {
    "Nom": "Claude",
    "age" : 66,
    "qualiter" : "BG"
}

# Une autre manière de faire en utilisant la fonction dict
dico = dict(Nom ="Claude", age=66, qualiter = "BG")
```

### Accéder à une valeur

La syntaxe pour parcourir un dictionnaire est similaire au liste sauf que ce n'est pas l'indice qu'on donne mais la clé du dictionnaire.

```python
dico = {
    "Nom": "Claude",
    "age" : 66,
    "qualiter" : "BG"
}

print(dico["Nom"])
>>> Claude
```

### Ajouter ou Modifier une valeur

C'est exactement comme pour les listes, cependant pour les dictionnaires on modifie une valeur à travers la clé.

```python

dico = dict(Nom ="Claude", age=66, qualiter = "BG")

dico["age"] = 20

# Crée une nouvelle clé qu'on associe à la valeur gros
dico["poid"] = "gros"

print(dico)
>>> {'Nom': 'Claude', 'age': 20, 'qualiter': 'BG', 'poid': 'gros'}
```

### Parcourir un dictionnaire

On peu parcourir un dictionnaire selon sa clé ou bien sa va valeur.

**Parcours pour afficher les clés du dictionnaire.**

```python
dico = dict(Nom ="Claude", age=66, qualiter = "BG")

for cle in dico :
    print(cle)

>>> Nom
>>> age
>>> qualiter
```

**Parcours pour afficher les valeurs de chaque clé du dictionnaire**

```python
dico = dict(Nom ="Claude", age=66, qualiter = "BG")

for values in dico.values() :
    print(values)

>>> Claude
>>> 66
>>> BG
```

### Fonctions utiles pour les dictionnaires

| **Méthode**         | **Description**                                          | **Exemple**                          |
|----------------------|----------------------------------------------------------|--------------------------------------|
| `get(clé, défaut)`   | Retourne la valeur associée à une clé, ou une valeur par défaut si la clé n'existe pas | `mon_dict.get("âge", 0)`            |
| `keys()`             | Retourne toutes les clés du dictionnaire                | `mon_dict.keys()`                   |
| `values()`           | Retourne toutes les valeurs du dictionnaire             | `mon_dict.values()`                 |
| `pop(clé, défaut)`   | Supprime une clé et retourne sa valeur, ou une valeur par défaut si la clé n'existe pas | `mon_dict.pop("nom", "Inconnu")`    |
| `clear()`            | Vide complètement le dictionnaire                       | `mon_dict.clear()`                  |

Tu te demandes peut-être l'utilité des dictionnaires et c'est normal !

A tes yeux tu ne vois qu'une collection représentant des clés et des valeurs, cependant si tu réfléchis bien les dictionnaires sont utilisés un peu partout et surtout en combinaisons avec des listes.

Au vu des exercices que te donne le prof, tu n'auras surement pas besoin de savoir ça mais je te montre quand même un exemple.

Imagine que tu es sur Amazon et que j'ai rajouté 3 produits dans mon panier voici à quoi cela ressemblerait sous formes de dictionnaire.

```python
panier = {
    "client" : "Claude",
    "produits" : ["bague", "chapeau", "tapis"],
    "prixDesProduits": [5,13,15],
    "prixTotal": 0
}
```

Cette syntaxe a beau être plus complexe qu'en utilisant la fonction `dict`, elle reste plus facile à comprendre selon moi mais, je te conseil d'apprendre la syntaxe en utilisant la fonction dict pour l'instant (c'est plus simple).

Comme tu as pu le voir le dictionnaire ci-dessus correspond à ma commande sur amazon cependant, il faut effectuer une somme du prix des produits afin d'avoir le prix totale de ma commande.

Si tu as bien compris le fonctionnement des dictionnaires ainsi que sa syntaxe essaye de mettre à jour le dictionnaire afin que la clé prixTotal correspond à la somme des prix des produits.

**Voici les étapes qu'il faut faire :**

* **créer une variable somme**
* **parcourir le tableau des prix des produits**
* **effectuer la somme à l'intérieur de la boucle (à l'intérieur du parcours du tableau)**
* **affecter cette valeur à notre clé prixTotal**

**Solution :**

```python
panier = {
    "client" : "Claude",
    "produits" : ["bague", "chapeau", "tapis"],
    "prixDesProduits": [5,13,15],
    "prixTotal": 0
}
somme = 0

for i in panier["prixDesProduits"]:
    somme = somme + i

panier["prixTotal"] = somme
print(panier["prixTotal"])

>>> 33
```

### Exercices

**4.1** Créer un dictionnaire **personne** comportant les clés : **nom, prenom, poid, et age**, je vous laisse le choix des valeurs cependant, vous devrez le faire de **2 manières : avec un dictionnaire vide et un dictionnaire avec des valeurs par défauts**.

**4.2** Vérifier si, il existe une clé "nom" dans le dictionnaire ci-dessous, dans le cas ou il existerait cette clé, lui affecter la valeur "Alpha" dans le cas contraire afficher une erreur avec `print()`.

Vérifier par la même occasion si il existe une valeur "Alpha" au sein de ce dictionnaire et dans le cas ou cette valeur existe afficher sa clé.

```python
dico = {
    "nope":"Alpha",
    "prenom" : "Beta",
    "age" : 56
}

# ... a vous de jouer
```

**4.3** Dans le code ci-dessous, la valeur associé à la clé prixDesProduits est un tableau, faite en sorte qu'ils contiennent les valeurs des prix de chaque produit. Effectuer ensuite la mise a jour pour que la valeur lié a la clé "prixTotal" correspondent à la somme des prix des produits.

```python
prixBague = 5
prixChapeau = 12
prixTapis = 22

panier = {
    "client" : "Claude",
    "produits" : ["bague", "chapeau", "tapis"],
    "prixDesProduits": [],
    "prixTotal": 0
}

# ... à vous de jouer
```

### Réponses

**4.1** Créer un dictionnaire **personne** comportant les clés : **nom, prenom, poid, et age**, je vous laisse le choix des valeurs cependant, vous devrez le faire de **2 manières : avec un dictionnaire vide et un dictionnaire avec des valeurs par défauts**.

```python

# dictionnaire vide
personne = {}

personne["nom"] = "je pleure"
personne["prenom"] = "sur le poulet"
personne["poid"] = 10
personne["age"] = 5

# dictionnaire personne avec des valeurs par défauts
personne = {
    "nom" :"je pleure",
    "prenom" : "sur le poulet",
    "poid" : 10,
    "age" : 5
}
```

**4.2** Vérifier si, il existe une clé "nom" dans le dictionnaire ci-dessous, dans le cas ou il existerait cette clé, lui affecter la valeur "Alpha" dans le cas contraire afficher une erreur avec `print()`.

Vérifier par la même occasion si il existe une valeur "Alpha" au sein de ce dictionnaire et dans le cas ou cette valeur existe afficher sa clé.

```python
dico = {
    "nope":"Alpha",
    "prenom" : "Beta",
    "age" : 56
}

if "nom" in dico :
    dico["nom"] = "Alpha"
else :
    print("Le dictionnaire n'a pas de clé nom")

if "Alpha" in dico.values():
    for cle, val in dico.items() :
        if val == "Alpha":
            print(f"la clé lié a la valeur alpha est : {cle}")
            break
else :
    print("Le dictionnaire ne comporte pas de valeur Alpha")
```

**4.3** Dans le code ci-dessous, la valeur associé à la clé prixDesProduits est un tableau, faite en sorte qu'ils contiennent les valeurs des prix de chaque produit. Effectuer ensuite la mise a jour pour que la valeur lié a la clé "prixTotal" correspondent à la somme des prix des produits.

```python
prixBague = 5
prixChapeau = 12
prixTapis = 22

panier = {
    "client" : "Claude",
    "produits" : ["bague", "chapeau", "tapis"],
    "prixDesProduits": [],
    "prixTotal": 0
}

panier["prixDesProduits"].append(prixBague)
panier["prixDesProduits"].append(prixChapeau)
panier["prixDesProduits"].append(prixTapis)

# il est préférable d'utiliser une boucle au lieu de le faire a la main même si cela est possible.
somme = 0
for i in panier["prixDesProduits"]:
    somme = somme + i

print(somme)
>>> 39
```

## Les fonctions récursives

Les **fonctions récursifs** est juste un terme qui **signifie qu'une fonction s'appel elle même**. Une fonction récursif a le même objetif qu'une boucle qui est d'executer plusieurs fois un bloc d'instruction.

Il faut donc comme pour une boucle `while`, **un point d'arrêt** permettant de sortir d'arreter notre fonction lorsque la tâche a été effectué, dans le cas contraire la fonction s'appelerait elle même jusqu'a l'infini.

Par exemple si l'on souhaite afficher 10 fois le message "je pleure" en utilisant une fonction récursif, on aurait quelque chose comme ça :

```python
def recursif(n):
    print("je pleure")
    if n == 0 :
        print("fin de la fonction")
    else :
        recursif(n -1)

recursif(10)
```

Ce qui est bien avec les fonctions récursifs c'est que le code est similaire a la demande par exemple si on vous demande d'effectuer le factorielle d'un nombre avec une fonction récursif. **Il suffit d'un point d'arret et d'effectuer le return de la formule**.

Voici la formule du factorielle d'un nombre :

* ### n!=n×(n−1)!

Fonction récursif d'un factorielle d'un nombre :

```python
def factorielle(n):
    if n == 0:
        return 1
    return n * factorielle(n-1)
```

La logique est la même avec d'autres formules, je vous mets ici quelques exemples :

* **La suite de Fibonacci : `F(n)=F(n−1)+F(n−2)`**
* **Somme des nombres naturels : `S(n)=n+S(n−1)`**

```python
def fibonnaci(n):
    if n == 0 :
        return 0
    elif n == 1:
        return 1
    return fibonnaci(n - 1) + fibonnaci(n - 2)

def somme(n):

    if n == 0:
        return 0
    return n + somme(n - 1)
```

Comme tu as pu le voir, on ne se casse pas vraiment la tête, **il suffit d'un point d'arret pour arreter la fonction puis de littéralement copier coller la formule donné dans le return**.

Malheuresement pour toi, il est possible que tu es affaire à des exercices n'ayant pas forcément de formule. C'est à ce moment la ou, il faudra se servir de sa petite tête pour réfléchir a comment effectuer cette exercice.

### Exercices

**4.1 Calculer la puissance d'un nombre par n**

**Formule de la puissance d'un nombre par n :**

$$
\text{puissance}(x, n) =
\begin{cases} 
1 & \text{si } n = 0, \\
x \times \text{puissance}(x, n-1) & \text{si } n > 0.
\end{cases}
$$

**4.2 Calculer la somme d'une liste**

```python
def somme(liste):
    # ... a vous de jouer

t = [1,2,3,4,77,-5]
print(somme(t))
# la fonction doit afficher 82
>>> 82
```

**4.3 Vérifier si le caractère `"t"` est dans la chaine de caractère, si le caractère est présent renvoyé True dans le cas contraire False**

```python
def is_character_present(chaine,caractere):
    # ... a vous de jouer

print(is_character_present("Wallah je souffre trop","t"))
>>> True
```

**4.4 Vérifier si une chaine de caractère est un palindrome, c'est à dire qu'il se lit dans les deux sens. Par exemple radar, non, kayak sont un palindrome. Si il s'avère que la chaine de caractère est un palindrome renvoyé True sinon False.**

```python
def is_palindrome(chaine):
    # ... a vous de jouer

print(is_palindrome("kayak"))
>>> True
print(is_palindrome("shifumi"))
>>> False
```

### Réponses

**4.1 Calculer la puissance d'un nombre par n**

```python
def puissance(x, n):
    if n == 0:
        return 1
    return x * puissance(x, n-1)
```

**4.2 Calculer la somme d'une liste**

```python
def somme(liste):
    if len(liste) == 0:
        return 0
    return liste[0] + somme(liste[1:len(liste)])

t = [1,2,3,4,77,-5]
print(somme(t))
>>> 82
```

On peu récupérer une partie d'une liste en la spécifiant comme une intervalle de cette manière `liste[start : end]`. Etant donné que c'est une somme, il faut forcément la sauvegarder quelque part, on va la sauvegarder directement dans le return a travers `liste[0]` **qui va sauvegarder l'addition des éléments**. Et enfin, il faut forcément désincrementer ou incrémenter afin de sortir de la fonction récursif, dans notre cas on va désincrementer. La désincrémentation se fait à travers `liste[1:len(liste)]` qui peu également être fait sans spécifier le end (optionnel) de cette manière : `liste[1:]`. Ici on enleve a chaque fois le premièr indice ce qui nous permet de **réduire la taille de notre tableau (désincrémenter)**.

Cette logique sera utilisé pour les prochains exercices également.

**4.3 Vérifier si le caractère `"t"` est dans la chaine de caractère, si le caractère est présent renvoyé True dans le cas contraire False**

```python
def is_character_present(chaine,caractere):
    if len(chaine) == 0 :
        return False
    
    elif chaine[0] == caractere:
        return True
    return is_character_present(chaine[1:],caractere)

print(is_character_present("Wallah je souffre trop","t"))
>>> True
```

**4.4 Vérifier si une chaine de caractère est un palindrome, c'est à dire qu'il se lit dans les deux sens. Par exemple radar, non, kayak sont un palindrome. Si il s'avère que la chaine de caractère est un palindrome renvoyé True sinon False.**

```python
def is_palindrome(chaine):
    if len(chaine) <= 1:
        return True
    
    if chaine[0] != chaine[len(chaine)-1]:
        return False

    return is_palindrome(chaine[1:len(chaine)-1])
        
print(is_palindrome("kayak"))
>>> True
print(is_palindrome("shifumi"))
>>> False
```

On compare au fur et a mesure **le premier et le dernier caractère** et **dans le cas ou celle-ci ne sont pas égale on renvoie False**, dans le cas contraire **on reduit la taille de la chaine de 2 (1 pour le premier indice et 1 autre pour le dernier indice)**. Lorsqu'on arrive à une longueur inférieur ou égal a 1 cela signifie que notre chaine de caractère est un **palindrome**.

### Résumé

Les **fonctions récursives demandent énormément de réflexion** contrairement aux boucles cependant celle-ci peu s'averer plus lisible notamment dans le cas ou on aurait besoin d'utiliser des formules mathématiques.


**Liste des conditions à impérativement savoir sur les fonctions récursives :**

| **Condition**           | **Description**                                                                 | **Exemple**                         |
|--------------------------|---------------------------------------------------------------------------------|-------------------------------------|
| **Condition d'arrêt**    | La fonction doit savoir quand s'arrêter pour éviter une boucle infinie.         | Retourner `1` si `n == 0` pour une factorielle. |
| **Appel récursif**       | La fonction doit s'appeler sur un sous-problème plus petit.                     | Appeler `fibonacci(n-1)` pour réduire l'échelle du problème. |
| **Transformation du problème** | Le problème doit être réduit à chaque étape pour converger vers la condition d'arrêt. | Réduire une liste avec `liste[1:]` ou un entier avec `n-1`. |
| **Retour du résultat**   | Chaque appel récursif doit retourner un résultat pour construire la solution finale. | Retourner `x * puissance(x, n-1)` pour une puissance. |

