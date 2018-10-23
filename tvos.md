# TVOS

### Quand je change de vue je n'ai plus de focus / le focus ne semble pas marcher
ex: Player qui se superpose avec un overlay

Solution :
Penser à faire une mise à jour du focus pour que le système mette à jour son système de focus.
```swift
self.setNeedsFocusUpdate()
```
