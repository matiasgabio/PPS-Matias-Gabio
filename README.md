![Logo Institucional](images/LogoInstitucional.png)
# PPS - Matias Gabio

# Índice

- [1. Introducción](#1-introducción)
- [2. Descripción de la Empresa](#2-descripción-de-la-empresa)

- [3. Proyecto 1 – Sistema de Control de Premix](#3-proyecto-1--sistema-de-control-de-premix-software)
  - [3.1 Objetivo](#31-objetivo)
  - [3.2 Funcionalidades](#32-funcionalidades)
  - [3.3 Desarrollo del Software](#33-desarrollo-del-software)
  - [3.4 Pruebas y Validación](#34-pruebas-y-validación)
  - [3.5 Resultados y Aportes](#35-resultados-y-aportes)
  - [3.6 Conclusiones del Proyecto 1](#36-conclusiones-del-proyecto-1)

- [4. Proyecto 2 – Máquina de Reproceso de Pan y Rebozado](#4-proyecto-2--máquina-de-reproceso-de-pan-y-rebozado)
  - [4.1 Objetivo](#41-objetivo)
  - [4.2 Requerimientos](#42-requerimientos)
  - [4.3 Diseño Mecánico](#43-diseño-mecánico)
  - [4.4 Diseño Eléctrico](#44-diseño-eléctrico)
  - [4.5 Diseño Electrónico y Control](#45-diseño-electrónico-y-control)
  - [4.6 Integración y Montaje](#46-integración-y-montaje)
  - [4.7 Pruebas y Validación](#47-pruebas-y-validación)
  - [4.8 Resultados y Aportes](#48-resultados-y-aportes)
  - [4.9 Conclusiones del Proyecto 2](#49-conclusiones-del-proyecto-2)

- [5. Conclusiones Generales](#5-conclusiones-generales)
- [6. Agradecimientos](#6-agradecimientos)
- [7. Anexos](#7-anexos)


# 1. Introducción

Este repositorio reúne los trabajos realizados en el marco del proyecto desarrollado durante las Prácticas Profesionales Supervisadas (PPS) de la carrera Ingeniería en Mecatrónica de la Facultad de Ingeniería, Universidad Nacional de Lomas de Zamora. 

El proyecto fue llevado a cabo en Molinos Río de la Plata. Comprendió el desarrollo de un software específico ("Programa para control de premix") y el diseño de una máquina que integra componentes mecánicos y eléctricos, orientada a mejorar procesos internos y aportar una solución aplicable al entorno industrial de la empresa ("Sistema de reproceso de pan y rebozado").

# 2. Descripción de la Empresa


# 3. Proyecto 1 – Sistema de Control de Premix
## 3.1 Objetivo
El objetivo principal de este software es garantizar la trazabilidad, precisión y eficiencia en la elaboración de premix, reduciendo errores humanos, tiempos y asegurando el cumplimiento de los estándares de calidad.

## 3.2 Funcionalidades
El software está diseñado para optimizar y controlar el proceso de elaboración de premix de horneables en la planta de Esteban Echeverría. Este programa permite realizar un seguimiento preciso de las recetas seleccionadas, asegurando que los ingredientes sean los correctos, sus pesos sean verificados adecuadamente y que las cantidades pesadas sean notificadas de manera automática en SAP.
### Principales funcionalidades:
- Identificación de usuario: El operador podrá identificarse en el programa con la tarjeta RFID única e irrepetible que proporciona la empresa.
- Selección de recetas: El usuario puede elegir la receta correspondiente al premix que se está elaborando.
- Verificación de ingredientes: Se valida cada ingrediente mediante un script que conecta el software con SAP, utilizando las etiquetas generadas en el almacén.
- Control de peso: La conexión con una balanza permite registrar los pesos de los ingredientes en tiempo real, asegurando la precisión en cada etapa del proceso y advirtiendo al operador el pesaje incorrecto del ingrediente.
- Notificación automatizada: Una vez pesadas las cantidades requeridas, el software se encarga de notificar automáticamente a SAP (mediante la transacción CORK) la cantidad de bolsas procesadas, simplificando la carga administrativa.
