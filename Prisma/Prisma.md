#Prisma Cheat Sheet

##Installation

```bash
npm install @prisma/cli --save-dev
npm install @prisma/client
```

##Initializing Prisma

```bash
npx prisma init
```
This creates a new prisma directory with a schema file.

##Prisma Schema

Located in prisma/schema.prisma.
Defines your database models and relationships.

###Migrations

####Creating migrations

```bash
npx prisma migrate dev --name init
```
