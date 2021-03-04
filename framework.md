# Framework

## Chose à checker
* Penser à mettre les méthodes/classes en **open/publique** pour pouvoir les utiliser dans le composant qui utilise le framework
* Ne pas utiliser le *main* bundle sinon ça ne marchera pas sur les autres executables

## Crash dyld: Library not loaded: @rpath/AdManager.framework/AdManager
* POC AppClip, check if cocoapods is on last version when using a new target

## Error like : Umbrella header 'Tracking.h' not found
* Check if .h file of framework is under Public domain

## Erorr on .plist
* If you moved project structure make sure to reflect change on .pbxproj under Packaging > Info.plist File
