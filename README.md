<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Slides</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <main>
        <h1>SlideShow</h1>
        <img class="slideshow" width="600" height="400"/>
    </main>
    <script src="script.js"></script>
</body>
</html>


//css 

body {
    background-color: darkblue;
}
main {
    width: 100%;
    height: 100hv;
    align-items: center;
    justify-content: center;
    display: flex;
    flex-direction: column;
}
h1 {
    text-align: center;
    color: #aa0000;
}

img{

    border-radius: 20px;
}

//JavaScript

var slide = document.querySelector('.slideshow');
var imagens = [
      'chinelo1.jpg',
      'chinelo2.jpg',
      'chinelo3.jpg',

];
var time = 2000;
var count = 0;

function moveSlideShow(){
    slide.src = imagens[count];

    if(count < imagens.length - 1){
        count++;
} else {
        count = 0;
   }

    setTimeout("moveSlideShow()", time);

   }

window.onload = moveSlideShow;
