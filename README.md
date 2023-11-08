<html>
<head>
<title> My First Page</title>

<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sofia">

<style>
#hello_image{

   position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);

 -webkit-filter: drop-shadow(5px 5px 5px #4682B4);
  filter: drop-shadow(5px 5px 5px #4682B4);
}

body{
background-color: rgba(173, 216, 230, 0.5);
}

.container {
  text-align: center;
  color: magenta;
 text-shadow: 0 0 3px #FF0000, 0 0 5px #0000FF;
}

.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}


#demo {
  position: absolute;
  top: 10%;
  left: 50%;
  transform: translate(-50%, -50%);
 font-family: "Sofia", sans-serif;
font-size: 30px;
color: blue;
}

.rotate {
  animation: rotation 18s infinite linear;
}

@keyframes rotation {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(359deg);
  }
}


</style>
<script>


var btn =document.getElementById('hello_world');

var flag=false;

function playAudio(url) {
 
if (!flag){
  var audio = new Audio(url);

  
  audio.loop=true;
  audio.play();
  flag=true;}



}
</script>
</head>
<body>


<div class="container">

<div id="hello_image">
<img src="images/world.png" class="rotate" width=50% height=auto >
</div>

<div id="hello_world">
<div class="centered"> 
<h1 onclick="playAudio('images/song.mp3')">Hello, World !</h1>
</div>
</div>

</div>

<p id="demo"></p>
<script>

document.getElementById("hello_image").addEventListener("click", function() {
  document.getElementById("demo").innerHTML = "Happy New Year";
});
</script>

</body>
</html>
