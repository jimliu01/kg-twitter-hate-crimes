- `KG back to big.ipynb` constructs a KG with all the nodes described in the paper, and all 5 groups.
- `KG New.ipynb` is the newest notebook without crimes.
- `exploring tweet-topic.ipynb` Uses A^TA idea to project tweet-topic bipartite graph onto tweet space. Also used to choose tweets for the NLP Pipeline figure.
- `KG weighted.ipynb` experiments with assigning weights to the tweet-topic edge and traversing the path between user and hate crime. 
- `KG with Multiple Topics.ipynb` is the first to implement .01 threshold and multiple tweet-topic edges.
- `KG with Black Topics.ipynb` is the oldest notebook exploring just a KG with the black topics and includes a has_sentiment relation.

Constructed KGs are placed in the `/data/` folder. For select KGs, entities and relations are encoded to maintain confidentiality.
