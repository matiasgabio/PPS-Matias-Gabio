<img width="1920" height="850" alt="image" src="https://github.com/user-attachments/assets/6b823177-2214-43a0-a31b-f84b89a5ea9c" />

# PPS - Matias Gabio

# Índice

- [1. Introducción](#1-introducción)
- [2. Descripción de la Empresa](#2-descripción-de-la-empresa)

- [3. Proyecto 1 – Sistema de Control de Premix](#3-proyecto-1--sistema-de-control-de-premix-software)
  - [3.1 Objetivo](#31-objetivo)
  - [3.2 Funcionalidades](#32-funcionalidades)
  - [3.3 Uso del Software](#34-uso-del-software)

- [4. Proyecto 2 – Equipo de Reproceso de Pan y Rebozado](#4-proyecto-2--equipo-de-reproceso-de-pan-y-rebozado)
  - [4.1 Objetivo](#41-objetivo)
  - [4.2 Funcionalidades](#42-funcionalidades)
  - [4.3 Uso del equipo](#43-uso-del-equipo)

- [5. Conclusiones Generales](#5-conclusiones-generales)


# 1. Introducción

Este repositorio reúne los trabajos realizados en el marco del proyecto desarrollado durante las Prácticas Profesionales Supervisadas (PPS) de la carrera Ingeniería en Mecatrónica de la Facultad de Ingeniería, Universidad Nacional de Lomas de Zamora. 

El proyecto fue llevado a cabo en Molinos Río de la Plata. Comprendió el desarrollo de un software específico ("Programa para control de premix") y el diseño de una máquina que integra componentes mecánicos y eléctricos, orientada a mejorar procesos internos y aportar una solución aplicable al entorno industrial de la empresa ("Sistema de reproceso de pan y rebozado").

# 2. Descripción de la Empresa
Molinos Río de la Plata S.A. es una de las principales compañías del sector alimenticio en Argentina. Fundada en 1902, posee una trayectoria de más de un siglo elaborando alimentos, consolidándose como un referente en la industria. La empresa cuenta con más de 2.800 colaboradores y opera 14 plantas productivas distribuidas en el país, donde se fabrican productos pertenecientes a marcas ampliamente reconocidas, tales como Matarazzo, Lucchetti, Granja del Sol, Gallo, Gallo Snacks, Cocinero, Exquisita, La Salteña, Bodega Nieto Senetiner, entre otras.
Dentro de su infraestructura industrial se destaca la planta de Esteban Echeverría, donde se producen rebozador, pan rallado, horneables, premezclas, obleas y bizcochos sin TACC. Es en esta planta donde se desarrollaron los proyectos correspondientes a la Práctica Profesional Supervisada.

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

## 3.3 Uso del Software
- Inicio sesión SAP
  Inicialmente para evitar errores futuros en el programa se debe iniciar sesión en SAP GUI
  <img width="915" height="481" alt="image" src="https://github.com/user-attachments/assets/4705d130-4a80-4ee7-979b-061a2c8089e5" />
  Una vez iniciada la sesión no se requiere ninguna acción más dentro de SAP.
  
- Identificación del usuario
  <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/d745091e-aa7d-45b5-98ea-fd99cc8c7c96" />

  Al aproximar la tarjeta al lector automáticamente se detectará el nombre del usuario:
  <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/d42456d0-2d76-4b6c-a306-a00948403110" />

  En caso de que el usuario no este registrado el programa lo advertirá y pedirá nuevamente la aproximación de la tarjeta
  <img width="915" height="515" alt="image" src="https://github.com/user-attachments/assets/814ae7d7-9c01-41d1-be14-b38a15c749dc" />

- Selección de receta
  <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/855d2c8f-4c5f-4ecd-bcd8-774f9cfe1361" />

- Verificación de ingredientes
  <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/e48c627f-7729-4da1-8b96-5039d2d0d286" />

  Botón 'CAMBIAR RECETA': regresa a la pantalla anterior. Permite editar la selección de receta en caso de haber seleccionado una incorrecta.

  Para verificar los ingredientes se debe escanear el código de barras de la etiqueta del insumo proveniente del almacén.
  <img width="849" height="345" alt="image" src="https://github.com/user-attachments/assets/5741f3dd-6f64-49ea-9e1b-c043e37ed7a2" />

  Una vez escaneada pedirá el programa acceso a SAP. Solo se debe hacer click en 'OK'.
  <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/b5774775-bb82-4738-b9e7-ddf6ff8a55bb" />

  - Ingrediente pertenece a la receta:
    <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/f16a6cbb-582d-44ee-b188-813f7b89b749" />

    Se colocará el fondo en verde del ingrediente escaneado.

  - Ingrediente no pertenece a la receta:
    <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/61707f47-84cb-4afc-8f2f-14357c8f4ad4" />

    Saldrá un cartel de advertencia indicando el desvío.

Una vez escaneados todos los ingredientes de la receta, el programa pasará automáticamente a la próxima pantalla.

- Seteo de cantidad de bolsas
  <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/d3724dc2-51b4-4070-adfe-c0f5fada93af" />

  En esta sección el operador deberá colocar la cantidad de bolsas que pesará y presionar en el botón 'COMENZAR PESADAS'.

  <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/cecd6aa3-5333-4747-9182-af008708ddf2" />

  Automáticamente, se enviarán a imprimir las etiquetas que se deben pegar en las bolsas de los premix con los siguientes datos completados por el programa:
  
  <img width="352" height="207" alt="image" src="https://github.com/user-attachments/assets/a57c4267-60f6-4075-8020-bcb9e4222bdd" />

- Pesadas
  Seteadas la cantidad de bolsas, el programa comenzará a hacer un control sobre la lectura de la balanza y el peso del ingrediente actual.
  
  <img width="915" height="515" alt="image" src="https://github.com/user-attachments/assets/395cbe43-91e8-4b84-89eb-7851b8183906" />

  Botón 'Siguiente Ingrediente': Este permite pasar al próximo ingrediente (solamente en el primer ingrediente) sin necesidad de completar las bolsas que en la pantalla anterior seteo el usuario.
  Una vez que el usuario coloque el ingrediente en la bolsa y el peso se encuentre dentro del rango de tolerancia permitido, al presionar la tecla 'Enter', los datos se guardarán automáticamente. Se descontará la bolsa de la cantidad restante, y se mostrará el mensaje: 'EL PESO DEL INGREDIENTE ES CORRECTO'.

  <img width="915" height="513" alt="image" src="https://github.com/user-attachments/assets/8b16e30b-b31f-4c60-ab25-4266c2efb951" />

  En caso de que el valor pesado no corresponde al peso de la receta, el valor de la bolsa no se restará y se hará una advertencia al usuario indicando el peso incorrecto.

  <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/9f524fa4-3634-4102-9e0d-998e824f040f" />

  Una vez completadas las bolsas con el ingrediente, el programa mostrará un cartel indicando el cambio de ingrediente con su respectivo nombre.

  <img width="915" height="516" alt="image" src="https://github.com/user-attachments/assets/9903de1b-6fa2-4cb4-a2b3-2642d0b10e57" />

  El proceso se repite con todos los ingredientes de la receta.
  Finalizada la receta, el programa se lo indicará al usuario y se pasará a la pantalla de notificación.

  <img width="915" height="515" alt="image" src="https://github.com/user-attachments/assets/618c306d-4c2d-4cfd-92d5-2f1feaa074c7" />

  Como dato a completar manualmente se pide la orden de proceso y el tipo de notificación a realizar.

  <img width="915" height="514" alt="image" src="https://github.com/user-attachments/assets/2851fc67-01a2-4b9b-babb-cace901216bc" />

  Con estos valores al presionar el botón 'NOTIFICAR', el programa ejecutará un script en SAP automáticamente con la transacción CORK.

# 4. Proyecto 2 – Equipo de Reproceso de Pan y Rebozado
## 4.1 Objetivo
El objetivo principal de este equipo es asegurar un reproceso eficiente, continuo y seguro del pan rallado y rebozador, evitando acumulaciones, optimizando el flujo hacia el silo de producto terminado y garantizando la calidad del material reprocesado mediante una operación confiable y autónoma.

## 4.2 Funcionalidades
El equipo de reproceso está diseñado para garantizar un flujo continuo, seguro y eficiente del pan rallado y rebozador hacia el silo de producto terminado. Su operación automática, junto con los enclavamientos, asegura que cada etapa del proceso se realice en el orden correcto para evitar saturaciones.

### Principales funcionalidades:
- Secuencia automática de encendido:
El sistema garantiza que los equipos arranquen únicamente en el orden correcto: Turbina → Exclusa → Tamiz
Esto evita acumulaciones o sobrecargas de producto en cualquier punto del circuito.
- Selección y derivación del producto:
La selectora permite elegir Pan o Rebozador, accionando automáticamente la válvula derivadora del ciclón para dirigir el material a la línea correspondiente.
- Tamizado y extracción de impurezas:
El producto ingresado por la tolva pasa por el tamiz, que retira cuerpos extraños y los expulsa por la descarga, asegurando calidad del material reprocesado.
- Transporte y envío al silo:
El material tamizado es impulsado por la bomba hacia el ciclón superior y descargado directamente al silo final, permitiendo un reproceso continuo y sin acumulación de producto.

## 4.3 Uso del equipo
El orden de encendido de los equipos es:

1 – Turbina

2 – Exclusa

3 – Tamiz

<img width="408" height="326" alt="image" src="https://github.com/user-attachments/assets/9f556318-9860-4ad5-aa86-ddb533a27a13" />

Los equipos se encuentran enclavados para no permitir ningún encendido incorrecto para evitar saturaciones de producto en los distintos puntos.

La selectora superior permite elegir el tipo de producto, y comanda la válvula (7) que se encuentra en la parte superior, a la salida del ciclón (8) y deriva a Pan (5) o Rebozador (6)

<img width="389" height="420" alt="image" src="https://github.com/user-attachments/assets/0085a8ef-79ff-46c5-b605-f894be5387b4" /> <img width="331" height="420" alt="image" src="https://github.com/user-attachments/assets/e7e8728e-2d99-4394-9c55-2296cbc160cf" />

El volcado del producto se realiza en la tolva (10), y pasa por el tamiz, que elimina cualquier cuerpo extraño, expulsándolos del sistema por la descarga (9). El producto sube impulsado por bomba a través de la cañería vertical hasta el ciclón en la parte superior:

<img width="355" height="420" alt="image" src="https://github.com/user-attachments/assets/4e216950-c7bc-4301-bbad-776ea380bb24" />

Foto del equipo:

<img width="598" height="797" alt="image" src="https://github.com/user-attachments/assets/4070e803-b14f-4d58-b787-b9f31365267b" /> 

Flujo del proceso:

<img width="254" height="405" alt="image" src="https://github.com/user-attachments/assets/3067b82b-382f-482c-8f68-721b8853f23e" />



# 5. Conclusiones Generales
- Desarrollo de programa para el guiado en la elaboración de premix
  Áreas disciplinares involucradas: Programación.
  Relación con la formación: La actividad se vincula con los conocimientos adquiridos en materias de programación, bases de datos y automatización de procesos. Permite aplicar conceptos de software orientado a la industria, como la interacción hombre-máquina, la validación de datos y la integración de sistemas con plataformas de gestión (SAP), asegurando precisión y trazabilidad en la elaboración de premix.

- Desarrollo de equipo para reproceso de pan rallado y rebozador
  Áreas disciplinares involucradas: Mecánica y electrónica.
  Relación con la formación: La experiencia se relaciona con los saberes adquiridos en diseño mecánico y electrónica aplicada. La instalación integra mecanismos de transporte y reproceso con actuadores y sensores, aplicando principios de automatización industrial. Esto permite llevar a la práctica la combinación de disciplinas propias de la Ingeniería Mecatrónica para optimizar procesos en la industria.


