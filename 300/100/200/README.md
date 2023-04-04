# 200 - Test GraphQL and REST queries

Based on "Test GraphQL queries" at https://hasura.io/docs/latest/graphql/core/getting-started/docker-simple.html#try-out-a-query

## 100 - Test GraphQL queries

After successful completion of the pevious steps, let us try out a query.

Head to the **API** tab in the Console at https://hasura-7exz.onrender.com/console/api/api-explorer and try running the following query:

![Render_Hasura_GraphQL-009](https://user-images.githubusercontent.com/1499433/229496040-cb6e4400-2363-4916-aa69-b2d5dde01269.png)

You'll see that you get all the inserted data!

Ultimately we can request the following query that will give us the required response:

![Render_Hasura_GraphQL-010](https://user-images.githubusercontent.com/1499433/229520177-86737598-3a90-4a6b-a7e7-06ba53bc3a88.png)

Hooray!

## 200 - Test REST queries

We can create an Endpoint from a GraphQL query to a REST request (e.g. GET, POST, PUT, PATCH, or DELETE) as follows.

In Hasura create an Endpoint for our cereal query as depicted below (we call it ```cereal```:

![Render_Hasura_GraphQL-013](https://user-images.githubusercontent.com/1499433/229817006-f3a01d4b-16a0-4324-b980-e2b63fdfc3a5.png)

Then click "Create Endpoint"

![Render_Hasura_GraphQL-014](https://user-images.githubusercontent.com/1499433/229817609-8075da98-f3b3-4862-a4eb-222ca8964a43.png)

See https://hasura-7exz.onrender.com/console/api/rest/list for above page

Now from a browser or from within code open this URL: https://hasura-7exz.onrender.com/api/rest/cereal

It will return the same result as if requested as a GraphQL request (which is always a POST method), but now using the REST protocol (here: using the GET method instead).

```

```
Response from REST request


Now we can use this query to draw our "Cereal" as a molecule (see https://github.com/vanHeemstraSystems/chemplexity-servings):

== screenshot should go here ==
