# Express

## Soucis

No 'Access-Control-Allow-Origin' header is present on the requested resource. Origin 'xxxxx' is therefore not allowed access.

Solution :
Utiliser un middleware qui injecte le header :
⚠️ L'ordre des insctructions comptes, le middleware doit petre crée avant le lancement du serveur

```javascript
// Add headers
app.use(function (req, res, next) {

    // Website you wish to allow to connect
    res.setHeader('Access-Control-Allow-Origin', 'http://localhost:8888');

    // Request methods you wish to allow
    res.setHeader('Access-Control-Allow-Methods', 'GET, POST, OPTIONS, PUT, PATCH, DELETE');

    // Request headers you wish to allow
    res.setHeader('Access-Control-Allow-Headers', 'X-Requested-With,content-type');

    // Set to true if you need the website to include cookies in the requests sent
    // to the API (e.g. in case you use sessions)
    res.setHeader('Access-Control-Allow-Credentials', true);

    // Pass to next layer of middleware
    next();
});
```
