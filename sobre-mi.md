---
layout: single
title: "Sobre mí"
author_profile: true
---

<!-- ========================================== -->
<!-- ESTILOS CSS DE LA PÁGINA "SOBRE MÍ"        -->
<!-- ========================================== -->
<style>
  /* 1. Enmarcar el perfil de autor (Sidebar lateral) */
  .sidebar {
    background: white !important;
    border: 1px solid #d5dce4 !important;
    border-radius: 12px !important;
    padding: 20px !important;
    box-shadow: 0 4px 15px rgba(0,0,0,0.05) !important;
  }
  .sidebar .author__avatar img {
    border-radius: 50% !important;
    border: 3px solid #0f4c75 !important;
  }
  .sidebar .author__name {
    color: #1d3557 !important;
    font-weight: bold !important;
  }
  .sidebar .author__bio {
    color: #495057 !important;
  }
  .sidebar .author__urls.social-links {
    border-top: 1px solid #eaeaea !important;
    margin-top: 15px !important;
    padding-top: 15px !important;
  }

  /* 2. Presentación y Tarjetas Base */
  .intro-card {
    background: white;
    border: 1px solid #d5dce4;
    border-radius: 12px;
    padding: 30px;
    margin-bottom: 40px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.05);
  }
  .intro-card h2 {
    margin-top: 0;
    color: #1d3557;
    border-bottom: 2px solid #0f4c75;
    padding-bottom: 10px;
    font-size: 1.4em;
  }
  .intro-text { 
    font-size: 1.1em; 
    line-height: 1.6; 
    color: #495057; 
    margin: 0; 
    text-align: justify; 
  }
  .intro-text p:last-child {
    margin-bottom: 0;
  }

  /* 3. Trayectoria PCB adaptada a una sola columna */
  .pcb-board {
    background-color: #021a30; 
    background-image: 
      linear-gradient(rgba(79, 195, 247, 0.05) 1px, transparent 1px),
      linear-gradient(90deg, rgba(79, 195, 247, 0.05) 1px, transparent 1px);
    background-size: 20px 20px; 
    border: 2px solid #0f4c75; 
    border-radius: 12px; 
    color: #bbe1fa; 
    padding: 30px; 
    margin-bottom: 40px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
  }
  
  .pcb-timeline { position: relative; z-index: 1; margin-top: 10px; padding-left: 10px; }
  .pcb-item { position: relative; padding-bottom: 30px; padding-left: 45px; border-left: 3px solid #0f4c75; transition: border-color 0.3s ease; }
  .pcb-item:last-child { border-left: 3px solid transparent; padding-bottom: 0; }
  
  .pcb-item::before { content: ''; position: absolute; top: 10px; left: 0; width: 25px; height: 3px; background-color: #0f4c75; transition: all 0.3s ease; }
  .pcb-pad { position: absolute; top: 3px; left: 22px; width: 16px; height: 16px; background-color: #021a30; border: 3px solid #0f4c75; border-radius: 50%; transition: all 0.3s ease; }
  
  .pcb-item:hover { border-left-color: #00ffcc; }
  .pcb-item:hover::before { background-color: #00ffcc; box-shadow: 0 0 10px #00ffcc; }
  .pcb-item:hover .pcb-pad { border-color: #00ffcc; background-color: #00ffcc; box-shadow: 0 0 15px #00ffcc; }
  
  .pcb-item h4 { margin: 0 0 5px 0; color: #3282b8; transition: all 0.3s; font-size: 1.1em; }
  .pcb-item:hover h4 { color: #ffffff; text-shadow: 0 0 8px #00ffcc; }
  
  .pcb-item ul { margin: 0; padding-left: 20px; color: #bbe1fa; font-size: 0.9em; }
  .pcb-item ul li { margin-bottom: 5px; }

  /* 4. Panel de Idiomas y Soft Skills */
  .skills-container { 
    display: flex; gap: 20px; flex-wrap: wrap; margin-bottom: 40px; 
  }
  .skill-box { 
    flex: 1; min-width: 250px; background: rgba(255,255,255,0.8); 
    border: 1px solid #d5dce4; border-radius: 12px; padding: 25px; 
    box-shadow: 0 4px 15px rgba(0,0,0,0.05); 
  }
  .skill-box h3 { margin-top: 0; color: #1d3557; border-bottom: 2px solid #0f4c75; padding-bottom: 10px; }
  .skill-list { list-style: none; padding: 0; margin: 0; }
  .skill-list li { margin-bottom: 15px; display: flex; align-items: flex-start; font-size: 1.05em; color: #495057; }
  
  /* Iconos de las Skills */
  .skill-list i { 
    font-size: 1.1em; color: #00ffcc; background: #021a30; 
    width: 35px; height: 35px; display: flex; align-items: center; 
    justify-content: center; border-radius: 8px; margin-right: 15px; 
    flex-shrink: 0; margin-top: 3px;
  }

  /* 5. Inventario Tecnológico (Tags) */
  .tech-stack-box { 
    background: #021a30; border-radius: 12px; padding: 30px; 
    text-align: center; border: 2px solid #0f4c75; 
  }
  .tech-stack-box h3 { color: #bbe1fa; margin-top: 0; margin-bottom: 10px; }
  .tech-tags { display: flex; flex-wrap: wrap; justify-content: center; gap: 15px; margin-top: 20px; }
  
  /* Etiquetas Neon */
  .tech-tag { 
    background: transparent; border: 2px solid #00ffcc; color: #00ffcc; 
    padding: 10px 20px; border-radius: 30px; font-weight: bold; 
    font-size: 1em; display: flex; align-items: center; gap: 10px; 
    transition: all 0.3s; cursor: default;
  }
  .tech-tag:hover { 
    background: #00ffcc; color: #021a30; box-shadow: 0 0 15px #00ffcc; 
    transform: translateY(-3px); 
  }
</style>

<!-- ========================================== -->
<!-- BLOQUE 1: PRESENTACIÓN                     -->
<!-- ========================================== -->
<div class="intro-card">
  <h2>Perfil Profesional</h2>
  <div class="intro-text">
    <p>Soy <strong>Alejandro Ramiro</strong>, estudiante del Doble Grado en Ingeniería. Mi pasión siempre ha sido entender cómo funcionan las cosas en el mundo físico y cómo podemos darles "cerebro" para automatizarlas.</p>
    <p>Actualmente me encuentro en mi último año, desarrollando mi Trabajo de Fin de Grado y preparándome para dar el salto definitivo a la industria. Busco conectar la mecánica de precisión con el control electrónico, aportando una visión completa que puentea el diseño físico y la lógica de programación.</p>
  </div>
</div>

<!-- ========================================== -->
<!-- BLOQUE 1.5: DOCENCIA Y COMUNICACIÓN        -->
<!-- ========================================== -->
<div class="intro-card" style="border-left: 4px solid #00ffcc;">
  <h2 style="border-bottom: none; margin-bottom: 15px; display: flex; align-items: center; gap: 10px;">
    <i class="fas fa-chalkboard-teacher" style="color: #00ffcc; background: #021a30; padding: 8px; border-radius: 8px; font-size: 0.8em;"></i> 
    Docencia y Comunicación Técnica
  </h2>
  <div class="intro-text">
    <p>
      Durante mi etapa universitaria, he compaginado mi formación con la impartición de clases particulares de <strong>Física, Matemáticas y Robótica</strong>. Más allá de la enseñanza académica, esta experiencia ha forjado una de mis competencias profesionales más valiosas: la capacidad de comunicación.
    </p>
    <p>
      La docencia me ha entrenado para desgranar problemas complejos, estructurar la información y transmitir conceptos altamente técnicos de forma clara y accesible, adaptándome siempre al nivel de quien me escucha. Estoy convencido de que en el sector industrial actual, <strong>saber diseñar un sistema eficiente es tan importante como saber explicarlo, documentarlo y defenderlo</strong> ante un equipo de trabajo o un cliente.
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
      <h4>2026 - 2027: Último Año e Industria (Actualidad)</h4>
      <ul>
        <li>Desarrollo del Trabajo de Fin de Grado (TFG).</li>
        <li>Consolidación de conocimientos y transición hacia el sector profesional.</li>
      </ul>
    </div>
    
    <div class="pcb-item">
      <div class="pcb-pad"></div>
      <h4>2025 - 2026: Especialización Mecánica (Erasmus+)</h4>
      <ul>
        <li>Estancia en la <strong>Politechnika Lubelska</strong> (Lublin, Polonia).</li>
        <li>Inmersión en un entorno internacional con docencia íntegramente en inglés.</li>
        <li>Desarrollo de competencias de adaptabilidad y trabajo con equipos multiculturales.</li>
      </ul>
    </div>

    <div class="pcb-item">
      <div class="pcb-pad"></div>
      <h4>2024 - 2025: Especialización Electrónica</h4>
      <ul>
        <li>Profundización en la rama de electrónica dentro del plan de estudios de la Universidad de Jaén.</li>
      </ul>
    </div>

    <div class="pcb-item">
      <div class="pcb-pad"></div>
      <h4>2022 - 2024: Inicio y Base Científica</h4>
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
    <h3><i class="fas fa-comment-dots" style="color: #0f4c75; font-size: 1em; background: transparent; width: auto; height: auto; margin:0;"></i> Comunicación y Docencia</h3>
    <ul class="skill-list">
      <li><i class="fas fa-award"></i> <span><strong>Inglés (C1):</strong>&nbsp; Competencia profesional completa y técnica.</span></li>
      <li><i class="fas fa-language"></i> <span><strong>Español:</strong>&nbsp; Nativo.</span></li>
      <li><i class="fas fa-chalkboard-teacher"></i> <span><strong>Mentoría STEM:</strong>&nbsp; Experiencia impartiendo clases particulares, desarrollando capacidad para simplificar conceptos complejos.</span></li>
    </ul>
  </div>

  <!-- Caja Derecha: Aptitudes Transversales -->
  <div class="skill-box">
    <h3><i class="fas fa-users-cog" style="color: #0f4c75; font-size: 1em; background: transparent; width: auto; height: auto; margin:0;"></i> Aptitudes Transversales</h3>
    <ul class="skill-list">
      <li><i class="fas fa-tools"></i> <span><strong>Resolución de problemas:</strong> Enfoque analítico y práctico.</span></li>
      <li><i class="fas fa-exchange-alt"></i> <span><strong>Adaptabilidad:</strong> Comodidad en entornos internacionales y equipos multiculturales.</span></li>
      <li><i class="fas fa-project-diagram"></i> <span><strong>Visión Global:</strong> Capacidad para entender el ciclo de vida completo del producto (Mecánica + Electrónica).</span></li>
    </ul>
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
    <div class="tech-tag"><i class="fas fa-microchip"></i> Arduino</div>
    <div class="tech-tag"><i class="fab fa-python"></i> Python</div>
    <div class="tech-tag"><i class="fas fa-bolt"></i> KiCad</div>
  </div>
</div>