# Migrate-Airflow-Meta-Database-to-PostgreSQL

- Need the airflow db and airflow db user
```sql
CREATE DATABASE airflow_db;
CREATE USER airflow_user WITH PASSWORD 'your_secure_password';
ALTER ROLE airflow_user SET search_path TO public;
GRANT ALL PRIVILEGES ON DATABASE airflow_db TO airflow_user;
```

```sql
GRANT ALL PRIVILEGES ON SCHEMA public TO anower_airflow_handle;
GRANT CREATE, USAGE ON SCHEMA public TO anower_airflow_handle;
ALTER DEFAULT PRIVILEGES IN SCHEMA public GRANT ALL ON TABLES TO anower_airflow_handle;
ALTER DEFAULT PRIVILEGES IN SCHEMA public GRANT ALL ON SEQUENCES TO anower_airflow_handle;
```


