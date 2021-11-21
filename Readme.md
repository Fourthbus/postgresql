# PostgreSQL

## Install PostgreSQL

Install using Homebrew

```
$ brew install postgresql
```



## Using PSQL

Also found on https://dev.to/letsbsocial1/installing-pgadmin-only-after-installing-postgresql-with-homebrew-part-2-4k44

#### Start PSQL

```bash
brew services start postgresql
```

#### Creating DB

```bash
createdb 'thelab'
```

#### Entering program

```bash
psql
```

possible error see https://stackoverflow.com/questions/13410686/postgres-could-not-connect-to-server

Quitting prgram

```sql
QUIT;
```



## Install PostGIS

```bash
$ brew install postgis
```

Import postGIS in pgsl

```sql
CREATE EXTENSION postgis;
```



## Install GUI for PSQL

#### Creating the default postgres user needed for pgAdmin

When in program, create superuser

```bash
$ createuser -s postgres
```

Set password 'postgres' for the user created

```sql
ALTER USER  postgres  WITH PASSWORD 'postgres';
```

#### Install pgAdmin GUI using Homebrew

```bash
brew install --cask pgadmin4
```

#### Add new server in pgAdmin

Host: 

```
localhost
```

Port:

```
5432
```



## Management with pgAdmin

##### Create new table (SQL command)

```sql
CREATE SCHEMA "thelaboffice";
CREATE TABLE "thelaboffice"."ga_updated"
(
    "id" INT,
    "floor_id" INT,
    "geom" geometry,
    PRIMARY KEY (id)
);

```



## Use geopandas to work with database

Install Python supports

```bash
$ pip3 install geopandas
$ pip3 install numpy
$ pip3 install matplotlib
$ pip3 install psycopg2
```

