# CommonIssue

### Navigation Controller
#### Changer la couleur de la status bar
* Regarder dans le **.plist** ou autre part que la propriété _UIStatusBarStyleLightContent_ est pas utilisé
* http://stackoverflow.com/questions/33103831/change-status-bar-text-color-to-light-in-ios-9-with-objective-c

#### Mettre une image sur la top bar
* Setter l'image dans le view controller qui utilise la navigation bar, et non pas la navigation elle même
``` Swift
self.navigationItem.titleView = UIImageView(...)
```
