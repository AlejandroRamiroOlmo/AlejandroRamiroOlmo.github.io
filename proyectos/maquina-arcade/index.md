---
layout: splash
title: ""
permalink: /proyectos/maquina-arcade/
author_profile: false
---

<!-- ============================================================ -->
<!-- PLANTILLA DE PROYECTO — instrucciones de uso                 -->
<!-- Para crear un proyecto nuevo:                                -->
<!-- 1. Duplica este archivo y cámbiale el nombre (ej. estacion-industrial.md) -->
<!-- 2. Cambia el "permalink" de arriba a la URL del nuevo proyecto -->
<!-- 3. Edita solo las zonas marcadas con "CAMBIA AQUÍ" — el resto -->
<!--    (estilos, estructura) es igual para todos los proyectos    -->
<!-- ============================================================ -->

<!-- ========================================== -->
<!-- ESTILOS CSS (no hace falta tocar esto)     -->
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

  /* --- GALERÍA: TIRA CON SCROLL HORIZONTAL --- */
  .gallery-strip {
    display: flex; gap: 16px; overflow-x: auto; padding-bottom: 14px;
    scroll-snap-type: x mandatory; -webkit-overflow-scrolling: touch;
  }
  .gallery-strip img {
    flex: 0 0 auto; width: 320px; height: 220px; object-fit: cover;
    border-radius: 10px; border: 2px solid #0f4c75; scroll-snap-align: start;
    transition: 0.3s; cursor: pointer;
  }
  .gallery-strip img:hover { border-color: #00ffcc; transform: scale(1.02); box-shadow: 0 10px 20px rgba(0,0,0,0.15); }
  .gallery-strip::-webkit-scrollbar { height: 8px; }
  .gallery-strip::-webkit-scrollbar-track { background: #f1f1f1; border-radius: 10px; }
  .gallery-strip::-webkit-scrollbar-thumb { background: #0f4c75; border-radius: 10px; }
  .gallery-strip::-webkit-scrollbar-thumb:hover { background: #00ffcc; }

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
    .gallery-strip img { width: 260px; height: 180px; }
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
    <!-- CAMBIA AQUÍ: añade tantas <img> como fotos quieras, la tira se desplaza sola -->
    <div class="gallery-strip">
      <img src="/assets/images/maquina.png" alt="Máquina Arcade - vista general">
      <img src="/assets/images/maquina.png" alt="Máquina Arcade - detalle 2">
      <img src="/assets/images/maquina.png" alt="Máquina Arcade - detalle 3">
    </div>
  </div>

  <!-- CAMBIA AQUÍ: el enlace al repositorio real del proyecto -->
  <div class="project-actions">
    <a href="https://github.com/AlejandroRamiroOlmo" class="btn-neon" target="_blank" rel="noopener">Ver código en GitHub &rarr;</a>
    <a href="/proyectos/" class="back-link">&larr; Volver a Proyectos</a>
  </div>

</div>