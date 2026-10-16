# Reglas y Estados del Juego

## Descripción de la sección

Define las reglas globales y los estados que puede atravesar el videojuego.

## Estados principales

- Menú principal
- Selección de personaje
- Carga
- Cuenta regresiva
- Jugando
- Menú de boons
- Transición de nivel (salto al siguiente piso)
- Tienda
- Pausa
- Combate contra mini-jefe
- Combate contra jefe final
- Victoria
- Derrota / Game Over
- Créditos

> [!note] La Coladera
> La Coladera **no es un estado jugable**: solo existe en el lore. Lo único jugable son las oficinas; todo lo demás es interfaz.

## Transiciones

| Estado origen | Evento | Estado destino | Condición |
|---|---|---|---|
| Menú principal | Jugar | Selección de personaje | — |
| Selección de personaje | Elegir a Niko o a Mr. Wobbles | Cuenta regresiva | — |
| Cuenta regresiva | Termina el "¡GO!" | Jugando | — |
| Jugando | Último enemigo de la ronda fuera | Jugando (siguiente ronda) | Quedan rondas en el nivel |
| Jugando | Último enemigo del nivel fuera | Menú de boons | Hay boons o mejoras disponibles |
| Jugando | Último enemigo del nivel fuera | Transición de nivel | No queda nada que ofrecer |
| Menú de boons | Elegir boon | Transición de nivel | — |
| Transición de nivel | Llega al nuevo piso | Combate contra jefe final | Nivel 100 |
| Transición de nivel | Llega al nuevo piso | Combate contra mini-jefe | Nivel múltiplo de 20 (excepto el 100) |
| Transición de nivel | Llega al nuevo piso | Tienda | Nivel 10, 19, 30, 39, 50, 59, 70, 79, 90 o 99 |
| Transición de nivel | Llega al nuevo piso | Jugando | En cualquier otro caso |
| Tienda | Salir | Jugando | — |
| Combate contra mini-jefe | Derrotar al mini-jefe | Menú de boons | — |
| Combate contra jefe final | Derrotar al jefe final | Victoria | La partida termina |
| Jugando | Pierde la última vida | Derrota / Game Over | — |
| Victoria / Derrota | Continuar | Menú principal | — |
| Jugando | Esc / Start | Pausa | — |
| Pausa | Esc / Start | Jugando | — |

## Reglas globales

1. Se pierde una vida al salir de los límites del escenario. El jugador tiene 3 vidas.
2. Entre más porcentaje tiene un personaje, más lejos sale volando.
3. Los enemigos son más susceptibles al daño que el jugador.
4. Un nivel termina cuando todos sus enemigos quedan fuera.
5. Las ventanas se rompen con golpes muy fuertes, se regeneran después de un rato y se reparan al cambiar de nivel.
6. No se puede cambiar de personaje durante la partida.
7. Las monedas y los boons solo duran una partida. No hay progreso permanente.
8. Mini-jefe (enemigo élite) cada 20 niveles; jefe final en el nivel 100. Vencer al jefe final termina la partida.

## Casos especiales

- **Reaparición:** al perder una vida, el jugador reaparece en una plataforma temporal, con 0% e invulnerable por unos instantes.
- **Sin boons disponibles:** si todos los boons están al máximo, se pasa directo al siguiente nivel.
- **Cambio de nivel:** los proyectiles en pantalla desaparecen y las ventanas se reparan.
- **Tienda antes de un jefe:** si al nivel múltiplo de 10 le toca un mini-jefe o el jefe final, la tienda se adelanta un nivel (19, 39, 59, 79, 99) para que el jugador se prepare.


> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
