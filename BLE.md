# Bluetooth

## Infos :
* Sur iOS11> désactiver le bluetooth via le control-center ne le désactive pas totalement, les appareils BLE marchent même si il est désactivé
dans le control center.
* Lors de l'instanciation de CBPeripheralManager() une popup sytème est affichée dans le cas ou le bluetooth est totalement désactivé,
il faut donc instancier cette objet quand on à vraiment besoin du bluetooth.
* Quand l'application autorise la mise à jour de la position en background une nouvelle position peut redémarer l'application.
* Sur iOS9 les clés de .plist pour les demandes d'autorisation de geoloc ne sont pas les même que sur iOS10 et +
