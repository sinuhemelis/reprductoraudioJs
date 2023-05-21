Reproductor de audios JS con lista de reproduccion

PD: Google chrom. amo de la oscuridad. te hace dar mil vueltas con la reproducción automatica de multimedia con SONIDO. (osea sin sonido todo bien). buscando y buscando unos chinos dieron con la solucion
Solucion:
Google te propone hacer una "PROMESA"

<script>
  var playPromise = audio.play();
 
  if (playPromise !== undefined) {
    playPromise.then(_ => {
      // Automatic playback started!
      // Show playing UI.
      // We can now safely pause video...
      video.pause();
    })
    .catch(error => {
      // Auto-play was prevented
      // Show paused UI.
    });
}

</script>

Son puras patrañas...

Código que funciona:
<script>

        audio.src = song;
        urlsong = song;
        audio.load();
        setTimeout(function(){
        	audio.play();
        	}, 0);
 </script>
 
 
 Saludos, y google chrom vete al infierno.
