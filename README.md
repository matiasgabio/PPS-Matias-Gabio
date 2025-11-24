![Logo Institucional](images/LogoInstitucional.png)
# PPS - Matias Gabio

# Índice

- [1. Introducción](#1-introducción)
- [2. Descripción de la Empresa](#2-descripción-de-la-empresa)

- [3. Proyecto 1 – Sistema de Control de Premix](#3-proyecto-1--sistema-de-control-de-premix-software)
  - [3.1 Objetivo](#31-objetivo)
  - [3.2 Funcionalidades](#32-funcionalidades)
  - [3.3 Uso del Software](#34-uso-del-software)

- [4. Proyecto 2 – Máquina de Reproceso de Pan y Rebozado](#4-proyecto-2--máquina-de-reproceso-de-pan-y-rebozado)
  - [4.1 Objetivo](#41-objetivo)
  - [4.2 Funcionalidades](#42-funcionalidades)
  - [4.3 Uso del Software](#34-uso-del-software)

- [5. Conclusiones Generales](#5-conclusiones-generales)
- [6. Anexos](#6-anexos)


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

# 4. Proyecto 2 – Máquina de Reproceso de Pan y Rebozado
## 4.1 Objetivo



  
