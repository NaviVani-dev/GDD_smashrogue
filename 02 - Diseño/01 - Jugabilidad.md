# Jugabilidad

## Descripción de la sección

La jugabilidad explica **qué hace el jugador, qué recibe a cambio y cómo evoluciona la experiencia**.

## Bucle principal de juego

Describe el ciclo que se repite durante la experiencia.

**Ejemplo conceptual:**

`Explorar → Encontrar desafío → Resolver → Obtener recompensa → Mejorar → Explorar`

**Bucle del proyecto:**
MAKE ’EM FALL es un roguelike de combate de plataformas al estilo Smash Bros. El jugador sube piso por piso un rascacielos corporativo, peleando contra oleadas de enemigos y construyendo su personaje con boons hasta llegar al jefe.

`Elegir personaje → Pelear contra una o varias rondas de enemigos → Elegir o mejorar un boon, si hay opciones disponibles → Saltar rompiendo el techo hacia el siguiente piso → Cafetería cuando corresponda → Mr. Big Data cada 50 pisos → Seguir subiendo hasta perder las 3 vidas → Pantalla de resultados → Reintentar o volver al menú`

Cada **nivel** es un piso del rascacielos. Al completar todas sus rondas, el jugador elige un boon o una mejora, si hay opciones disponibles. Después, el personaje **salta automáticamente y atraviesa el techo** para llegar al siguiente piso (transición con cámara lenta). En los pisos de cafetería, el jugador camina hasta la salida y pulsa el botón de agarre para subir.

## Acciones principales del jugador

| Acción                                                               | Propósito                                   | Resultado                                         |
| --------------------------------------------------------------------- | -------------------------------------------- | ------------------------------------------------- |
| Atacar (básicos, habilidades y ataques fuertes en todas direcciones) | Subir el porcentaje de daño de los enemigos | Entre más porcentaje, más lejos salen volando   |
| Sacar enemigos del escenario                                          | Derrotarlos (KO)                             | Al eliminar a todos, se limpia el nivel           |
| Escudo y esquive                                                      | Evitar el daño propio                       | Mantener tu porcentaje bajo para no salir volando |
| Moverse y saltar (doble salto)                                        | Posicionarse y volver al escenario           | Sobrevivir y alcanzar a los enemigos              |
| Elegir boons                                                          | Personalizar el estilo de pelea              | Cada partida se juega diferente                   |
| Comprar en la tienda                                                  | Curarse o mejorar boons                      | Llegar más lejos en la partida                   |

## Experiencia segundo a segundo

La partida comienza con la entrada del personaje seleccionado a la primera arena (la recepción). Después aparece la cuenta regresiva **3, 2, 1, MAKE 'EM FALL** y los enemigos entran al escenario (los guardias caen; los drones llegan volando). El jugador se mueve, combina ataques básicos, habilidades y ataques fuertes, se cubre con el escudo o esquiva, y busca subir el porcentaje de los enemigos hasta lanzarlos por las ventanas del edificio.

## Experiencia minuto a minuto

1. Limpiar las rondas de enemigos del nivel (de 1 a 3 rondas, según la altura).
2. Limpiar las rondas de enemigos del piso. Cada ronda tiene hasta 4 enemigos; al subir, hay más enemigos y, por lo tanto, más rondas.
3. Recoger el boon que suelta un **enemigo élite** al ser derrotado (se toma con el botón de ataque).
4. Elegir uno de los 3 boons o mejoras ofrecidos. Si no quedan opciones, se omite esta elección.
5. Saltar automáticamente al siguiente piso atravesando el techo.
6. Visitar la **cafetería (Café Corp)** para comprar boons nuevos o mejoras con las monedas obtenidas. Aparece **cada 10 pisos** y **un piso antes de cada jefe**. En la cafetería no se pelea.
7. Cada **50 pisos,** enfrentar a  **Mr. Big Data** , el CEO de Nuddle. Al vencerlo, el jugador cobra una recompensa de 60 monedas y sigue subiendo.

## Experiencia a largo plazo

Cada partida es diferente gracias a las combinaciones de boons, la aparición aleatoria de enemigos, élites y tipos de piso, y la elección entre Niko, Mateo Cruz, Mr. Wobbles, Atsuko y Craub. El jugador quiere volver para probar otras combinaciones, dominar el combate, superar su piso máximo y mejorar su calificación.

## Condición de victoria

**No hay una condición de victoria final**: el juego es un ascenso sin fin. El objetivo es llegar lo más alto posible y derrotar a Mr. Big Data cada vez que aparece (cada 50 pisos). Al terminar la partida, la pantalla de **Resultados** muestra el piso alcanzado, los KO, las monedas, los boons y el tiempo, junto con una calificación de **S** a  **D** .

## Condición de derrota

Perder las **3 vidas**. Se pierde una vida al salir disparado del escenario (por una ventana rota o por los límites del escenario). Aparece el aviso **GAME!**, la acción se ralentiza y se pasa a la pantalla de Resultados, donde el jugador puede **Reintentar** o volver al **Menú**. En la historia, el personaje escapa en paracaídas y regresa a La Coladera. **La Coladera no es un lugar jugable:** solo existe en el lore. Lo único jugable son las oficinas; todo lo demás es interfaz (UI).

## Ritmo

* **Acción:** la mayor parte del tiempo. Peleas cortas e intensas en cada piso.
* **Desafío:** sube de forma gradual: más enemigos y rondas por piso, enemigos más fuertes, nuevos tipos y más élites. Hay un pico con Mr. Big Data cada 50 pisos.
* **Recompensa:** después de cada piso (boon), al derrotar élites (boon que sueltan) y en cada cafetería.
* **Descanso:** breve, en el menú de boons, durante el salto entre pisos y en la cafetería.
* **Historia:** en los diálogos del encargado de la cafetería y en la presentación del jefe. Nunca interrumpe el combate.
* **Exploración:** no hay.

## Principios de interacción

* Entre más porcentaje tiene un personaje, más lejos sale volando. Esta regla aplica igual para el jugador y los enemigos.
* Siempre debe verse el porcentaje de todos los personajes en pantalla.
* Los golpes deben sentirse: congelación breve del golpe (hitlag), destello y estela al salir volando.
* El último KO de cada nivel se marca con cámara lenta.
* Las ventanas rotas deben distinguirse con claridad de las que están intactas.

> **Navegación:** [[00 - Índice]] · ← [[04 - Pilares de Diseño]] · [[02 - Mecánicas]] →
