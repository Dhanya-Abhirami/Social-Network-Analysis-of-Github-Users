# Social-Network-Analysis-of-Github-Users

Github is the most popular online code versioning system used by engineers, software developers, research scholars and students. The Github user base itself forms a social community. Github offers many features like code repositories, starring, forking and following. In this project Github API is utilised to access the Github Data and apply social network analysis techniques on the fetched data. The tasks include constructing graphs, finding influential users and performing community detection on the Github user data.
## Graph Modelling
Github can be modeled using two types of networks namely, commit network and follower network.
Follow Network deals with developers following other developers whom they admire. In this network, the entities are homogeneous. Bob follows Alice, and Chris follows Alice and Bob. <br>
![alt tag](https://github.com/Dhanya-Abhirami/Social-Network-Analysis-of-Github-Users/blob/master/follow_network.png)

Commit Network consists of developers connected to the repositories they contribute to. This is a bipartite network, with direct edges emanating from the developer node to the repository node. Alice commits in Repository 1, and Alice, Bob and Chris commit in Repository 2. <br>
![alt_tag](https://github.com/Dhanya-Abhirami/Social-Network-Analysis-of-Github-Users/blob/master/commit_network.png)

## Architecture
GitHub user open data is accessed using the GitHub API. After initial rounds of preprocessing of the API result, social network graphs are constructed for the relations “A follows B”, “A stars repository R” and “A forks repository R”. <br>
![alt_tag](https://github.com/Dhanya-Abhirami/Social-Network-Analysis-of-Github-Users/blob/master/architecture.png)
## Implementation
The techstack used for our analysis includes Python, PyGitHub (GitHub API Python interface), Networkx (Network analysis library) and Matplotlib.,<br>
Our target repository is titled “Hacktoberfest” and owner by GitHub user with username @ahmedawais. Hacktoberfest is a month long celebration of open source conducted in October every year, wherein developers contributing to publicly hosted GitHub Projects are rewarded suitably. During this period, GitHub repositories are observed with high degree of activity.
Stargazers network and forks network of the chosen repository is constructed. <br>
Next a GitHub user with a small number of followers (@Dhanya-Abhirami) is chosen. Follower network of that user is contructed. Next the graph is extended to add the followers of the followers of the user into the same network. Analysis of the graph is performed to find influential users using Pagerank and HITS algorithms. The communities formed here are also discovered.
## How to run
Install the dependencies
```
pip install pygithub
pip install numpy
pip install networkx
```
Clone this repo<br>
Open the file in Jupyter Notebook <br>
Add your GitHub API Credentials <br>
Run!
## References
* [Book](https://www.oreilly.com/library/view/mining-the-social/9781449368180/ch07.html)
* [Tutorial](https://chase-seibert.github.io/blog/2016/07/22/pygithub-examples.html)
* [More](https://github.com/ericmjl/Network-Analysis-Made-Simple?files=1)
