# 100 - One-Click Deploy

Following the instructions at https://render.com/docs/deploy-hasura-graphql

Click Deploy to Render below to set up Hasura GraphQL Engine on your Render account. This will deploy the Hasura GraphQL Engine web service and create a PostgreSQL database used to store both your application data and GraphQL Engine’s metadata.

[Deploy to Render](https://render.com/deploy?repo=https://github.com/render-examples/hasura-graphql)

![Render_Hasura_GraphQL-001](https://user-images.githubusercontent.com/1499433/229482309-854523b1-c96c-403c-a6f4-a2be534a392c.png)
Result from "Deploy to Render".

For the **Blueprint Name**, we enter: **Servings**

A unique name for your Blueprint.

For the **Branch**, we enter: **master** (default)

The repository branch with the render.yaml file.

Confirm by clicking the "Apply" button.

Next, a hasura database will be created. See https://dashboard.render.com/d/dpg-cglaj0grddleudqvvub0-a

Finally, a hasura web service will be created. See https://dashboard.render.com/web/srv-cglaj98rddleudr00ku0

You will be prompted as follows:

"*Your changes were applied successfully! See your Blueprint instance's [managed resources](https://dashboard.render.com/blueprint/exs-cglaesseoogkndnaou3g/resources).*"

![Render_Hasura_GraphQL-002](https://user-images.githubusercontent.com/1499433/229484456-7110644c-5537-4125-93b1-a3642beb4d97.png)
Result from "Apply".

![Render_Hasura_GraphQL-003](https://user-images.githubusercontent.com/1499433/229485085-d5d55b24-411a-4863-b6b6-ce45dd4cba17.png)
The created instance of Hasura GraphQL

By default, the Hasura GraphQL web console is not password-protected. To secure it, create an environment variable named ```HASURA_GRAPHQL_ADMIN_SECRET``` for the web service you just deployed in the Render Dashboard.

For this go to https://dashboard.render.com/web/srv-cglaj98rddleudr00ku0/env and add an Environment Variable Key and Value as follows:

![Render_Hasura_GraphQL-004](https://user-images.githubusercontent.com/1499433/229489663-c8db66d9-e7b5-49ea-bd58-17506c9c4206.png)
Result from Adding an Environment Variable

**REMEMBER** the value of the ```HASURA_GRAPHQL_ADMIN_SECRET``` well, as you may need to enter it later on.

Now you can start working with Hasura:

## 100 - Create a table

See [README.md](./100/README.md)

## 200 - Test GraphQL and REST queries

See [README.md](./200/README.md)

## 300 - Read how Hasura GraphQL Engine works

See [README.md](./300/README.md)
