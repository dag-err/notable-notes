---
tags: [database]
title: psql
created: '2019-07-30T06:19:49.220Z'
modified: '2019-08-18T14:21:22.536Z'
---

# psql

```sql
psql DBNAME USERNAME

\?                # help for psql commands
\h                # help for SQL commands

\conninfo         # information about the current database connection

\list             # list all databases

\connect DATABASE # switch to database

\dt               # list all tables in the current database

\z                # list all of the tables, views, and sequences in the database

\q                # exit the psql program

\d+ table         # describe
DESCRIBE TABLE

\x auto         # output format
```
[PSQL-META-COMMANDS](https://www.postgresql.org/docs/current/static/app-psql.html#APP-PSQL-META-COMMANDS)
[alternate-output-format-for-psql](https://stackoverflow.com/questions/9604723/alternate-output-format-for-psql)

### init
```sql
CREATE DATABASE bookstore;
CREATE USER bookstore_user WITH ENCRYPTED PASSWORD 'secret';
GRANT ALL PRIVILEGES ON DATABASE bookstore TO bookstore_user;
GRANT ALL PRIVILEGES ON TABLE books TO bookstore_user;

psql "dbname=bookstore host=localhost user=bookstore_user password=secret port=5432"

sslmode=require
```

### dryrun
```sql
BEGIN;
UPDATE users SET admin = 't' WHERE id = '38';
select admin from users where id = '38';
ROLLBACK;
```
