# Documentation du package `data_structures`

Le package `data_structures` est une collection d'implémentations de structures de données de base. Ce package offre des implémentations pour plusieurs structures de données courantes, qui sont utilisées dans de nombreux algorithmes et applications logicielles.

## Contenu du package

Ce package fournit des implémentations des structures de données suivantes :
- **Tableaux** (basés sur `numpy`)
- **Piles** (Stacks)
- **Files** (Queues)
- **Listes chaînées** (Linked Lists)
- **Arbres binaires de recherche** (Binary Search Trees)
- **Graphes** (Graphs)

## Modules et classes

### `array`
- **`MyArray`** : Une extension de `numpy.ndarray`, ajoutant des méthodes supplémentaires pour effectuer des calculs comme la somme, la moyenne, la recherche du maximum et du minimum.

### `stack`
- **`Stack`** : Une implémentation de pile (Stack) basée sur une liste, permettant d'ajouter (`push`) et de retirer (`pop`) des éléments dans un ordre LIFO (Last In, First Out).

### `queue`
- **`Queue`** : Une implémentation de file (Queue) basée sur une liste, permettant d'ajouter (`enqueue`) et de retirer (`dequeue`) des éléments dans un ordre FIFO (First In, First Out).

### `linked_list`
- **`LinkedList`** : Une implémentation de liste simplement chaînée, permettant d'ajouter, de supprimer et de rechercher des éléments à une position donnée dans la liste.

### `tree`
- **`BinarySearchTree`** : Une implémentation d'arbre binaire de recherche (BST), permettant d'insérer, de rechercher et de traverser l'arbre de différentes manières (infixe, préfixe et postfixe).
- **`TreeNode`** : Classe représentant un nœud dans un arbre binaire, avec un attribut `value` pour stocker la valeur du nœud et des pointeurs vers ses sous-arbres gauche et droit.

### `graph`
- **`Graph`** : Une implémentation de graphe en utilisant une liste d'adjacence, permettant d'ajouter des arêtes et de parcourir le graphe à l'aide de recherches en profondeur (DFS) ou en largeur (BFS).

## Variables globales

### `__all__`
La variable `__all__` définit les objets que ce package exporte lorsqu'il est importé avec `from package import *`. Elle contient les éléments suivants :
```python
['MyArray', 'Stack', 'Queue', 'LinkedList', 'BinarySearchTree', 'TreeNode', 'Graph']
