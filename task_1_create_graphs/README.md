Reference: https://github.com/JasonZhangzy1757/Diet-ODIN/tree/main/code/preprocessing

## Notes: 

The goals of this task are: 

1. Create subgraphs for opioid users and recovered users groups
2. Join these 2 graphs together, through constructing metapaths, to create a joined graph

In the notebook I uploaded, there are 2 main sections: 

* Step 1: I created the 2 subgraphs and joined graph, but forgot include the health tags for the user nodes
* Step 2: I added the user's heath tags to the joined graph directly

TODO: in hindsight, I realized that a better approach would be to add the health tags to each individual subgraph, then join them together, instead of adding the health tags only to the joined graph later on.
