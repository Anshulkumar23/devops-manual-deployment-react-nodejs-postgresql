# Prisma Migrations

## Overview

Prisma is used as the ORM to connect the Node.js backend with PostgreSQL.

Database configuration is defined using:

```text
DATABASE_URL
```

The Prisma schema is located at:

```text
server/prisma/schema.prisma
```

## Generate Prisma Client

```bash
npx prisma generate
```

## Check Migration Status

```bash
npx prisma migrate status
```

## Apply Migrations

```bash
npx prisma migrate deploy
```

This applies the existing migration files to the PostgreSQL database.

Migration files are stored in:

```text
server/prisma/migrations/
```

## Verify Database

Connect to PostgreSQL and check the tables:

```sql
\dt
```

Prisma creates and maintains the following migration tracking table:

```text
_prisma_migrations
```

The application data is stored in the PostgreSQL tables created through Prisma migrations.

## Migration Flow

```text
schema.prisma
      ↓
Migration Files
      ↓
prisma migrate deploy
      ↓
PostgreSQL Database
      ↓
Tables Created
```
