## Node + Stripe

[![Build Status](https://travis-ci.org/mjhea0/node-stripe-charge.svg?branch=master)](https://travis-ci.org/mjhea0/node-stripe-charge)
[![Coverage Status](https://coveralls.io/repos/github/mjhea0/node-stripe-charge/badge.svg?branch=master)](https://coveralls.io/github/mjhea0/node-stripe-charge?branch=master)

This is a template for you to use on your own projects for processing one-time Stripe charges. Follow the directions below to get started.

![main](https://raw.github.com/mjhea0/node-stripe-charge/master/images/final.gif)

> Looking for a simple example? [Node Stripe Example](https://github.com/mjhea0/node-stripe-example)

The back-end API includes:

1. User auth
1. Stripe integration
1. Testing via Mocha and Chai as well as Istanbul for code coverage

## Quick Start

1. Fork/Clone
1. Install dependencies - `npm install`
1. Rename the *.env_sample* file to *.env* and update
1. Create two local Postgres databases - `node_stripe_charge` and `node_stripe_charge_test`
1. Migrate - `knex migrate:latest --env development`
1. Seed - `knex seed:run --env development`
1. Run the development server - `gulp`
1. Server should be listening on [http://localhost:3000](http://localhost:3000)

## Development Workflow

1. Create feature branch
1. Develop/test locally
1. Create PR, which triggers Travis CI
1. After tests pass, merge the PR
1. Tests run again on Travis CI

## Tests

Without code coverage:

```sh
$ npm test
```

With code coverage:

```sh
$ npm run coverage
```

## Changelog

1. 04/15/2018 - updated dependencies, added bootstrap 4, increased test coverage
1. 11/14/2016 - refactored all code, updated to es6, moved to postgres from mongo, added tests
1. 02/09/2016 - refactored passport, tests, error handlers, client-side javascript (view [commit](https://github.com/mjhea0/node-stripe-charge/commit/f32c6eb731dbf14b194ac07795671931100139b4))
1. 04/23/2015 - major refactor
1. 03/11/2015 - updated to Express 4.x

## JSON API Documentation

Admin required for all routes!

### Users

- GET `/api/v1/users` - get all users
- GET `/api/v1/users/:id` - get user
- POST `/api/v1/users` - create user
- PUT `/api/v1/users/:id` - update user
- DELETE `/api/v1/users/:id` - delete user

### Products

- GET `/products` - get all products
- GET `/products/:id` - get products
- POST `/products` - create products
- PUT `/products/:id` - update products
- DELETE `/products/:id` - delete products

## Screenshots

### Main Page

![main](https://raw.githubusercontent.com/mjhea0/node-stripe-charge/master/images/main.png)

### Charge Page

![charge](https://raw.githubusercontent.com/mjhea0/node-stripe-charge/master/images/charge.png)

### Admin Page

![admin](https://raw.githubusercontent.com/mjhea0/node-stripe-charge/master/images/admin.png)
