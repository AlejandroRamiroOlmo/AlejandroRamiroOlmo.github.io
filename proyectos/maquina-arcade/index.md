---
layout: single
title: "Máquina Arcade"
permalink: /proyectos/maquina-arcade/

author_profile: false
---

<!-- ESTILOS PARA CONSERVAR EL DISEÑO DEL PORTFOLIO -->
<style>
  /* Fondo oscuro y texto claro para toda la página */
  body { background-color: #021220; color: #bbe1fa; }
  h1, h2, h3, h4, h5, h6 { color: #ffffff; }
  
  /* Subtítulos con toque cian */
  h2 { border-bottom: 1px solid #0f4c75; padding-bottom: 8px; color: #00ffcc; margin-top: 45px; }
  
  /* Diseño de la Ficha Técnica */
  .ficha-tecnica {
    background: #021a30; border: 1px solid #0f4c75; border-radius: 12px;
    padding: 20px; margin-bottom: 35px; box-shadow: 0 4px 15px rgba(0,0,0,0.2);
  }
  .ficha-tecnica ul { list-style: none; padding: 0; margin: 0; display: flex; flex-wrap: wrap; gap: 12px; }
  .ficha-tecnica li { background: rgba(0,255,204,0.05); border: 1px solid rgba(0,255,204,0.3); color: #00ffcc; padding: 6px 14px; border-radius: 20px; font-size: 0.85em; font-weight: 600; }
  
  /* Botón Neón */
  .btn-neon {
    display: inline-block; padding: 10px 22px; border: 1.5px solid #00ffcc;
    color: #00ffcc !important; text-decoration: none; border-radius: 5px;
    font-weight: bold; transition: 0.3s; font-size: 0.9em; background: #021a30; margin-top: 15px;
  }
  .btn-neon:hover { background: #00ffcc; color: #021a30 !important; box-shadow: 0 0 12px rgba(0,255,204,0.5); }
  
  /* Galería Multimedia */
  .multimedia-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 15px; margin-top: 20px; }
  .multimedia-grid img { width: 100%; aspect-ratio: 1/1; object-fit: cover; border-radius: 8px; border: 2px solid #0f4c75; transition: 0.3s; cursor: pointer; }
  .multimedia-grid img:hover { border-color: #00ffcc; transform: scale(1.03); box-shadow: 0 8px 20px rgba(0,255,204,0.15); }
</style>

<!-- FICHA TÉCNICA -->
<div class="ficha-tecnica">
  <ul>
    <li><i class="fas fa-tag"></i> Proyecto Personal</li>
    <li><i class="fas fa-cogs"></i> Desarrollo Integral</li>
    <li><i class="fas fa-clock"></i> 3 meses</li>
  </ul>
</div>

## 1. El Reto y Objetivo
El objetivo de este proyecto era construir una máquina recreativa desde cero. No quería limitarme a comprar un mueble prefabricado, sino diseñar los planos, cortar la madera, realizar la instalación eléctrica y configurar el sistema de emulación por software.

## 2. Desarrollo y Solución Técnica
Se diseñó la estructura principal utilizando SolidWorks para garantizar que las medidas fueran ergonómicas. La gestión de los controles se centralizó a través de una placa Arduino configurada como dispositivo HID.

## 3. Contenido Multimedia
En esta galería puedes ver la evolución del montaje físico, desde los tableros de madera en bruto hasta la instalación del cableado interno y el resultado final.

<div class="multimedia-grid">
  <!-- Sustituye estas rutas por tus fotos reales -->
  <img src="/assets/images/placeholder.png" alt="Proceso 1">
  <img src="/assets/images/placeholder.png" alt="Proceso 2">
  <img src="/assets/images/placeholder.png" alt="Proceso 3">
  <img src="/assets/images/placeholder.png" alt="Proceso 4">
</div>

<a href="#" class="btn-neon"><i class="fas fa-play"></i> Ver Vídeo Demostrativo</a>

## 4. Resultados, Aprendizajes y Mejoras
El proyecto final es completamente funcional. Descubrí que la gestión del cableado interno debe planificarse antes de ensamblar el mueble. Para versiones futuras, implementaría una fuente de alimentación de mayor eficiencia para evitar sobrecalentamientos.