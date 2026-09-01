---
layout: splash
title: ""
permalink: /proyectos/estacion-industrial/
author_profile: false
---

<!-- ========================================== -->
<!-- ESTILOS CSS (Mantenidos de tu plantilla)   -->
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
  .specs-table { width: 100%; border-collapse: collapse; margin-top: 10px; margin-bottom: 20px; }
  .specs-table th, .specs-table td { padding: 12px 16px; text-align: left; border-bottom: 1px solid #eaeaea; font-size: 0.95em; }
  .specs-table th { background: #021a30; color: #00ffcc; font-weight: 700; text-transform: uppercase; font-size: 0.78em; letter-spacing: 0.5px; }
  .specs-table th:first-child { border-top-left-radius: 8px; }
  .specs-table th:last-child { border-top-right-radius: 8px; }
  .specs-table td:first-child { font-weight: 600; color: #1d3557; width: 25%; }
  .specs-table td { color: #495057; }
  .specs-table tr:last-child td { border-bottom: none; }
  .specs-table tr:hover td { background: #f8fafb; }

  /* --- BLOQUE DE CÓDIGO --- */
  .code-block {
    background: #f4f6f9; border: 1px solid #d5dce4; border-left: 4px solid #0f4c75;
    border-radius: 6px; padding: 15px; font-family: 'Courier New', Courier, monospace;
    font-size: 0.95em; color: #333; overflow-x: auto; margin-top: 15px;
  }

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
    display: none; position: fixed; z-index: 9999; padding-top: 40px;
    left: 0; top: 0; width: 100%; height: 100%; background-color: rgba(0, 0, 0, 0.85); backdrop-filter: blur(4px); 
  }
  .image-modal-content {
    margin: auto; display: block; max-width: 95%; max-height: 90vh; object-fit: contain;
    border-radius: 8px; box-shadow: 0 5px 25px rgba(0,0,0,0.5);
  }
  .close-modal {
    position: absolute; top: 15px; right: 35px; color: #f1f1f1; font-size: 40px; font-weight: bold; transition: 0.3s; cursor: pointer;
  }
  .close-modal:hover { color: #00ffcc; }

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
    <h1 style="color: #ffffff; border-bottom: none; margin: 0;">Estación Industrial</h1>
    <div class="project-hero-tags">
      <span class="project-tag">Proyecto Académico</span>
      <span class="project-tag">PLC Siemens S7-1200</span>
      <span class="project-tag">Lenguaje SCL</span>
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
      El proyecto consistía en automatizar una estación de clasificación de piezas simulada. El sistema debía ser capaz de detectar distintos tipos de materiales mediante el uso de sensores inductivos y ópticos, para posteriormente clasificarlos de forma automatizada empleando actuadores neumáticos.
    </p>
  </div>

  <div class="content-card">
    <h2>Especificaciones Técnicas</h2>
    <table class="specs-table">
      <thead>
        <tr><th>Característica</th><th>Detalle</th></tr>
      </thead>
      <tbody>
        <tr><td>Hardware</td><td>PLC Siemens S7-1200</td></tr>
        <tr><td>Lenguaje de Programación</td><td>SCL (Structured Control Language)</td></tr>
        <tr><td>Detección</td><td>Sensores ópticos (presencia) e inductivos (material)</td></tr>
        <tr><td>Actuadores</td><td>Electroválvulas de empuje neumáticas</td></tr>
      </tbody>
    </table>
  </div>

  <div class="content-card">
    <h2>Desarrollo y Solución Técnica</h2>
    <p>
      En lugar de utilizar el clásico lenguaje de contactos (Ladder), se optó por programar la lógica en <strong>SCL (Structured Control Language)</strong> debido a la complejidad matemática requerida para el proceso de clasificación. Toda la programación se estructuró en bloques lógicos independientes (FBs) para mantener un código modular y escalable.
    </p>

    <h3 style="color: #1d3557; margin-top: 25px;">Fragmento de Lógica (SCL)</h3>
    <p>Ejemplo de la lógica implementada para el control del temporizador de clasificación (los detalles completos de E/S están disponibles en la documentación técnica):</p>
    <div class="code-block">
<pre><code>IF "S_Pieza" AND NOT "S_Metal" THEN
    "T_Clasificacion".TON(IN := TRUE, PT := T#2S);
    
    IF "T_Clasificacion".Q THEN
        "Cil_Avance" := TRUE;
    END_IF;
ELSE
    "Cil_Avance" := FALSE;
END_IF;</code></pre>
    </div>
  </div>

  <!-- SECCIÓN DE GALERÍA -->
  <div class="content-card">
    <h2>Galería de Capturas</h2>
    <p><em>Imágenes de la programación en TIA Portal y esquemas del proyecto. Haz clic para ampliar.</em></p>
    <div class="gallery-wrapper">
      <button class="gallery-arrow" aria-label="Anterior" onclick="scrollGallery(this, -1)"><i class="fas fa-chevron-left"></i></button>

      <div class="gallery-strip">
        <!-- Sustituye estas rutas por las tuyas -->
        <div class="gallery-item"><img src="/assets/images/placeholder_tia1.png" alt="Captura TIA Portal 1" onclick="abrirModal(this.src)"></div>
        <div class="gallery-item"><img src="/assets/images/placeholder_tia2.png" alt="Esquema eléctrico" onclick="abrirModal(this.src)"></div>
        <div class="gallery-item"><img src="/assets/images/placeholder_tia3.png" alt="Bloques de programa" onclick="abrirModal(this.src)"></div>
      </div>

      <button class="gallery-arrow" aria-label="Siguiente" onclick="scrollGallery(this, 1)"><i class="fas fa-chevron-right"></i></button>
    </div>
  </div>

  <!-- TARJETA FINAL: DESCARGA DE MANUAL PDF -->
  <div class="content-card" style="text-align: center;">
    <h2>Documentación del Proyecto</h2>
    <p style="text-align: center; margin-bottom: 25px;">
      Si quieres profundizar en los detalles técnicos, mapas de Entradas/Salidas (E/S), configuración de hardware y bloques lógicos del proyecto, puedes consultar el manual de software completo.
    </p>
    <!-- Actualiza el href con la ruta real de tu PDF -->
    <a href="/assets/docs/manual_estacion_industrial.pdf" target="_blank" class="btn-neon" rel="noopener">
      <i class="fas fa-file-pdf" style="margin-right: 8px;"></i> Ver Manual de Software (PDF)
    </a>
  </div>

  <div class="project-actions">
    <!-- Puedes dejar este botón o quitarlo si el código no está en GitHub -->
    <a href="https://github.com/TuUsuario" class="btn-neon" target="_blank" rel="noopener">Ver repositorio &rarr;</a>
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
  function abrirModal(src) {
    document.getElementById("miModalImagen").style.display = "block";
    document.getElementById("imagenAmpliada").src = src;
  }
  function cerrarModal() {
    document.getElementById("miModalImagen").style.display = "none";
  }
  function scrollGallery(btn, direction) {
    const wrapper = btn.closest('.gallery-wrapper');
    const strip = wrapper.querySelector('.gallery-strip');
    const amount = strip.clientWidth * 0.85;
    strip.scrollBy({ left: direction * amount, behavior: 'smooth' });
  }
</script>