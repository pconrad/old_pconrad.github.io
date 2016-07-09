---
topic: "GraphViz"
desc: "Graph drawing software"
---

# Graphviz on the web

<http://www.webgraphviz.com/>

# Example DOT file for an AST for arithmetic expressions

```
digraph G {
    p [label="+"]
    p -> 2
    t [label="*"]
    p -> t
    t -> 3
    t -> 4
}
```



