# logger

simple leveled logger.

## usage:

First import with the desired dialect:  
```
import "github.com/ozkar99/logger"
import _ "github.com/ozkar99/logger/dialects/sqlite"
// import _ "github.com/ozkar99/logger/dialects/mysql"
```

Then to use pass a db connection in the options struct:  
```
logger := logger.New(logger.Options{Writer: os.Stdout, Database: db})
logger.Debug("Hello %s", "mom")
```

this will create the `logs` table as well as an entry with type `Debug` on the table.  

if you only want to log to `stdout` or any other `writer` just dont pass the `db` parameter to the `Options` struct.  
```
logger := logger.New(logger.Options{Writer: os.Stdout})
```

like wise if you only want to log to the database:  
```
logger := logger.New(logger.Options{Database: db})
```

## supported levels:

- Debug
- Info
- Warn
- Error
- Fatal

## todo:
 - add postgresql dialect
 - add mssql dialect
