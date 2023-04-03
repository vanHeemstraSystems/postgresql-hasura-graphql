postgresql-hasura-graphql
# PostgreSQL &amp; Hasura GraphQL

Based on "Deploy Hasura GraphQL Engine" at https://render.com/docs/deploy-hasura-graphql

The [Hasura GraphQL engine](https://hasura.io/docs/latest/graphql/core/index.html) makes your data instantly accessible over a real-time GraphQL API, so you can build and ship modern apps and APIs faster. Hasura connects to your databases, REST servers, GraphQL servers, and third party APIs to provide a unified realtime GraphQL API across all your data sources.

Related to "Chemplexity Servings" at https://github.com/vanHeemstraSystems/chemplexity-servings where we try to display a chemical molecule - aka a servings - (called: "Cereals") that sources it data from our Hasura GraphQL https://hasura-7exz.onrender.com/console/api/api-explorer backed by a Postgress Database, hosted on Render.com 

**TO DO**: Try out **Nested Object Queries** in PostgreSQL as described at https://hasura.io/docs/latest/queries/postgres/nested-object-queries/ to format our JSON for cereals as follows:

```
{
  "nodes": [
    {"atom": "Mi", "size": 5, "color": "#FFFFFF"},
    {"atom": "OF", "size": 5, "color": "#FFFFFF"},
    {"atom": "MG", "size": 5, "color": "#FFFFFF"},
    {"atom": "OM", "size": 5, "color": "#FFFFFF"}
  ],
  "links": [
    {"source": 0, "target": 1,  "bond": 1},
    {"source": 1, "target": 2,  "bond": 1},
    {"source": 1, "target": 3,  "bond": 1}
  ]
}
```

# 100 - Introduction

See [README.md](./100/README.md)

# 200 - Requirements

See [README.md](./200/README.md)

# 300 - Building Our Application

See [README.md](./300/README.md)

# 400 - Conclusion

See [README.md](./400/README.md)
