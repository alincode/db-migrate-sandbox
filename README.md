# node db migrate sandbox

**init project**

```
npm init -y
npm i db-migrate -S
npm i db-migrate-mysql -S
```

**setting up db config**

```
touch database.json
vi database.json
```

**create empty db**

`mysql> create schema db_migrate_test default character set utf8mb4;`


Another way

```
db-migrate db:create node_db_migrate
db-migrate db:create node_db_migrate_test
```

Sometime this way is not reliable. I dont recommend it.


**create migrate script**

`db-migrate create add-user`


**execute migrate**

`db-migrate up`

**rollback migrate**

`db-migrate down`

### reference

* [node-db-migrate repository](https://github.com/db-migrate/node-db-migrate)
* [node-db-migrate doc](https://db-migrate.readthedocs.io/en/latest/)
