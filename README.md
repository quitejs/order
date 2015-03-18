# order
a sql builder, database query tool for node and postgres database

# documentation
order adopt `O` as namespace as `$` in jquery and `_` in underscore
## connect
### parameters
- _object_ __config__: can contain any of the following optional properties
  - _string_ __user__:
     - default value: `process.env.USER`
     - PostgreSQL user
  - _string_ __database__:
     - default value: `process.env.USER`
     - database to use when connecting to PostgreSQL server
  - _string_ __password__:
     - default value: `null`
     - user's password for PostgreSQL server
  - _number_ __port__:
     - default value: `5432`
     - port to use when connecting to PostgreSQL server
     - will support unix domain sockets in future
     - used to initialize underlying net.Stream()
  - _string_ __host__:
     - default value: `null`
     - host address of PostgreSQL server
     - used to initialize underlying net.Stream()
  - _bool_ __ssl__:
     - default value: `false`
     - whether to try SSL/TLS to connect to server

### tcp example

```coffeescript
    O.connect(
      user: 'brianc'
      password: 'boom!'
      database: 'test'
      host: 'example.com'
      port: 5313
    )
```
## end
will end the connection

## run 
you can run sql string directly, or run a `sql object`, which contains a prepare statement and it's parametars.

## get
run to get single result

## all
run to get collection result





#warning
order is under heavy development.
