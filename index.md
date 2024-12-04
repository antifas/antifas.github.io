---
title:
layout: page
feature_text:
feature_image: "imgs/banda.jpg"
aside: false
---

<script type="text/javascript" src="//ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js">
</script>
       

<audio id="player" controls>
  <source src="assets/Arte/01-31 de janeiro.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

<ul id="playlist">
<li class="selected" data-ogg="assets/Arte/01-31 de janeiro.mp3">31 de janeiro</li>  
<li data-ogg="assets/Arte/02-Pra quem o sol nasce.mp3">Pra quem o sol nasce</li>  
<li data-ogg="assets/Arte/03-Maconha.mp3">Maconha</li>  
<li data-ogg="assets/Arte/04-Davi e golias.mp3">Davi e golias</li>  
<li data-ogg="assets/Arte/05-A arte de não fazer sentido.mp3">A arte de não fazer sentido</li>  
<li data-ogg="assets/Arte/06-minas gerais.mp3">minas gerais</li>  
<li data-ogg="assets/Arte/07-1811.mp3">1811</li>  
<li data-ogg="assets/Arte/08-se n gosta de mim.mp3">se n gosta de mim</li>  
<li data-ogg="assets/Arte/09-Ze qualquer.mp3">Ze qualquer</li>  
<li data-ogg="assets/Arte/10-15 segundos.mp3">15 segundos</li>  
</ul>

<button id="stop">Play/Pause</button>
<button id="next" onclick="playNext()" >Next</button>
<button id="previous" onclick="playPrevious()">Previous</button>

<script>

var _player = document.getElementById("player"),
    _playlist = document.getElementById("playlist"),
    _stop = document.getElementById("stop");

// functions
function playlistItemClick(clickedElement) {
    var selected = _playlist.querySelector(".selected");
    if (selected) {
        selected.classList.remove("selected");
    }
    clickedElement.classList.add("selected");

    _player.src = clickedElement.getAttribute("data-ogg");
    _player.play();
}

 function playNext() {
    var selected = _playlist.querySelector("li.selected");
    if (selected && selected.nextElementSibling) {
        playlistItemClick(selected.nextElementSibling);
    }
}
 function playPrevious() {
    var selected = _playlist.querySelector("li.selected");
    if (selected && selected.previousElementSibling) {
        playlistItemClick(selected.previousElementSibling);
    }
}

// event listeners
_stop.addEventListener("click", function () {
	if(_player.paused){
    _player.play();
	}else{
	_player.pause();
	}
});

_player.addEventListener("ended", playNext);
_playlist.addEventListener("click", function (e) {
     if (e.target && e.target.nodeName === "LI") {
        playlistItemClick(e.target);
    }
});
</script>

