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

  /* --- ANIMACIÓN BLUEPRINT (PLANO TÉCNICO) --- */
  @keyframes blueprintReveal {
    0% { 
      color: transparent; 
      -webkit-text-stroke: 1px #00ffcc; 
      opacity: 0; 
      transform: translateY(10px) scale(0.98); 
    }
    40% { 
      color: transparent; 
      -webkit-text-stroke: 1.5px #00ffcc; 
      opacity: 1; 
      transform: translateY(0) scale(1); 
      text-shadow: none;
    }
    100% { 
      color: #ffffff; 
      -webkit-text-stroke: 0px transparent; 
      text-shadow: 0 0 15px rgba(0, 255, 204, 0.4); 
    }
  }

  .animated-title {
    animation: blueprintReveal 2.5s cubic-bezier(0.25, 1, 0.5, 1) forwards;
    font-size: 3.5em;
    font-weight: 900;
    letter-spacing: 4px;
    margin: 0 0 15px 0;
    border-bottom: none;
  }

  /* --- PÍLDORA DE ESTADÍSTICAS EN EL BANNER --- */
  .stats-pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(2, 26, 48, 0.6);
    border: 1px solid rgba(0, 255, 204, 0.3);
    border-radius: 50px;
    padding: 8px 20px;
    font-size: 0.9em;
    color: #bbe1fa;
    backdrop-filter: blur(4px);
    animation: fadeInPill 2.5s ease-in forwards;
    opacity: 0;
  }
  
  .stats-pill .highlight {
    color: #00ffcc;
    font-weight: 800;
    font-size: 1.1em;
  }

  @keyframes fadeInPill {
    0%, 60% { opacity: 0; transform: translateY(10px); }
    100% { opacity: 1; transform: translateY(0); }
  }

  /* --- BANNER PRINCIPAL --- */
  .hero-banner {
    background: linear-gradient(135deg, #1d3557 0%, #021a30 100%);
    width: 100vw;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
    padding: 70px 1em;
    margin-bottom: 50px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    text-align: center;
    border-bottom: 1px solid rgba(0, 255, 204, 0.1);
  }

  /* --- GRID DE PROYECTOS --- */
  .projects-full-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(380px, 1fr)); gap: 35px; }
  .project-full-card {
    background: #021a30; border: 2px solid #0f4c75; border-radius: 14px;
    overflow: hidden; transition: 0.3s; display: flex; flex-direction: column;
  }
  .project-full-card:hover { border-color: #00ffcc; box-shadow: 0 15px 35px rgba(0,255,204,0.15); transform: translateY(-6px); }
  .project-full-img { width: 100%; height: 220px; object-fit: cover; display: block; }
  .project-full-body { padding: 28px; display: flex; flex-direction: column; flex: 1; }
  .project-full-body h3 { color: #fff; margin: 0 0 10px 0; border-bottom: none; font-size: 1.35em; }
  .project-full-body p { color: #bbe1fa; font-size: 0.95em; line-height: 1.6; margin-bottom: 18px; flex: 1; }
  .project-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 22px; }
  .project-tag {
    background: transparent; border: 1.5px solid #00ffcc; color: #00ffcc;
    padding: 6px 14px; border-radius: 20px; font-size: 0.82em; font-weight: 600;
    display: inline-flex; align-items: center; gap: 6px;
  }
  .project-full-body .btn-neon { align-self: flex-start; }

  /* --- BOTÓN NEÓN --- */
  .btn-neon {
    display: inline-block; padding: 12px 25px; border: 2px solid #00ffcc;
    color: #00ffcc !important; text-decoration: none; border-radius: 5px;
    font-weight: bold; transition: 0.3s; font-size: 1em; background: #021a30;
  }
  .btn-neon:hover { background: #00ffcc; color: #021a30 !important; box-shadow: 0 0 15px #00ffcc; }

  @media (max-width: 768px) {
    .animated-title { font-size: 2.5em; }
    .project-full-img { height: 180px; }
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