# Estructura del Contenido

## Descripción de la sección

Organiza el contenido del videojuego en unidades manejables: mundos, capítulos, zonas, niveles, misiones y desafíos.

## Estructura

Cada **nivel** corresponde a un **piso del edificio**. La partida comienza en el piso 1 y puede avanzar hasta el piso 100, donde se encuentra el jefe final.

Cada piso de combate funciona como una **arena** en la que se desarrollan las rondas de enemigos. El jugador se desplaza dentro de ella para combatir, posicionarse y recuperarse de los lanzamientos, sin recorrer distintas zonas para completar el nivel. Las plataformas y los obstáculos que se incorporen forman parte del espacio de combate.

Las **secciones** agrupan pisos según su ambientación dentro del edificio. Cada sección puede utilizar distintos **arquetipos de escenario**: diseños reutilizables que representan tipos de espacios corporativos y pueden presentar pequeñas variaciones entre pisos.

Un arquetipo de escenario puede utilizarse en varios niveles. Por tanto, los 100 niveles no requieren 100 escenarios únicos.

El edificio de Nuddle se divide en **5 secciones de 20 pisos**. Cada sección termina con un mini-jefe (pisos 20, 40, 60 y 80) y la última, con Big Data, de modo que la ambientación cambia junto con los picos de dificultad. Cada sección tiene dos tiendas.

| Sección | Pisos | Arquetipos de escenario | Tiendas | Cierre |
|---|---|---|---|---|
| Planta baja | 1–20 | La Recepción (piso 1), sala de espera y vestíbulo de ascensores | 10 y 19 | Mini-jefe en el piso 20 |
| Oficinas abiertas | 21–40 | Oficina de cubículos y sala de impresoras y archivo | 30 y 39 | Mini-jefe en el piso 40 |
| Centro de datos | 41–60 | Sala de servidores y pasillo de cableado | 50 y 59 | Mini-jefe en el piso 60 |
| Marketing y publicidad | 61–80 | Estudio de publicidad y sala de pantallas con anuncios | 70 y 79 | Mini-jefe en el piso 80 |
| Pisos ejecutivos | 81–100 | Oficina ejecutiva, sala de juntas y Oficina del CEO (piso 100) | 90 y 99 | Big Data en el piso 100 |

La Recepción y la Oficina del CEO son arquetipos únicos. Los demás se reutilizan entre los pisos de su sección.

```text
Edificio de Nuddle — Hasta 100 niveles por partida
├── Secciones de ambientación
│   ├── Planta baja (pisos 1–20)
│   ├── Oficinas abiertas (pisos 21–40)
│   ├── Centro de datos (pisos 41–60)
│   ├── Marketing y publicidad (pisos 61–80)
│   └── Pisos ejecutivos (pisos 81–100)
├── Niveles o pisos
│   ├── Encuentros con rondas de enemigos
│   └── Mini-jefes en los pisos 20, 40, 60 y 80
└── Nivel 100: Oficina del CEO — Jefe final
```
## Cantidad estimada

| Tipo                      |                               Cantidad |
| ------------------------- | -------------------------------------: |
| Edificios                 |              1 para la entrega: Nuddle |
| Secciones de ambientación |                                      5 |
| Arquetipos de escenario   |     12; 10 reutilizables entre pisos y 2 únicos |
| Niveles / pisos           |                  Hasta 100 por partida |
| Misiones                  |      No aplica: el juego no tiene misiones |
| Enemigos                  |                                      5 |
| Jefes                     |                                  1 o 2 |
| NPC                       |                                  1 o 2 |
| Objetos                   |                                      2 |
## Dependencias

¿Qué contenido debe existir antes de otro?

* **Dirección de Arte y Modelado:** Los assets principales (personajes y enemigos) deben estar modelados y texturizados antes de su integración final en los escenarios reutilizables.
* **Mecánicas Base:** El sistema de combate debe estar programado y pulido antes de balancear la dificultad de los niveles.
* **Escenarios y progresión:** Los arquetipos de escenario deben ensamblarse y probarse para su reutilización en distintos pisos. La introducción de las mecánicas se organizará en los primeros niveles. Las secciones y sus arquetipos se distribuyen en bloques de 20 pisos, de la Planta baja a los Pisos ejecutivos.

Navegación:[[00 - Índice]] · ← [[04 - Diálogos y Narrativa]] · [[02 - Niveles]] →
