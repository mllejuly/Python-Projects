# **Social Network Analysis - Notes Summary**

by: Qi Fang


## **1. NetworkX Basic**
   * **Network(Graph), Nodes, Edges**
   * **Symmetric Relationships, Asymmetric Relationships**
   * **Undirected Network, Directed Network, Weighted Network, Signed Network, Multigraph**
        * Undirected: G = nx.Graph()
        * Directed: G = nx.DiGraph()
        * Weighted: G.add_edge('A', 'B', weight = 6)
        * Signed: G.add_edge('A', 'B', sign = '+')
        * Multigraph: G = nx.MultiGraph()
   * **Bipartite Graphs**


## **2. Network Connectivity**
   * **Clustering Coefficient(聚类系数)**
        * Clustering Coefficient measures the degree to which nodes in a network tend to cluster or form triangles.
        * Triadic Closure(三元闭包)
        * Local Clustering Coefficient(LCC, 局部集聚系数)
           * Local Clustering Coefficient of node C = # pairs of C's friends who are friends / # pairs of C's friends
           * Local Clustering Coefficient of node C = nx.clustering(G, 'C')
        * Global Clustering Coefficient(局部集聚系数)
            * Average Local Clustering Coefficient over all nodes in the graph = nx.average_clustering(G)
            * Transitivity
   * **Distance Measures**
        * Path
            * Shortest Path = nx.shortest_path(G, 'A', 'H')
        * Distance
            * BFS
            * Distance = nx.shortest_path_length(G, 'A', 'H')
            * Average Distance = nx.average_shortest_path_length(G)
        * Diameter(直径)
            * The Diameter of a graph is the Maximum Distance between any pair of nodes.
            * nx.diameter(G)
        * Eccentricity(偏心率)
            * The Eccentricity of a node n is the largest distance between n and all the other nodes in the network.
            * nx.eccentricity(G)
        * Radius(半径)
            * The Radius of a graph is the Minimum Eccentricity.
            * nx.radius(G)
        * Periphery(边缘)
            * The periphery of a graph is the set of nodes that have eccentricity equal to the diameter.
            * nx.periphery(G)
        * Center(中心)
            * The center of a graph is the set of nodes that have eccentricity equal to the radius.
            * nx.center(G)
        * Karate Club Graph(空手道俱乐部数据集)
            * G = nx.karate_club_graph()
   * **Connected Components(连通分量)**
        * Connected Graph
            * An undirected graph is connected if, for every pair nodes, there is a path between them.
            * nx.is_connected(G)
        * Strongly Connected, Weakly Connected
            * nx.is_strongly_connected(G)
            * nx.is_weakly_connected(G)
        * Strongly Connected Component, Weakly Connected Component
            * nx.strongly_connected_components(G)
            * nx.weakly_connected_components(G)
   * **Network Robustness**
        * Disconnecting a Graph
            * Minimum nodes cut to disconnect a graph: nx.node_connectivity(G)
            * Nodes cut to disconnect a graph: nx.minimum_node_cut(G)
            * Minimum edges cut to disconnect a graph: nx.edge_connectivity(G)
            * Edges cut to disconnect a graph: nx.minimum_edge_cut(G)
            * Robust networks have large minimum node and edges cuts
   
## **3. Influence Measures and Network Centralization**
   * **Degree and Closeness Centrality**
        * Centrality Measures
          * Degree centrality(度中心性)
          * Closeness centrality(紧密中心性)
          * Betweenness centrality(中介中心性)
          * Page Rank(网页排名)
          * Load centrality, Katz centrality, Percolation centrality
   * **Node Importance**
        * Clustering Coefficient measures the degree to which nodes in a network tend to cluster or form triangles.
        * Triadic Closure(三元闭包)
        * Local Clustering Coefficient(LCC, 局部集聚系数)
           * Local Clustering Coefficient of node C = # pairs of C's friends who are friends / # pairs of C's friends
           * Local Clustering Coefficient of node C = nx.clustering(G, 'C')
        * Global Clustering Coefficient(局部集聚系数)
            * Average Local Clustering Coefficient over all nodes in the graph = nx.average_clustering(G)
            * Transitivity
   * **Betweenness Centrality**
   * **Page-Rank**
   * **Hubs and Authorities***
   
   * **Calculation Summary**
        * degree centrality
        * closeness centrality
        * betweenness centrality, normalized betweenness centrality
        * alpha (damping parameter) in the NetworkX function pagerank maximizes the PageRank of node X
 
 
 ## **4. Preferential Attachment Model**
   * **Degree Distribution**
        * degrees = G.degree()
   * **Link Prediction(链接预测)**
        * 1. Common Neighbors
        * 2. Jaccared Coefficient
        * 3. Resource Allocation
        * 4. Adamic-Adar Index
        * 5. Preferential Attachment
        * 6. Community Common Neighbors
        * 7. Community Resource Allocation
        
 ## **Appendix**
   * **Related Model**
       * Preferential Attachment Model(优先连接模型)
       * Small World Model(六度空间理论)
         * Path Length: nx.average_shortest_path_length(G)
         * Clustering: nx.average_clustering(G)
       
   * **Related Algorithm**
       * Page Rank Algorithm(网页排名算法，Google)
         * Rank Leak
         * Rank Sink
       * Link Prediction Algorithms(链接预测算法)
       

 
 
