# Challenge Chapter 7 Submission

Binar Academy Bootcamp Chapter 7 Submission by Paull Ronaldo

This is CRUD app using NodeJS, ExpressJS, Sequelize, PostgreSQL, and EJS. There are 4 tables on the database after installation: `user_game`, `rooms`, `logs`, `SequelizeMeta` (store for postgres setting).

Routes:

```
/login
/register
```

API:

```
GET - /
POST - /login
POST - /register
GET - /whoami
GET - /api/players
POST - /api/create-room
GET - /api/rooms
POST - /api/fight/:room
POST - /api/play/:room
POST - /api/result/:room
```

Info

- memory-cache helps to store temporary data on server
- accessControl module is middleware for role-based access
- `/utils/restrict.js` is passport jwt strategy implementation
- `/db/migrations` contains sequelize migration files
- `db/seeders` contains sequelize seeders
- `db/models` contains sequelize models for tables inside database
- `config.js` setting for sequelize
- `utils/logger.js` logging handler middleware
- `utils/middleware.js` unknown endpoints and error handler middleware
- `.sequelizerc` setting for sequelize initialization

## Installation

**Step 1. Clone the code into a fresh folder.**

```
$ git clone https://github.com/paullronaldo/binar-chapter7-paull.git
$ cd binar-chapter7-paull
```

**Step 2. Install Dependencies.**

Next, we need to install the project dependencies, which are listed in `package.json`.

```
$ npm install
```
or

```
$ yarn
```

**Step 3: Update environment variables.**

Create a new file named `.env`. Update the new file with your database credentials. It should look similar to this:

```
# .env file
USER="[INSERT_DATABASE_USER]"
PASS="[INSERT_DATABASE_PASSWORD]"
HOST="[INSERT_DATABASE_HOST]"
DB_DEV="[INSERT_DATABASE_DEVELOPMENT]"
DB_TEST="[INSERT_DATABASE_TEST]"
USER_PROD="[INSERT_USER_PRODUCTION]"
PASS_PROD="[INSERT_PASSWORD_PRODUCTION]"
HOST_PROD="[INSERT_HOST_PRODUCTION]"
DB_PROD="[INSERT_DATABASE_PRODUCTION]"
PORT=8080
```

**Step 4. Run sequelize**

Run sequelize to migrate and create table with seeders.

```
$ npx sequelize db:migrate
$ npx sequelize db:seed:all
```

**Step 5. Run the Server**
Now we're ready to start our server which is as simple as:

```
$ npm run dev
```

or

```
$ yarn run dev
```

Open http://localhost:8080 or http://localhost:3000 (default port if there is no PORT on .env file) to view it in your browser.

The app will automatically reload if you make changes to the code.
You will see the build errors and warnings in the console.
