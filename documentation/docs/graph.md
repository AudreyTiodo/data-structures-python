# Documentation de la classe `Graph`

La classe `Graph` implémente un graphe à l'aide d'une liste d'adjacence, et offre des méthodes pour effectuer des traversées en profondeur (DFS) et en largeur (BFS), ainsi que pour ajouter des arêtes et afficher le graphe sous forme de chaîne.

## Attributs

- `graph` : Un dictionnaire de type `defaultdict(list)` représentant les arêtes du graphe. Chaque clé est un sommet, et la valeur associée est la liste des voisins de ce sommet.
- `directed` : Booléen indiquant si le graphe est dirigé (`True`) ou non dirigé (`False`).

## Méthodes

### `__init__(self, directed=False)`
Initialise un graphe vide.

#### Arguments :
- `directed` : Booléen. Si `True`, crée un graphe dirigé, sinon crée un graphe non dirigé (par défaut `False`).

#### Retour :
- Aucun retour. La méthode initialise simplement le graphe.

### `add_edge(self, u, v)`
Ajoute une arête entre les sommets `u` et `v`.

#### Arguments :
- `u` : Premier sommet de l'arête.
- `v` : Deuxième sommet de l'arête.

#### Retour :
- Aucun retour. Les arêtes sont ajoutées dans la liste d'adjacence du graphe. Si le graphe est non dirigé, l'arête est ajoutée dans les deux sens (`u -> v` et `v -> u`).

### `dfs(self, start)`
Effectue une traversée en profondeur (Depth-First Search, DFS) à partir du sommet `start`.

#### Arguments :
- `start` : Sommet de départ pour la traversée DFS.

#### Retour :
- Une liste des sommets dans l'ordre de leur visite lors de la traversée DFS.

### `bfs(self, start)`
Effectue une traversée en largeur (Breadth-First Search, BFS) à partir du sommet `start`.

#### Arguments :
- `start` : Sommet de départ pour la traversée BFS.

#### Retour :
- Une liste des sommets dans l'ordre de leur visite lors de la traversée BFS.

### `__str__(self)`
Retourne une représentation en chaîne du graphe sous forme de liste d'adjacence triée.

#### Retour :
- Une chaîne représentant le graphe, chaque ligne correspondante à un sommet et ses voisins sous forme de liste.

## Exemple d'utilisation

```python
# Création d'un graphe non dirigé
graph = Graph(directed=False)

# Ajout d'arêtes
graph.add_edge(1, 2)
graph.add_edge(1, 3)
graph.add_edge(2, 4)

# Affichage du graphe
print(graph)
# Affiche :
# 1: [2, 3]
# 2: [1, 4]
# 3: [1]
# 4: [2]

# Traversée DFS
print(graph.dfs(1))  # Affiche : [1, 3, 2, 4]

# Traversée BFS
print(graph.bfs(1))  # Affiche : [1, 2, 3, 4]
