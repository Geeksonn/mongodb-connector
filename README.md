# mongodb-connector

A simple, yet useful, mongoDB connector.

[![npm](https://img.shields.io/npm/v/@geekson/mongodb-connector)](https://www.npmjs.com/package/@geekson/mongodb-connector)

## Install

```bash
npm install @geekson/mongodb-connector
```

## Usage

Ensure to have a `.env` file with the following properties: 
`MONGODB_URI`: the URI to connect to
`MONGODB_DB`: the database to connect to

```js
import { connectToDatabase } from '@geekson/mongodb-connector';

async getAllPosts() {
    const { db } = await connectToDatabase();

    return await db.collection('Post').find().toArray();
}
```

## Changelog

**2021-12-04**  
Updated version of underlying library (mongodb).  
Please refer to [this page](https://github.com/mongodb/node-mongodb-native/blob/HEAD/docs/CHANGES_4.0.0.md) for instructions (many changes).