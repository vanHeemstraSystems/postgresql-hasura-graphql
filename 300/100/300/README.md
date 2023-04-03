# 300 - Read how Hasura GraphQL Engine works

Based on "Read how Hasura GraphQL Engine works" at https://hasura.io/docs/latest/graphql/core/how-it-works/index.html

**Recap**

What did we just do? Well, you just created a powerful, full-featured GraphQL API in less than five minutes. 🎉

We started two Docker containers - one for the Hasura GraphQL Engine and one for the Postgres database. In this example, our Postgres database also contains the Hasura Metadata; which is how Hasura records its information about the GraphQL schema, the relationships between tables, and much more. Finally, we connected our Postgres database to the Hasura GraphQL Engine, which allowed Hasura Engine to automatically create a full CRUD GraphQL API for our Postgres database which we could then easily query, mutate and subscribe to.

## 100 - Introduction

MORE ...
