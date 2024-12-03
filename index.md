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

Antifas! é uma força incendiária que surge dos subterrâneos do cenário underground, para desafiar e confrontar. Com Z de Deus no baixo e voz, Flávio Schiavoni nas guitarras, voz e percussão, e Fábio Almeida na bateria, se tornam uma trindade sonora do caos.


Suas músicas são como socos no estômago, expressando raiva e indignação contra as injustiças sociais. Faixas como "Eu me demito", "Homofobia é vômito no chão", "Help Brazil" e "Minas gerais" são hinos de resistência e denúncia.


O som dos Antifas! é uma mistura furiosa de crossover metal e punk, criando uma energia intensa que faz o público se contorcer e os tímpanos explodirem. Suas letras cortantes e críticas sociais são um grito de guerra contra o sistema opressor.


A energia visceral e a atitude provocadora dos Antifas! são uma faísca em meio à apatia musical, incendiando corações e mentes com sua música enraivecida. Prepare-se para ser impactado e desafiado pela avalanche sonora da Antifas!.

<cite>ChatGPT</cite>

