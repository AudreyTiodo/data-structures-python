# Documentation de la classe `MyArray`

La classe `MyArray` est une extension de la classe `numpy.ndarray`, ajoutant des méthodes supplémentaires pour faciliter l'interaction avec des tableaux numériques. Elle hérite de toutes les fonctionnalités de `numpy.ndarray` tout en ajoutant des fonctionnalités supplémentaires pour la somme, la moyenne, la forme, le tri, et d'autres opérations.

## Attributs

- Hérite de tous les attributs de `numpy.ndarray`.

## Méthodes

### `__new__(cls, input_array)`
Crée une nouvelle instance de la classe `MyArray`.

#### Arguments :
- `input_array` : Les données d'entrée qui peuvent être converties en un tableau numpy.

#### Retour :
- Retourne une instance de `MyArray` contenant les données spécifiées.

### `__array_finalize__(self, obj)`
Finalise la création de l'array. Cette méthode est appelée lors de la création ou de la modification de l'array, mais dans ce cas, elle ne fait rien de spécifique à part vérifier si l'objet est `None`.

#### Arguments :
- `obj` : L'objet auquel l'array est associé (par exemple, une vue ou une modification).

#### Retour :
- Aucun retour.

### `sum(self)`
Calcule la somme des éléments du tableau.

#### Retour :
- Retourne la somme de tous les éléments dans l'array, équivalent à `numpy.sum()`.

### `mean(self)`
Calcule la moyenne des éléments du tableau.

#### Retour :
- Retourne la moyenne des éléments dans l'array, équivalent à `numpy.mean()`.

### `shape(self)`
Retourne la forme du tableau.

#### Retour :
- Retourne un tuple représentant la forme du tableau (le nombre de dimensions et la taille dans chaque dimension).

### `reshape(self, new_shape)`
Redimensionne le tableau à une nouvelle forme.

#### Arguments :
- `new_shape` : La nouvelle forme souhaitée pour le tableau. Cela doit être un tuple représentant les dimensions du tableau redimensionné.

#### Retour :
- Retourne un nouvel objet `MyArray` redimensionné avec la forme spécifiée.

### `max(self)`
Retourne la valeur maximale dans le tableau.

#### Retour :
- Retourne la valeur maximale parmi les éléments du tableau, équivalent à `numpy.max()`.

### `min(self)`
Retourne la valeur minimale dans le tableau.

#### Retour :
- Retourne la valeur minimale parmi les éléments du tableau, équivalent à `numpy.min()`.

### `sort(self, axis=-1)`
Trie les éléments du tableau.

#### Arguments :
- `axis` : L'axe le long duquel trier les éléments. Par défaut, il trie le tableau à plat (sur l'axe `-1`).

#### Retour :
- Retourne un nouvel objet `MyArray` avec les éléments triés selon l'axe spécifié.

## Exemple d'utilisation

```python
import numpy as np

# Création d'un tableau MyArray à partir d'une liste
arr = MyArray([1, 2, 3, 4, 5])

# Somme des éléments
print(arr.sum())  # Affiche : 15

# Moyenne des éléments
print(arr.mean())  # Affiche : 3.0

# Forme du tableau
print(arr.shape())  # Affiche : (5,)

# Redimensionnement
arr_reshaped = arr.reshape((1, 5))
print(arr_reshaped.shape())  # Affiche : (1, 5)

# Valeur maximale
print(arr.max())  # Affiche : 5

# Tri des éléments
print(arr.sort())  # Affiche : [1 2 3 4 5]
