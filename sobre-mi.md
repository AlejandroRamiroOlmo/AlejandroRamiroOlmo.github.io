---
layout: single
title: "Sobre mí"
author_profile: true
classes: wide
---

<!-- ========================================== -->
<!-- ESTILOS CSS DE LA PÁGINA "SOBRE MÍ"        -->
<!-- ========================================== -->
<style>
  /* 1. Sidebar de autor */
  .sidebar {
    background: white !important;
    border: 1px solid #d5dce4 !important;
    border-radius: 12px !important;
    padding: 20px !important;
    box-shadow: 0 4px 15px rgba(0,0,0,0.05) !important;
  }
  .sidebar .author__avatar img { border-radius: 50% !important; border: 3px solid #0f4c75 !important; }
  .sidebar .author__name { color: #1d3557 !important; font-weight: bold !important; }
  .sidebar .author__bio { color: #495057 !important; }
  .sidebar .author__urls.social-links { border-top: 1px solid #eaeaea !important; margin-top: 15px !important; padding-top: 15px !important; }

  /* 2. Tarjetas base */
  .intro-card {
    background: white; border: 1px solid #d5dce4; border-radius: 12px;
    padding: 30px; margin-bottom: 40px; box-shadow: 0 4px 15px rgba(0,0,0,0.05);
  }
  .intro-card h2 { margin-top: 0; color: #1d3557; border-bottom: 2px solid #0f4c75; padding-bottom: 10px; font-size: 1.4em; }
  .intro-text { font-size: 1.1em; line-height: 1.6; color: #495057; margin: 0; text-align: justify; }
  .intro-text p:last-child { margin-bottom: 0; }

  /* 3. Franja de cifras destacadas */
  .stats-strip { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-bottom: 40px; }
  .stat-card {
    background: #021a30; border: 2px solid #0f4c75; border-radius: 12px;
    padding: 26px 18px; text-align: center; transition: 0.3s;
  }
  .stat-card:hover { border-color: #00ffcc; box-shadow: 0 10px 25px rgba(0,255,204,0.2); transform: translateY(-4px); }
  .stat-card i { font-size: 2em; color: #00ffcc; display: block; margin-bottom: 10px; }
  .stat-number { font-size: 1.5em; font-weight: 800; color: #ffffff; margin-bottom: 6px; line-height: 1.1; }
  .stat-label { font-size: 0.82em; color: #bbe1fa; line-height: 1.4; }

  /* 4. Bloque Docencia con número circular */
  .docencia-header { display: flex; align-items: center; gap: 20px; margin-bottom: 15px; flex-wrap: wrap; }
  .docencia-number {
    flex-shrink: 0; background: #021a30; border: 3px solid #00ffcc; color: #00ffcc;
    font-weight: 800; font-size: 1.6em; width: 80px; height: 80px; border-radius: 50%;
    display: flex; flex-direction: column; align-items: center; justify-content: center;
    line-height: 1; box-shadow: 0 0 15px rgba(0,255,204,0.25);
  }
  .docencia-number span { font-size: 0.38em; font-weight: 600; color: #bbe1fa; margin-top: 4px; }
  .docencia-header h2 { margin: 0; border-bottom: none; padding-bottom: 0; flex: 1; min-width: 200px; }

  /* 5. Trayectoria PCB */
  .pcb-board {
    background-color: #021a30;
    background-image:
      linear-gradient(rgba(79, 195, 247, 0.05) 1px, transparent 1px),
      linear-gradient(90deg, rgba(79, 195, 247, 0.05) 1px, transparent 1px);
    background-size: 20px 20px;
    border: 2px solid #0f4c75; border-radius: 12px; color: #bbe1fa;
    padding: 30px; margin-bottom: 40px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);
  }
  .pcb-timeline { position: relative; z-index: 1; margin-top: 10px; padding-left: 10px; }
  .pcb-item { position: relative; padding-bottom: 30px; padding-left: 45px; border-left: 3px solid #0f4c75; transition: border-color 0.3s ease; }
  .pcb-item:last-child { border-left: 3px solid transparent; padding-bottom: 0; }
  .pcb-item::before { content: ''; position: absolute; top: 10px; left: 0; width: 25px; height: 3px; background-color: #0f4c75; transition: all 0.3s ease; }
  .pcb-pad { position: absolute; top: 3px; left: 22px; width: 16px; height: 16px; background-color: #021a30; border: 3px solid #0f4c75; border-radius: 50%; transition: all 0.3s ease; }
  .pcb-item:hover { border-left-color: #00ffcc; }
  .pcb-item:hover::before { background-color: #00ffcc; box-shadow: 0 0 10px #00ffcc; }
  .pcb-item:hover .pcb-pad { border-color: #00ffcc; background-color: #00ffcc; box-shadow: 0 0 15px #00ffcc; }
  .pcb-item h4 { margin: 0 0 5px 0; color: #3282b8; transition: all 0.3s; font-size: 1.1em; display: inline-block; }
  .pcb-item:hover h4 { color: #ffffff; text-shadow: 0 0 8px #00ffcc; }
  .pcb-item ul { margin: 0; padding-left: 20px; color: #bbe1fa; font-size: 0.9em; }
  .pcb-item ul li { margin-bottom: 5px; }

  /* Badge de duración en cada hito */
  .pcb-duration {
    display: inline-block; background: rgba(0,255,204,0.08); border: 1px solid #00ffcc;
    color: #00ffcc; font-size: 0.72em; font-weight: 600; padding: 2px 10px;
    border-radius: 12px; margin-left: 10px; vertical-align: middle;
  }

  /* 6. Panel de Idiomas y Soft Skills */
  .skills-container { display: flex; gap: 20px; flex-wrap: wrap; margin-bottom: 40px; }
  .skill-box {
    flex: 1; min-width: 250px; background: rgba(255,255,255,0.8);
    border: 1px solid #d5dce4; border-radius: 12px; padding: 25px; box-shadow: 0 4px 15px rgba(0,0,0,0.05);
  }
  .skill-box h3 { margin-top: 0; color: #1d3557; border-bottom: 2px solid #0f4c75; padding-bottom: 10px; }
  .skill-list { list-style: none; padding: 0; margin: 0; }
  .skill-list li { margin-bottom: 15px; display: flex; align-items: flex-start; font-size: 1.05em; color: #495057; }
  .skill-list i {
    font-size: 1.1em; color: #00ffcc; background: #021a30; width: 35px; height: 35px;
    display: flex; align-items: center; justify-content: center; border-radius: 8px;
    margin-right: 15px; flex-shrink: 0; margin-top: 3px;
  }

  /* Aptitudes Transversales desarrolladas */
  .aptitud-list { display: flex; flex-direction: column; gap: 18px; }
  .aptitud-item h4 { margin: 0 0 6px 0; color: #1d3557; font-size: 1.02em; display: flex; align-items: center; gap: 10px; }
  .aptitud-item h4 i {
    color: #00ffcc; background: #021a30; width: 32px; height: 32px; border-radius: 8px;
    display: flex; align-items: center; justify-content: center; font-size: 0.85em; flex-shrink: 0;
  }
  .aptitud-item p { margin: 0; color: #495057; font-size: 0.92em; line-height: 1.5; padding-left: 42px; }

  /* 7. Inventario Tecnológico (Tags) */
  .tech-stack-box { background: #021a30; border-radius: 12px; padding: 30px; text-align: center; border: 2px solid #0f4c75; }
  .tech-stack-box h3 { color: #bbe1fa; margin-top: 0; margin-bottom: 10px; }
  .tech-tags { display: flex; flex-wrap: wrap; justify-content: center; gap: 15px; margin-top: 20px; }
  .tech-tag {
    background: transparent; border: 2px solid #00ffcc; color: #00ffcc; padding: 10px 20px;
    border-radius: 30px; font-weight: bold; font-size: 1em; display: flex; align-items: center;
    gap: 10px; transition: all 0.3s; cursor: default;
  }
  .tech-tag:hover { background: #00ffcc; color: #021a30; box-shadow: 0 0 15px #00ffcc; transform: translateY(-3px); }

  @media (max-width: 600px) {
    .docencia-header { flex-direction: column; text-align: center; }
  }
</style>

<!-- ========================================== -->
<!-- BLOQUE 1: PRESENTACIÓN                     -->
<!-- ========================================== -->
<div class="intro-card">
  <h2>Perfil Profesional</h2>
  <div class="intro-text">
    <p>Soy <strong>Alejandro Ramiro</strong>, estudiante del Doble Grado en Ingeniería. Mi pasión siempre ha sido entender cómo funcionan las cosas en el mundo físico y cómo podemos darles "cerebro" para automatizarlas.</p>
    <p>Actualmente me encuentro en mi último año, desarrollando mi Trabajo de Fin de Grado y preparándome para dar el salto definitivo a la industria. Busco conectar la mecánica con el control electrónico, aportando una visión completa que puentea el diseño físico y la lógica de programación.</p>
  </div>
</div>

<!-- ========================================== -->
<!-- FRANJA DE CIFRAS DESTACADAS                -->
<!-- ========================================== -->
<div class="stats-strip">
  <div class="stat-card">
    <i class="fas fa-graduation-cap"></i>
    <div class="stat-number">5º Año</div>
    <div class="stat-label">Doble Grado en curso</div>
  </div>
  <div class="stat-card">
    <i class="fas fa-layer-group"></i>
    <div class="stat-number">2</div>
    <div class="stat-label">Especializaciones: Mecánica y Electrónica</div>
  </div>
  <div class="stat-card">
    <i class="fas fa-plane-departure"></i>
    <div class="stat-number">1</div>
    <div class="stat-label">Estancia Erasmus+ en Polonia</div>
  </div>
</div>

<!-- ========================================== -->
<!-- BLOQUE 1.5: DOCENCIA Y COMUNICACIÓN        -->
<!-- ========================================== -->
<div class="intro-card">
  <div class="docencia-header">
    <div class="docencia-number">3+<span>AÑOS</span></div>
    <h2><i class="fas fa-chalkboard-teacher" style="color: #0f4c75; margin-right: 10px;"></i> Docencia y Comunicación Técnica</h2>
  </div>
  <div class="intro-text">
    <p>
      Durante mi etapa universitaria, he compaginado mi formación con la impartición de clases particulares de <strong>Física, Matemáticas y Tecnología</strong>. Más allá de la enseñanza académica, esta experiencia ha forjado una de mis competencias profesionales más valiosas: la capacidad de comunicación.
    </p>
    <p>
      La docencia me ha enseñado a estructurar la información y transmitir conceptos técnicos de forma clara y accesible. Estoy convencido de que en el sector industrial actual, <strong>saber diseñar un sistema eficiente es tan importante como saber explicarlo, documentarlo y defenderlo</strong> ante un equipo de trabajo o un cliente.
    </p>
  </div>
</div>

<!-- ========================================== -->
<!-- BLOQUE 2: TRAYECTORIA ACADÉMICA            -->
<!-- ========================================== -->
<div class="pcb-board">
  <h2 style="margin-top: 0; color: #bbe1fa; text-align: center; border-bottom: 1px solid #0f4c75; padding-bottom: 15px;">Trayectoria Académica</h2>

  <div class="pcb-timeline">

    <div class="pcb-item">
      <div class="pcb-pad"></div>
      <h4>2026 - 2027: Último Año e Industria (Actualidad)</h4><span class="pcb-duration">1 año</span>
      <ul>
        <li>Desarrollo de dos Trabajos de Fin de Grado (TFGs).</li>
      </ul>
    </div>

    <div class="pcb-item">
      <div class="pcb-pad"></div>
      <h4>2025 - 2026: Especialización Mecánica (Erasmus+)</h4><span class="pcb-duration">1 año</span>
      <ul>
        <li>Estancia en la <strong>Politechnika Lubelska</strong> (Lublin, Polonia).</li>
        <li>Inmersión en un entorno internacional con docencia íntegramente en inglés.</li>
        <li>Desarrollo de competencias de adaptabilidad y trabajo con equipos multiculturales.</li>
      </ul>
    </div>

    <div class="pcb-item">
      <div class="pcb-pad"></div>
      <h4>2024 - 2025: Especialización Electrónica</h4><span class="pcb-duration">1 año</span>
      <ul>
        <li>Profundización en la rama de electrónica dentro del plan de estudios de la Universidad de Jaén.</li>
      </ul>
    </div>

    <div class="pcb-item">
      <div class="pcb-pad"></div>
      <h4>2022 - 2024: Inicio y Base Científica</h4><span class="pcb-duration">2 años</span>
      <ul>
        <li>Comienzo del Doble Grado en la <strong>Universidad de Jaén</strong>.</li>
        <li>Adquisición de la base matemática, física y especialización común a la rama industrial.</li>
      </ul>
    </div>

  </div>
</div>

<!-- ========================================== -->
<!-- BLOQUE 3: IDIOMAS, DOCENCIA Y SOFT SKILLS  -->
<!-- ========================================== -->
<div class="skills-container">
  <!-- Caja Izquierda: Comunicación -->
  <div class="skill-box">
    <h3><i class="fas fa-comment-dots" style="color: #0f4c75; font-size: 1em; background: transparent; width: auto; height: auto; margin:0;"></i> Idiomas</h3>

    <ul class="skill-list">
      <li><i class="fas fa-award"></i> <span><strong>Inglés:</strong>&nbsp; Nivel avanzado (C1).</span></li>
      <li><i class="fas fa-language"></i> <span><strong>Español:</strong>&nbsp; Nativo.</span></li>
    </ul>
  </div>

  <!-- Caja Derecha: Aptitudes Transversales (mismas que en Inicio, desarrolladas) -->
  <div class="skill-box">
    <h3><i class="fas fa-users-cog" style="color: #0f4c75; font-size: 1em; background: transparent; width: auto; height: auto; margin:0;"></i> Aptitudes Transversales</h3>
    <div class="aptitud-list">
      <div class="aptitud-item">
        <h4><i class="fas fa-users"></i> Liderazgo y Comunicación</h4>
        <p>Mi experiencia como profesor particular ha reforzado mi comunicación técnica y mi capacidad para liderar y coordinar equipos.</p>
      </div>
      <div class="aptitud-item">
        <h4><i class="fas fa-tools"></i> Resolución de Problemas</h4>
        <p>Afronto los problemas de ingeniería con un enfoque analítico: identifico la causa raíz antes de proponer soluciones.</p>
      </div>
      <div class="aptitud-item">
        <h4><i class="fas fa-exchange-alt"></i> Adaptabilidad y Trabajo en Equipo</h4>
        <p>La estancia Erasmus+ en Polonia me enfrentó a un entorno de trabajo internacional, donde aprendí a adaptar mi forma de comunicar y colaborar según el contexto del equipo.</p>
      </div>
    </div>
  </div>
</div>

<!-- ========================================== -->
<!-- BLOQUE 4: STACK TECNOLÓGICO                -->
<!-- ========================================== -->
<div class="tech-stack-box">
  <h3>Herramientas y Tecnologías</h3>
  <p style="color: #bbe1fa; margin-bottom: 0; font-size: 0.95em;">Software y entornos de desarrollo con los que me formo y trabajo actualmente:</p>
  <div class="tech-tags">
    <div class="tech-tag"><i class="fas fa-cube"></i> SolidWorks</div>
    <div class="tech-tag"><i class="fas fa-microchip"></i> C/C++</div>
    <div class="tech-tag"><i class="fab fa-python"></i> Python</div>
    <div class="tech-tag"><i class="fas fa-bolt"></i> KiCad</div>
  </div>
</div>
