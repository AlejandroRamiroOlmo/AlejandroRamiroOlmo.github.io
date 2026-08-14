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

  /* --- FRANJA DE CIFRAS DESTACADAS --- */
  .stats-strip { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 20px; }
  .stat-card {
    background: #021a30; border: 2px solid #0f4c75; border-radius: 12px;
    padding: 28px 20px; text-align: center; transition: 0.3s;
  }
  .stat-card:hover { border-color: #00ffcc; box-shadow: 0 10px 25px rgba(0,255,204,0.2); transform: translateY(-4px); }
  .stat-card i { font-size: 2.2em; color: #00ffcc; display: block; margin-bottom: 12px; }
  .stat-number { font-size: 1.5em; font-weight: 800; color: #ffffff; margin-bottom: 6px; line-height: 1.1; }
  .stat-label { font-size: 0.85em; color: #bbe1fa; line-height: 1.4; }

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

  @media (max-width: 600px) {
    .project-full-img { height: 180px; }
  }
</style>

<!-- ========================================== -->
<!-- CABECERA                                   -->
<!-- ========================================== -->
<div style="background-color: #1d3557; width: 100vw; position: relative; left: 50%; right: 50%; margin-left: -50vw; margin-right: -50vw; padding: 60px 1em; margin-bottom: 40px; box-shadow: 0 4px 15px rgba(0,0,0,0.2);">
  <div style="max-width: 1280px; margin: 0 auto; text-align: center;">
    <h1 style="color: #ffffff; border-bottom: none; margin-top: 0;">Proyectos</h1>
    <p style="color: #f1faee; font-size: 1.1em; max-width: 700px; margin: 0 auto;">Diseño mecánico, electrónica y automatización industrial aplicados a casos reales — documentando el proceso completo, de la idea al prototipo funcional.</p>
  </div>
</div>

<!-- ========================================== -->
<!-- FRANJA DE CIFRAS DESTACADAS                -->
<!-- ========================================== -->
<div class="section-wrapper">
  <div class="stats-strip">
    <div class="stat-card">
      <i class="fas fa-cogs"></i>
      <div class="stat-number">2</div>
      <div class="stat-label">Proyectos documentados</div>
    </div>
    <div class="stat-card">
      <i class="fas fa-layer-group"></i>
      <div class="stat-number">2</div>
      <div class="stat-label">Áreas: Mecánica y Electrónica</div>
    </div>
    <div class="stat-card">
      <i class="fas fa-tools"></i>
      <div class="stat-number">4+</div>
      <div class="stat-label">Herramientas aplicadas</div>
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

<!-- ========================================== -->
<!--prueba              -->
<!-- ========================================== -->