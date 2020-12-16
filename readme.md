# Install Visulat Studio Code Extension for Graphviz

# Install Dot in MAC/Linux 

# Convert Dot to Json 

> dot -Txdot_json -ogrpaph.json graph.dot

# Reading and Convertign in Adjacency Matix 

```
#!/usr/bin/env python

import sys
import pygraphviz
import json

def main():
    G = pygraphviz.AGraph()
    G.read("foo.dot")
    adj = { 'adjacency_matrix_rows' : [] }
    for n in G.nodes():
        row = { n : [G.has_edge(n, tn)*1 for tn in G.nodes()] }
        adj['adjacency_matrix_rows'].append(row)
    sys.stdout.write("%s\n" % (json.dumps(adj)))

if __name__ == "__main__":
    main()
   ```
   
  
