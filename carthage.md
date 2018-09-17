# Carthage

## Je peux pas debug !
* Installer la dépendance en sépcifiant bien le flag **--configuration Debug**

## Stuck sur un update
* Tenter un *ssh-add*

## Ma dépendance ne se met pas à jour
* Faire un clean du cache **rm -rf ~/Library/Caches/org.carthage.CarthageKit**

## Erreur du type module compiled with swift xxx cannot be imported in swift xxx carthage
* Regarder dans le cartfile si on utilise bien une version récente de la lib, les anciennes ne sont pas forcément compatibles avec la version actuelle.
