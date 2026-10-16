# Personajes y Animación

## Descripción de la sección

Documenta cómo deben verse y comportarse visualmente los personajes.

## Requisitos por personaje

| Personaje  | Modelo/Sprite                                                                                                                            | Animaciones                                                                             | VFX                                                                     | Estado                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Mateo Cruz | Personaje anime de identidad deportiva y urbana. Chamarra roja, pants negros, guantes y tenis de taekwondo; conservar emblema y amuleto. | Reposo, desplazamiento, salto, caída, ataques de taekwondo, reacción al daño y derrota. | Impactos blancos y efectos de los boons que correspondan a sus ataques. | Diseño visual trabajado. Adaptación al estilo final, producción y animaciones pendientes de documentar. |
| Niko       |                                                                                                                                          |                                                                                         |                                                                         |                                                                                                         |
|            |                                                                                                                                          |                                                                                         |                                                                         |                                                                                                         |
|            |                                                                                                                                          |                                                                                         |                                                                         |                                                                                                         |

## Animaciones

### Movimiento

- **Idle o reposo:** debe conservar la postura característica del personaje y comunicar su disposición para combatir.
- **Caminar:** desplazamiento coherente con su anatomía, vestimenta y actitud.
- **Correr:** debe distinguirse claramente de caminar y comunicar la dirección del movimiento.
- **Saltar:** debe mostrar el impulso del personaje y mantener una silueta comprensible.
- **Caer:** debe diferenciarse del ascenso y preparar visualmente el regreso al suelo.

### Interacción

Las interacciones físicas todavía están **por definir**. La obtención de boons y el avance entre pisos necesitan una respuesta visual, pero no se ha establecido si se representarán mediante animaciones del personaje, efectos, interfaz o transiciones de escena.

No se consideran confirmadas animaciones de abrir puertas, usar elevadores, recoger objetos o conversar.
### Combate

==🟡***Niko***==

***Mateo*** 
utiliza principalmente patadas de taekwondo para controlar la distancia. Sus golpes con los puños cumplen una función de apoyo para desestabilizar o alejar al rival. Sus animaciones deben mostrar equilibrio, coordinación y una dirección clara del ataque.

Cada ataque debe permitir reconocer preparación, ejecución y recuperación. Los tiempos, cadenas de golpes, ataques aéreos y especiales están por definir.
### Daño

Las reacciones al daño deben indicar que un golpe ha conectado, manteniendo la identidad corporal de cada personaje.

Las diferencias entre daño leve, daño fuerte, aturdimiento, retroceso y derribo están **por definir**, según las reglas de combate. No todos estos estados se consideran confirmados.
### Muerte / derrota

La eliminación ocurre cuando un personaje es expulsado fuera de los límites del escenario, siguiendo una presentación similar a _Super Smash Bros._ Durante el lanzamiento, permanece visible con una pose que comunica la dirección y la fuerza del impacto.

Al cruzar el límite de eliminación, el personaje desaparece y se genera un **destello en el punto de salida**, confirmando visualmente que ha quedado fuera del combate. No se muestra una animación de muerte ni queda un cuerpo en el escenario.
## Convenciones

Define nombres de archivos, tamaños, esqueletos, rigging, frames o formatos cuando sea necesario.

**Por definir**

> **Navegación:** [[00 - Índice]] · ← [[01 - Dirección de Arte]] · [[03 - Entornos]] →
