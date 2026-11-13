# Reglas y Estados del Juego

## Descripción de la sección

Define las reglas globales y los estados que puede atravesar el videojuego.

## Estados principales

* Pantalla de título ("Pulsa cualquier botón")
* Menú principal (Jugar, Tutorial, Opciones, Créditos, Salir y Mundo debug)
* Mundo debug (escena de pruebas)
* Selección de personaje
* Tutorial
* Cuenta regresiva
* Jugando (rondas de enemigos)
* Piso limpio (recoger boons de élites)
* Menú de boons
* Salto al siguiente piso
* Cafetería
* Combate contra Mr. Big Data
* Pausa
* Fin de la partida ("GAME!")
* Resultados

> [!note] ✏️ La Coladera
> La Coladera **no es un estado jugable**: solo existe en el lore. Lo único jugable son las oficinas; todo lo demás es interfaz.

## Transiciones

| Estado origen               | Evento                                    | Estado destino              | Condición                                     |
| --------------------------- | ----------------------------------------- | --------------------------- | ---------------------------------------------- |
| Pantalla de título         | Pulsar cualquier botón                   | Menú principal             | —                                             |
| Menú principal             | Jugar                                     | Selección de personaje     | —                                             |
| Menú principal             | Tutorial                                  | Tutorial                    | —                                             |
| Tutorial                    | Completar todos los pasos                 | Menú principal             | —                                             |
| Menú principal             | Mundo debug                               | Mundo debug                 | —                                             |
| Menú principal             | Salir                                     | Cierra el juego             | Sin confirmación                               |
| Selección de personaje     | Elegir personaje y START                  | Cuenta regresiva            | —                                             |
| Cuenta regresiva            | Termina el "MAKE 'EM FALL"              | Jugando                     | —                                             |
| Jugando                     | Último enemigo de la ronda fuera         | Jugando (siguiente ronda)   | Quedan rondas en el piso                       |
| Jugando                     | Último enemigo del piso fuera            | Piso limpio                 | —                                             |
| Piso limpio                 | Se recogen los boons soltados por élites, si los hay | Menú de boons              | Hay boons o mejoras disponibles                |
| Piso limpio                 | Se recogen los boons soltados por élites | Salto al siguiente piso     | No quedan boons o mejoras disponibles          |
| Menú de boons              | Elegir boon                               | Salto al siguiente piso     | —                                             |
| Salto al siguiente piso     | Aterriza en el nuevo piso                 | Cafetería                  | Piso múltiplo de 10 que no sea múltiplo de 50, o piso anterior a un jefe |
| Salto al siguiente piso     | Aterriza en el nuevo piso                 | Combate contra Mr. Big Data | Piso múltiplo de 50                           |
| Salto al siguiente piso     | Aterriza en el nuevo piso                 | Jugando                     | En cualquier otro caso                         |
| Cafetería                  | Pulsar agarrar en la salida (SUBIR)       | Salto al siguiente piso     | —                                             |
| Combate contra Mr. Big Data | Derrotar al jefe                          | Menú de boons              | Se cobran 60 monedas; si no hay opciones, pasa al salto de piso |
| Jugando / Combate con jefe  | Pierde la última vida                    | Fin de la partida           | —                                             |
| Fin de la partida           | Termina la cámara lenta                  | Resultados                  | —                                             |
| Resultados                  | Reintentar                                | Cuenta regresiva            | Mismo personaje, desde el piso 1               |
| Resultados                  | Menú                                     | Menú principal             | —                                             |
| Jugando / Combate con jefe / Tutorial | Esc / Start                     | Pausa                       | No con el menú de boons o la tienda abiertos   |
| Pausa                       | Continuar (Esc / Start)                   | Estado anterior             | Vuelve a donde estaba el jugador               |
| Pausa                       | Volver al inicio                          | Menú principal             | Sin confirmación; también sale del tutorial    |

## Reglas globales

1. Se pierde una vida al salir de los límites del escenario. El jugador tiene 3 vidas.
2. Entre más porcentaje tiene un personaje, más lejos sale volando.
3. Cada enemigo recibe el daño multiplicado por su susceptibilidad, que baja conforme se sube de piso.
4. Un piso termina cuando todos sus enemigos quedan fuera.
5. Las ventanas (y las paredes de las salas cerradas) se rompen con lanzamientos fuertes y se regeneran unos segundos después.
6. No se puede cambiar de personaje durante la partida.
7. Las monedas y los boons solo duran una partida. No hay progreso permanente.
8. Mr. Big Data aparece cada 50 pisos. Vencerlo da 60 monedas y la partida continúa.
9. Se pasa al siguiente piso automáticamente después de elegir el boon (o directamente, si no hay opciones).
10. La partida no tiene final: termina únicamente al perder las 3 vidas o al volver al menú desde la pausa.

## Casos especiales

* **Reaparición:** al perder una vida, el jugador reaparece cayendo desde arriba, con 0% e invulnerable unos 2 segundos.
* **Sin boons disponibles:** si todos los boons están al máximo, se pasa directo al siguiente piso.
* **Cambio de piso:** las cáscaras de plátano y los proyectiles en pantalla desaparecen; el nuevo piso se genera con ventanas y paredes intactas.
* **Gato de la suerte:** si el jugador tiene este boon, puede salvarse de un KO por sala en lugar de perder una vida.

> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
