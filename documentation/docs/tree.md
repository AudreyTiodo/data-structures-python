# Documentation de la classe `BinarySearchTree`

La classe `BinarySearchTree` implémente un arbre binaire de recherche (BST) permettant d'insérer des éléments, de les rechercher, et de traverser l'arbre de différentes manières (infixe, préfixe et postfixe).

## Attributs

- `root` : Le nœud racine de l'arbre, initialisé à `None`.

## Méthodes

### `__init__(self)`
Initialise un nouvel arbre binaire de recherche (BST) vide.

#### Retour :
- Aucun retour. L'arbre est initialisé avec une racine `None`.

### `insert(self, value)`
Insère une valeur dans l'arbre binaire de recherche (BST).

#### Arguments :
- `value` : La valeur à insérer dans l'arbre.

#### Retour :
- Aucun retour. La valeur est insérée dans l'arbre.

### `_insert_recursive(self, node, value)`
Méthode auxiliaire pour l'insertion récursive dans l'arbre.

#### Arguments :
- `node` : Le nœud actuel à partir duquel la recherche d'insertion commence.
- `value` : La valeur à insérer dans l'arbre.

#### Retour :
- Aucun retour. La valeur est insérée récursivement à la position correcte dans l'arbre.

### `search(self, value)`
Recherche une valeur dans l'arbre binaire de recherche (BST).

#### Arguments :
- `value` : La valeur à rechercher dans l'arbre.

#### Retour :
- `True` si la valeur est trouvée dans l'arbre, `False` sinon.

### `_search_recursive(self, node, value)`
Méthode auxiliaire pour la recherche récursive d'une valeur dans l'arbre.

#### Arguments :
- `node` : Le nœud actuel où la recherche commence.
- `value` : La valeur à rechercher dans l'arbre.

#### Retour :
- `True` si la valeur est trouvée dans l'arbre, `False` sinon.

### `inorder_traversal(self)`
Retourne une liste des valeurs de l'arbre en utilisant un parcours infixe (inorder).

#### Retour :
- Une liste des valeurs de l'arbre en ordre croissant.

### `_inorder_recursive(self, node, result)`
Méthode auxiliaire pour le parcours infixe récursif de l'arbre.

#### Arguments :
- `node` : Le nœud actuel pour le parcours.
- `result` : La liste qui contient les valeurs du parcours.

#### Retour :
- Aucun retour. Les valeurs sont ajoutées à la liste `result` par récursion.

### `preorder_traversal(self)`
Retourne une liste des valeurs de l'arbre en utilisant un parcours préfixe (preorder).

#### Retour :
- Une liste des valeurs de l'arbre dans l'ordre préfixe.

### `_preorder_recursive(self, node, result)`
Méthode auxiliaire pour le parcours préfixe récursif de l'arbre.

#### Arguments :
- `node` : Le nœud actuel pour le parcours.
- `result` : La liste qui contient les valeurs du parcours.

#### Retour :
- Aucun retour. Les valeurs sont ajoutées à la liste `result` par récursion.

### `postorder_traversal(self)`
Retourne une liste des valeurs de l'arbre en utilisant un parcours postfixe (postorder).

#### Retour :
- Une liste des valeurs de l'arbre dans l'ordre postfixe.

### `_postorder_recursive(self, node, result)`
Méthode auxiliaire pour le parcours postfixe récursif de l'arbre.

#### Arguments :
- `node` : Le nœud actuel pour le parcours.
- `result` : La liste qui contient les valeurs du parcours.

#### Retour :
- Aucun retour. Les valeurs sont ajoutées à la liste `result` par récursion.

### `__str__(self)`
Retourne une représentation sous forme de chaîne de caractères de l'arbre binaire de recherche en utilisant un parcours infixe.

#### Retour :
- Une chaîne de caractères représentant les valeurs de l'arbre dans l'ordre infixe sous la forme de liste.

## Exemple d'utilisation

```python
# Création d'un arbre binaire de recherche
bst = BinarySearchTree()

# Insertion des valeurs
bst.insert(10)
bst.insert(5)
bst.insert(15)
bst.insert(2)
bst.insert(7)
bst.insert(12)
bst.insert(18)

# Recherche d'une valeur dans l'arbre
print(bst.search(7))  # Affiche : True
print(bst.search(20))  # Affiche : False

# Parcours infixe (inorder)
print(bst.inorder_traversal())  # Affiche : [2, 5, 7, 10, 12, 15, 18]

# Parcours préfixe (preorder)
print(bst.preorder_traversal())  # Affiche : [10, 5, 2, 7, 15, 12, 18]

# Parcours postfixe (postorder)
print(bst.postorder_traversal())  # Affiche : [2, 7, 5, 12, 18, 15, 10]

# Affichage de l'arbre sous forme de chaîne
print(bst)  # Affiche : [2, 5, 7, 10, 12, 15, 18]
