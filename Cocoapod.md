# Cocoapod

### Erreurs

## LoadError - cannot load such file -- xyz
Si on spécifie juste le fichier le load ira le cherche dans le répertoire courant &

## Mes pods n'apparaissent pas !
* Bien regarder si le Pod est activé sur la bonne target
* Faire un clean des derived data

## Auto-Linking framework not found
* Regarder si la target est bien inclue dans le podfile (core ...)

### Pod custom
* Si une lib n'est pas compatible Swift, essayer de pécho un framework et de l'intégrer tel quel (pas ouf ...)
* Quand on intègre une lib externe il faut utiliser l'instruction *vendored_frameworks*
* Si on a l'erreur : target has transitive dependencies that include static frameworks, Utiliser le workaround suivant :

pre_install do |installer|
	# workaround for https://github.com/CocoaPods/CocoaPods/issues/3289
	Pod::Installer::Xcode::TargetValidator.send(:define_method, :verify_no_static_framework_transitive_dependencies) {}
end

