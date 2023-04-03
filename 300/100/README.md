# 100 - Using local JSON file for input

See also https://www.tutorialsteacher.com/d3js/loading-data-from-file-in-d3js#d3.json

Our local JSON file is **cereals.json** and contains the following:

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
cereals.json

The above file can thus be read into d3 as follows:

```
...
d3.json("cereal.json", function(graph) {
   MORE LOGIC HERE
}
...
```
