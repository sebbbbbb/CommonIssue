
#### Faire des ombres
Utiliser (dans le .xib ou dans le code) :

* layer.shadowRadius
* layer.shadowOpacity
* layer.shadowOffset
* layer.cornerRadius

⚠️ Le radius coupe une partie de la vue, si une sous-vue à est collé sur cette vue il faut lui appliquer une marge ou lui appliqué l'arrondis aussi sinon l'arrondis de la vue parente sera recouvert.

#### Augmenter la taille d'une image de bouton

Changer les propriétés control alignement du bouton.

#### Gradient

Bien penser à mettre la bounds et non la frame pour avoir le bon repère.

‘‘‘
   let gradient = CAGradientLayer()
        gradient.colors = [
            UIColor(red: 120/255, green: 36/255, blue: 130/255, alpha: 1.0).cgColor,
            UIColor(red: 90/255, green: 180/255, blue: 210/255, alpha: 1.0).cgColor
        ]
        
        gradient.startPoint = CGPoint.zero
        gradient.endPoint = CGPoint(x: 0, y: 1)
        gradient.frame = self.viewGradient.bounds
        self.viewGradient.layer.insertSublayer(gradient, at: 0)
‘‘‘
