# logger

simple leveled logger.

## usage:

```
logger := logger.New(logger.Options{Writer: os.Stdout, Database: db})
logger.Debug("Hello %s", "mom")
```

this will create an entry on the `logs` table.  