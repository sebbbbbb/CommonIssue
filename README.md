# CommonIssue

## UIKit
### Navigation Controller
#### Changer la couleur de la status bar
* Regarder dans le **.plist** ou autre part que la propriété _UIStatusBarStyleLightContent_ est pas utilisé
* http://stackoverflow.com/questions/33103831/change-status-bar-text-color-to-light-in-ios-9-with-objective-c

#### Mettre une image sur la top bar
* Setter l'image dans le view controller qui utilise la navigation bar, et non pas la navigation elle même
``` Swift
self.navigationItem.titleView = UIImageView(...)
```

#### Une cellule est vided alors que j'ai tout bien fait / Bug avec une collection view
* Bien regarder si on a pas crée une simple UIView a la place du composant qui va bien (cf: Gunjin)

### UITableView

#### Cellules superposées
* Ne surtout pas appeler dequeuReusableCell deux fois, sinon la cellule sera instancié même si le résultat n'est pas utilisé.

### Rotation
#### Layout tout cassé quand je fais une rotation alors que l'écran est pas visible (Ludo ...)
* Simplifier au maximum le layout pour que le moteur de rendu puisse se dépatouiller tout seul (ex: ne pas avoir des élement lourd imbriqué, type collectionView dans scrollView)
