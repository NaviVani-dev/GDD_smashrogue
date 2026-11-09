# Registro de Decisiones

## Descripción de la sección

Esta sección conserva las decisiones importantes del proyecto y el razonamiento detrás de ellas.

## Decisión

**Fecha:**

**Tema:**

**Problema:**

**Opciones consideradas:**

**Decisión tomada:**

**Motivo:**

**Consecuencias:**

**Responsable:**

## Registro

| Fecha | Tema | Decisión | Responsable |
| ----- | ---- | --------- | ----------- |
|       |      |           |             |


## Decisiones clave

### Quitar los agarres del juego

**Fecha:** 2026-10-16

**Tema:** Moveset y controles.

**Problema:** El prototipo en Unity todavía tiene un botón de agarre, pero el diseño del combate no lo contempla.

**Opciones consideradas:**

Mantener el agarre como en el prototipo.
Quitar el agarre y dejar solo ataques, escudo y esquive.

**Decisión tomada:** No hay agarres. El botón del prototipo debe eliminarse.

**Motivo:** No está documentado en el GDD. (Por confirmar con el equipo. El esquema de controles busca pocas teclas y muchos movimientos según la dirección.)

**Consecuencias:** Hay que quitar el agarre del prototipo. Ver [[02 - Mecánicas]] y [[04 - Controles]].

**Responsable:** Equipo


### Máximo de 3 boons por partida

**Fecha:** 2026-10-17

**Tema:** Boons.

**Problema**: La idea original permitía 3 o 4 boons a la vez.

**Opciones consideradas:**

Máximo de 3 boons.
Máximo de 4 boons.

**Decisión tomada:** Máximo de 3 boons, con hasta 5 niveles cada uno (valor del prototipo).

**Motivo:** Es lo que implementa el prototipo actual. (Se puede reajustar durante el balance.)

**Consecuencias:** Con los espacios llenos, solo se ofrecen mejoras de los boons que ya tiene. Ver [[02 - Mecánicas]].

**Responsable:** Equipo


### Descartar el sistema de puntaje inspirado en Balatro

**Fecha:** 2026-10-16

**Tema:** Economía y puntaje.

**Problema:** Se evaluó agregar un puntaje para incentivar a repetir partidas.

**Opciones consideradas:**

Agregar un sistema de puntaje inspirado en Balatro.
No tener puntaje por ahora.

**Decisión tomada:** Queda descartado por ahora.

**Motivo:** No está documentado en el GDD. (Por confirmar con el equipo.)

**Consecuencias**: El interés por repetir se apoya en las combinaciones de boons y en los tres personajes. Ver [[06 - Economía y Recursos]] y [[02 - Referencias e Inspiración]].

**Responsable:** Equipo

## Registro

| Fecha      | Tema                  | Decisión                                                                              | Responsable    |
| ---------- | --------------------- | -------------------------------------------------------------------------------------- | -------------- |
| 2026-09-25 | Perspectiva           | El juego es 2.5D, con desplazamiento lateral.                                          | Equipo         |
| 2026-09-28 | Motor                 | Se desarrolla en Unity con C#.                                                         | Equipo         |
| 2026-09-28 | Alcance de la entrega | La entrega se centra en la compañía Nuddle y su jefe, Bernard "Big Data" Nuddleman.  | Equipo         |
| 2026-10-16 | Combate               | No hay agarres. Ver decisión detallada.                                               | Equipo         |
| 2026-10-16 | Derrota               | El jugador tiene 3 vidas y pierde una al salir del escenario.                          | Equipo         |
| 2026-10-16 | Boons                 | Máximo de 3 boons por partida. Ver decisión detallada.                               | Equipo         |
| 2026-10-16 | Economía             | Tienda cada 10 niveles, o un nivel antes si el siguiente tiene mini-jefe o jefe final. | Equipo         |
| 2026-10-16 | Economía             | Sistema de puntaje descartado por ahora. Ver decisión detallada.                      | Equipo         |
| 2026-10-16 | Controles             | Teclado y gamepad, sin reasignación de controles.                                     | Equipo         |
| 2026-10-16 | Mundo                 | La Coladera solo existe en el lore; lo único jugable son las oficinas.                | Equipo         |
| 2026-10-16 | Narrativa             | La historia no se explica en combate: solo en tiendas y en el almanaque.               | Equipo         |
| 2026-10-16 | Arte                  | Estética anime con sombreado plano tipo cel-shading.                                  | Anthony Duarte |
| 2026-10-16 | Personajes            | Mateo Cruz se agrega como personaje jugable junto a Niko.                              | Hector Ulises  |
| 2026-10-25 | Personajes            | Niko, Mateo Cruz y Mr. Wobbles están disponibles desde el inicio.                     | Anthony Duarte |

> **Navegación:** [[00 - Índice]] · ← [[02 - Referencias e Inspiración]] · [[04 - Historial de Versiones]] →
