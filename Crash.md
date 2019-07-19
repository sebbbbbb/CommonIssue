## Crash
#### Crash sur iOS10
* Si le crash se produit lors d'une opération qui nécessite une demande d'autorisation vérifier le *.plist* pour voir si l'autorisation est bien inscrite

#### UIKit

## *** Terminating app due to uncaught exception 'CALayerInvalid', reason: 'layer <CALayer: 0x7fda42c66e30> is a part of cycle in its layer tree'

* Regarder si on ajoute pas un view controller dans lui même (idp ...)

### Crash with a constraint which can be installed or nord
* If you wanted to uninstall a constraint and reinstal it later make sure to don't make it weak otherwise it will be deallocated


##### Crash sans raison après avoir déplacé des fichiers (Xcode9)

* Regarde si Xcode n'a pas virer la target membership des fichiers déplacés

#### Sans raison

* Si c'est une vue qui est chargé, regarder si tous les IBOutlet sont connectés

#### Je n'arrive pas a checker mes crash sur fabrics
* Uploader les dsym de l'archive sur fabrics
* Si possible actier le bitcode pour avoir accès aux .dsym depuis itunes 
