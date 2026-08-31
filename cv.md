---
layout: single
title: "Currículum Vítae"
author_profile: true
---

<style>
  /* ========================================== */
  /* ESTILOS DE LA PÁGINA DE CV                 */
  /* ========================================== */

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

  /* 2. Tarjeta central de descarga */
  .cv-download-card {
    background-color: #021a30; 
    background-image: 
      linear-gradient(rgba(79, 195, 247, 0.05) 1px, transparent 1px),
      linear-gradient(90deg, rgba(79, 195, 247, 0.05) 1px, transparent 1px);
    background-size: 20px 20px; 
    border: 2px solid #0f4c75;
    border-radius: 12px;
    color: #bbe1fa;
    padding: 40px 30px;
    text-align: center;
    position: relative;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
    max-width: 600px;
    margin: 40px auto;
  }

  .cv-icon-wrapper {
    font-size: 3.5em;
    color: #00ffcc;
    margin-bottom: 20px;
    text-shadow: 0 0 15px rgba(0, 255, 204, 0.3);
  }

  .cv-download-card h2 {
    margin-top: 0;
    color: #ffffff;
    font-size: 1.6em;
    border-bottom: none;
    margin-bottom: 15px;
  }

  .cv-download-card p {
    color: #bbe1fa;
    font-size: 1.05em;
    line-height: 1.6;
    margin-bottom: 30px;
    max-width: 450px;
    margin-left: auto;
    margin-right: auto;
  }

  .cv-meta {
    font-size: 0.85em;
    color: #3282b8;
    margin-bottom: 25px;
    letter-spacing: 1px;
    text-transform: uppercase;
  }

  .btn-download-neon {
    display: inline-block;
    padding: 14px 30px;
    border: 2px solid #00ffcc;
    color: #00ffcc !important;
    text-decoration: none;
    border-radius: 6px;
    font-weight: bold;
    font-size: 1.1em;
    transition: all 0.3s ease;
    background: transparent;
    box-shadow: 0 0 10px rgba(0, 255, 204, 0.1);
  }

  .btn-download-neon:hover {
    background: #00ffcc;
    color: #021a30 !important;
    box-shadow: 0 0 25px #00ffcc;
    transform: translateY(-3px);
  }

  .btn-download-neon i {
    margin-right: 8px;
  }

  .cv-secondary-action {
    margin-top: 20px;
  }
  
  .cv-secondary-action a {
    color: #a8dadc;
    text-decoration: none;
    font-size: 0.9em;
    transition: color 0.2s;
  }

  .cv-secondary-action a:hover {
    color: #00ffcc;
    text-decoration: underline;
  }
</style>

<!-- TARJETA CENTRAL DE DESCARGA -->
<div class="cv-download-card">
  
  <div class="cv-icon-wrapper">
    <i class="fas fa-file-pdf"></i>
  </div>

  <h2>Currículum Vítae Oficial</h2>
  
  <div class="cv-meta">
    Actualizado 2026
  </div>

  <p>
    ¿Necesitas una copia física o un documento formal para procesos de selección? Puedes descargar mi currículum completo directamente en formato PDF.
  </p>

 <!-- Enlace de descarga  -->
  <a href="/assets/pdf/cv-alejandro-ramiro.pdf" class="btn-download-neon" download>
    <i class="fas fa-download"></i> Descargar CV en PDF
  </a>

  <!-- Enlace para abrir en pestaña nueva (Corregido) -->
  <div class="cv-secondary-action">
    <a href="/assets/pdf/cv-alejandro-ramiro.pdf" target="_blank" type="application/pdf" rel="noopener noreferrer">
      <i class="fas fa-external-link-alt" style="font-size: 0.8em; margin-right: 4px;"></i> Abrir documento en una nueva pestaña
    </a>
  </div>

</div>