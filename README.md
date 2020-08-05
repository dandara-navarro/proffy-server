# proffy-server

The creation of this server was with the command

```sh
npm init -y

or

yarn init -y
```

#### To install Typescript
```sh
npm install typescrypt

or

yarn add typescript
```

#### To create the config file for typescript
```sh
npx tsc --init

or

yarn tsc --init
```

This command above is going to create the file tsconfig.json. And The only thing I will change on it is

"target": "es5" => "target": "es2017"

Because Node.js compiles until this version of the ECMA Script.

#### To install the library **ts-node-dev**
This lib is used to reload our application automatically when we have any change on our server.

```sh
npm install ts-node-dev -D

or

yarn add ts-node-dev -D 
```

#### To run our code easily
We are going to create a session in our *package.json* file called scripts with these configurations

```json
"scripts": {
    "start": "ts-node-dev src/server.ts"
}
```

With advanced configurations and "ts-node-dev" abbreviated to "tsnd"
```json
"tsnd --transpile-only --ignore-watch node_modules --respond src/server.ts"
```

#### Installing Express
We are using TypeScript and some dependencies we are installing for our project are not developed in TypeScript, so we must also install @types/express, for example.

```sh
npm install express
npm install @types/express -D
```
#### Installing Knex and SQlite 3
The Knex allows us to write the SQL queries in JavaScript. See the example below
```sql
SELECT * FROM users
```
will be
```javascript
knex('users').select('*')
```


### HTTP

#### Requisition Params
**Request body** comes the date for the creation or update of a registry

**Route Params** identify a source in our route

**Query Params** used mainly with pagination, filters, ordenations

### Proffy Functionalities Routes

#### Connections
- Route to list the total of done connections;
- Route to create a new connection;

#### Classes
- Route to create a class;
- Route do list classes;
    - Filter by course, weekday, and time; 
