# Prisma Cheat Sheet

## Installation

```bash
npm install @prisma/cli --save-dev
npm install @prisma/client
```

## Initializing Prisma

```bash
npx prisma init
```
This creates a new prisma directory with a schema file.

## Prisma Schema

Located in prisma/schema.prisma.
Defines your database models and relationships.

### Migrations

#### Creating migrations

```bash
npx prisma migrate dev --name init
```

Creates new migration files based on schema changes.
Applies migrations to the development database.

#### Applying Migrations
```bash
npx prisma migrate deploy
```
Applies pending migrations in production.

### Seeding the Database
Add a seed script in prisma/seed.js or prisma/seed.ts.
#### Running the Seed Script
```bash
npx prisma db seed
```

#### Prisma Client

Generating Prisma Client
```bash
npx prisma generate
```
Generates Prisma Client based on your schema.

#### Using Prisma Client
```javascript
const { PrismaClient } = require('@prisma/client')
const prisma = new PrismaClient()

// Example: Fetching all users
async function main() {
  const allUsers = await prisma.user.findMany()
  console.log(allUsers)
}

main()
  .catch(e => {
    throw e
  })
  .finally(async () => {
    await prisma.$disconnect()
  })
```

### Basic CRUD Operations

#### Create
```javascript
const newUser = await prisma.user.create({
  data: {
    name: 'Alice',
    email: 'alice@example.com',
  },
})
```

#### Read
```javascript
const users = await prisma.user.findMany()
const user = await prisma.user.findUnique({ where: { id: 1 } })
```

#### Update
```javascript
const updatedUser = await prisma.user.update({
  where: { id: 1 },
  data: { email: 'alice@prisma.io' },
})
```

#### Delete
```javascript
const deletedUser = await prisma.user.delete({ where: { id: 1 } })
```
### Filtering, Sorting, and Pagination
#### Filtering
```javascript
const filteredUsers = await prisma.user.findMany({
  where: { name: 'Alice' },
})
```
#### Sorting
```javascript
const sortedUsers = await prisma.user.findMany({
  orderBy: { name: 'asc' },
})
```
#### Pagination
```javascript
const paginatedUsers = await prisma.user.findMany({
  skip: 10,
  take: 5,
})
```
## Advanced Features
Relations, transactions, raw queries, etc., are also supported.
Refer to the Prisma Documentation for more detailed information.

