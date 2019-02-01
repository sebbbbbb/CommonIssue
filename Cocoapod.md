# Cocoapod

### Erreurs

## LoadError - cannot load such file -- xyz
Si on spécifie juste le fichier le load ira le cherche dans le répertoire courant &

## Mes pods n'apparaissent pas !
* Bien regarder si le Pod est activé sur la bonne target
* Faire un clean des derived data

## Auto-Linking framework not found
* Regarder si la target est bien inclue dans le podfile (core ...)

## Gros crash lors d'un pod install
* Si cela fait suite à un merge foireux regarder la tronche du .pxproj si il est corrompu le pod install peut échouer à cause de ça

### Pod custom
* Si une lib n'est pas compatible Swift, essayer de pécho un framework et de l'intégrer tel quel (pas ouf ...)
* Quand on intègre une lib externe il faut utiliser l'instruction *vendored_frameworks*
* Si on a l'erreur : target has transitive dependencies that include static frameworks, Utiliser le workaround suivant :

pre_install do |installer|
	# workaround for https://github.com/CocoaPods/CocoaPods/issues/3289
	Pod::Installer::Xcode::TargetValidator.send(:define_method, :verify_no_static_framework_transitive_dependencies) {}
end


### Erreur genre “non-modular header inside framework module” sur un Pod objc
* Inclure son umbrella header dans le bridging header


### Specs satisfying the `CocoaLumberjack (~> 2.0)` dependency were found, but they required a higher minimum deployment target.
* Si des pods utilisent ma même lib mais avec des versions différentes cela peut conduire à ce genre de bug un peu chelou ...

### Erreur du type 
[!] The following Swift pods cannot yet be integrated as static libraries:

The Swift pod `JeunesseChromecast` depends upon `Protobuf`, which do not define modules. To opt into those targets generating module maps (which is necessary to import them from Swift when building as static libraries), you may set `use_modular_headers!` globally in your Podfile, or specify `:modular_headers => true` for particular dependencies.

Solution :
* Utiliser l'instruction *use_modular_headers!* si `:modular_headers => true` ne marche pas
