---
layout: single
title: "Estación Industrial"
author_profile: false
---

<!-- ESTILOS PARA CONSERVAR EL DISEÑO DEL PORTFOLIO -->
<style>
  body { background-color: #021220; color: #bbe1fa; }
  h1, h2, h3, h4, h5, h6 { color: #ffffff; }
  h2 { border-bottom: 1px solid #0f4c75; padding-bottom: 8px; color: #00ffcc; margin-top: 45px; }
  
  .ficha-tecnica {
    background: #021a30; border: 1px solid #0f4c75; border-radius: 12px;
    padding: 20px; margin-bottom: 35px; box-shadow: 0 4px 15px rgba(0,0,0,0.2);
  }
  .ficha-tecnica ul { list-style: none; padding: 0; margin: 0; display: flex; flex-wrap: wrap; gap: 12px; }
  .ficha-tecnica li { background: rgba(0,255,204,0.05); border: 1px solid rgba(0,255,204,0.3); color: #00ffcc; padding: 6px 14px; border-radius: 20px; font-size: 0.85em; font-weight: 600; }
  
  .btn-neon {
    display: inline-block; padding: 10px 22px; border: 1.5px solid #00ffcc;
    color: #00ffcc !important; text-decoration: none; border-radius: 5px;
    font-weight: bold; transition: 0.3s; font-size: 0.9em; background: #021a30; margin-top: 15px;
  }
  .btn-neon:hover { background: #00ffcc; color: #021a30 !important; box-shadow: 0 0 12px rgba(0,255,204,0.5); }
  
  /* Ajustes para tablas en modo oscuro */
  table { width: 100%; border-collapse: collapse; margin-top: 15px; background: #021a30; color: #bbe1fa; border-radius: 8px; overflow: hidden; }
  th { background: #0f4c75; color: #ffffff; padding: 12px; text-align: left; }
  td { padding: 10px 12px; border-bottom: 1px solid #0f4c75; }
</style>

<!-- FICHA TÉCNICA -->
<div class="ficha-tecnica">
  <ul>
    <li><i class="fas fa-tag"></i> Proyecto Académico</li>
    <li><i class="fas fa-microchip"></i> PLC Siemens S7-1200</li>
    <li><i class="fas fa-code"></i> Lenguaje SCL</li>
  </ul>
</div>

## 1. El Reto y Objetivo
El proyecto consistía en automatizar una estación de clasificación de piezas simulada. El sistema debía ser capaz de detectar materiales mediante sensores inductivos y ópticos, y clasificarlos usando actuadores neumáticos.

## 2. Desarrollo y Solución Técnica
En lugar de utilizar lenguaje de contactos (Ladder), se optó por SCL (Structured Control Language) debido a la complejidad matemática del proceso de clasificación. Se estructuró el código en bloques lógicos (FBs) independientes.

## 3. Contenido Multimedia (Diagramas y Lógica)
A falta de imágenes físicas de gran volumen, aquí presento el mapa de Entradas/Salidas conectado al autómata y la lógica de programación empleada.

| Dirección | Símbolo | Tipo | Descripción |
| :--- | :--- | :--- | :--- |
| `%I0.0` | `S_Pieza` | BOOL | Sensor óptico de presencia |
| `%I0.1` | `S_Metal` | BOOL | Sensor inductivo de material |
| `%Q0.0` | `Cil_Avance` | BOOL | Electroválvula de empuje |

**Fragmento de la lógica del temporizador en SCL:**

```scl
IF "S_Pieza" AND NOT "S_Metal" THEN
    "T_Clasificacion".TON(IN := TRUE, PT := T#2S);
    
    IF "T_Clasificacion".Q THEN
        "Cil_Avance" := TRUE;
    END_IF;
ELSE
    "Cil_Avance" := FALSE;
END_IF;