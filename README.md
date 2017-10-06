# GraphQL Integration Example

## About the example

Mini API developed to exemplify the integration between NodeJS and GraphQL for data query.

## Running the project

Enter the api directory root and install dependecies:

```$ npm install```

After your install the dependencies, run the application with the following command:

```$ node index.js```


## Availables querys:

Listing all users:

```http://localhost:3000/user?query={users{id,name,age,knowledge{language,frameworks}}}```


Listing a user by id:

```http://localhost:3000/user?query={user(id:2){id,name,age,knowledge{language,frameworks}}}```


To select only certain fields, just specify them based on the template defined in the users.json file and define them in the query as in the example below:

```http://localhost:3000/user?query={user(id:1){id,knowledge{language,frameworks}}}```