# 200 - Using remote JSON GraphQL for input

See also https://www.tutorialsteacher.com/d3js/loading-data-from-file-in-d3js#d3.json

We will query a remote GraphQL endpoint https://hasura-7exz.onrender.com/console/api/api-explorer as follows:

```
{
  nodes {
    atom
    size   
    color
  }  
  links {
    source
    target
    bond    
  }
}
```
Query of GraphQL for JSON data

See also https://github.com/vanHeemstraSystems/postgresql-hasura-graphql

The outcome is:

```
{
  "data": {
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
}
```
Response from GraphQL query

In order for d3.json() to be able to handle this response we need to do the following:

MORE ...
