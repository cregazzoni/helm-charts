## Before to apply the chart

Configure external PostgreSQL with proper user and database: 
```
psql -d template1 -c "CREATE USER gitlab CREATEDB;"
psql -d template1 -c "CREATE EXTENSION IF NOT EXISTS pg_trgm;"
psql -d template1 -c "CREATE EXTENSION IF NOT EXISTS btree_gist;"
psql -d template1 -c "CREATE EXTENSION IF NOT EXISTS plpgsql;"
psql -d template1 -c "CREATE DATABASE gitlab OWNER gitlab;"
psql -d template1 -c "ALTER USER user_name WITH PASSWORD 'new_password';"
```