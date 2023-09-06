
`/bigbabies/` (not included for confidentiality)
- `bigbaby_og.csv`: original csv containing all 28 million, after combining from /csv/ folder
- `bigbaby.csv`: same as og but removing some ~50k corrupted rows
- `bigbaby_all.csv`: filtering `bigbaby.csv` by keywords given in `/keywords/asian.txt`, `/keywords/black.txt`, `/keywords/hispanic.txt`, `/keywords/jewish.txt`, and `/keywords/lgbt.txt`
- `bigbaby_all_t.csv`: topic modeling on `bigbaby_all.csv` with no parameters
- `bigbaby_r.csv`: filtering `bigbaby.csv` by keywords given in `/keywords/new.txt`
- `bigbaby_r_t.csv`: multiple topics modeling on `bigbaby_r.csv` with no parameters
- `bigbaby_r_t_30.csv`: multiple topics modeling on `bigbaby_r.csv` with `min_topic_size=30`


`/topics/`
- `bigbaby_all_docs.csv`: `get_document_info()` on the `bigbaby_all_t.csv` topic model (not included due to size)
- `bigbaby_all_tops.csv`: `get_topic_info()` on the `bigbaby_all_t.csv` topic model (not included due to size)
- `bigbaby_r_docs.csv`: `get_document_info()` on the `bigbaby_r_t.csv` topic model
- `bigbaby_r_tops.csv`: `get_topic_info()` on the `bigbaby_r_t.csv` topic model
- `bigbaby_r_30_docs.csv`: `get_document_info()` on the `bigbaby_r_t_30.csv` topic model
- `bigbaby_r_30_tops.csv`: `get_topic_info()` on the `bigbaby_r_t_30.csv` topic model


`/keywords/`
- `asian.txt`: list of asian keywords
- `black.txt`: list of black keywords
- `hispanic.txt`: list of hispanic keywords
- `jewish.txt`: list of jewish keywords
- `lgbt.txt`: list of lgbt keywords
- `other.txt`: list of other relevant keywords not specific to any group
- `new.txt`: list of combined keywords and further filtering done on 7/24
