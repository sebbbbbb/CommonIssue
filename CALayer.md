# CALayer

### Mon gradient est peté en cas de rotation

* Quand on ajoute le gradient en tant que sous layer il est n'est pas dans le même repère que la vue, il faut donc
crée une vue qui contient directement le layer.
eg : https://stackoverflow.com/questions/17555986/cagradientlayer-not-resizing-nicely-tearing-on-rotation


### Animation qui ne marche pas sur une collectionView après un recyclage (iOS9)

* Lancer l'animation sur *cell.contentView* et non pas *cell*.
