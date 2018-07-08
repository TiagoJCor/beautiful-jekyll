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

DIVIDER

<html>
<head>
<style>
* {
    box-sizing: border-box;
}

.column {
    float: left;
    width: 50.0%;
    padding: 5px;
}

/* Clearfix (clear floats) */
.row::after {
    content: "";
    clear: both;
    display: table;
}

.container { 
  width: 50%
}

.overlay {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: .5s ease;
  background-color: #008CBA;
}


.column:hover .overlay {
  opacity: 1;
}

.text {
  color: white;
  font-size: 20px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  text-align: center;
}
</style>
</head>
<body>

<div class="row">
  <div class="column">
           <img src="/img/columbia_campus.jpg" alt="Snow" style="width:100%">
              <div class="overlay">
                <div class="text">Hello World1</div>
              </div>
           </div>
  </div>
  <div class="column">
           <img src="/img/columbia_campus.jpg" alt="Snow2" style="width:100%">
              <div class="overlay">
                <div class="text">Hello World2</div>
              </div>
       </div>
  </div>
  
  
</div>

</body>
</html>
