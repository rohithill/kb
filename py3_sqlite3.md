

## sqlite3 in python3
### To list tables and their metadata:

`cursor.execute("SELECT name FROM sqlite_master WHERE type='table';")`

https://stackoverflow.com/questions/305378/list-of-tables-db-schema-dump-etc-using-the-python-sqlite3-api

### To open a database in read only mode:

`db = sqlite3.connect('file:path/to/database?mode=ro', uri=True)`

https://docs.python.org/3/library/sqlite3.html#sqlite3.connect

### To update a column which may violate UNIQUE constraint:

Make the column nullable and use null instead of any value.

https://stackoverflow.com/questions/43274214/how-to-temporarily-break-column-uniqueness-in-sqlite