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

## todo:
 - add postgresql dialect
 - add mssql dialect