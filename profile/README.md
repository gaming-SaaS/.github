# Description

## Introduction

I analyzed the system and put some time to understand how the requested ecosystem must be. The communication, safety, speed, and scalability.

### Tools:
- NestJs - Node + TypeScript + Fastify
- REST API - Communicate from outside of ecosystem
- GRPC - Faster communication for internal communications
- Graph QL - Get data from database
- PostgreSQL
- TypeORM - Nest uses to communicate with database
- Jest - Nest uses to create test cases
- Github
  - projects
  - issues
  - standard git-flow for branching

### Services:
1. [Managing users - Oxygen](https://github.com/gaming-SaaS/oxygen) (Because users are the important part of a LIVE system)
2. [Messaging - Rhenium](https://github.com/gaming-SaaS/rhenium) (Because this chemical element used in electrical contact materials)
3. [Wallet - Nickel](https://github.com/gaming-SaaS/nickel) (Because it is a money unit)
4. [Grouping(club) - Carbon](https://github.com/gaming-SaaS/carbon) (Because it creates very strong groups like diamonds)
5. [Readable data provider - Francium](https://github.com/gaming-SaaS/francium) (Because it likes to give the electrons)
6. [Writable data provider - Fluorine](https://github.com/gaming-SaaS/fluorine) (Because it like to receive electrons)

### nest-plus

This is a wrapper on the Nestjs server, it provides all common filters, middlewares, interceptors, guards, and... It is published on NPM, so for services, you can use it without being worried about common feature implementations.

You can find it here, *[nest-plus](https://github.com/gaming-SaaS/nest-plus)*.

### Middlewares:

### Guard:
1. Authorizer
2. Access control

### Pipe:
1. Validator
2. Extractor

### Interceptor:
1. Logging

### Filter:
1. Invalid request
2. Endpoint NotFound
3. Internal error
4. Operation failed

## Naming

Services and parts of systems need name. so I decided to choose chemical elements for services as a metaphor for elements that create the system. Also tried to choose elements which has similar usage with the server itself.


## Services

I divided the whole system into 6 services which every one of them has only one porpose and responsibility.

These services are:

1. Managing users - Oxygen
   - This service manages the users who can be any type of entity; Real, legal or fictional.
2. Messaging - Rhenium
   - This service broadcast a message or receive messages.
3. Wallet - Nickel
   - This service manages the assets belonging to an entity. Assets can be anything and they all connect to a unique code.
4. Grouping(club) - Carbon
   - This service can put several entities in an abstract group and perform activities on it.
5. Readable data provider - Francium
   - This service responsible for fetching data as fast as possible.
6. Writable data provider - Fluorine
   - This service responsible for registering data fast and sync with readable data provider.
   
![communications](https://user-images.githubusercontent.com/3008331/180456717-e12a765c-fb53-4c7a-b3bc-1021955f9d7c.png)

# JWT

JWT generated by a PEM secret key.
