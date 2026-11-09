# Estructura del Contenido

## Descripción de la sección

Organiza el contenido del videojuego en unidades manejables: mundos, capítulos, zonas, niveles, misiones y desafíos.

## Estructura

Cada **nivel** corresponde a un **piso del edificio**. La partida comienza en el piso 1 y puede avanzar hasta el piso 100, donde se encuentra el jefe final.

Cada piso de combate funciona como una **arena** en la que se desarrollan las rondas de enemigos. El jugador se desplaza dentro de ella para combatir, posicionarse y recuperarse de los lanzamientos, sin recorrer distintas zonas para completar el nivel. Las plataformas y los obstáculos que se incorporen forman parte del espacio de combate.

Las **secciones** agrupan pisos según su ambientación dentro del edificio. Cada sección puede utilizar distintos **arquetipos de escenario**: diseños reutilizables que representan tipos de espacios corporativos y pueden presentar pequeñas variaciones entre pisos.

Un arquetipo de escenario puede utilizarse en varios niveles. Por tanto, los 100 niveles no requieren 100 escenarios únicos. La cantidad de secciones, sus rangos de pisos y los arquetipos de cada una están por definir.

```text
Edificio de Nuddle — Hasta 100 niveles por partida
├── Secciones de ambientación
│   ├── Agrupan varios niveles o pisos
│   └── Utilizan arquetipos de escenario reutilizables
├── Niveles o pisos
│   ├── Encuentros con rondas de enemigos
│   └── Mini-jefes en los pisos 20, 40, 60 y 80
└── Nivel 100: Oficina del CEO — Jefe final
```
## Cantidad estimada

| Tipo                      |                               Cantidad |
| ------------------------- | -------------------------------------: |
| Edificios                 |              1 para la entrega: Nuddle |
| Secciones de ambientación |                            Por definir |
| Arquetipos de escenario   | Por definir; reutilizables entre pisos |
| Niveles / pisos           |                  Hasta 100 por partida |
| Misiones                  |                            Sin definir |
| Enemigos                  |                                      5 |
| Jefes                     |                                  1 o 2 |
| NPC                       |                                  1 o 2 |
| Objetos                   |                                      2 |
## Dependencias

¿Qué contenido debe existir antes de otro?

* **Dirección de Arte y Modelado:** Los assets principales (personajes y enemigos) deben estar modelados y texturizados antes de su integración final en los escenarios reutilizables.
* **Mecánicas Base:** El sistema de combate debe estar programado y pulido antes de balancear la dificultad de los niveles.
* **Escenarios y progresión:** Los arquetipos de escenario deben ensamblarse y probarse para su reutilización en distintos pisos. La introducción de las mecánicas se organizará en los primeros niveles. La distribución de secciones y arquetipos a lo largo de los 100 pisos está por definir.

Navegación:[[00 - Índice]] · ← [[04 - Diálogos y Narrativa]] · [[02 - Niveles]] →
