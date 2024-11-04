# Motion-cut
➢ HTML Code :

<!DOCTYPE html>

<html lang="en">

<head>

 <meta charset="UTF-8">

 <meta name="viewport" content="width=device-width, initial-scale=1.0">

 <title>Image Slider</title>

 <link rel="stylesheet" href="styles.css">

</head>

<body>

 <div class="slider">

 <div class="slides">

 <div class="slide"><img src="image1.jpg" alt="Image 1"></div>

 <div class="slide"><img src="image2.jpg" alt="Image 2"></div>

 <div class="slide"><img src=" image3.jpg " alt="Image 3"></div>

 <div class="slide"><img src=" image4.jpg " alt="Image 4"></div>

 </div>

 <div class="navigation">

 <button class="prev" onclick="prevSlide()">❮</button>

 <button class="next" onclick="nextSlide()">❯</button>

 </div>

 </div>

 

 <script src="script.js"></script>

 <div class="thumbnails">

 <img src=" image1.jpg " onclick="showSlide(0)">

 <img src=" image2.jpg " onclick="showSlide(1)">

 <img src=" image3.jpg " onclick="showSlide(2)">

 <img src=" image4.jpg " onclick="showSlide(3)">

 </div>

</body>

</html>➢ CSS Code :

body {

 display: flex;

 justify-content: center;

 align-items: center;

 height: 100vh;

 margin: 0;

 background: rgb(255, 255, 255);

 font-family: Arial, sans-serif;

}

.slider {

 width: 80%;

 max-width: 800px;

 position: relative;

 overflow: hidden;

}

.slides {

 display: flex;

 transition: transform 0.5s ease-in-out;

}

.slide {

 min-width: 100%;

 box-sizing: border-box;

}

.slide img {

 width: 100%;

 display: block;

}

.navigation {position: absolute;

 top: 50%;

 width: 100%;

 display: flex;

 justify-content: space-between;

 transform: translateY(-50%);

}

.navigation button {

 background: rgba(0,0,0,0.5);

 color: white;

 border: none;

 padding: 10px;

 cursor: pointer;

 transition: background 0.3s ease;

}

.navigation button:hover {

 background: rgba(0,0,0,0.7);

}

.thumbnails {

 display: flex;

 justify-content: center;

 margin-top: 10px;

}

.thumbnails img {

 width: 50px;

 margin: 0 5px;

 cursor: pointer;

 transition: transform 0.3s ease;

}

.thumbnails img:hover {

 transform: scale(1.1);

➢ Java script :

let currentIndex = 0;

const slides = document.querySelectorAll('.slide');

function showSlide(index) {

 if (index >= slides.length) currentIndex = 0;

 if (index < 0) currentIndex = slides.length - 1;

 const offset = -currentIndex * 100;

 document.querySelector('.slides').style.transform = translateX($,ts(1190));

}

function nextSlide() {

 currentIndex++;

 showSlide(currentIndex);

}

function prevSlide() {

 currentIndex--;

 showSlide(currentIndex);

}

setInterval(nextSlide, 3000); // Auto-slide every 3 seconds
