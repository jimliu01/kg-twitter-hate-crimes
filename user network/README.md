**User Dataset Folders are Omitted for Confidentiality**

`user network.ipynb` is used to create the following folder. It also includes analysis of negative users.

`/user networks/` contains the following files:
- `relations_black.pkl` is formed by filtering `bigbaby_r_t_30_s.csv` by only users who tweeted at least 10 times in the entire time span (there are 1195 of them) and computing similarity between each pair of users by considering black topics. This weight increases if both users tweeted frequently in similar black topics. 
- `user_network_black.csv` is formed by creating a graph from `relations_black.pkl` and calculating weighted degree, eigenvector centrality. It also includes the number of tweets from each user, the follower count, their screen name, the average sentiment of their tweets, and the product of the number of followers and the weighted degree (a sort of 'weighted weighted degree')
- `relations_all.pkl` is the same as `relations_black.pkl` but using black and LGBTQ+ topics.
- `user_network_all.csv` is same as `user_network_black.csv` but using `relations_all.pkl`.
- `relations_lgbtq.pkl` is the same but using LGBTQ+ topics.
- `user_network_lgbtq.csv` is same but using `relations_lgbtq.csv`.

`user network monthly.ipynb` is used to create the following folders:
- `/usersbymonth-black-10/` is a folder containing the same process on `relations_black.pkl` and `user_network_black.csv`, but after splitting `bigbaby_r_t_30_s.csv` into 16 partitions by month. In particular, we continue to filter users by those who tweeted at least 10 times in the time span, as well as consider black topics.
- `/usersbymonth-black-5/` is the same as previous one but we filter users by those who tweeted at least 5 times.
- `/usersby2w-black-5/` is the same as previous one but we split into 33 2-week partitions
- `/usersby2w-black/` splits into 33 2-week partitions, but we don't filter each biweek separately; instead, we just form user networks from the 1195 users originally included in `user_network_black.csv` who tweeted at least 10 times in the entire time period. So we have smaller user networks but preserve information on every user.
- `/usersby2w-all/` is the same as previous one but by forming weights using the LGBTQ+ topics as well.
- `/usersby2w-lgbtq/` is the same as previous one but by forming weights using just the LGBTQ+ topics.

`user network analysis.ipynb` is used to analyze the user networks.

`user network communities.ipynb` is used to generate and analyze communities on the user networks.