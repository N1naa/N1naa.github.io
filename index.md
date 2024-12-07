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

    <h1>Some music to accompany you through your experience ... </h1>
    <iframe src="https://open.spotify.com/embed/track/YOUR_TRACK_ID" width="300" height="380" frameborder="0" allowtransparency="true" allow="encrypted-media"></iframe>

    <h1>Data's Origin Story</h1>
    <p>Talk about where our data comes from, how it is collected etc.</p>

    <h3>Graphical Statistical Analysis</h3>
    <h>To gain a better understanding of the data, some basics but important characteristics of the graph are computed/displayed. This will help guide us in selecting the most appropriate approach for the next steps. Here is a distribution of common neighbors:</h>

    <iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/4nOOoo9OJbgnTBNHe5b6nD?utm_source=generator&theme=0" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>


    <iframe width="560" height="315" src="https://music.youtube.com/watch?v=xfV8SLbHWYs&si=Jr2P27dUc22_i0iw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


    <h3>Feature Engineering</h3>
    <h>To train the model, we introduce a set of handcrafted features tailored to the context of link prediction. These features are selected based on the project's aim and the statistical analysis conducted above. They are intended to be the most relevant for achieving effective link creation.</h>

    <img src="{{ '/assets/img/distr_common_neighbors.png' | relative_url }}" alt="Image Description">

    <h1>Data's Analysis</h1>
    <p>Talk about our model and metrics</p>

    <h1>Data's Finale</h1>
    <p>Talk about what happend to our data after connections</p>
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
