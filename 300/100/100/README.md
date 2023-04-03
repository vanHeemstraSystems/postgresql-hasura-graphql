# 100 - Create a table

Based on "Create a table" at https://hasura.io/docs/latest/graphql/core/getting-started/docker-simple.html#create-a-table

After successful completion of the previous steps, follow the instructions from https://hasura.io/docs/latest/getting-started/docker-simple/#step-3-try-out-hasura as detailed here:

## 100 - Create a table and insert some demo data

On the Hasura Console (here: https://hasura-7exz.onrender.com/console), navigate to Data -> Create table.

![Render_Hasura_GraphQL-005](https://user-images.githubusercontent.com/1499433/229491078-d1de22c3-c1f3-4cd2-bb46-d90f35ff7028.png)
Hasura Console

And create a sample table called ```cereals``` with the following columns:

Table Name: **cereals**

Columns:

| Column Name | Column Type |
| --- | --- |
| id | Integer auto-increment | 
| atom | Text | 
| size | Integer |
| color | Text |

Primary Key: **id**

![Render_Hasura_GraphQL-006](https://user-images.githubusercontent.com/1499433/229492864-40e56cb7-ee20-47ab-80ae-6f34a6bdec3f.png)

Click "**Add Table**"

Now, insert some sample data into the table using the ```Insert Row``` tab of the cereals table.

![Render_Hasura_GraphQL-007](https://user-images.githubusercontent.com/1499433/229493549-e1e92cfe-a6bf-4373-a379-ee78cc6fe312.png)

The newly created rows should contain the following:

| id | atom | size | color |
| --- | --- | --- | --- |
| auto-incremented integer | Milk | 5 | #FFFFFF |
| auto-incremented integer | Oat Flakes | 5 | #FFFFFF |
| auto-incremented integer | Multigrain | 5 | #FFFFFF |
| auto-incremented integer | Oat Meal | 5 | #FFFFFF |

![Render_Hasura_GraphQL-008](https://user-images.githubusercontent.com/1499433/229494820-f38f1680-480b-401e-8c12-a2bf00e846bf.png)

In order to feed data for a chemcomplexity diagram (see https://github.com/vanHeemstraSystems/chemplexity-servings), we are going to create two more tabels: **nodes** and **links** as follows:

![Render_Hasura_GraphQL-011](https://user-images.githubusercontent.com/1499433/229521560-7d864316-8554-4492-9cb6-5e71f02dcaa6.png)
"Nodes" table


"Links" table

Ultimately we can request the following query that will give us the required response:

![Render_Hasura_GraphQL-010](https://user-images.githubusercontent.com/1499433/229520177-86737598-3a90-4a6b-a7e7-06ba53bc3a88.png)

Now we can use this query to draw our "Cereal" as a molecule (see https://github.com/vanHeemstraSystems/chemplexity-servings):

== screenshot should go here ==

Hooray!
