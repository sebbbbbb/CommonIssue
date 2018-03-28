### Tests unitaires

### Configuration
- Utiliser l'annotation @testable import pour ne pas avoir à mettre toute les classes publiques
- Ne **surtout pas** inclure les fichiers sources de l'app principale dans la target de test
- Vérifier que le nom de module de la target de test est différent de celui de l'app principale
- Ne **surtout pas** inclure deux fois les pods, utiliser *inherit! :search_paths* pour la target de tests sinon les symboles
seront dupliqués ce qui créera des undefined behavior (cf ZZ)
