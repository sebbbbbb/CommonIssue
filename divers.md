# Charles

### Ça ne marche pas sur mon simu 

Installer le certificat root sur le simu : Help > SSL Proxying > Install Charles Root Certificate in iOS Simulators

### Autres

Le certif charles expire tous les 1 ans, il peut être regeneré en faisant *reset certficat*, un peu fourbe car dans le cas ou il est expiré il 
ne sera pas ajouter auto au keychain.
Quand on un certificat expiré on a des messages du type: Le certificat xyz n'est pas une autorité valide.


# Git

### Je peux plus push (Permission denied (publickey)

Faire un gros reset sur les clés ssh et tout regenerer

# AppStore

### Je n'arrive pas à ouvrir une app sur le store 

Tester avec un vrai device et non pas un simu

### Regarder les entitlements d'un IPA récupérer via Appstore
Utiliser la commande :
```shell
codesign -d --entitlements - /Applications/Whatever.app/
```

### Extraire un IPA
https://emm.how/t/downloading-ipa-file-from-app-store-onto-a-mac/525
