<template>
  <div>
    <div class="container">

        <h1 class="title">Bienvenid</h1>
        <h1 id="x">x</h1>

    </div>

    
    <div class="container_bio">
        <div class="img_bio">
          <img class="yo" src="../static/yo.png" />
        </div>
        <h2 id="saludo">Hola!</h2>
        <style type="text/css">
          #info_belen {
            opacity: 0;
            -webkit-transform: scale(0.9);
              -moz-transform: scale(0.9);
                -ms-transform: scale(0.9);
                -o-transform: scale(0.9);
                    transform: scale(0.9);
            -webkit-transition: all 1s ease-in-out;
              -moz-transition: all 1s ease-in-out;
                -ms-transition: all 1s ease-in-out;
                -o-transition: all 1s ease-in-out;
                    transition: all 1s ease-in-out;
          }
          #info_belen.visible {
            opacity: 1;
            -webkit-transform: none;
              -moz-transform: none;
                -ms-transform: none;
                -o-transform: none;
                    transform: none;
          }
        </style>
        <div class="info_bio">
          <p id="info_belen">
            <br>Mi nombre es Belén Oliva y soy estudiante de diseño gráfico en Madrid, aunque soy natural de Granada.
            <br>En este portfolio se encuentran algunos de los trabajos que he ido seleccionando a lo largo de los años cursados en la escuela. Todos ellos están organizados por orden cronológico.
            <br>Como estoy empezando en este camino, no tengo mucha variedad en cuanto a trabajos. Aún así, espero que les guste.
          </p>
        </div>

    </div>
    <div class="container1">
        <span id="animate_filmin">FILMIN</span>
        
    </div>
    <div class="container1_1">
      <video  class="video" src="../assets/intro.mp4" autoplay controls></video>
      
    </div>

    <div class="container1_2">
      <img class="mockup1" src="../static/filmin_pc.jpg" />
      <img class="mockup2" src="../static/filmin_movil.jpg" />
    </div>
        
    <div class="container2">
        <span id="animate1">Vive Madrid, Madrid Vive</span>
        
    </div>
    <div class="container2_1">
      <div class="mupis">
          <img class="bolso" src="../static/bolso.jpg" />
          <img class="camiseta" src="../static/camiseta.jpg" />
        </div>
    </div>
    <div class="container2_2">
      <div class="mupis_madrid">
          <img class="mupi1" src="../static/mupi1.jpg" />
          <img class="mupi2" src="../static/mupi2.jpg" />
          <img class="mupi3" src="../static/mupi3.jpg" />
        </div>
    </div>

    <div class="container3">
        <span id="animate2">Mermeladas Hacendado</span>
    </div>
    <div class="container3_1">
      <div class="mermeladas">
          <img class="mermelada1" src="../static/mermelada1.jpg" />
          <img class="mermelada2" src="../static/mermelada2.jpg" />
          <img class="mermelada3" src="../static/mermelada3.jpg" />
        </div>
    </div>
    <div class="container3_2">
      <div class="confituras">
          <img class="confitura1" src="../static/confitura1.jpg" />
          <img class="confitura2" src="../static/confitura2.jpg" />
        </div>
    </div>

     <div class="container4">
        <span id="animate3">Portada Libro</span>
    </div>
    <div class="container4_1">
      <div class="mockup_libro">
          <img class="libro" src="../static/libro.png" />
        </div>
    </div>

    <div class="container_final">
      <h1 class="title">Gracias</h1>
      <h1 id="exc">!</h1>
    </div>

    <div class="container_info">
      <div class="info_final">
        <p class="contacto"> belenolijea@hotmail.es</p>
        <p class="telefono">660382937</p>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  mounted(){


    const controller = new this.$scrollmagic.Controller();

    
		// build scene
    new this.$scrollmagic.Scene({
							triggerElement: ".info_bio",
							triggerHook: 0.9, // show, when scrolled 10% into view
							duration: "80%", // hide 10% before exiting view (80% + 10% from bottom)
							offset: 50 // move trigger to center of element
						})
						.setClassToggle("#info_belen", "visible") // add class to reveal
						//.addIndicators() // add indicators (requires plugin)
						.addTo(controller);


    // var scene = new this.$scrollmagic.Scene({ triggerElement: '.info_bio', duration: 100 })
    //   .setPin("#info_belen")
    //   .addTo(controller);


    var scene1 =new this.$scrollmagic.Scene({
							triggerElement: ".container"
						})
						.setTween("#x", { rotation: 360, duration: 300}) // trigger a TweenMax.to tween
						//.addIndicators({name: "1 (duration: 0)"}) // add indicators (requires plugin)
						.addTo(controller);


		var scene2 =new this.$scrollmagic.Scene({
							triggerElement: ".container_bio"
						})
						.setTween("#saludo", 0.5, { scale: 1.5}) // trigger a TweenMax.to tween
						//.addIndicators({name: "1 (duration: 0)"}) // add indicators (requires plugin)
						.addTo(controller);

    var scene3 = new this.$scrollmagic.Scene({ triggerElement: '.container1' })
      // trigger a TweenMax.to tween
      .setTween("#animate_filmin", 0.5, { scale: 2.5,  yoyo: true})
      .addTo(controller);

    var scene4 = new this.$scrollmagic.Scene({ triggerElement: '.container2' })
      // trigger a TweenMax.to tween
      .setTween("#animate1", 0.5, { scale: 2.5,  yoyo: true})
      .addTo(controller);

    var scene5 = new this.$scrollmagic.Scene({ triggerElement: '.container3'})
      // trigger a TweenMax.to tween
      .setTween("#animate2", 0.5, { scale: 2.5, yoyo: true})
					//.addIndicators() // add indicators (requires plugin)
					.addTo(controller);

    var scene6 = new this.$scrollmagic.Scene({ triggerElement: '.container4'})
      // trigger a TweenMax.to tween
      .setTween("#animate3", 0.5, { scale: 2.5, yoyo: true})
					//.addIndicators() // add indicators (requires plugin)
					.addTo(controller);
    
    var scene7 =new this.$scrollmagic.Scene({
							triggerElement: ".container_final"
						})
						.setTween("#exc", { rotation: 360, duration: 300}) // trigger a TweenMax.to tween
						//.addIndicators({name: "1 (duration: 0)"}) // add indicators (requires plugin)
						.addTo(controller);

  }
}
</script>

<style lang="scss">

//CONTENEDORES

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: #48bee2;
}

.container_bio{
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  align-items: center;
  
 
}
.container1 {
  padding: 10rem 10rem 5rem 10rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container1_1 {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container1_2 {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
.container2 {
  padding: 10rem 10rem 5rem 10rem;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
.container2_1{
  display: flex;
  justify-content: center;
  align-items: center;
}
.container2_2{
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;

}

.container3 {
  padding: 10rem 10rem 5rem 10rem;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.container3_1{
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.container3_2{
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.container4 {
 padding: 10rem 10rem 5rem 10rem;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.container4_1{
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
#saludo{
  margin-left: 2rem;
  color: white;
  font-size: 80px;
  justify-content: center;
  letter-spacing: 1px;
}
.info_bio{
  color:  #232323;
  justify-content: flex-end;
  margin-left: 9rem;
}

.video{
  width: 53rem;
}
.container_final{
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: #48bee2;
}
.container_info{
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-color: #48bee2;
}


//TITULO-SUBTITULOS
.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 200px;
  color: white;
  letter-spacing: 1px;
}
#x{
   font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 200px;
  color: white;
  letter-spacing: 1px;

}

#exc{
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 200px;
  color: white;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #ffd3b4;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
#animate1{
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 25px;
  font-weight: bolder;
}
#animate2{
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 25px;
  font-weight: bolder;
}

#animate_filmin{
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 25px;
  font-weight: bolder;
}
#animate3{
  
  font-size: 25px;
  font-weight: bolder;
}

.info_final{
  font-size: 20px;
  color: white;
  margin: 4rem;
}


//ESTILOS ANIMACIONES
#animate_filmin{
  color: #073963;
}
#animate1{
  color: #1768ac;
}
#animate2{
  color: #073963;
}

#animate3{
  color: #1768ac;
}

//IMAGENES
.img{
  height: 100%;
  width: 100%;
  object-fit: cover;
}

.mupi1{
  width: 27rem;
}

.mupi2{
  width: 27rem;
}
.mupi3{
  width: 27rem;
}

.img_bio{
  width: 10rem;
}
.yo{
  width: 40rem;
}
.mockup1{
  width: 660px;
}
.mockup2{
  width: 360px;
}
.bolso{
  width: 40.5rem;
}
.camiseta{
  width: 40.5rem;
}

.mermelada1{
  width: 25rem;
}
.mermelada2{
  width: 25rem;
}
.mermelada3{
  width: 25rem;
}
.confitura2{
  width: 35rem;
}
.confitura1{
  width: 35rem;
}

.libro{
  width: 70rem;
  margin-bottom: 4rem;
}


</style>