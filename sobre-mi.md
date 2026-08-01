---
layout: single
title: "Sobre mí"
author_profile: true
---

<style>
  /* ========================================== */
  /* ESTILOS DE LA PÁGINA "SOBRE MÍ"            */
  /* ========================================== */

  /* 1. Presentación (Textos) */
  .intro-text { 
    font-size: 1.15em; 
    line-height: 1.6; 
    color: #495057; 
    margin-bottom: 40px; 
    text-align: justify; 
  }

  /* 2. Trayectoria PCB adaptada a una sola columna */
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

  /* 3. Panel de Idiomas y Soft Skills */
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
  .skill-list li { margin-bottom: 15px; display: flex; align-items: center; font-size: 1.05em; color: #495057; }
  
  /* Iconos de las Skills */
  .skill-list i { 
    font-size: 1.2em; color: #00ffcc; background: #021a30; 
    width: 35px; height: 35px; display: flex; align-items: center; 
    justify-content: center; border-radius: 8px; margin-right: 15px; 
  }

  /* 4. Inventario Tecnológico (Tags) */
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

<!-- BLOQUE 1: PRESENTACIÓN -->
<div class="intro-text">
  <p>Soy <strong>Alejandro Ramiro</strong>, estudiante del Doble Grado en Ingeniería. Mi pasión siempre ha sido entender cómo funcionan las cosas en el mundo físico y cómo podemos darles "cerebro" para automatizarlas. </p>
  <p>Actualmente me encuentro en mi último año, desarrollando mi Trabajo de Fin de Grado y preparándome para dar el salto definitivo a la industria. Busco conectar la mecánica de precisión con el control electrónico, aportando una visión completa que puentea el diseño físico y la lógica de programación.</p>
</div>

<!-- BLOQUE 2: TRAYECTORIA ACADÉMICA (ESTILO PCB) -->
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

<!-- BLOQUE 3: IDIOMAS Y SOFT SKILLS -->
<div class="skills-container">
  <!-- Caja Izquierda: Idiomas -->
  <div class="skill-box">
    <h3><i class="fas fa-globe-europe" style="color: #0f4c75; font-size: 1em; background: transparent; width: auto; height: auto; margin:0;"></i> Idiomas</h3>
    <ul class="skill-list">
      <li><i class="fas fa-certificate"></i> <strong>Inglés:</strong>&nbsp; Nivel C1 (Avanzado)</li>
      <li><i class="fas fa-language"></i> <strong>Español:</strong>&nbsp; Nativo</li>
    </ul>
  </div>

  <!-- Caja Derecha: Soft Skills -->
  <div class="skill-box">
    <h3><i class="fas fa-users-cog" style="color: #0f4c75; font-size: 1em; background: transparent; width: auto; height: auto; margin:0;"></i> Soft Skills</h3>
    <ul class="skill-list">
      <li><i class="fas fa-tools"></i> Resolución de problemas</li>
      <li><i class="fas fa-exchange-alt"></i> Adaptabilidad internacional</li>
      <li><i class="fas fa-project-diagram"></i> Enfoque multidisciplinar</li>
    </ul>
  </div>
</div>

<!-- BLOQUE 4: STACK TECNOLÓGICO -->
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