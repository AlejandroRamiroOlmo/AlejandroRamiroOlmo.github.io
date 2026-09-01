---
layout: splash
title: ""
permalink: /proyectos/maquina-arcade/
author_profile: false
---

<!-- ========================================== -->
<!-- ESTILOS CSS      -->
<!-- ========================================== -->
<style>
  .section-wrapper-narrow { max-width: 900px; margin: 0 auto 60px auto; padding: 0 20px; }

  /* --- CABECERA OSCURA --- */
  .project-hero-tags { display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; margin-top: 18px; }
  .project-tag {
    background: transparent; border: 1.5px solid #00ffcc; color: #00ffcc;
    padding: 6px 14px; border-radius: 20px; font-size: 0.85em; font-weight: 600;
  }

  /* --- TARJETAS DE CONTENIDO (fondo claro) --- */
  .content-card {
    background: #ffffff; border: 1px solid #d5dce4; border-radius: 12px;
    padding: 35px 30px; margin-bottom: 30px; box-shadow: 0 4px 15px rgba(0,0,0,0.05);
  }
  .content-card h2 { margin-top: 0; color: #1d3557; border-bottom: 2px solid #0f4c75; padding-bottom: 10px; font-size: 1.3em; }
  .content-card p { color: #495057; font-size: 1.05em; line-height: 1.7; text-align: justify; margin: 0; }
  .content-card p + p { margin-top: 14px; }

  /* --- TABLA DE ESPECIFICACIONES --- */
  .specs-table { width: 100%; border-collapse: collapse; margin-top: 10px; }
  .specs-table th, .specs-table td { padding: 12px 16px; text-align: left; border-bottom: 1px solid #eaeaea; font-size: 0.95em; }
  .specs-table th { background: #021a30; color: #00ffcc; font-weight: 700; text-transform: uppercase; font-size: 0.78em; letter-spacing: 0.5px; }
  .specs-table th:first-child { border-top-left-radius: 8px; }
  .specs-table th:last-child { border-top-right-radius: 8px; }
  .specs-table td:first-child { font-weight: 600; color: #1d3557; width: 35%; }
  .specs-table td { color: #495057; }
  .specs-table tr:last-child td { border-bottom: none; }
  .specs-table tr:hover td { background: #f8fafb; }

  /* --- VÍDEO PRINCIPAL --- */
  .video-feature-wrapper { max-width: 380px; margin: 0 auto; }
  .video-feature-frame {
    position: relative; width: 100%; aspect-ratio: 9 / 16;
    border-radius: 12px; overflow: hidden; border: 2px solid #0f4c75;
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
  }
  .video-feature-frame iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0; }

  /* --- GALERÍA: TIRA CON SCROLL HORIZONTAL --- */
  .gallery-wrapper { position: relative; display: flex; align-items: center; gap: 12px; }
  .gallery-strip {
    display: flex; gap: 16px; overflow-x: auto; padding-bottom: 14px; scroll-behavior: smooth;
    scroll-snap-type: x mandatory; -webkit-overflow-scrolling: touch; flex: 1;
  }
  .gallery-item {
    flex: 0 0 auto; width: 260px; height: 260px; border-radius: 10px; overflow: hidden;
    border: 2px solid #0f4c75; scroll-snap-align: start; transition: 0.3s;
  }
  .gallery-item:hover { border-color: #00ffcc; box-shadow: 0 10px 20px rgba(0,0,0,0.15); }
  .gallery-item img { width: 100%; height: 100%; object-fit: cover; display: block; cursor: pointer; transition: transform 0.3s; }
  .gallery-item img:hover { transform: scale(1.03); }
  .gallery-item iframe, .gallery-item video { width: 100%; height: 100%; border: 0; display: block; object-fit: cover; }
  .gallery-strip::-webkit-scrollbar { height: 8px; }
  .gallery-strip::-webkit-scrollbar-track { background: #f1f1f1; border-radius: 10px; }
  .gallery-strip::-webkit-scrollbar-thumb { background: #0f4c75; border-radius: 10px; }
  .gallery-strip::-webkit-scrollbar-thumb:hover { background: #00ffcc; }

  .gallery-arrow {
    flex-shrink: 0; width: 44px; height: 44px; border-radius: 50%;
    background: #021a30; border: 2px solid #0f4c75; color: #00ffcc;
    display: flex; align-items: center; justify-content: center;
    cursor: pointer; transition: 0.3s; font-size: 1.1em;
  }
  .gallery-arrow:hover { border-color: #00ffcc; box-shadow: 0 0 12px rgba(0,255,204,0.4); }

  /* --- MODAL PARA AMPLIAR IMÁGENES --- */
  .image-modal {
    display: none; 
    position: fixed;
    z-index: 9999;
    padding-top: 40px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.85); 
    backdrop-filter: blur(4px); 
  }
  .image-modal-content {
    margin: auto;
    display: block;
    max-width: 95%;
    max-height: 90vh; 
    object-fit: contain;
    border-radius: 8px;
    box-shadow: 0 5px 25px rgba(0,0,0,0.5);
  }
  .close-modal {
    position: absolute;
    top: 15px;
    right: 35px;
    color: #f1f1f1;
    font-size: 40px;
    font-weight: bold;
    transition: 0.3s;
    cursor: pointer;
  }
  .close-modal:hover,
  .close-modal:focus {
    color: #00ffcc;
    text-decoration: none;
    cursor: pointer;
  }

  /* --- ACCIONES FINALES --- */
  .project-actions { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 20px; margin-top: 10px; }
  .back-link { color: #1d3557; text-decoration: none; font-weight: 600; transition: 0.3s; }
  .back-link:hover { color: #0f4c75; text-decoration: underline; }

  .btn-neon {
    display: inline-block; padding: 12px 25px; border: 2px solid #00ffcc;
    color: #00ffcc !important; text-decoration: none; border-radius: 5px;
    font-weight: bold; transition: 0.3s; font-size: 1em; background: #021a30;
  }
  .btn-neon:hover { background: #00ffcc; color: #021a30 !important; box-shadow: 0 0 15px #00ffcc; }

  @media (max-width: 600px) {
    .gallery-item { width: 190px; height: 190px; }
    .gallery-arrow { width: 36px; height: 36px; font-size: 0.95em; }
    .project-actions { justify-content: center; text-align: center; }
  }
</style>

<!-- ========================================== -->
<!-- CABECERA OSCURA -->
<!-- ========================================== -->
<div style="background-color: #1d3557; width: 100vw; position: relative; left: 50%; right: 50%; margin-left: -50vw; margin-right: -50vw; padding: 70px 1em 50px 1em; margin-bottom: 40px; box-shadow: 0 4px 15px rgba(0,0,0,0.2);">
  <div style="max-width: 900px; margin: 0 auto; text-align: center;">
    <h1 style="color: #ffffff; border-bottom: none; margin: 0;">Máquina Arcade</h1>
    <div class="project-hero-tags">
      <span class="project-tag">Proyecto Personal</span>

    </div>
  </div>
</div>

<!-- ========================================== -->
<!-- CUERPO CLARO -->
<!-- ========================================== -->
<div class="section-wrapper-narrow">

  <div class="content-card">
    <h2>Objetivo</h2>
    <p>
      Diseñar y construir una máquina Arcade completa desde cero, integrando una estructura física a medida con un software de juego personalizado y tematizado.
    </p>
  </div>

  <div class="content-card">
    <h2>Especificaciones Técnicas</h2>
    <table class="specs-table">
      <thead>
        <tr><th>Característica</th><th>Detalle</th></tr>
      </thead>
      <tbody>
        <tr><td>Estructura</td><td>Mueble de madera a medida, diseño en SolidWorks</td></tr>
        <tr><td>Control</td><td>Botonera y Joystick arcade controlados por ESP32</td></tr>
        <tr><td>Software</td><td>Programado en C++ usando Arduino IDE</td></tr>
        <tr><td>Pantalla</td><td>Guition JC4728W453 ESP32S3. (480x272 pixels)</td></tr>
        <tr><td>Tiempo de desarrollo</td><td>6 meses</td></tr>
      </tbody>
    </table>
  </div>


  <div class="content-card">
    <h2>Galería</h2>
    <div class="gallery-wrapper">
      <button class="gallery-arrow" aria-label="Anterior" onclick="scrollGallery(this, -1)"><i class="fas fa-chevron-left"></i></button>

      <div class="gallery-strip">
        <div class="gallery-item">
          <video src="/assets/videos/Maquina_Arcade_web.mp4" autoplay loop muted playsinline></video>
        </div>
        <div class="gallery-item"><img src="/assets/images/maqueta_madera.jpeg" alt="Máquina Arcade - vista general" onclick="abrirModal(this.src)"></div>
        <div class="gallery-item"><img src="/assets/images/collage.jpeg" alt="collage fotos mapa" onclick="abrirModal(this.src)"></div>
        <div class="gallery-item"><img src="/assets/images/maquina.jpeg" alt="Máquina Arcade - detalle general" onclick="abrirModal(this.src)"></div>
      </div>

      <button class="gallery-arrow" aria-label="Siguiente" onclick="scrollGallery(this, 1)"><i class="fas fa-chevron-right"></i></button>
    </div>
  </div>

  <div class="content-card">
    <h2>Vídeo del Proyecto</h2>
    <div class="video-feature-wrapper">
      <div class="video-feature-frame">
        <iframe src="https://www.youtube.com/embed/ZXM2ZdQEvQA" title="Máquina Arcade en funcionamiento" allowfullscreen></iframe>
      </div>
    </div>
  </div>

    <!-- ========================================== -->
  <!-- TARJETA: DIAGRAMA DE FLUJO                 -->
  <!-- ========================================== -->
  <div class="content-card">
    <h2>Diagrama de Flujo</h2>
    <p>
      Estructura de la máquina de estados que controla el flujo principal del software, desde el arranque hasta la navegación por los distintos menús y juegos. <em>Haz clic en la imagen para ampliarla.</em>
    </p>
    <img src="/assets/images/diagrama_flujo_arcade.jpeg" alt="Diagrama de flujo de la máquina arcade" onclick="abrirModal(this.src)" style="width: 100%; height: auto; border-radius: 8px; border: 1px solid #d5dce4; margin-top: 15px; cursor: zoom-in; box-shadow: 0 4px 10px rgba(0,0,0,0.05);">
  </div>

    <div class="content-card">
    <h2>Proceso de Desarrollo</h2>
    <p>
      El proyecto arrancó diseñando la temática (Disney Aladdin) y las funcionalidades del programa. Una historia de introducción daría paso al menú principal. Los vídeos, imágenes y sticker usados se programaron en formato .avi, .bmp y .png respectivamente, almacenadas en una tarjeta microSD en la placa de la pantalla. 
    </p>
    <p>
      El software se diseñó como una máquina de estados, controlado por el microcontrolador principal, integrado en la pantalla (ESP32S3). Debido a la falta de GPIOs, un microcontrolador externo se encarga del control de periféricos y se comunica con el principal vía UART.
    </p>
    <p>
      En paralelo se desarrolló la parte electrónica usando ESP32 Wroom externo para gestionar los controles físicos. Tenemos integrado 4 botones de juego, 2 de Pause y Play que dan acceso al menú de pausa durante los juegos, un joystick arcade, un lector de tarjetas RFID y un led emisor IR para control de la tira led.
    </p>
     <p>
      Por último y no menos importante, se diseñó la maqueta en 3D usando Solidworks, con el objetivo puesto en fabricar un mueble que combinase poco volumen pero integrando la disposición de todos los componentes de manera adecuada y accesible para el usuario. Posteriormente se eligió madera de densidad media (DMF) para la construcción y se incluyó decoración como vinilos y poliestireno rígido transparente.
    </p>
  </div>

  <div class="content-card">
    <h2>Resultado y Aprendizajes</h2>
    <p>
      <strong>Resultado:</strong> El resultado de este proyecto es una máquina Arcade 100% operativa y robusta, diseñada y construida desde cero, siendo el reto perfecto para materializar mi formación mecatrónica. Todo empezó en SolidWorks, donde modelé el chasis y los ensamblajes pensando siempre en la viabilidad de su fabricación y en la ergonomía del usuario. Sin embargo, el verdadero hito fue darle vida a ese diseño: programé el software de control y las interfaces gráficas utilizando C++. Logré optimizar la latencia del sistema, garantizando que la comunicación entre el hardware (joysticks y botones) y el software fuera instantánea, resultando en una experiencia de usuario fluida y sin retardos.
    </p>
    <p>
      <strong>Aprendizajes:</strong> Más allá de ver la máquina funcionando, el mayor valor de este proyecto fue darme cuenta de que un encaje perfecto en la pantalla del ordenador no garantiza el éxito en la vida real. Aprendí a base de prueba y error a gestionar tolerancias mecánicas reales, peleando con los materiales físicos para que las pantallas y botoneras encajaran a la perfección. Además, al integrar mecánica, electrónica y software por mi cuenta, desarrollé una mentalidad de troubleshooting muy analítica: cuando el sistema fallaba, aprendí a aislar el problema metódicamente para descubrir si se trataba de un desajuste físico, un falso contacto en el cableado o un error lógico en mi código. Fue un baño de realidad que me enseñó a pensar y resolver problemas como un verdadero ingeniero.
    </p>
  </div>

  <div class="project-actions">
    <a href="https://github.com/AlejandroRamiroOlmo/Aladdin-Arcade-JC4827W543 class="btn-neon" target="_blank" rel="noopener">Ver código en GitHub &rarr;</a>
    <a href="/proyectos/" class="back-link">&larr; Volver a Proyectos</a>
  </div>

</div>

<!-- ========================================== -->
<!-- MODAL INVISIBLE PARA IMÁGENES              -->
<!-- ========================================== -->
<div id="miModalImagen" class="image-modal" onclick="cerrarModal()">
  <span class="close-modal">&times;</span>
  <img class="image-modal-content" id="imagenAmpliada">
</div>

<!-- ========================================== -->
<!-- SCRIPTS DE LA PÁGINA                       -->
<!-- ========================================== -->
<script>
  // Función para abrir la imagen del modal
  function abrirModal(src) {
    document.getElementById("miModalImagen").style.display = "block";
    document.getElementById("imagenAmpliada").src = src;
  }

  // Función para cerrar el modal
  function cerrarModal() {
    document.getElementById("miModalImagen").style.display = "none";
  }

  // Función para mover la galería
  function scrollGallery(btn, direction) {
    const wrapper = btn.closest('.gallery-wrapper');
    const strip = wrapper.querySelector('.gallery-strip');
    const amount = strip.clientWidth * 0.85;
    strip.scrollBy({ left: direction * amount, behavior: 'smooth' });
  }
</script>