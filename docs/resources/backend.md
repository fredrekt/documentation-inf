---
sidebar_position: 1
---

# Backend

Backend is built with StrapiJS **Node.js Headless CMS**.

StrapiJS has Model & Controller so feel free to browse over the project src. 

```
/api/${collection}/config is where to define your endpoints
/api/${collection}/controller is where to define your functions
/api/${collection}/models define your collection model (you can either just alter in Strapi Dashboard)

```

### Datatables

We're using MongoDB Aggregation for this see [reference here](https://docs.mongodb.com/manual/aggregation/). Below is a snippet for said aggregation.

```bash
await strapi.query('<collection-name>').model.aggregate([
    {
        $match: {
            userId: { $exists: true },
            createdAt: {
                $gte: start_date,
                $lt: end_date
            }
        }
    },
    {
        $sort: { 'createdAt': -1 }
    },
    {
        $lookup: {
            from: '<collection-name-join>',
            localField: 'userId',
            foreignField: 'userId',
            as: '<assign collection new name>'
        }
    }
])
```

### Datatables: Betting History

We're using MongoDB Aggregation for this see [reference here](https://docs.mongodb.com/manual/aggregation/). Below is a snippet for said aggregation. Betting history is quite complicated, for one there are two providers with different models. Two is they are combined by roundId or referenceId to produce 1 record. 

<strong>Game Provider</strong>

1. Pragmatic Play: 3 records 
2. Evolution: 2 Records

```bash
await strapi.query('<pragmatic betting hisory || evolution betting history>').model.aggregate([
    {
        $match: {
            userId: { $exists: true },
            createdAt: {
                $gte: start_date,
                $lt: end_date
            }
        }
    },
    {
        $sort: { 'createdAt': -1 }
    },
    {
        $lookup: {
            from: '<collection-name-join>',
            localField: 'userId',
            foreignField: 'userId',
            as: '<assign collection new name>'
        }
    }
])
```

<strong>note:</strong> If confused refer to mongodb documentation and cross ref it with our code.
