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
