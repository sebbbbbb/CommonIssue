# Charles

### Ça ne marche pas sur mon simu 

Installer le certificat root sur le simu : Help > SSL Proxying > Install Charles Root Certificate in iOS Simulators

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
