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

Try it by clicking the "Run Request" button:

![Render_Hasura_GraphQL-015](https://user-images.githubusercontent.com/1499433/229818490-eedc1f54-c712-4802-8edb-b634aa036624.png)

```
{
    "nodes": [
        {
            "atom": "Milk",
            "size": 5,
            "color": "#FFFFFF"
        },
        {
            "atom": "Oat Flakes",
            "size": 5,
            "color": "#FFFFFF"
        },
        {
            "atom": "Multigrain",
            "size": 5,
            "color": "#FFFFFF"
        },
        {
            "atom": "Oat Meal",
            "size": 5,
            "color": "#FFFFFF"
        }
    ],
    "links": [
        {
            "source": 0,
            "target": 1,
            "bond": 1
        },
        {
            "source": 1,
            "target": 2,
            "bond": 1
        },
        {
            "source": 1,
            "target": 3,
            "bond": 1
        }
    ]
}
```
Response from REST request

Now we can use this query to draw our "Cereal" as a molecule (see https://github.com/vanHeemstraSystems/chemplexity-servings):

```
...
// d3.json("cereal.json", function(graph) {
d3.json("https://hasura-7exz.onrender.com/api/rest/cereal", function(graph) {
  ...
}
...
```
index.html

In ```index.html``` we replace the reference for d3 to the local json data file ```cereal.json``` by the REST GET request URL ```https://hasura-7exz.onrender.com/api/rest/cereal```

To test the index.html file locally, you can visit https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb and click the "Launch app" button after installation of the "Web Server for Chrome" extension. Set the folder in which you host index.html and visit the URL (here: http://127.0.0.1:8887) to see your web page.


== screenshot should go here ==
