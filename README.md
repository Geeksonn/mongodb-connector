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
import connectToDatabase from '@geekson/mongodb-connector';

async getAllPosts() {
    const { db } = await connectToDatabase();

    return await db.collection('Post').find().toArray();
}
```
