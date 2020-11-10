# Appstore

## My app is reject and Apple doesn't give me much warning

### Kids App
* Check your app doesn't link *AdSupport*
* Check if 3rd dependencies don't link *AdSupport*
* Use *otool* CLI to inspect apps framework to know if framework is linked or not
* ⚠️ #ifCanImport macro doesn't perform check at app level but at plateform level so if a ifCan... is performed on AdSupport the framework will be link
against your project even if it's not linked in your project setup
