# Livraison

## Bug de m***e

Erreur lors de l'export de l'archive :


"Error Domain=IDEProvisioningErrorDomain Code=10 \"MZAppearance.framework does not support provisioning profiles.\" UserInfo={NSLocalizedDescription=MZAppearance.framework does not support provisioning profiles., NSLocalizedRecoverySuggestion=MZAppearance.framework does not support provisioning profiles, but provisioning profile Zouzous inhouse provisionning has been manually specified. Remove this item from the \"provisioningProfiles\" dictionary in your Export Options property list.}",

Solution :
  * Voir du cote de cocoapods
  * Regarder si un *xconfig* n'override pas les pods
