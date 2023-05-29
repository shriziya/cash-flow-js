# Steps to follow for every typescript + nodejs project

---

### for typescaript project always install these packages as `dev`

```shell
"ts-node"
"ts-node-dev"
"typescript"
```

> so, `yarn add --dev ts-node ts-node-dev typescript`

## also, `yarn add --dev @types/node`

### always keep these scripts in `pakage.json` for typescript project

```json
"dev": "tsnd --respawn --transpile-only --exit-child src/server.ts",
"build": "tsc",
"start": "node ./dist/server.js",
"format": "pretty-quick"
```

> use above scripts as yarn .... `e.g.` `yarn format`

### always keep copy of these

```bash
.gitignore
.prettierignore
.prettierrc.json
tsconfig.json
```

### install these pacakges as `dev` for formatting

```bash
"husky"
"prettier"
"pretty-quick"
```

# Choose your framework for createing REST APIs in nodejs

- Express
  - `yarn add express`
  - `yarn add --dev @types/express`
- Fastify
  - `yarn add fastify`
  - `yarn add @fastify/cors`
  - `yarn add @fastify/env`
  - `yarn add @fastify/jwt`
  - `yarn add @fastify/redis`
  - `yarn add @fastify/static`
  - `yarn add @fastify/swagger`
  - `yarn add @fastify/swagger-ui`
  - `yarn add @mgcrea/fastify-request-logger`
  - `yarn add @mgcrea/pino-pretty-compact`

> in short, `yarn add fastify @fastify/cors @fastify/env @fastify/jwt @fastify/redis @fastify/static @fastify/swagger @fastify/swagger-ui @mgcrea/fastify-request-logger @mgcrea/pino-pretty-compact`

### Install `zod` and `fastify-zod` for generating and managing fastify schemas with auto types generation for typescript

> `yarn add zod fastify-zod`

### For dastabase - `MySQL` using Prisma ORM

`yarn add --dev prisma` and `yarn add @prisma/client`

Step-1: `yarn prisma init`
Step-2: in `.env` file set `DATABASE_URL="mysql://root:password@localhost:3306/dbname"` (set your password, username, host, port and dbname)

Step-3: set `mysql` in `prisma\schema.prisma` for `provider`
Step-4: `yarn prisma db pull`
Step-5: `yarn prisma db generate`
Step-6: use `@prisma/client`

```javascript
import { PrismaClient } from '@prisma/client';
const prisma = new PrismaClient();
```

Step-7: Install Prisma extension from VSCode

> Database setup is done!

- Vercel test
