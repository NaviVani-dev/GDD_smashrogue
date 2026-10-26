# Personajes y Animación

## Descripción de la sección

Documenta cómo deben verse y comportarse visualmente los personajes.

## Requisitos por personaje

| Personaje   | Modelo/Sprite                                                                                                                                                                                                                                                                                                                 | Animaciones                                                                                      | VFX                                                                     | Estado                                                                                                  |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Mateo Cruz  | Personaje anime de identidad deportiva y urbana. Chamarra roja, pants negros, guantes y tenis de taekwondo; conservar emblema y amuleto.                                                                                                                                                                                      | Reposo, desplazamiento, salto, caída, ataques de taekwondo, reacción al daño y derrota.          | Impactos blancos y efectos de los boons que correspondan a sus ataques. | Diseño visual trabajado. Adaptación al estilo final, producción y animaciones pendientes de documentar. |
| Niko        | Personaje anime de estilo urbano y rebelde. Piel morena clara, ojos dorados y cabello morado oscuro recogido en coleta, con flequillo y mechones laterales. Chaqueta blanca amplia y abierta, top negro corto, pantalones cargo gris oscuro, cinturón con estoperoles y botas negras. Gargantilla negra y accesorios dorados. | Reposo, desplazamiento, salto, caída, ataques con los puños, reacción al daño y derrota.         | Impactos y efectos de los boons que correspondan a sus ataques.         | Diseño y modelo 3D de referencia disponibles. Rigging y animaciones pendientes de documentar.           |
| Mr. Wobbles | Personaje jugable de apariencia de payaso. Diseño físico y objetos de combate pendientes de definir.                                                                                                                                                                                                                          | Reposo, desplazamiento, salto, caída, ataques con objetos de payaso, reacción al daño y derrota. | Efectos de sus objetos de combate y de los boons; detalles por definir. | Diseño visual y animaciones pendientes de documentar.                                                   |

## Animaciones

### Movimiento

- **Idle o reposo:** debe conservar la postura característica del personaje y comunicar su disposición para combatir.
- **Caminar:** desplazamiento coherente con su anatomía, vestimenta y actitud.
- **Correr:** debe distinguirse claramente de caminar y comunicar la dirección del movimiento.
- **Saltar:** debe mostrar el impulso del personaje y mantener una silueta comprensible.
- **Caer:** debe diferenciarse del ascenso y preparar visualmente el regreso al suelo.

### Interacción

Al comenzar una nueva partida, una animación breve muestra la apertura de las puertas del ascensor y la salida del personaje seleccionado a la primera arena. Al finalizar, comienza la cuenta regresiva. Esta presentación no incluye diálogos ni exposición narrativa.

El avance entre pisos se representa mediante una interacción con el ascensor. Después de completar el combate y resolver la elección de boon, el jugador puede acercarse al ascensor y activarlo.

La transición muestra el cierre de las puertas, el cambio del indicador de piso y la apertura de las puertas en la siguiente arena. La animación concreta del personaje al entrar, activar y salir del ascensor está por definir.

La selección de boons se realiza mediante interfaz. No se requiere recoger una tarjeta para avanzar.
### Combate

***Niko***
Utiliza principalmente los puños para combatir cuerpo a cuerpo. Sus animaciones deben permitir reconocer la dirección y el alcance de los golpes. Los movimientos concretos están por definir.

***Mateo*** 
Utiliza principalmente patadas de taekwondo para controlar la distancia. Sus golpes con los puños cumplen una función de apoyo para desestabilizar o alejar al rival. Sus animaciones deben mostrar equilibrio, coordinación y una dirección clara del ataque.

Cada ataque debe permitir reconocer preparación, ejecución y recuperación. Los tiempos, cadenas de golpes, ataques aéreos y especiales están por definir.

***Mr. Wobbles***

Combate con objetos de payaso, como globos explosivos y otras herramientas de su oficio. Sus animaciones deben comunicar con claridad el uso de cada objeto y distinguir su estilo del combate de Niko y Mateo. Los movimientos concretos están por definir.
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
