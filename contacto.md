---
layout: single
title: "Contacto"
author_profile: false
---

<style>
  /* Contenedor central de la página */
  .contact-container {
    max-width: 650px;
    margin: 40px auto;
    text-align: center;
  }
  
  /* Texto introductorio */
  .contact-intro {
    font-size: 1.2em;
    color: #495057;
    margin-bottom: 40px;
    line-height: 1.6;
  }
  
  /* Estilo de los bloques de conexión */
  .contact-link {
    display: flex;
    align-items: center;
    background-color: #021a30; /* Azul oscuro de la placa */
    color: #bbe1fa !important;
    padding: 20px 30px;
    margin-bottom: 20px;
    border-radius: 8px;
    text-decoration: none;
    font-size: 1.2em;
    border: 1px solid #0f4c75;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }
  
  /* Iconos (Email, GitHub, LinkedIn) */
  .contact-link i {
    font-size: 1.8em;
    margin-right: 25px;
    color: #00ffcc; /* Cyan eléctrico */
    min-width: 40px;
    text-align: center;
  }
  
  /* Textos de los enlaces */
  .contact-link span {
    font-weight: 500;
    letter-spacing: 0.5px;
  }
  
  /* Animación Hover: Desplazamiento y brillo */
  .contact-link:hover {
    transform: translateX(15px); /* Se desliza a la derecha */
    border-color: #00ffcc;
    box-shadow: 0 4px 15px rgba(0, 255, 204, 0.15);
    color: #ffffff !important;
  }
  
  /* Barra lateral que se enciende en Hover */
  .contact-link::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    height: 100%;
    width: 6px;
    background-color: #00ffcc;
    transform: scaleY(0);
    transition: transform 0.3s ease;
    transform-origin: bottom;
  }
  
  .contact-link:hover::before {
    transform: scaleY(1);
  }
</style>

<div class="contact-container">
  
  <p class="contact-intro">
    ¿Tienes algún proyecto en mente, una propuesta profesional o simplemente quieres comentar algún desarrollo? <strong>Mis canales están abiertos.</strong>
  </p>

  <!-- 1. Email -->
  <a href="mailto:alejandroramiroolmo@gmail.com" class="contact-link">
    <i class="fas fa-envelope"></i>
    <span>alejandroramiroolmo@gmail.com</span>
  </a>

  <!-- 2. GitHub -->
  <a href="https://github.com/AlejandroRamiroOlmo" class="contact-link" target="_blank">
    <i class="fab fa-github"></i>
    <span>github.com/AlejandroRamiroOlmo</span>
  </a>

  <!-- 3. LinkedIn -->
  <a href="https://www.linkedin.com/in/TU-ENLACE-AQUI" class="contact-link" target="_blank">
    <i class="fab fa-linkedin"></i>
    <span>Conecta conmigo en LinkedIn</span>
  </a>

</div>