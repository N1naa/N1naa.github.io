---
layout: home
title: "Collectif Metisser"
subtitle: "A Data Story of Connected Nodes <333"
---

<div class="main-content">

    <div class="video-container">
        <video autoplay muted loop playsinline class="centered-video">
            <source src="{{ '/assets/videos/3130284-uhd_3840_2160_30fps.mp4' | relative_url }}" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </div>

    <h1>Data's Origin Story</h1>
    <p>This is the static content I want to display in the middle of my page.</p>

    <h1>Data's Analysis</h1>
    <p>This is the static content I want to display in the middle of my page.</p>

    <h1>Data's Finale</h1>
    <p>This is the static content I want to display in the middle of my page.</p>
</div>

<style>
  /* Center the video container */
  .video-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 30px;  /* Add space between video and content */
  }

  /* Limit the video's size */
  .centered-video {
    width: 100%;      /* Allow the video to take the full width of its container */
    max-width: 1000px; /* Limit the width to 1000px, adjust if necessary */
    height: auto;    /* Keep aspect ratio intact */
  }
</style>