# TVOS

### Quand je change de vue je n'ai plus de focus / le focus ne semble pas marcher
ex: Player qui se superpose avec un overlay

Solution :
Penser à faire une mise à jour du focus pour que le système mette à jour son système de focus.
```swift
self.setNeedsFocusUpdate()
```
### Je n'arrive pas a jouer de son, pourtant ça marche sur mon simu 

Il n'y a pas de local storage sur l'apple TV, tout le contenu stocké peut être supprimé au démarage.
Si on stock des données la clé de directory .documentDirectory ne va pas marcher il faut utiliser .cachesDirectory.

### Liens sympas 
[Doc Focus Engine](https://www.bignerdranch.com/blog/10-tips-for-mastering-the-focus-engine-on-tvos/)
