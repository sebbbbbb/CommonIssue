## UICollectionView

### 

La méthode suivant n'est pas appelée:
```swift
 func collectionView(_ collectionView: UICollectionView, layout collectionViewLayout: UICollectionViewLayout, sizeForItemAt indexPath: IndexPath) -> CGSize 
```
 
 Solution:
 Bien implémenter les deux protocoles:
 * UICollectionViewDelegate
 * UICollectionViewDelegateFlowLayout

### 

Collection View mal redimensionnée mais cellules avec la bonne taille

Solution
Désactiver les contraintes


### Ma cellule change de données quand je scroll !

Solution :
* Si la cellule dispose de state pour afficher son contenu (ex: vue à cacher) bien penser à le réinitialiser à chaque fois
pour ne pas avoir une cellule mal recyclée

### Ma Collection View rame à mort quand je scroll plusieurs fois

Solution : 
* Si on y ajoute une cellule depuis un nib, vérifier que la vue n'est pas déja contenue dedans sinon elle va s'ajouter add vitam eternam

### Soucis de performance, ex: result AM

* Possiblité de désactiver le recyclage en mettant des index unique pour les identifiants

### Le layout casse sans raison

* Bien tester en enlevant toutes les opérations sur la collection view, eg: performBatchUpdates. (soucis rencontré sur Ludo) ...

### Crash quand je recupère ma cellule alors qu'elle est bien register !

* Regarder si le .xib utilise bien la bonne classe et non pas la classe de base.


### CellForItem appelé tout le temp
* Eviter d'avoir une collectionView embed dans une scrollView ...
