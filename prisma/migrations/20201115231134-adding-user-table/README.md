# Migration `20201115231134-adding-user-table`

This migration has been generated by Jesús Enrique Rascón at 11/16/2020, 12:11:34 AM.
You can check out the [state of the schema](./schema.prisma) after the migration.

## Database Steps

```sql
CREATE TABLE "User" (
"id" SERIAL,
    "name" TEXT NOT NULL,
    "age" INTEGER NOT NULL,

    PRIMARY KEY ("id")
)
```

## Changes

```diff
diff --git schema.prisma schema.prisma
migration ..20201115231134-adding-user-table
--- datamodel.dml
+++ datamodel.dml
@@ -1,0 +1,19 @@
+// This is your Prisma schema file,
+// learn more about it in the docs: https://pris.ly/d/prisma-schema
+
+datasource db {
+  provider = "postgresql"
+  url = "***"
+}
+
+generator client {
+  provider = "prisma-client-js"
+}
+
+model User {
+  id Int @id @default (autoincrement())
+  name String
+  age Int
+
+
+}
```

