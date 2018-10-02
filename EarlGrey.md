# EarlGrey

### Test qui mouline dans le vide
* Sur des écrans avec du traitement continue (Player, ...) la synchro EarlGrey peut bloquer le bon déroulement des tests
Solutions/HACK:
```swift
  GREYConfiguration.sharedInstance().setValue(false, forConfigKey: kGREYConfigKeySynchronizationEnabled)
  GREYUIThreadExecutor.sharedInstance().drain(forTime: 2.0)
  // Asserts Earlgrey ...
  GREYConfiguration.sharedInstance().setValue(true, forConfigKey: kGREYConfigKeySynchronizationEnabled)
```
