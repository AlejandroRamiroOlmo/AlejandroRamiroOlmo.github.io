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
    font-size: 2.4em; 
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
    opacity: 0; 
    animation: fadeInPill 0.5s ease-out 0.3s forwards; 
  }
  
  .stats-pill .highlight { color: #00ffcc; font-weight: 800; font-size: 1.1em; }

  /* --- 3. EFECTO DE FONDO FLUIDO (AURAS SIN GRID) --- */
  .hero-banner {
    position: relative;
    background-color: #021220;
    overflow: hidden; 
    width: 100vw;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
    padding: 60px 1em;
    margin-bottom: 50px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    text-align: center;
    border-bottom: 1px solid rgba(0, 255, 204, 0.1);
  }

  .hero-banner::before {
    content: "";
    position: absolute;
    top: -50%; left: -10%; width: 60%; height: 200%;
    background: radial-gradient(circle, rgba(15, 76, 117, 0.5) 0%, transparent 60%);
    animation: floatAura1 12s infinite alternate ease-in-out;
    pointer-events: none;
    z-index: 0;
  }

  .hero-banner::after {
    content: "";
    position: absolute;
    bottom: -50%; right: -10%; width: 50%; height: 200%;
    background: radial-gradient(circle, rgba(0, 255, 204, 0.1) 0%, transparent 60%);
    animation: floatAura2 15s infinite alternate-reverse ease-in-out;
    pointer-events: none;
    z-index: 0;
  }

  @keyframes floatAura1 {
    0% { transform: translate(0, 0) scale(1); }
    100% { transform: translate(20%, 10%) scale(1.2); }
  }

  @keyframes floatAura2 {
    0% { transform: translate(0, 0) scale(1); }
    100% { transform: translate(-20%, -10%) scale(1.3); }
  }

  .hero-content {
    position: relative;
    z-index: 1;
    max-width: 1280px; 
    margin: 0 auto;
  }

  /* --- 4. ANIMACIÓN Y FORMATO DE LAS TARJETAS --- */
  @keyframes cardSlideUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* GRID: Máximo 3 tarjetas por fila, alineadas a la izquierda */
  .projects-full-grid { 
    display: grid; 
    gap: 25px; /* Espacio entre tarjetas ligeramente reducido */
    grid-template-columns: repeat(1, 1fr); 
  }
  @media (min-width: 768px) {
    .projects-full-grid { grid-template-columns: repeat(2, 1fr); }
  }
  @media (min-width: 1024px) {
    .projects-full-grid { grid-template-columns: repeat(3, 1fr); }
  }
  
  .project-full-card {
    background: #021a30; border: 2px solid #0f4c75; border-radius: 12px;
    overflow: hidden; transition: 0.3s; display: flex; flex-direction: column;
    opacity: 0; 
    animation: cardSlideUp 0.5s ease-out forwards;
  }
  
  .project-full-card:nth-child(1) { animation-delay: 0.5s; }
  .project-full-card:nth-child(2) { animation-delay: 0.65s; }
  .project-full-card:nth-child(3) { animation-delay: 0.8s; } 

  .project-full-card:hover { border-color: #00ffcc; box-shadow: 0 10px 20px rgba(0,255,204,0.12); transform: translateY(-4px); }
  
  /* Imagen estrictamente cuadrada */
  .project-full-img { 
    width: 100%; 
    aspect-ratio: 1 / 1; 
    object-fit: cover; 
    display: block; 
  }
  
  /* Padding interior reducido para hacerla más compacta */
  .project-full-body { padding: 20px; display: flex; flex-direction: column; flex: 1; }
  .project-full-body h3 { color: #fff; margin: 0 0 8px 0; border-bottom: none; font-size: 1.15em; }
  
  /* TEXTO LIMITADO A 3 LÍNEAS */
  .project-full-body p { 
    color: #bbe1fa; 
    font-size: 0.85em; 
    line-height: 1.5; 
    margin-bottom: 16px; 
    flex: 1;
    display: -webkit-box;
    -webkit-line-clamp: 3; /* Número máximo de líneas */
    -webkit-box-orient: vertical;
    overflow: hidden;
  }
  
  .project-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 18px; }
  .project-tag {
    background: transparent; border: 1px solid #00ffcc; color: #00ffcc;
    padding: 4px 10px; border-radius: 20px; font-size: 0.75em; font-weight: 600;
    display: inline-flex; align-items: center; gap: 5px;
  }
  
  /* --- BOTÓN NEÓN --- */
  .project-full-body .btn-neon { align-self: flex-start; }
  .btn-neon {
    display: inline-block; padding: 8px 18px; border: 1.5px solid #00ffcc;
    color: #00ffcc !important; text-decoration: none; border-radius: 5px;
    font-weight: bold; transition: 0.3s; font-size: 0.85em; background: #021a30;
  }
  .btn-neon:hover { background: #00ffcc; color: #021a30 !important; box-shadow: 0 0 10px rgba(0,255,204,0.4); }

  @media (max-width: 768px) {
    .animated-title { font-size: 2em; }
  }
</style>

<!-- ========================================== -->
<!-- CABECERA CON TÍTULO ANIMADO Y PÍLDORA      -->
<!-- ========================================== -->
<div class="hero-banner">
  <div class="hero-content">
    <h1 class="animated-title">Conoce mi Trabajo</h1>
    <div class="stats-pill">
      <span class="highlight">3</span> Proyectos documentados
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

    <!-- Tarjeta 3 (Nueva) -->
    <div class="project-full-card">
      <!-- Cambia la ruta de la imagen cuando tengas una nueva -->
      <img src="/assets/images/placeholder.png" alt="Nuevo Proyecto" class="project-full-img">
      <div class="project-full-body">
        <h3>Título del Nuevo Proyecto</h3>
        <p>Aquí puedes escribir la descripción de tu tercer proyecto. Si escribes mucho texto, el sistema automáticamente lo cortará al llegar a la tercera línea con puntos suspensivos.</p>
        <div class="project-tags">
          <span class="project-tag"><i class="fas fa-microchip"></i> Tecnología 1</span>
          <span class="project-tag"><i class="fas fa-code"></i> Tecnología 2</span>
        </div>
        <!-- Cambia el enlace de abajo hacia donde apunte el proyecto -->
        <a href="#" class="btn-neon">Ver más &rarr;</a>
      </div>
    </div>

  </div>
</div>