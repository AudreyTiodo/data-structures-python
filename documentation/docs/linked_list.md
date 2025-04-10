# Documentation des classes `Node` et `LinkedList`

Les classes `Node` et `LinkedList` implémentent une liste simplement chaînée. La classe `Node` représente un élément de la liste, et la classe `LinkedList` gère la liste elle-même avec des méthodes pour insérer, supprimer, rechercher et parcourir les éléments.

## Classe `Node`

La classe `Node` représente un noeud individuel dans la liste chaînée. Chaque noeud contient des données et une référence vers le prochain noeud dans la liste.

### Attributs

- `data` : Les données stockées dans le noeud.
- `next` : Référence vers le prochain noeud dans la liste (par défaut `None`).

### Méthodes

#### `__init__(self, data)`
Initialise un nouveau noeud avec les données fournies.

##### Arguments :
- `data` : Les données à stocker dans le noeud.

#### `__repr__(self)`
Retourne une représentation sous forme de chaîne du noeud.

##### Retour :
- Une chaîne représentant le noeud, par exemple `Node(5)`.

## Classe `LinkedList`

La classe `LinkedList` implémente une liste simplement chaînée avec des méthodes pour insérer, supprimer, rechercher, et parcourir les éléments.

### Attributs

- `head` : Référence vers le premier noeud de la liste (par défaut `None`).
- `size` : Taille de la liste, c'est-à-dire le nombre d'éléments dans la liste.

### Méthodes

#### `__init__(self)`
Initialise une nouvelle liste chaînée vide.

##### Retour :
- Aucun retour. La méthode initialise une liste vide.

#### `insert(self, data, position=0)`
Insère un nouveau noeud contenant `data` à la position spécifiée dans la liste.

##### Arguments :
- `data` : Les données à insérer dans le nouveau noeud.
- `position` : La position (index basé sur 0) où insérer le noeud. Par défaut, le noeud est inséré au début de la liste (`position=0`).

##### Exceptions :
- `IndexError` : Si la position spécifiée est en dehors des limites de la liste.

##### Retour :
- Aucun retour. Le noeud est inséré à la position spécifiée.

#### `delete(self, position)`
Supprime le noeud à la position spécifiée dans la liste.

##### Arguments :
- `position` : La position (index basé sur 0) du noeud à supprimer.

##### Exceptions :
- `IndexError` : Si la position spécifiée est en dehors des limites de la liste ou si la liste est vide.

##### Retour :
- Aucun retour. Le noeud est supprimé de la liste.

#### `search(self, data)`
Recherche un noeud contenant `data` dans la liste.

##### Arguments :
- `data` : Les données à rechercher dans la liste.

##### Retour :
- La position du premier noeud contenant `data` si trouvé.
- `-1` si `data` n'est pas trouvé dans la liste.

#### `traverse(self)`
Retourne une liste contenant toutes les données des noeuds de la liste chaînée.

##### Retour :
- Une liste des données dans l'ordre de la liste chaînée.

#### `__len__(self)`
Retourne la taille de la liste chaînée.

##### Retour :
- Le nombre d'éléments dans la liste.

#### `__str__(self)`
Retourne une représentation sous forme de chaîne de la liste chaînée.

##### Retour :
- Une chaîne représentant la liste chaînée. Les noeuds sont séparés par " -> ".
- Si la liste est vide, retourne "Empty LinkedList".

## Exemple d'utilisation

```python
# Création d'une liste chaînée
ll = LinkedList()

# Insertion de noeuds
ll.insert(10)
ll.insert(20)
ll.insert(30, position=1)

# Affichage de la liste
print(ll)  # Affiche : 10 -> 30 -> 20

# Recherche d'un élément
print(ll.search(20))  # Affiche : 2
print(ll.search(40))  # Affiche : -1

# Traversée de la liste
print(ll.traverse())  # Affiche : [10, 30, 20]

# Suppression d'un noeud
ll.delete(1)  # Supprime le noeud à la position 1 (30)

# Affichage après suppression
print(ll)  # Affiche : 10 -> 20

# Taille de la liste
print(len(ll))  # Affiche : 2
