<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
  font-family: Arial;
  margin: 0px;
  display: block;
}

* {
  box-sizing: border-box;
}

img {
  vertical-align: middle;
}

/* Position the image container (needed to position the left and right arrows) */
.container {
  position: relative;
}

/* Hide the images by default */
.mySlides {
  display: none;
}

/* Add a pointer when hovering over the thumbnail images */
.cursor {
  cursor: pointer;
}

/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 16px;
  margin-top: -50px;
  color: white;
  font-weight: bold;
  font-size: 20px;
  border-radius: 0 3px 3px 0;
  user-select: none;
  -webkit-user-select: none;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

/* Container for image text */
.caption-container {
  text-align: center;
  background-color: #737373;
  padding: .5px 8px;
  color: white;
}

.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Six columns side by side */
.column {
  float: left;
  width: 16.66%;
}

/* Add a transparency effect for thumnbail images */
.demo {
  opacity: 0.6;
}

.active,
.demo:hover {
  opacity: 1;
}
</style>
<body>

<div class="container">
  <div class="mySlides">
    <div class="numbertext">1 / 6</div>
    <img src="images/demi_2.jpeg" style="width:100%">
  </div>

  <div class="mySlides">
    <div class="numbertext">2 / 6</div>
    <img src="images/demi_1.jpg" style="width:100%">
  </div>

  <div class="mySlides">
    <div class="numbertext">3 / 6</div>
    <img src="images/darius_use.jpg" style="width:100%">
  </div>
    
  <div class="mySlides">
    <div class="numbertext">4 / 6</div>
    <img src="images/darius_4.JPG" style="width:100%">
  </div>

  <div class="mySlides">
    <div class="numbertext">5 / 6</div>
    <img src="images/darius_3.JPG" style="width:100%">
  </div>
    
  <div class="mySlides">
    <div class="numbertext">6 / 6</div>
    <img src="images/darius_2.JPG" style="width:100%">
  </div>
    
  <a class="prev" onclick="plusSlides(-1)">❮</a>
  <a class="next" onclick="plusSlides(1)">❯</a>

  <div class="caption-container">
    <p id="caption"></p>
  </div>

  <div class="row">
    <div class="column">
      <img class="demo cursor" src="images/demi_2.jpeg" style="width:100%" onclick="currentSlide(1)" alt="The golden fried calamari, served with lemons and tartar sauce, is a hit appetizer with customers. Photo by Demetria Osei-Tutu.">
    </div>
    <div class="column">
      <img class="demo cursor" src="images/demi_1.jpg" style="width:100%" onclick="currentSlide(2)" alt=" Moules Marinières, which combines Prince Edward Island mussels with white wine, shallots and garlic parsley, can be ordered alongside quesadillas, which are made with Monterrey cheese, and caramelized onions and your choice of any protein filling. Photo by Demetria Osei-Tutu. ">
    </div>
    <div class="column">
      <img class="demo cursor" src="images/darius_use.jpg" style="width:100%" onclick="currentSlide(3)" alt="One of the most popular dishes, Steak Frites is a black Angus strip steak served with peppercorn sauce. Photo by Darius Johnson.">
    </div>
    <div class="column">
      <img class="demo cursor" src="images/darius_4.JPG" style="width:100%" onclick="currentSlide(4)" alt="The specialty cocktail, Dupont, photographed on the left, combines Grey Goose, Mezcal, lime, grapefruit, cilantro and ginger reduction for a great smoky cocktail. The Frida, served with a tajin rim, combines Herradura, Cointreau, lime, and raspberry to make a fruity, flavorful cocktail. Photo by Darius Johnson.">
    </div>
    <div class="column">
      <img class="demo cursor" src="images/darius_3.JPG" style="width:100%" onclick="currentSlide(5)" alt="This fried ice cream dessert, coated in a thin brioche bread and coconut flakes, is served with fresh fruit. Photo by Darius Johnson.">
    </div>    
    <div class="column">
      <img class="demo cursor" src="images/darius_2.JPG" style="width:100%" onclick="currentSlide(6)" alt="This decadent chocolate lava cake is served with a warm chocolate center and topped with vanilla ice cream and fresh fruit. Photo by Darius Johnson.">
    </div>
  </div>
</div>

<script>
let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("demo");
  let captionText = document.getElementById("caption");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
  captionText.innerHTML = dots[slideIndex-1].alt;
}
</script>
    
</body>
</html>
