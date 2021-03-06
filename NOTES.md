Relational

- well defined structure for the data
- relationships that go more than 2 level deep
- lots fo writes

Non Relational

- shallow relationships
- lots fo reads, less writes
- unstructured data

There are different types of NoSQL (Not Only SQL)

- document
- graph
- key-value
- object
- more...

{ } > [ ]

- categories
  - products
    - orders
      - order lines

Remember to save (Write Changes) your DB file.

Connecting from Node.

- raw driver
- query builder <== we'll use one of these
- full blown ORM (Object Relational Mapper)

Steps

- npm init -y
- yarn add express knex sqlite3
- yarn add nodemon -D
- add "server": "nodemon" to package.json
- npx knex init > generated the knexfile.js
  - or install knex globally `yarn global add knex` or `npm i -g knex` and just do `knex init`
- update knexfile to point to right file
- add `useNullAsDefault: true` to the development key inside knexfile.js

## Migrations

- install knex globally `yarn global add knex` or `npm i -g knex`
- knex to see available options
- knex migrate:make migration_name to create a new migration.
- knex migrate:latest to run all new migrations
- knex migrate:rollback to undo the last batch of migrations

## Seeds
- Use number to order seeds, e.g.: knex seed:make 001-cohorts
- Change del() to truncate()

A Foreign Key Constraint is a column that points to or references the Primary Key on another table.