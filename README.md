---
layout: home
title: Home
nav_exclude: false
permalink: /:path/
seo:
  type: Course
  name: CS 171
---

<style>
  .row {
    display: flex;
    justify-content: space-between; /* Positions children at the start and end of the container */
    align-items: center; /* Vertically centers the items in the row */
  }

  .column {
    flex: 1; /* Allows columns to grow and shrink as needed */
    padding: 10px;
    margin: 10px; /* Adds margin around each column */
  }

  .text-container {
    text-align: left; /* Aligns text to the left */
    display: flex;
    justify-content: flex-start; /* Aligns the text container to the left */
  }

  .image-container {
    display: flex;
    justify-content: flex-end; /* Aligns the image to the right of the column */
  }

  .image-container img {
    max-width: 60%; /* Sets maximum width of the image */
    height: auto; /* Keeps the aspect ratio of the image */
  }

  /* Responsive layout for smaller screens */
  @media screen and (max-width: 600px) {
    .row {
      flex-direction: column;
    }

    .text-container, .image-container {
      justify-content: center; /* Centers content on smaller screens */
      text-align: center;
    }

    .column, .image-container img {
      max-width: 100%;
    }
  }

  .header-container {
    display: none; /* Hides the header container */
  }
</style>

<div class="row">
  <div class="column text-container">
     <h1>Welcome to CS 171!</h1>
  </div>
  <div class="column image-container">
    <img src="assets/images/alicebob.png" alt="Alice and Bob">
  </div>
</div>

{% for module in site.modules %}
{{ module }}
{% endfor %}
