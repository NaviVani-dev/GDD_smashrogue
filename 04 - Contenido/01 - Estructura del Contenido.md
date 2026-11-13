# Estructura del Contenido

## Descripción de la sección

Organiza el contenido del videojuego en unidades manejables: mundos, capítulos, zonas, niveles, misiones y desafíos.

## Estructura

Cada **nivel** corresponde a un **piso del edificio**. La partida comienza en el piso 1 y la subida no tiene fin: termina cuando el jugador pierde sus 3 vidas.

Cada piso de combate funciona como una **arena** en la que se desarrollan las rondas de enemigos. El jugador se desplaza dentro de ella para combatir, posicionarse y recuperarse de los lanzamientos, sin recorrer distintas zonas para completar el nivel. Las plataformas flotantes y el mobiliario forman parte del espacio de combate.

Cada piso utiliza un **arquetipo de escenario**: un diseño reutilizable que representa un tipo de espacio corporativo y presenta pequeñas variaciones entre pisos. No hay secciones de ambientación: el arquetipo de los pisos de combate se elige al azar y se mantiene en bloques de 3 pisos.

Un arquetipo de escenario puede utilizarse en muchos niveles. Por tanto, los pisos no requieren escenarios únicos.

| Arquetipo de escenario | Dónde aparece |
|---|---|
| La Recepción | Solo en el piso 1. Se ve la calle afuera del edificio |
| Oficina | Pisos de combate, al azar |
| Sala de juntas | Pisos de combate, al azar |
| Sala de descanso | Pisos de combate, al azar |
| Mantenimiento | Pisos de combate, al azar (sin ventanas) |
| Sala de servidores | Pisos de combate, al azar (sin ventanas) |
| Café Corp (tienda) | Cada 10 pisos y en el piso anterior a cada jefe: 10, 20, 30, 40, 49, 60, 70, 80, 90, 99… |
| Oficina ejecutiva | Pisos del jefe, cada 50 pisos: 50, 100, 150… |

La Recepción es el único arquetipo que aparece en un solo piso. Los demás se reutilizan durante toda la subida.

```text
Edificio de Nuddle — Subida sin límite de pisos
├── Piso 1: La Recepción
├── Pisos de combate (arquetipos al azar en bloques de 3 pisos)
│   └── Encuentros con rondas de enemigos
├── Tiendas: Café Corp (cada 10 pisos y antes de cada jefe)
└── Cada 50 pisos: Oficina ejecutiva — Mr. Big Data
```
## Cantidad estimada

| Tipo                      |                               Cantidad |
| ------------------------- | -------------------------------------: |
| Edificios                 |              1 para la entrega: Nuddle |
| Secciones de ambientación |        No aplica: no hay secciones |
| Arquetipos de escenario   |     8; 7 reutilizables entre pisos y 1 único (La Recepción) |
| Niveles / pisos           |                  Sin límite por partida |
| Misiones                  |      No aplica: el juego no tiene misiones |
| Enemigos                  |                                      6 |
| Jefes                     |                                      1 |
| NPC                       |                         1 (el tendero) |
| Objetos                   | 1: boons en el suelo (los sueltan los élites y, a veces, los muebles rotos) |
## Dependencias

¿Qué contenido debe existir antes de otro?

* **Dirección de Arte y Modelado:** Los assets principales (personajes y enemigos) deben estar modelados y texturizados antes de su integración final en los escenarios reutilizables.
* **Mecánicas Base:** El sistema de combate debe estar programado y pulido antes de balancear la dificultad de los niveles.
* **Escenarios y progresión:** Los arquetipos de escenario deben ensamblarse y probarse para su reutilización en distintos pisos. La introducción de las mecánicas se organizará en los primeros niveles.

Navegación:[[00 - Índice]] · ← [[04 - Diálogos y Narrativa]] · [[02 - Niveles]] →
