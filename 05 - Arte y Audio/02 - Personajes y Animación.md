# Personajes y Animación

## Descripción de la sección

Documenta cómo deben verse y comportarse visualmente los personajes.

## Requisitos por personaje

| Personaje   | Modelo/Sprite                                                                                                                                                                                                                                                                                                                 | Animaciones                                                                                      | VFX                                                                     | Estado                                                                                                  |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Mateo Cruz  | Personaje anime de identidad deportiva y urbana. Chamarra roja, pants negros, guantes y tenis de taekwondo.                                                                                                                                                                                      | Reposo, desplazamiento, salto, caída, ataques de taekwondo, agarre y lanzamientos, reacción al daño, derrota y victoria.          | Impactos blancos y efectos de los boons que correspondan a sus ataques. | Modelo 3D, moveset completo y animaciones integrados en el juego. |
| Niko        | Personaje anime de estilo urbano y rebelde. Piel morena clara, ojos dorados y cabello morado oscuro recogido en coleta, con flequillo y mechones laterales. Chaqueta blanca amplia y abierta, top negro corto, pantalones cargo gris oscuro, cinturón con estoperoles y botas negras. Gargantilla negra y accesorios dorados. | Reposo, desplazamiento, salto, caída, ataques con los puños, agarre y lanzamientos, reacción al daño, derrota y victoria.         | Impactos y efectos de los boons que correspondan a sus ataques.         | Modelo 3D, moveset completo y animaciones integrados en el juego.           |
| Mr. Wobbles | Personaje jugable de apariencia de payaso. Cabello pelirrojo, sombrero de copa negro con bandas blancas y rombos azules, chaqueta de cola roja con detalles amarillos, azules y morados, corsé blanco y negro, pantalón blanco y botas café de cordones. Pelea con objetos de payaso, como globos explosivos, un mazo de goma, pasteles y un cañón de confeti. | Reposo, desplazamiento, salto, caída, ataques con objetos de payaso, agarre y lanzamientos, reacción al daño, derrota y victoria. | Confeti del cañón de confeti y efectos de los boons. | Modelo 3D, moveset completo y animaciones integrados en el juego. |
| Atsuko      | Estudiante de preparatoria de cabello morado corto, suéter rosa, falda gris de cuadros y calcetas blancas. Usa una motosierra como arma; conservar la motosierra y la venda como elementos de identidad. | Reposo, desplazamiento, salto, caída, ataques con motosierra, agarre y lanzamientos, reacción al daño, derrota y victoria. | Efectos de la motosierra y de los boons que correspondan a sus ataques. | Modelo 3D, moveset completo y animaciones integrados en el juego. |
| Craub       | Cangrejo pixel art rojo, con ojos negros alargados y garras siempre visibles. Su cuerpo es semi-tangible. | Reposo, desplazamiento, salto, caída, ataques con garras, cohete, fuego y giro, agarre y lanzamientos, reacción al daño, derrota y victoria. | Efectos del cohete, del fuego y de los boons. | Personaje pixel art con moveset completo y animaciones integrados en el juego. |

## Animaciones

### Movimiento

- **Idle o reposo:** debe conservar la postura característica del personaje y comunicar su disposición para combatir.
- **Caminar:** desplazamiento coherente con su anatomía, vestimenta y actitud.
- **Correr:** debe distinguirse claramente de caminar y comunicar la dirección del movimiento.
- **Saltar:** debe mostrar el impulso del personaje y mantener una silueta comprensible.
- **Caer:** debe diferenciarse del ascenso y preparar visualmente el regreso al suelo.

### Interacción

Al comenzar una nueva partida, el personaje seleccionado aparece directamente en la primera arena y comienza la cuenta regresiva. Esta presentación no incluye diálogos ni exposición narrativa. Los enemigos entran saltando al escenario desde el fondo; los drones entran volando.

No hay ascensor. Después de completar el combate y resolver la elección de boon, el personaje celebra unos instantes y la transición al siguiente piso es automática:

- **Salto:** el personaje salta hacia arriba con un grito.
- **Ruptura del techo:** golpea el techo, que se rompe en pedazos; el juego se pone en cámara lenta un instante.
- **Llegada:** la cámara sube con él, el techo se cierra detrás y el personaje aterriza en el siguiente piso.

En la tienda, el personaje sube de la misma forma al usar la salida ("SUBIR").

La selección de boons se realiza mediante interfaz. Los boons que sueltan los élites se recogen del suelo con el botón de ataque.

Al terminar la partida, la pantalla de resultados muestra al personaje con su animación de victoria.
### Combate

Cada ataque debe permitir reconocer preparación, ejecución y recuperación. Las cadenas de golpes, los ataques aéreos y los especiales de cada personaje están definidos en el moveset de Personajes.

***Niko***
Utiliza principalmente los puños para combatir cuerpo a cuerpo. Sus animaciones deben permitir reconocer la dirección y el alcance de los golpes. Sus movimientos están definidos en el moveset de Personajes.

***Mateo*** 
Utiliza principalmente patadas de taekwondo para controlar la distancia. Sus golpes con los puños cumplen una función de apoyo para desestabilizar o alejar al rival. Sus animaciones deben mostrar equilibrio, coordinación y una dirección clara del ataque.

***Mr. Wobbles***

Combate con objetos de payaso, como globos explosivos, un mazo de goma, pasteles y un cañón de confeti. Sus animaciones deben comunicar con claridad el uso de cada objeto y distinguir su estilo del combate de Niko y Mateo. Sus movimientos están definidos en el moveset de Personajes.

***Atsuko***

Combate con su motosierra. Sus habilidades son: acelerar la motosierra para dar varios golpes seguidos (neutral), una embestida con la motosierra (lado), un ataque que la eleva (arriba) y un barrido pesado (abajo). Sus animaciones deben dejar claro el alcance de la motosierra. Sus habilidades están definidas en Personajes.

***Craub***

Combate con sus garras. Sus habilidades son: un golpe cercano (neutral), un cohete que lanza hacia adelante (lado), un ataque de fuego hacia arriba (arriba) y un giro tipo ciclón (abajo). Como personaje pixel art, sus animaciones avanzan cuadro por cuadro, sin interpolación. Sus habilidades están definidas en Personajes.
### Daño

Las reacciones al daño deben indicar que un golpe ha conectado, manteniendo la identidad corporal de cada personaje.

| Estado | Cuándo ocurre | Animación |
|---|---|---|
| Daño leve | Golpe con poco retroceso | Retroceso corto con un gesto de dolor |
| Daño fuerte | Golpe con mucho retroceso | Pose de lanzamiento con estela que comunica la dirección del golpe |
| Aturdimiento | Al romperse el escudo | El personaje queda tambaleándose unos instantes |
| Retroceso | Al recibir un parry | El atacante queda expuesto en una pose abierta |
| Derribo | Al chocar contra el suelo después de un lanzamiento | El personaje cae y se levanta |
| Agarrado | Al ser atrapado por un agarre | El personaje queda sujeto, recibe golpes y es lanzado |
### Muerte / derrota

La eliminación ocurre cuando un personaje es expulsado fuera de los límites del escenario, siguiendo una presentación similar a _Super Smash Bros._ Durante el lanzamiento, permanece visible con una pose que comunica la dirección y la fuerza del impacto.

Al cruzar el límite de eliminación, el personaje desaparece y se genera un **destello en el punto de salida**, confirmando visualmente que ha quedado fuera del combate. No se muestra una animación de muerte ni queda un cuerpo en el escenario. Los drones son la excepción: al romperse caen hechos pedazos.
## Convenciones

Define nombres de archivos, tamaños, esqueletos, rigging, frames o formatos cuando sea necesario.

- Cada personaje tiene su propia carpeta con sus archivos `.fbx`, `.fbm` y `.asset`.
- Los materiales empiezan con `MT_`.
- Los modelos se hacen en Blender y se importan con rig Legacy (no Humanoid).

> **Navegación:** [[00 - Índice]] · ← [[01 - Dirección de Arte]] · [[03 - Entornos]] →
