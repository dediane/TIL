# Troubleshooting: Prisma & PostgreSQL Permissions

## Steps and Commands Summary

### 1. Double-Check User Permissions
- Log in to PostgreSQL:
  ```bash
  psql -U postgres```

Verify Permissions for public Schema:
```sql
\c your_database_name
\dn+ public```


### 2. Verify Prisma Configuration
Check DATABASE_URL in .env File:
```sql
DATABASE_URL="postgresql://myuser:mypassword@localhost:5432/myappdb?schema=public"
```

### 3. Grant Additional Permissions
Execute in PostgreSQL:
```sql
GRANT ALL PRIVILEGES ON SCHEMA public TO myuser;
ALTER DEFAULT PRIVILEGES IN SCHEMA public GRANT ALL PRIVILEGES ON TABLES TO myuser;
ALTER DEFAULT PRIVILEGES IN SCHEMA public GRANT ALL PRIVILEGES ON SEQUENCES TO myuser;```

### 4. Check Role Inheritance
Check Role Memberships:

\du myuser

### 5. Refresh Database Connection
Restart Application Server (if applicable)

### 6. Other Potential Issues
Schema Ownership:
```
ALTER SCHEMA public OWNER TO myuser;
```
