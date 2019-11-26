# Livraison

## Bug de m***e

Erreur lors de l'export de l'archive :


"Error Domain=IDEProvisioningErrorDomain Code=10 \"MZAppearance.framework does not support provisioning profiles.\" UserInfo={NSLocalizedDescription=MZAppearance.framework does not support provisioning profiles., NSLocalizedRecoverySuggestion=MZAppearance.framework does not support provisioning profiles, but provisioning profile Zouzous inhouse provisionning has been manually specified. Remove this item from the \"provisioningProfiles\" dictionary in your Export Options property list.}",

Solution :
  * Voir du cote de cocoapods
  * Regarder si un *xconfig* n'override pas les pods


"Error Domain=IDEFoundationErrorDomain Code=1 "exportOptionsPlist error for key 'method': expected one of {}, but found enterprise" UserInfo={NSLocalizedDescription=exportOptionsPlist error for key 'method': expected one of {}, but found enterprise}"

Solution :
  * Checker la version de cocoapod

## Application loader qui râle

*ERROR ITMS-90596: “Invalid Bundle. The asset catalog at Payload”*

Solution :
 * Regarder si on utilise bien la dernière version d'Application Loader, elle diffère entre les versions d'Xcode

*ERROR ITMS-90205: "Invalid Bundle. contains disallowed nested bundles*

Solution : (Soucis rencontré sur Ludo)
  * Faire une archive via Xcode et checker son contenu
  * S'assurer que l'extension de l'app ( de l'archive) ne contient pas de framework, c'est l'app container qui doit la contenir

## TestFlight

### Redeem code paumé
* Si user interne, le supprimer du groupe et le rajouter pour pouvoir ressoumettre le code par mail ...


### App tej a cause de Missing Purpose String in Info.plist
* Avoir le nom du framework qui nécessite cette autorisation
* Utiliser la fonction suivante Missing Purpose String in Info.plist (dans le *.app) 
```shell
find *.framework ! -name '*CodeResources*' -type f ! -name "*.*" -exec nm -o -- {} + | grep <#MonFrameWork#>
```
