---
layout: splash
author_profile: false
title: ""
---

<!-- ========================================== -->
<!-- ESTILOS CSS                                -->
<!-- ========================================== -->
<style>
  .section-wrapper { max-width: 1280px; margin: 0 auto 60px auto; padding: 0 20px; }

  /* --- 1. ANIMACIÓN ELEGANTE (TÍTULO) --- */
  @keyframes titleFadeIn {
    from { opacity: 0; transform: translateY(-15px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .animated-title {
    animation: titleFadeIn 0.6s ease-out forwards;
    font-size: 2.4em; /* Tamaño más discreto y profesional */
    font-weight: 700;
    letter-spacing: 3px;
    color: #ffffff;
    margin: 0 0 12px 0;
    border-bottom: none;
  }

  /* --- 2. ANIMACIÓN DE LA PÍLDORA --- */
  @keyframes fadeInPill {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .stats-pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(2, 26, 48, 0.6);
    border: 1px solid rgba(0, 255, 204, 0.3);
    border-radius: 50px;
    padding: 6px 18px;
    font-size: 0.85em;
    color: #bbe1fa;
    backdrop-filter: blur(4px);
    opacity: 0; /* Oculto hasta que toque su turno */
    animation: fadeInPill 0.5s ease-out 0.3s forwards; /* Entra casi justo después del título */
  }
  
  .stats-pill .highlight { color: #00ffcc; font-weight: 800; font-size: 1.1em; }

  /* --- BANNER PRINCIPAL --- */
  .hero-banner {
    background: linear-gradient(135deg, #1d3557 0%, #021a30 100%);
    width: 100vw;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
    padding: 60px 1em;
    margin-bottom: 50px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    text-align: center;
    border-bottom: 1px solid rgba(0, 255, 204, 0.1);
  }

  /* --- 3. ANIMACIÓN Y FORMATO DE LAS TARJETAS (MÁS CUADRADAS Y RÁPIDAS) --- */
  @keyframes cardSlideUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Grid ajustado para favorecer un formato de tarjeta más equilibrado */
  .projects-full-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 35px; }
  
  .project-full-card {
    background: #021a30; border: 2px solid #0f4c75; border-radius: 14px;
    overflow: hidden; transition: 0.3s; display: flex; flex-direction: column;
    opacity: 0; /* Oculto al inicio */
    animation: cardSlideUp 0.5s ease-out forwards;
  }
  
  /* Retrasos reducidos para que entren rápido de una en una */
  .project-full-card:nth-child(1) { animation-delay: 0.5s; }
  .project-full-card:nth-child(2) { animation-delay: 0.65s; }
  .project-full-card:nth-child(3) { animation-delay: 0.8s; } 

  .project-full-card:hover { border-color: #00ffcc; box-shadow: 0 12px 25px rgba(0,255,204,0.12); transform: translateY(-4px); }
  
  /* Imagen cuadrada */
  .project-full-img { 
    width: 100%; 
    aspect-ratio: 1 / 1; /* Esto fuerza a la imagen a ser un cuadrado perfecto */
    object-fit: cover; 
    display: block; 
  }
  
  .project-full-body { padding: 25px; display: flex; flex-direction: column; flex: 1; }
  .project-full-body h3 { color: #fff; margin: 0 0 10px 0; border-bottom: none; font-size: 1.25em; }
  .project-full-body p { color: #bbe1fa; font-size: 0.9em; line-height: 1.6; margin-bottom: 18px; flex: 1; }
  
  .project-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 22px; }
  .project-tag {
    background: transparent; border: 1px solid #00ffcc; color: #00ffcc;
    padding: 5px 12px; border-radius: 20px; font-size: 0.8em; font-weight: 600;
    display: inline-flex; align-items: center; gap: 6px;
  }
  
  /* --- BOTÓN NEÓN --- */
  .project-full-body .btn-neon { align-self: flex-start; }
  .btn-neon {
    display: inline-block; padding: 10px 22px; border: 1.5px solid #00ffcc;
    color: #00ffcc !important; text-decoration: none; border-radius: 5px;
    font-weight: bold; transition: 0.3s; font-size: 0.9em; background: #021a30;
  }
  .btn-neon:hover { background: #00ffcc; color: #021a30 !important; box-shadow: 0 0 12px rgba(0,255,204,0.5); }

  @media (max-width: 768px) {
    .animated-title { font-size: 2em; }
  }
</style>

<!-- ========================================== -->
<!-- CABECERA CON TÍTULO ANIMADO Y PÍLDORA      -->
<!-- ========================================== -->
<div class="hero-banner">
  <div style="max-width: 1280px; margin: 0 auto;">
    <h1 class="animated-title">PROYECTOS</h1>
    <div class="stats-pill">
      <span class="highlight">2</span> Proyectos documentados
    </div>
  </div>
</div>

<!-- ========================================== -->
<!-- GRID DE PROYECTOS                          -->
<!-- ========================================== -->
<div class="section-wrapper">
  <div class="projects-full-grid">

    <!-- Tarjeta 1 -->
    <div class="project-full-card">
      <img src="/assets/images/maquina.png" alt="Máquina Arcade" class="project-full-img">
      <div class="project-full-body">
        <h3>Máquina Arcade</h3>
        <p>Diseño físico de una máquina Arcade completa, combinando una estructura a medida con un software personalizado y tematizado para la experiencia de juego.</p>
        <div class="project-tags">
          <span class="project-tag"><i class="fas fa-cube"></i> SolidWorks</span>
          <span class="project-tag"><i class="fas fa-microchip"></i> Arduino</span>
          <span class="project-tag"><i class="fab fa-python"></i> Python</span>
        </div>
        <a href="/proyectos/maquina-arcade/" class="btn-neon">Ver más &rarr;</a>
      </div>
    </div>

    <!-- Tarjeta 2 -->
    <div class="project-full-card">
      <img src="/assets/images/Automatizacion.png" alt="Estación Industrial" class="project-full-img">
      <div class="project-full-body">
        <h3>Estación Industrial</h3>
        <p>Programación de un PLC Siemens en lenguaje SCL para automatizar un proceso industrial completo, desde la lógica de control hasta la puesta en marcha.</p>
        <div class="project-tags">
          <span class="project-tag"><i class="fas fa-industry"></i> PLC Siemens</span>
          <span class="project-tag"><i class="fas fa-code"></i> SCL</span>
          <span class="project-tag"><i class="fas fa-bolt"></i> KiCad</span>
        </div>
        <a href="/proyectos/estacion-industrial/" class="btn-neon">Ver más &rarr;</a>
      </div>
    </div>

  </div>
</div>