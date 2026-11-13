# Pilares de Diseño

## Descripción de la sección

Los pilares son los principios que deben mantenerse durante todo el desarrollo. Cuando dos ideas entren en conflicto, los pilares ayudan a decidir cuál encaja mejor con la identidad del juego.

## Pilar 1 — Unicidad

**Descripción:** Cada personaje jugable, nuevo tipo de enemigo, jefe, power-up y partida de juego deberá ser única, el juego depende de que cada que el jugador inicie una nueva partida se sienta diferente a la anterior

**¿Cómo se refleja en el juego?**

- Personajes jugables tienen movesets lo suficientemente diferentes
- Aunque se usen los mismos tipos de enemigos repetidamente, cada nuevo enemigo tiene una dinámica diferente que lo destaca
- Cada power-up que el jugador obtiene durante sus partidas es diferente, pueden existir similitudes entre como funcionan pero tienen que ser lo suficientemente únicos en sus habilidades.

## Pilar 2 — Combate con impacto y legible

**Descripción:** Cada golpe debe sentirse y entenderse. El jugador siempre debe saber qué está pasando en el combate: a quién golpeó, cuánto porcentaje tiene cada personaje y por qué alguien salió volando.

**¿Cómo se refleja en el juego?**

* Cada golpe conectado tiene congelación breve (hitlag), destello y vibración del personaje golpeado. Los lanzamientos fuertes dejan una estela y el último KO de cada nivel se marca con cámara lenta.
* El porcentaje de todos los personajes en pantalla es visible en todo momento.
* Entre más porcentaje tiene un personaje, más lejos sale volando. La regla aplica igual para el jugador y para los enemigos.
* Las ventanas rotas se distinguen con claridad de las intactas.
* Los estados alterados, la carga de ataques fuertes y el parry se comunican con parpadeos y destellos de color.

## Pilar 3 — Ascenso con dificultad gradual

**Descripción:** El jugador sube piso por piso el rascacielos de Nuddle, y el desafío crece de forma gradual conforme sube. Cada tramo del edificio exige lo aprendido antes, con picos de dificultad reconocibles en los enfrentamientos contra Mr. Big Data.

**¿Cómo se refleja en el juego?**

* Los primeros pisos tienen 2 o 3 enemigos. Cada 4 pisos aparece un enemigo más (hasta 16), repartidos en rondas de 4; por eso, al subir, un piso puede tener varias rondas seguidas.
* Los enemigos se vuelven más fuertes poco a poco: reciben menos daño y su IA reacciona más rápido. También aparecen nuevos tipos: antidisturbios, drones y drones kamikaze.
* A partir del piso 3 pueden aparecer enemigos élite, y su número posible aumenta con la altura.
* Al piso 50 espera a Mr. Big Data, el CEO de Nuddle.
* La cafetería (tienda) aparece cada 10 pisos y un piso antes del jefe, para que el jugador se prepare.

## Reglas de decisión

Antes de incorporar una característica importante, preguntar:

- ¿Refuerza uno de nuestros pilares?
- ¿Mejora la experiencia principal?
- ¿Justifica el costo de desarrollo?
- ¿Complica innecesariamente otro sistema?

> [!warning] ⚠️ Evitar
> Convertir los pilares en frases genéricas como “que sea divertido”. Deben describir decisiones concretas de diseño.

> **Navegación:** [[00 - Índice]] · ← [[03 - Público y Plataforma]] · [[01 - Jugabilidad]] →
