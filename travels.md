---
layout: page
title: Travels
---

<html>
<head>
<style>
div.gallery {
    margin: 5px;
    border: 0px;
    float: center;
    width: 50%;
}

div.gallery:hover {
    border: 1px solid #CAEBF2;
}

div.gallery img {
    width: 100%;
    height: auto;
}

div.desc {
    padding: 10px;
    text-align: center;
}
</style>
</head>
<body>

<div class="gallery">
  <a target="_blank" href="/img/bates_campus.jpg">
    <img src="/img/bates_campus.jpg" alt="Tokyo, Japan" width="450" height="300">
  </a>
  <div class="desc">Tokyo, Japan</div>
</div>

<div class="gallery">
  <a target="_blank" href="/img/columbia_campus.jpg">
    <img src="/img/columbia_campus.jpg" alt="Tokyo, Japan" width="450" height="300">
  </a>
  <div class="desc">Kyoto, Japan</div>
</div>


</body>
</html>

<div class="row">
  <div class="column">
    <img src="/img/bates_campus.jpg" alt="Snow" style="width:100%">
  </div>
  <div class="column">
    <img src="/img/bates_campus.jpg" alt="Forest" style="width:100%">
  </div>
  <div class="column">
    <img src="/img/bates_campus.jpg" alt="Mountains" style="width:100%">
  </div>
</div>

.column {
  float: left;
  width: 50%;
  padding: 5px;
}

/* Clear floats after image containers */
.row::after {
  content: "";
  clear: both;
  display: table;
}
