# 200 - Test GraphQL and REST queries

Based on "Test GraphQL queries" at https://hasura.io/docs/latest/graphql/core/getting-started/docker-simple.html#try-out-a-query

## 100 - Test GraphQL queries

After successful completion of the pevious steps, let us try out a query.

Head to the **API** tab in the Console at https://hasura-7exz.onrender.com/console/api/api-explorer and try running the following query:

![Render_Hasura_GraphQL-009](https://user-images.githubusercontent.com/1499433/229496040-cb6e4400-2363-4916-aa69-b2d5dde01269.png)

You'll see that you get all the inserted data!

Ultimately we can request the following query that will give us the required response:

![Render_Hasura_GraphQL-010](https://user-images.githubusercontent.com/1499433/229520177-86737598-3a90-4a6b-a7e7-06ba53bc3a88.png)

Now we can use this query to draw our "Cereal" as a molecule (see https://github.com/vanHeemstraSystems/chemplexity-servings):

== screenshot should go here ==

Hooray!

## 200 - Test REST queries

We can create an Endpoint from a GraphQL query to a REST request (e.g. GET, POST, PUT, PATCH, or DELETE) as follows.

In Hasura create an Endpoint for our cereal query as depicted below (we call it ```cereal```:



Then click "Create Endpoint"

Now from a browser or from within code open this URL: https://hasura-7exz.onrender.com/api/rest/cereal

It will return the same result as if requested as a GraphQL request (which is always a POST method), but now using the REST protocol (here: using the GET method instead).

```

```
Response from REST request
