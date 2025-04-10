# Documentation de la classe `Queue`

La classe `Queue` implémente une file (queue) en utilisant une liste comme stockage sous-jacent. Elle permet d'ajouter des éléments à la fin de la file, de les retirer du début, et de vérifier l'état de la file.

## Attributs

- `queue` : Liste qui contient les éléments de la file.

## Méthodes

### `__init__(self, initial_items=None)`
Initialise une nouvelle file.

#### Arguments :
- `initial_items` : Liste optionnelle d'éléments pour initialiser la file. Si non spécifiée, la file sera vide.

#### Retour :
- Aucun retour. La méthode initialise la file avec les éléments fournis (ou une file vide si aucun élément n'est donné).

### `enqueue(self, item)`
Ajoute un élément à la fin de la file.

#### Arguments :
- `item` : L'élément à ajouter à la fin de la file.

#### Retour :
- Aucun retour. L'élément est ajouté à la fin de la file.

### `dequeue(self)`
Retire et retourne l'élément du début de la file.

#### Exceptions :
- `IndexError` : Si la file est vide.

#### Retour :
- L'élément retiré du début de la file.

### `peek(self)`
Retourne l'élément du début de la file sans le retirer.

#### Exceptions :
- `IndexError` : Si la file est vide.

#### Retour :
- L'élément du début de la file sans le retirer.

### `is_empty(self)`
Retourne `True` si la file est vide, sinon `False`.

#### Retour :
- `True` si la file est vide, `False` sinon.

### `size(self)`
Retourne le nombre d'éléments dans la file.

#### Retour :
- Le nombre d'éléments dans la file.

### `__str__(self)`
Retourne une représentation sous forme de chaîne de la file.

#### Retour :
- Une chaîne représentant la file sous la forme `Queue([element1, element2, ...])`.

### `__len__(self)`
Retourne le nombre d'éléments dans la file.

#### Retour :
- Le nombre d'éléments dans la file (équivalent à `self.size()`).

## Exemple d'utilisation

```python
# Création d'une file avec des éléments initiaux
queue = Queue([1, 2, 3])

# Ajout d'un élément à la fin de la file
queue.enqueue(4)

# Affichage de la file
print(queue)  # Affiche : Queue([1, 2, 3, 4])

# Retrait d'un élément du début de la file
print(queue.dequeue())  # Affiche : 1

# Affichage de la file après le retrait
print(queue)  # Affiche : Queue([2, 3, 4])

# Vérification de l'élément au début de la file
print(queue.peek())  # Affiche : 2

# Vérification si la file est vide
print(queue.is_empty())  # Affiche : False

# Taille de la file
print(queue.size())  # Affiche : 3

# Utilisation de la méthode __len__ pour obtenir la taille
print(len(queue))  # Affiche : 3
