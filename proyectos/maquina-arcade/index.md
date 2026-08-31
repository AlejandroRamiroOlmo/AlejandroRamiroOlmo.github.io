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

  /* --- VÍDEO PRINCIPAL (fuera de la galería, formato Shorts vertical) --- */
  .video-feature-wrapper { max-width: 380px; margin: 0 auto; }
  .video-feature-frame {
    position: relative; width: 100%; aspect-ratio: 9 / 16;
    border-radius: 12px; overflow: hidden; border: 2px solid #0f4c75;
    box-shadow: 0 10px 25px rgba(0,0,0,0.15);
  }
  .video-feature-frame iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0; }

  /* --- GALERÍA: TIRA CON SCROLL HORIZONTAL Y FLECHAS --- */
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
  .gallery-item iframe { width: 100%; height: 100%; border: 0; display: block; }
  .gallery-item video { width: 100%; height: 100%; border: 0; display: block; object-fit: cover; }
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
<!-- CABECERA OSCURA — CAMBIA AQUÍ: título y tags -->
<!-- ========================================== -->
<div style="background-color: #1d3557; width: 100vw; position: relative; left: 50%; right: 50%; margin-left: -50vw; margin-right: -50vw; padding: 70px 1em 50px 1em; margin-bottom: 40px; box-shadow: 0 4px 15px rgba(0,0,0,0.2);">
  <div style="max-width: 900px; margin: 0 auto; text-align: center;">
    <h1 style="color: #ffffff; border-bottom: none; margin: 0;">Máquina Arcade</h1>
    <div class="project-hero-tags">
      <span class="project-tag">Diseño Mecánico</span>
      <span class="project-tag">Electrónica</span>
      <span class="project-tag">Software</span>
    </div>
  </div>
</div>

<!-- ========================================== -->
<!-- CUERPO CLARO — CAMBIA AQUÍ: los textos     -->
<!-- ========================================== -->
<div class="section-wrapper-narrow">

  <div class="content-card">
    <h2>Objetivo</h2>
    <p>
      Diseñar y construir una máquina Arcade completa desde cero, integrando una estructura física a medida con un software de juego personalizado y tematizado, pensada para ofrecer una experiencia de usuario cuidada tanto en el hardware como en el software.
    </p>
  </div>

  <div class="content-card">
    <h2>Especificaciones Técnicas</h2>
    <!-- CAMBIA AQUÍ: ajusta filas y datos a tu proyecto real; añade o quita filas según necesites -->
    <table class="specs-table">
      <thead>
        <tr><th>Característica</th><th>Detalle</th></tr>
      </thead>
      <tbody>
        <tr><td>Estructura</td><td>Mueble de madera a medida, diseño en SolidWorks</td></tr>
        <tr><td>Control</td><td>Arduino + botonera arcade y joystick</td></tr>
        <tr><td>Software</td><td>Python, interfaz de juego tematizada</td></tr>
        <tr><td>Pantalla</td><td>[CAMBIA AQUÍ: pulgadas / resolución]</td></tr>
        <tr><td>Tiempo de desarrollo</td><td>[CAMBIA AQUÍ: ej. 3 meses]</td></tr>
      </tbody>
    </table>
  </div>

  <div class="content-card">
    <h2>Proceso de Desarrollo</h2>
    <p>
      El proyecto arrancó con el modelado 3D de la estructura en SolidWorks, definiendo las dimensiones ergonómicas del mueble y la disposición de los componentes internos (pantalla, altavoces, botonera).
    </p>
    <p>
      En paralelo se desarrolló la parte electrónica con Arduino para gestionar los controles físicos, y el software del juego en Python, ajustando la temática visual para que combinara con el diseño físico del mueble.
    </p>
  </div>

  <div class="content-card">
    <h2>Galería</h2>
    <!-- CAMBIA AQUÍ: añade tantos <div class="gallery-item"> como fotos/vídeos quieras -->
    <div class="gallery-wrapper">
      <button class="gallery-arrow" aria-label="Anterior" onclick="scrollGallery(this, -1)"><i class="fas fa-chevron-left"></i></button>

      <div class="gallery-strip">
        <!-- Clip corto en bucle (ej. modelo 3D girando). Duplica este bloque por cada clip nuevo que subas a /assets/videos/ -->
        <div class="gallery-item">
          <video src="/assets/videos/Maquina_Arcade_web.mp4" autoplay loop muted playsinline></video>
        </div>

        <div class="gallery-item"><img src="/assets/images/maquina.png" alt="Máquina Arcade - vista general"></div>
        <div class="gallery-item"><img src="/assets/images/maquina.png" alt="Máquina Arcade - detalle 2"></div>
        <div class="gallery-item"><img src="/assets/images/maquina.png" alt="Máquina Arcade - detalle 3"></div>
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

  <div class="content-card">
    <h2>Resultado y Aprendizajes</h2>
    <!-- CAMBIA AQUÍ: cuenta si funciona, cómo fue la puesta en marcha, y qué mejorarías -->
    <p>
      <strong>Resultado:</strong> [CAMBIA AQUÍ: describe el estado final — funciona correctamente, se probó con usuarios, quedó pendiente de X, etc.]
    </p>
    <p>
      <strong>Aprendizajes:</strong> [CAMBIA AQUÍ: qué aprendiste técnicamente, qué harías distinto si repitieras el proyecto]
    </p>
  </div>

  <!-- CAMBIA AQUÍ: el enlace al repositorio real del proyecto -->
  <div class="project-actions">
    <a href="https://github.com/AlejandroRamiroOlmo" class="btn-neon" target="_blank" rel="noopener">Ver código en GitHub &rarr;</a>
    <a href="/proyectos/" class="back-link">&larr; Volver a Proyectos</a>
  </div>

</div>

<script>
  function scrollGallery(btn, direction) {
    const wrapper = btn.closest('.gallery-wrapper');
    const strip = wrapper.querySelector('.gallery-strip');
    const amount = strip.clientWidth * 0.85;
    strip.scrollBy({ left: direction * amount, behavior: 'smooth' });
  }
</script>