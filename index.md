---
layout: home
title: "Collectif Metisser"
subtitle: "A Data Story of Connected Nodes <33"
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
    <h></h>

    <img src="{{ '/assets/img/degree_distribution.png' | relative_url }}">
    
    <h1>Data's feature Engineering</h1>
    <h>To train the model, we introduce a set of handcrafted features tailored to the context of link prediction. These features are selected based on the project's aim and the statistical analysis conducted above. They are intended to be the most relevant for achieving effective link creation. Some of the methods are discussed in the paper "The Link Prediction Problem for Social Networks", by Nowell et al. https://www.cs.cornell.edu/home/kleinber/link-pred.pdf</h>

    <h5>Node Features</h5>
    <h>PageRank algorithm: This algorithm ranks nodes based on their importance in the network, determined by the structure of incoming links. The basic idea is that a node with a higher PageRank is more influential because it receives more incoming connections from other important nodes.</h>

    <div style="display: flex; align-items: center; justify-content: center; gap: 20px; margin-top: 20px; margin-bottom: 40px;">
    <img src="{{ '/assets/img/PageRank.png' | relative_url }}" alt="PageRank Algorithm" style="max-width: 45%; height: auto;">
    <img src="{{ '/assets/img/EigenVectorCentrality.png' | relative_url }}" alt="Eigenvector Centrality" style="max-width: 45%; height: auto;">
    </div>

    <h>Eigenvector Centrality: This is a measure of a node's influence within a network, where connections to highly influential nodes contribute more to a node's score than connections to less influential ones.</h>

    <h>Now, we compare the number of common neighbors between two nodes x and y. Two nodes with a higher number of common neighbors have a higher probability to be linked in the future.</h>

    <img src="{{ '/assets/img/distr_common_neighbors.png' | relative_url }}">
    <br>
    <h>Cosine similarity between Text Embeddings: Cosine similarity is a measure of the resemblance between two vectors that represent word or text embeddings. The larger the angle between these vectors, the smaller the resemblance, and the smaller the cosine similarity. We compare the cosine similarity distribution for article titles and descriptions between unconnected and connected nodes. To avoid too large computational cost, we use a subset of our unconnected nodes.</h>
    <br>
    <img src="{{ '/assets/img/distributionCosine.png' | relative_url }}">
    <br>
    <h>Below we compare the cosine similarity between titles and descriptions of connected and unconnected node pairs. As expected, unconnected cases have smaller values.</h>
    <br>
    <img src="{{ '/assets/img/boxPlotCosine.png' | relative_url }}">
    <br>
    <h>The probability of being connected according to the cosine similarity distributions can be calculated and represented here below.</h>
    <br>
    <img src="{{ '/assets/img/connectionProba.png' | relative_url }}">
    <br>
    <h1>Data's Finale</h1>
    <p>Talk about what happend to our data after connections</p>

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
