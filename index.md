---
layout: home
---
<!-- title: "Collectif Metisser" -->
<!-- subtitle: "A Data Story of Connected Nodes <3" -->
<div class="video-container">
    <video autoplay muted loop playsinline class="centered-video">
        <source src="{{ '/assets/videos/universe-2.mp4' | relative_url }}" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>
<p>Some music to accompany you through your experience? </p>
<p>This music is courtesy of our friend, and music writer/producer DINA. Produced by Casper at Sounds of Africa Label.</p>
<audio controls>
    <source src="{{ '/assets/audio/RUNNIN-MASTER-CD.mp3' | relative_url }}" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>

<h1>Welcome to the Knowledge Cosmos, where <span style="font-weight: bold;">PLANET WIKIPEDIA</span> exists.</h1>
<p>&nbsp;</p>
<img src="{{ '/assets/img/Network.png' | relative_url }}" width="80%">
<p>&nbsp;</p>


<div class="main-content">
  <p>Planet Wikipedia is a huge and constantly expanding world where towns and cities represent articles. The roads connecting these towns allow citizen lifeforms to travel between ideas. For centuries, these roads were built manually by a group of people called the First Pathfinders, but their work, although amazing, was imperfect. Some important towns are difficult to reach, being connected only with winding paths, while other towns, despite their great history or usefulness, sit isolated.</p>
  
  <p>The President of Wikipedia Planet feels that the inefficient road network has left many of its citizens frustrated, wandering aimlessly or missing critical destinations. The president forms a team of visionaries known as the Architects of Connection, tasked with uncovering hidden connections and reshaping the planet's roads.</p>

  <p>&nbsp;</p>

  
  


  <h1> Chapter 1 | The Study: Getting to know Planet Wikipedia. </h1>
  <p>The Architects start by studying their planet, to gain a better understanding, helping guide them to select an appropriate approach for their plan.</p>
  <p>They start by crafting a directional map of Planet Wikipedia, visualizing the connections between towns (articles) to uncover the existing paths and gaps in the knowledge network.</p>

  <p>As they observe the map, they notice a clear pattern: the largest cities, representing the most influential articles, have the most roads and connections to neighboring towns. On the other hand, smaller cities, symbolic of lesser-known topics, are more isolated, with fewer paths linking them to others.</p>

  <div class="video-container">
      <video autoplay muted loop playsinline class="centered-video">
          <source src="{{ '/assets/videos/graphRecording2.mp4' | relative_url }}" type="video/mp4">
          Your browser does not support the video tag.
      </video>
  </div>

  <div style="display: flex; align-items: center; gap: 20px; width: 100%;">
    <div style="flex: 1;">
      <iframe 
        src="{{ '/assets/data/degree_distribution_dark.html' | relative_url }}"
        width="600"
        height="450"
        style="border: none;">
      </iframe>
    </div>
    <div style="flex: 2;">
      <p>
        The Architects of Connection perform some analysis of the relationships between towns. 
        Before moving on to more complicated features, they analyze the 
        degree of node connections in search of influential towns, meaning those with numerous 
        links serving as crucial hubs for fast travel. The graph is well-connected with a high average degree, local clusters, and a short average path length (~2.53), but low density suggests room for new links. Feature engineering should focus on local structures, short paths, and global features due to the graph's connectivity.
      </p>
    </div>
  </div>

  <!-- <h5>Graphical Statistical Analysis </h5>
  <br> -->
</div>





<div class="main content">
  <br>
  <div style="display: flex; align-items: flex-start; gap: 20px;">
    <div style="flex: 1;">
      <h1>Wikipedia's Feature Engineering</h1>
      <p>Now the Architects can finally explore the feature characteristics... They have an idea to train a model to help them in their task. But first, what could they examine? What would you examine? They want to determine the features that best represent the connection between two ideas (article hubs). To do so, both node features and edge features are examined. Wow, they have to get to work, there is a lot to discover on their own planet! </p>
    </div>
    <div>
      <img src="{{ '/assets/img/feature_architects.webp' | relative_url }}" alt="feature architects" style="width: 400px; height: auto;">
    </div>
  </div>
<div class="main-content">

  <p>&nbsp;</p>
  <h5>Node Features</h5>
  <p>The Architects focus on three important metrics that help them understand and improve the network: PageRank, Eigenvector Centrality, and Common Neighbors. First, using PageRank, they rank the towns (nodes) in order of their importance in the network, which is defined by the structure of the incoming roads (links). A town with higher PageRank has greater influence because it is connected to other well-connected towns. Eigenvector Centrality complements this by measuring the influence of a town in the broader network; here, connections to highly influential towns count more than connections to less critical ones. Last but not least, under Common Neighbors, the Architects study pairs of towns that have more neighbors in common, with the intuition that such pairs are more likely to benefit from a direct road (link) in the future. The following set of metrics informs Architects in reshaping the network to best navigate and stay better connected.</p>

  <div style="display: flex; align-items: center; justify-content: center; gap: 20px; margin-top: 20px; margin-bottom: 40px;">
      <img src="{{ '/assets/img/PageRank_dark.png' | relative_url }}" alt="PageRank Algorithm" style="max-width: 45%; height: auto; flex-shrink: 1;">
      <img src="{{ '/assets/img/Eigenvector_dark.png' | relative_url }}" alt="Eigenvector Centrality" style="max-width: 45%; height: auto; flex-shrink: 1;">
  </div>
<!-- </div> -->

  <div style="display: flex; justify-content: center; align-items: center; flex-direction: column; gap: 20px; width: 100%;">
    <!-- First Plot -->
    <iframe 
      src="/assets/data/common_neighbors_distribution.html"
      width="650"
      height="450"
      style="border: none;">
    </iframe>

    <!-- Second Plot -->
    <iframe 
      src="/assets/data/title_similarity_distribution.html"
      style="border: none; width: 80%; height: 550px; min-height: 400px;">
    </iframe>

    <!-- Third Plot -->
    <iframe 
      src="/assets/data/description_similarity_distribution.html"
      style="border: none; width: 90%; height: 550px; min-height: 400px;">
    </iframe>
  </div>
  <div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 600px;">
    <iframe 
      src="/assets/data/cosine_similarity_title_boxplot.html"
      width="600"
      height="450"
      style="border: none;">
    </iframe>
  </div>
  <div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 600px;">
    <iframe 
      src="/assets/data/conditional_probability_description_dark.html"
      width="600"
      height="450"
      style="border: none;">
    </iframe>
  </div>



  <!-- <div class="main content">
      <h>Below we compare the cosine similarity between titles and descriptions of connected and unconnected node pairs. As expected, unconnected cases have smaller values.</h>
      <br>
  </div> -->

  

  <!-- <div class="main content">
      <br>
      <p>&nbsp;</p>
      <h>The probability of being connected according to the cosine similarity distributions can be calculated and represented here below.</h>
      <p>&nbsp;</p>
      <br>
  </div> -->

  
    <!-- <div class="video-container">
        <video autoplay muted loop playsinline class="centered-video">
            <source src="{{ '/assets/videos/cool_crypto.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div> -->
    <p>&nbsp;</p>
    <h5>Edge Features</h5>
    <h>The Architects of Connection use advanced tools to improve the roads of Planet Wikipedia. Preferential Attachment reveals that bustling hubs are more likely to attract new roads, while isolated towns lag behind. Jaccard Similarity highlights shared neighbors, with connected towns showing stronger overlaps that reflect deeper relationships. The Adamic-Adar Index emphasizes rare, unique connections, identifying distinctive ties between linked towns. Finally, Node2Vec makes representations of towns by generating biased random walks to capture both local structures and global patterns. These techniques together allow the Architects to build a smarter and connected network.</h>
    <br>
  </div>

<!-- <div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 600px; padding-left: 50px;">
      <iframe 
        src="/assets/data/jaccard_histogram_2.html"
        width="850"
        height="550"
        style="border: none;">
      </iframe>
</div> -->

<div class="main content">
    <p>&nbsp;</p>
    <img src="{{ '/assets/img/pref_attach2.png' | relative_url }}">
    <p>&nbsp;</p>
    <br>
    <!-- <h>Jaccard similarity: The Jaccard's coefficient is a commonly used similarity metric in information retrieval. It measures the probability that both x and y have a feature f, knowing that x or y has the feature f (which is randomly selected). In our case, the features are the neighbors. It is defined as the size of the intersection divided by the size of the union of the sets.
    Discussion: Below we compare the Jaccard's coefficients for both connected and unconnected node pairs. As expected, the Jaccard coefficient values are higher for connected node pairs, as the likelihood of sharing a neighbor increases when nodes are directly connected.</h> -->
    <!-- <div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 600px; padding-left: 50px;">
      <iframe 
        src="/assets/data/jaccard_histogram_2.html"
        width="850"
        height="550"
        style="border: none;">
      </iframe>
    </div> -->
    <p>&nbsp;</p>
    <img src="{{ '/assets/img/jaccard_scatter.png' | relative_url }}">
    <p>&nbsp;</p>
    <!-- <h>Adamic adar index: To determine how closely two personal home pages are linked, Adamic and Adar examine their common features. Unlike a simple count of these shared features, this index weighs the contribution of each distinctive or less frequent feature by the inverse logarithm of its degree, assigning more weight to rarer features to measure the similarity between entities.
    Discussion: We observed the differences between connected and unconnected pairs of nodes. As expected, the values for connected pairs of nodes are larger than those for unconnected pairs of nodes because there is a greater likelihood of shared connections or features when nodes are directly linked.</h> -->

  <!-- <div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 600px;">
    <iframe 
      src="/assets/data/adamic_adar_distribution_merged.html"
      width="850"
      height="550"
      style="border: none;">
    </iframe>
  </div> -->
  <p>&nbsp;</p>
  <img src="{{ '/assets/img/adamic_adar_scatter.png' | relative_url }}">
  <p>&nbsp;</p>
  <br>

  <h1> Chapter 2 | The Machine Awakens: Training the Grand Predictor </h1>

  <div class="main content">
  <br>
  <div style="display: flex; align-items: flex-start; gap: 20px;">
    <div>
      <img src="{{ '/assets/img/training_architects.webp' | relative_url }}" alt="feature architects" style="width: 400px; height: auto;">
    </div>
    <div style="flex: 1;">
      <h1>Wikipedia's Feature Engineering</h1>
      <p>With the node and edge features in hand, the Architects move to the next stage of training the Graph Convolutional Network to predict new roads between unconnected hubs. They will make use of features such as cosine similarity, Jaccard similarity, Adamic-Adar index, preferential attachment, and PageRank to identify potential candidates for new connections.
      The GCN combines these features into enriched representations of towns and their relationships. As the model navigates through its layers, intricate patterns in the network are picked up, while an MLP provides a score for every pair, predicting the likelihood of a new road. Equipped with data-driven precision, the Architects are now ready to reshape Planet Wikipedia.</p>
    </div>
  </div>

  <h1> Chapter 3 | Exploring the Aftermath: The Connected Planet </h1>

  <div class="main content">
  <br>
  <div style="display: flex; align-items: flex-start; gap: 20px;">
    <div style="flex: 1;">
      <h1>Which nodes should be connected?</h1>
        <p>The Architects of Connection have completed their monumental task, reshaping the roads of Planet Wikipedia with the help of their predictive tools. Now, they turn their attention to the aftermath, evaluating the impact of their work. Have the new connections transformed isolated towns into bustling hubs? Are citizens finding it easier to navigate between ideas and discover new destinations? By analyzing which categories of towns have become more interconnected—whether scientific hubs now bridge to artistic villages or historical sites link to modern innovations—the Architects uncover the broader effects of their efforts. The newly connected network holds the promise of a more vibrant and accessible Planet Wikipedia, where no idea is too far to reach.</p>
    </div>
    <div>
      <img src="{{ '/assets/img/analysis_architects.webp' | relative_url }}" alt="feature architects" style="width: 400px; height: auto;">
    </div>
  </div>


<div class="main-content">
  <br>
  <!-- <h>Node2Vec: Node2Vec is an algorithm designed to create vector representations (embeddings) of nodes in a network by simulating biased random walks. This allows for capturing both local neighborhood structures and global network relationships. Node2Vec strikes a balance between breadth-first (BFS) and depth-first (DFS) strategies, enabling the embeddings to capture both homophilic (similar nodes connected) and structural equivalences (nodes playing similar roles in different parts of the graph). -->
</div>

<div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 600px;">
  <iframe 
    src="{{ '/assets/data/experiment_metrics_comparison.html' | relative_url }}"
    width="1200"
    height="450"
    style="border: none;">
  </iframe>
</div>

<div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 600px;">
  <iframe 
    src="{{ '/assets/data/all_experiments_validation_loss.html' | relative_url }}"
    width="1200"
    height="450"
    style="border: none;">
  </iframe>
</div>

<div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 600px; margin-bottom: 20px;">
  <iframe 
    src="/assets/data/source_categories_distribution.html"
    width="1000"
    height="750"
    style="border: none;">
  </iframe>
</div>

<div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 600px;">
  <iframe 
    src="/assets/data/target_categories_distribution.html"
    width="1000"
    height="750"
    style="border: none;">
  </iframe>
</div>



<div class="main content">
    <p>&nbsp;</p>
    <h1>Thank you for discovering Planet Wikipedia's story </h1>
    <p>&nbsp;</p>
    <div class="video-container">
        <video autoplay muted loop playsinline class="centered-video">
            <source src="{{ '/assets/videos/end_anim.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
</div>
<p> A project by Collectif Metisser: Alfred Arnaud, Nina Bodenstab, Alexis Limozin, Angeline Prasanna, Antoine Violet.

<style>
  /* Center the video container */
  .video-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 30px;  /* Add space between video and content */
    padding: 0 20px; /* Add some horizontal padding */
  }

  /* Make the video larger and higher */
  .centered-video {
    width: 100%;      /* Make video take full width of the container */
    height: 80vh;     /* Set the height to 80% of the viewport height (you can adjust this) */
    object-fit: cover; /* Ensures video covers the space without stretching */
  }

  /* Increase the content's margin for more spacing on the page */
  .main-content {
    margin: 0 auto;    /* Center content */
    max-width: 1200px;  /* You can adjust this width to make the content wider */
    padding: 20px;      /* Add some padding for spacing around the content */
  }

</style>
