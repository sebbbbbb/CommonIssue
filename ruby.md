# Ruby

## Ruby on rails

### Reset la BDD
```shell
rake db:reset
```
### Supprimer la BDD
```shell
rake db:drop
```

### Issues

#### ActiveRecord::StatementInvalid (SQLite3::ReadOnlyException: attempt to write a readonly database
* Regarder si les droits d'executions sont bien settés sur le dossier db
* Peut arriver suite à un reset de la db 
