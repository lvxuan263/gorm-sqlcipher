# GORM Sqlite Driver

![CI](https://github.com/go-gorm/sqlite/workflows/CI/badge.svg)

## USAGE

```go
import (
  "githun.com/lvxuan263/gorm-sqlcipher"
  "gorm.io/gorm"
)

key := url.QueryEscape("my password")
dbname := fmt.Sprintf("db", key)
dsn := fmt.Sprintf("%s?_pragma_key=x'%s'&_pragma_cipher_page_size=4096", dbname, key)
db, err := gorm.Open(sqlite.Open(dsn), &gorm.Config{})
```
