# Sistemas del Juego

## Descripción de la sección

Los sistemas son conjuntos de reglas y componentes que trabajan juntos: combate, inventario, IA, diálogo, progresión, economía, misiones, etc.

## Inventario de sistemas

| Sistema                          | Propósito                                                  | Dependencias                                                     | Estado         |
| -------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------- | -------------- |
| Combate: daño, empuje y ring-out | Resolver todos los golpes y determinar KO y derrota        | Controles, física.                                               | en definición. |
| Boons y mejoras                  | Construir la partida con habilidades que modifican ataques | con habilidades que modifican ataques	Combate, efectos de estado | en definición  |
| Oleadas y aparición de enemigos  | Generar enemigos por tandas y escalar la dificultad        | IA enemiga, progresión de salas                                  | en definción   |
| IA enemiga                       | Comportamiento de los enemigos y el jefe                   | Combate, oleadas                                                 | en definción.  |
| Puntaje y combo                  | Medir el desempeño y dar rejugabilidad                     | Combate                                                          | en definición. |

## Plantilla de sistema

### Nombre

**Objetivo:**

**Entradas:**

**Procesamiento / reglas:**

**Salidas:**

**Estados posibles:**

**Dependencias:**

**Interacciones:**

**Datos que necesita:**

**Datos que genera:**

**Riesgos:**

**Criterios de aceptación:**




Sistema de combate

Objetivo: Resolver cada golpe de forma consistente para jugador, enemigos y jefe, con la sensación de un juego de peleas de plataformas.

Entradas: Ataques (básico y especial), posición de los personajes, daño acumulado, efectos de estado activos.

Procesamiento / reglas:

Cada golpe aplica daño acumulado (%) y empuje.
El empuje crece con el daño acumulado del objetivo.
Salir de los límites del escenario = KO.
Los efectos de estado se evalúan al momento del impacto.

Salidas: Daño acumulado actualizado, empuje, KO, puntos y eventos para el sistema de oleadas.

Estados posibles: 
Libre 
Atacando 
Recibiendo golpe (aturdido) 
KO.

Dependencias: Controles, física del motor, efectos de estado.

Interacciones: Con boons (modifican ataques), IA (decide cuándo atacar) y puntaje (cada KO suma puntos).

Datos que necesita: Daño base y empuje de cada ataque; resistencia al empuje por tipo de enemigo.

Datos que genera: KO, daño recibido, combos.

Riesgos:

Enemigos difíciles de lanzar pueden alargar la sala demasiado.
Demasiados enemigos pueden hacer ilegible el combate.

Criterios de aceptación:

Los golpes siempre dan retroalimentación visual y sonora.
A igual daño acumulado, el empuje es predecible.
Un enemigo sacado del escenario cuenta como eliminado en todos los casos.

## Relaciones entre sistemas


Combate es el sistema central: casi todos los demás le entregan o le piden información.


> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
