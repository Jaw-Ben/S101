# SAÉ S1.01 : Community detection


Ce document correspond au sujet de la SAÉ S1.01 de l'année universitaire 2022/2023. Ce travail est à faire par binôme en autonomie.

## Évaluation

La SAÉ sera notée de la manière suivante : 
- Évaluation du rendu : 8 points répartis de la manière suivante
    - Correction automatique du code via des tests unitaires : 2 points
    - Tests unitaires rendus : 2 points
    - Qualité du code (clarté, efficacité, commentaires, docstring) : 2 points
    - Comparaison expérimentale et théorique (fichier notebook) : 2 points
- Contrôle : 12 points 

## Sujet


**Important :** Dans ce projet
- une personne fait référence à une chaîne de caractères qui est le prénom de cette personne ; par exemple `"Alice"` est une personne.
- un groupe de personnes est un tableau de personnes, c'est-à-dire un tableau de chaînes de caractères qui sont les prénoms des personnes. Par exemple, `["Alice", "Bob"]` est un groupe de deux personnes.
- le terme réseau (network en anglais) correspond à un dictionnaire dont les clés sont les prénoms des personnes et les valeurs des tableaux contenant la liste des amis de la personne, comme dans la SAÉ S01.01. Par exemple,
  ```python
  {
    "Alice" : ["Bob", "Dominique"],
    "Bob" : ["Alice", "Charlie", "Dominique"],
    "Charlie" : ["Bob"],
    "Dominique" : ["Alice", "Bob"]
  }
  ```
  est un réseau de 4 personnes : Alice, Bob, Charlie et Dominique. Bob est ami avec tout le monde et Alice est également amie avec Dominique.

  **Remarque :** L'ordre des amis d'une personne n'a pas d'importance. Le réseau aurait pu être représenté par ce dictionnaire : 
  ```python
  {
    "Alice" : ["Bob", "Dominique"],
    "Bob" : ["Alice", "Dominique", "Charlie"],
    "Charlie" : ["Bob"],
    "Dominique" : ["Bob", "Alice"]
  }
  ```
- une communauté est un groupe de personnes qui sont toutes amies entre elles, c'est-à-dire que lorsque l'on prend n'importe quelles deux personnes du groupe, elles sont amies. Pour le réseau donné en exemple, `["Alice", "Bob", "Dominique"]` est une communauté alors que `["Alice", "Bob", "Charlie"]` n'en est pas une.

# README - Analyse d'un réseau d'amitiés en Python

Ce projet propose une analyse d'un réseau d'amitiés en Python à travers plusieurs fonctions.
Chaque fonction réalise une tâche spécifique sur les données et est présentée sous forme d'exercice.

## Exercice 0 : Données de base
Nous avons une liste `p_amis` contenant des prénoms représentant un réseau d'amitiés.

```
["Joël","Muriel","Yasmine","Joël","Yasmine","Muriel",
"Yasmine","Thomas","Joël","Nassim","Andrea","Ali",
"Nassim","Ali","Joël","Andrea","Joël","Ali",
"Nassim","Andrea","Axel","Leo","Daria","Thomas",
"Carole","Thomas","Thierry","Axel","Thierry","Leo",
"Valentin","Leo","Valentin","Andrea"]
```
Nous avons une liste `p_amis` contenant des prénoms représentant un réseau d'amitiés.

## Exercice 1 : Compter les occurrences d'un prénom
Créez une fonction `nb_amis(amis, prenom)` qui renvoie le nombre de fois qu'un prénom apparaît dans la liste.

## Exercice 2 : Taille du réseau
Créez une fonction `taille_reseau(amis)` qui renvoie le nombre de personnes uniques dans la liste.

## Exercice 3 : Lecture d'un fichier de relations
Créez une fonction `lecture_reseau(path)` qui lit un fichier contenant des relations d'amitiés.

## Exercice 4 : Modélisation sous forme de dictionnaire
Créez une fonction `dico_reseau(amis)` qui renvoie un dictionnaire avec les relations d'amitiés.

## Exercice 5 : Nombre d'amis du plus populaire
Créez une fonction `nb_amis_plus_pop(dico_reseau)` qui retourne le nombre d'amis de la personne la plus populaire.

## Exercice 6 : Trouver les plus populaires
Créez une fonction `les_plus_pop(dico_reseau)` qui renvoie les prénoms des personnes les plus populaires (au moins 5 amis).

