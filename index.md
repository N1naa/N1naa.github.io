---
layout: home
title: "Collectif Metisser"
subtitle: "A Data Story of Connected Nodes <3"
---

<div class="main-content">
    <div class="video-container">
        <video autoplay muted loop playsinline class="centered-video">
            <source src="{{ '/assets/videos/3130284-uhd_3840_2160_30fps.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
    <h1>Some music to accompany you through your experience ... What's your mood? </h1>
    <div style="display: flex; gap: 10px; justify-content: center;">
        <iframe style="border-radius:12px; flex: 1;" 
                src="https://open.spotify.com/embed/track/3sP0pCSFv02t822yGiR5O5?utm_source=generator&theme=0" 
                width="100%" height="352" frameBorder="0" allowfullscreen="" 
                allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        <iframe style="border-radius:12px; flex: 1;" 
                src="https://open.spotify.com/embed/track/2FnMQEvfbdSI0AI9mKM5by?utm_source=generator&theme=0" 
                width="100%" height="352" frameBorder="0" allowfullscreen="" 
                allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
    </div>
    <audio controls>
        <source src="{{ '/assets/audio/your-audio.mp3' | relative_url }}" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>
    <p>This music is courtesy of our friend, and music writer/producer GRISP.</p>
    <h1>Data's Origin Story</h1>
    <p>To gain a better understanding of the data, some basics but important characteristics of the graph are computed/displayed. This will help guide us in selecting the most appropriate approach for the next steps.</p>
    <h5>Graphical Statistical Analysis</h5>
    <!-- <br>
    <img src="{{ '/assets/img/degree_distr_dark.png' | relative_url }}">
    <br> -->
    <br>
     <iframe 
    src="{{ '/assets/data/degree_distribution.html' | relative_url }}"
    style="width: 100%; height: 600px; border: none;">
    </iframe>
    <br>
    <h>To train the model, we introduce a set of handcrafted features tailored to the context of link prediction. These features are selected based on the project's aim and the statistical analysis conducted above. They are intended to be the most relevant for achieving effective link creation. Some of the methods are discussed in the paper "The Link Prediction Problem for Social Networks", by Nowell et al. https://www.cs.cornell.edu/home/kleinber/link-pred.pdf</h>
    <br>
    <p>&nbsp;</p>
    <h5>Node Features</h5>
    <p>&nbsp;</p>
    <h>PageRank algorithm: This algorithm ranks nodes based on their importance in the network, determined by the structure of incoming links. The basic idea is that a node with a higher PageRank is more influential because it receives more incoming connections from other important nodes.</h>
    <div style="display: flex; align-items: center; justify-content: center; gap: 20px; margin-top: 20px; margin-bottom: 40px;">
        <img src="{{ '/assets/img/PageRank_dark.png' | relative_url }}" alt="PageRank Algorithm" style="max-width: 45%; height: auto; flex-shrink: 1;">
        <img src="{{ '/assets/img/Eigenvector_dark.png' | relative_url }}" alt="Eigenvector Centrality" style="max-width: 45%; height: auto; flex-shrink: 1;">
    </div>
    <h>Eigenvector Centrality: This is a measure of a node's influence within a network, where connections to highly influential nodes contribute more to a node's score than connections to less influential ones.</h>
    <h>Now, we compare the number of common neighbors between two nodes x and y. Two nodes with a higher number of common neighbors have a higher probability to be linked in the future.</h>
    <p>&nbsp;</p>
    <img src="{{ '/assets/img/common_dark.png' | relative_url }}">
    <p>&nbsp;</p>
    <br>
    <h>Cosine similarity between Text Embeddings: Cosine similarity is a measure of the resemblance between two vectors that represent word or text embeddings. The larger the angle between these vectors, the smaller the resemblance, and the smaller the cosine similarity. We compare the cosine similarity distribution for article titles and descriptions between unconnected and connected nodes. To avoid too large computational cost, we use a subset of our unconnected nodes.</h>
    <br>
    <p>&nbsp;</p>
    <img src="{{ '/assets/img/cosine_similarity_dark.png' | relative_url }}">
    <p>&nbsp;</p>
    <br>
    <h>Below we compare the cosine similarity between titles and descriptions of connected and unconnected node pairs. As expected, unconnected cases have smaller values.</h>
    <br>
    <p>&nbsp;</p>
    <img src="{{ '/assets/img/cosine_bars_dark.png' | relative_url }}">
    <p>&nbsp;</p>
    <br>
    <p>&nbsp;</p>
    <h>The probability of being connected according to the cosine similarity distributions can be calculated and represented here below.</h>
    <p>&nbsp;</p>
    <br>
    <p>&nbsp;</p>
    <img src="{{ '/assets/img/probas_dark.png' | relative_url }}" width="600">
    <p>&nbsp;</p>
    <br>
    <h1>Data's Feature Engineering</h1>
    <h>Now we can finally explore the feature characteristics...</h>
    <div class="video-container">
        <video autoplay muted loop playsinline class="centered-video">
            <source src="{{ '/assets/videos/cool_crypto.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
    <p>&nbsp;</p>
    <h5>Edge Features</h5>
    <h>Preferential Attachment: Preferential attachment is the principle that a node with more connections is more likely to acquire additional links. This approach assumes that the likelihood of a new connection involving a node x is directly proportional to the number of its existing neighbors. Additionally, the likelihood of two nodes, x and y, forming a co-authorship connection is related to the product of their respective collaborator counts.
    Discussion: The preferential attachment scores for the connected pairs can have very large values because we have a very connected and sparse graph. However, some nodes have a very high degree, resulting in large values (x_value range). In contrast, the preferential attachment scores for unconnected pairs are significantly smaller. This is due to the fact that these unconnected nodes, lacking a direct link, generally have less common neighbors, reducing the likelihood of a connection (under the preferential attachment mechanism). This difference highlights the impact of common neighbors on connection probability and underscores the structural differences between connected and unconnected pairs in the network.</h>
    <br>
    <p>&nbsp;</p>
    <img src="{{ '/assets/img/prefAttachment_dark.png' | relative_url }}">
    <p>&nbsp;</p>
    <br>
    <h>Jaccard similarity: The Jaccard's coefficient is a commonly used similarity metric in information retrieval. It measures the probability that both x and y have a feature f, knowing that x or y has the feature f (which is randomly selected). In our case, the features are the neighbors. It is defined as the size of the intersection divided by the size of the union of the sets.
    Discussion: Below we compare the Jaccard's coefficients for both connected and unconnected node pairs. As expected, the Jaccard coefficient values are higher for connected node pairs, as the likelihood of sharing a neighbor increases when nodes are directly connected.</h>
    <br>
    <p>&nbsp;</p>
    <img src="{{ '/assets/img/Jaccard_dark.png' | relative_url }}">
    <p>&nbsp;</p>
    <br>
    <h>Adamic adar index: To determine how closely two personal home pages are linked, Adamic and Adar examine their common features. Unlike a simple count of these shared features, this index weighs the contribution of each distinctive or less frequent feature by the inverse logarithm of its degree, assigning more weight to rarer features to measure the similarity between entities.
    Discussion: We observed the differences between connected and unconnected pairs of nodes. As expected, the values for connected pairs of nodes are larger than those for unconnected pairs of nodes because there is a greater likelihood of shared connections or features when nodes are directly linked.</h>
    <br>
    <p>&nbsp;</p>
    <img src="{{ '/assets/img/adamicadar_dark.png' | relative_url }}">
    <p>&nbsp;</p>
    <br>
    <h5>Graph Features</h5>
    <br>
    <h>Node2Vec: Node2Vec is an algorithm designed to create vector representations (embeddings) of nodes in a network by simulating biased random walks. This allows for capturing both local neighborhood structures and global network relationships. Node2Vec strikes a balance between breadth-first (BFS) and depth-first (DFS) strategies, enabling the embeddings to capture both homophilic (similar nodes connected) and structural equivalences (nodes playing similar roles in different parts of the graph).
    <p>&nbsp;</p>
    <h1>Data's Finale</h1>
    <p>Talk about what happend to our data after connections</p>
    <p>&nbsp;</p>
    <h1>Thank you for discovering my story :) </h1>
    <p>&nbsp;</p>
    <div class="video-container">
        <video autoplay muted loop playsinline class="centered-video">
            <source src="{{ '/assets/videos/creepy_head.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>
</div>

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
