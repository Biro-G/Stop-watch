# Stop-watch
Another 

<div class="wrapper">
<h1>Stopwatch</h1>
<h2>Birogabby JavaScript Stopwatch</h2>
<p><span id="seconds">00</span>:<span id="tens">00</span></p>
<button id="button-start">Start</button>
<button id="button-stop">Stop</button>
<button id="button-reset">Reset</button>
</div> 



/* Variabes */  
$orange: #ffa600;
$grey:#f3f3f3;
$white: #fff;
$base-color:$orange ;


/* Mixin's */  
@mixin transition {
-webkit-transition: all 0.5s ease-in-out;
-moz-transition: all 0.5s ease-in-out;
transition: all 0.5s ease-in-out;
}
@mixin corners ($radius) {
-moz-border-radius: $radius;
-webkit-border-radius: $radius;
border-radius: $radius; 
-khtml-border-radius: $radius; 
}

body {
background:$base-color;
font-family: "HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif; 
height:100%;
}


window.onload = function () {
  
  var seconds = 00; 
  var tens = 00; 
  var appendTens = document.getElementById("tens")
  var appendSeconds = document.getElementById("seconds")
  var buttonStart = document.getElementById('button-start');
  var buttonStop = document.getElementById('button-stop');
  var buttonReset = document.getElementById('button-reset');
  var Interval ;

  buttonStart.onclick = function() {
    
     clearInterval(Interval);
     Interval = setInterval(startTimer, 10);
  }
  
    buttonStop.onclick = function() {
       clearInterval(Interval);
  }
  

  buttonReset.onclick = function() {
     clearInterval(Interval);
    tens = "00";



 
