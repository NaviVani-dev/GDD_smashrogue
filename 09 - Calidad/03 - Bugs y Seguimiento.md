# Bugs y Seguimiento

## Descripción de la sección

Registra problemas encontrados durante las pruebas y permite darles seguimiento.

## Reporte de bug

### B01 · El prototipo conserva el botón de agarre

**Título:** El prototipo conserva el botón de agarre.

**Versión:** Prototipo

**Nivel / escena:** Arena de combate

**Pasos para reproducir:**

1. Iniciar una partida con cualquier personaje.
2. Durante el combate, presionar I en el teclado o RB en el mando.
3. Observar la acción del personaje.

**Resultado esperado:** El personaje agarra al rival, puede golpearlo mientras lo sujeta y lanzarlo.

**Resultado actual:** El agarre (I / RB) funciona en todos los personajes, con golpes y lanzamientos. Ya no se considera un bug: el agarre forma parte del moveset (ver [[05 - Gestión de Cambios]]).

**Frecuencia:** Siempre

**Severidad:** Ninguna

**Evidencia:** 

**Estado:** Cerrado (no es un bug)

### B02 · La IA del paso 9 del tutorial tarda en conectar sus golpes

**Versión:** Versión final (1.0.0)

**Nivel / escena:** Tutorial, paso 9

**Pasos para reproducir:**

1. Avanzar el tutorial hasta el paso 9.
2. Esperar a que el enemigo conecte los 3 golpes requeridos para avanzar.

**Resultado esperado:** El enemigo conecta los 3 golpes en poco tiempo y el tutorial avanza.

**Resultado actual:** A la IA le cuesta conectar los 3 golpes, así que el paso se alarga.

**Frecuencia:** Frecuente

**Severidad:** Baja

**Estado:** Abierto

### B03 · El paso 10 del tutorial no cuenta el remate del enemigo

**Versión:** Versión final (1.0.0)

**Nivel / escena:** Tutorial, paso 10

**Pasos para reproducir:**

1. Avanzar el tutorial hasta el paso 10.
2. Rematar al enemigo como indica el paso.

**Resultado esperado:** El remate se cuenta y el tutorial pasa al siguiente paso.

**Resultado actual:** El remate no se cuenta y el tutorial no avanza.

**Frecuencia:** Por confirmar

**Severidad:** Alta (impide terminar el tutorial)

**Estado:** Abierto

### B04 · No se pueden elegir las opciones del menú de pausa

**Versión:** Versión final (1.0.0)

**Nivel / escena:** Menú de pausa

**Pasos para reproducir:**

1. Durante una partida, pulsar Esc / Start para abrir la pausa.
2. Intentar seleccionar CONTINUAR o VOLVER AL INICIO.

**Resultado esperado:** Las opciones se pueden seleccionar y ejecutan su acción.

**Resultado actual:** Ninguna opción se puede seleccionar. Solo se puede salir de la pausa pulsando Esc otra vez; no hay forma de volver al menú principal desde la partida.

**Frecuencia:** Siempre

**Severidad:** Media

**Estado:** Abierto

### B05 · El texto de los productos de la tienda se encima

**Versión:** Versión final (1.0.0)

**Nivel / escena:** Café Corp (tienda)

**Pasos para reproducir:**

1. Llegar a un piso con tienda.
2. Abrir la tienda en el mostrador y revisar la información de los productos.

**Resultado esperado:** El nombre, la descripción y el precio de cada producto se leen con claridad.

**Resultado actual:** Los textos se sobreponen unos con otros y dificultan la lectura.

**Frecuencia:** Siempre

**Severidad:** Media

**Estado:** Abierto

### B06 · Falta indicar cómo interactuar con la tienda

**Versión:** Versión final (1.0.0)

**Nivel / escena:** Café Corp (tienda)

**Pasos para reproducir:**

1. Llegar a un piso con tienda.
2. Observar si el juego indica cómo abrir la tienda.

**Resultado esperado:** Se muestra un aviso con el botón para comprar.

**Resultado actual:** El jugador no recibe una indicación clara de cómo usar la tienda.

**Frecuencia:** Siempre

**Severidad:** Media

**Estado:** Abierto

### B07 · Los drones vuelan demasiado alto

**Versión:** Versión final (1.0.0)

**Nivel / escena:** Pisos de combate con drones

**Pasos para reproducir:**

1. Jugar un piso en el que aparezcan drones.
2. Intentar alcanzarlos y destruirlos.

**Resultado esperado:** Los drones se pueden alcanzar con saltos y ataques aéreos sin demasiada dificultad.

**Resultado actual:** Los drones vuelan muy alto y cuesta mucho alcanzarlos para destruirlos rápido.

**Frecuencia:** Frecuente

**Severidad:** Baja (balance)

**Estado:** Abierto

### B08 · El tutorial dice que la cafetería aparece cada 5 pisos

**Versión:** Versión final (1.0.0)

**Nivel / escena:** Tutorial

**Pasos para reproducir:**

1. Desde el menú principal, entrar a TUTORIAL.
2. Leer el texto que explica la cafetería.

**Resultado esperado:** El tutorial indica que la cafetería aparece cada 10 pisos y un piso antes del jefe.

**Resultado actual:** El tutorial dice que la cafetería aparece cada 5 pisos.

**Frecuencia:** Siempre

**Severidad:** Baja

**Estado:** Abierto

## Registro

| ID | Bug | Severidad | Responsable | Estado |
|---|---|---|---|---|
| B01 | El prototipo conserva el botón de agarre (I / RB) | Ninguna | Mendoza Sanchez Axel Gibran (QA) | Cerrado: el agarre forma parte del juego |
| B02 | La IA del paso 9 del tutorial tarda en conectar sus 3 golpes | Baja | | Abierto |
| B03 | El paso 10 del tutorial no cuenta el remate del enemigo | Alta | | Abierto |
| B04 | No se pueden elegir las opciones del menú de pausa | Media | | Abierto |
| B05 | El texto de los productos de la tienda se encima | Media | | Abierto |
| B06 | Falta indicar cómo interactuar con la tienda | Media | | Abierto |
| B07 | Los drones vuelan demasiado alto | Baja | | Abierto |
| B08 | El tutorial dice que la cafetería aparece cada 5 pisos (es cada 10 y un piso antes del jefe) | Baja | | Abierto |

## Problemas conocidos

Características que no funcionan por completo o limitaciones pendientes en la versión entregada.

### Bugs abiertos

- **Tutorial, paso 10 (B03, severidad alta):** el remate del enemigo no se cuenta y el tutorial no avanza. No afecta a la partida normal, a la que se entra desde JUGAR.
- **Menú de pausa (B04):** no se pueden elegir CONTINUAR ni VOLVER AL INICIO. Para salir de la pausa hay que pulsar Esc / Start otra vez.
- **Tienda (B05 y B06):** los textos de los productos se enciman y falta una indicación clara de cómo usar la tienda.
- **Texto del tutorial (B08):** dice que la cafetería aparece cada 5 pisos, pero aparece cada 10 y un piso antes del jefe.
- **Tutorial, paso 9 (B02):** a la IA le cuesta conectar los 3 golpes requeridos, así que el paso se alarga.
- **Drones (B07):** vuelan muy alto y cuesta alcanzarlos.

### Limitaciones de la versión

- Los botones **OPCIONES** (menú principal y pausa) y **CRÉDITOS** aparecen, pero todavía no tienen función.
- No hay ajustes de audio, video, controles ni accesibilidad, y los controles no se pueden reasignar (ver [[04 - Guardado y Configuración]] y [[03 - Accesibilidad]]).
- El juego no guarda datos: si se cierra a mitad de partida, la partida se pierde.
- No se pide confirmación al volver al inicio desde la pausa ni al salir del juego.
- El mando no vibra.
- El rendimiento se comprobó jugando en una laptop de gama alta y otra de gama baja, pero no se midieron FPS, tiempos de carga ni uso de RAM con herramientas.


> **Navegación:** [[00 - Índice]] · ← [[02 - Pruebas]] · [[04 - Criterios de Aceptación]] →
