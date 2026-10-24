## THIS IS A REPO FOR ALL THE POSTGRESS LEARNINGS ILL MAKE
the current docker file is for postgres editing an administration

## CLI
### CONNECTING

youre gonna need psql
`apt install postgresql`

example vars
```bash
DP_PROTOCOL="postgresql"
DB_USER_NAME="admin"
DB_PASSWORD="admin"
DB_HOSTNAME="pipi-pupu-pipipupu-pooler.ap-southeast-1.aws.pipi.pupu"
DB_NAME="test_db"
DB_PORT="5432"
```
```bash
psql "$DP_PROTOCOL://$USERNAME:$DB_PASSWORD@$HOSTNAME:$DB_PORT/$DB_NAME"
psql "$DP_PROTOCOL://$USERNAME:$DB_PASSWORD@$HOSTNAME:$DB_PORT/$DB_NAME?$OPTIONAL_PARAMETERS"
```
###

|command|description|
|-|-|
|`\l`| list all databases in collection |
|`\dt *.*`| list all databases in every collection |
|`CREATE DATABASE $DATABASE_NAME;`| creates a database |
|`\c $DATABASE_NAME;`| connects to a database |
|`\d $TABLE_NAME`| gives details of a table |
|`\d+ $TABLE_NAME`| more verbose details |
```
CREATE TABLE greetings (
    id SERIAL PRIMARY KEY,
    message VARCHAR(255)
);
```
```
INSERT INTO greetings (message)
VALUES ('Hello, World!');

INSERT INTO greetings (message)
VALUES (DEFAULT);
```
```
SELECT message FROM greetings;
SELECT id, message FROM greetings;
```