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
