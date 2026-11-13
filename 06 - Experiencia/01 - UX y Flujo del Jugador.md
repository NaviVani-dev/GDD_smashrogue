# UX y Flujo del Jugador

## Descripción de la sección

UX (experiencia de usuario) describe qué tan comprensible, cómoda y coherente resulta la interacción con el videojuego.

## Flujo principal

```text
Elegir personaje → Cuenta regresiva → Combatir las rondas del piso → Elegir boon o mejora, si hay opciones → El personaje salta, rompe el techo y sube al siguiente piso → Tienda o combate según el piso → Jefe cada 50 pisos → La subida continúa hasta perder las 3 vidas → Resultados
```

## Primeros minutos

El jugador elige a su personaje; no se puede cambiar a mitad de partida. El personaje aparece directamente en la primera arena, sin diálogos ni explicación del lore, y comienza la cuenta regresiva de 3, 2, 1, ¡GO! mientras los enemigos saltan al escenario. Los pisos 1 y 2 tienen una sola ronda de 2 enemigos débiles; a partir del piso 3 aumenta la cantidad de enemigos.

Lo que el jugador descubre y aprende:

Moverse, saltar y usar ataques básicos.
Entender el porcentaje: entre más daño, más lejos sale volando un enemigo.
Usar las ventanas: lanzar enemigos contra ellas para romperlas y sacarlos.
Usar ataques fuertes, habilidades y agarres en todas direcciones.
Elegir y combinar boons de forma estratégica.
Recoger los boons que sueltan los enemigos élite.
Administrar monedas en las tiendas.

Al limpiar el primer piso se abre el menú de boons. Después de elegir una mejora, el personaje celebra unos instantes y salta automáticamente: rompe el techo y llega al siguiente piso, sin necesidad de interactuar con nada.

## Retroalimentación

Para cada acción importante define:

**Entrada → Respuesta visual → Respuesta sonora → Resultado**


Golpe conectado

Entrada: un ataque conecta con un personaje.
Respuesta visual: congelación breve del golpe (hitlag), destello blanco y vibración del personaje golpeado. Con 100 %, 125 % y 150 % o más, el personaje además pulsa en rojo con más intensidad.
Respuesta sonora: respuesta sonora diferenciada que confirma que el personaje fue golpeado.
Resultado: se suma porcentaje a quien recibe el golpe.

Lanzamiento fuerte

Entrada: un personaje sale volando por el golpe recibido.
Respuesta visual: estela naranja detrás del personaje.
Respuesta sonora: sonido de lanzamiento según la fuerza del golpe.
Resultado: entre más porcentaje tiene, más lejos sale volando.

Estado alterado

Entrada: un golpe activa el efecto de un boon.
Respuesta visual: el personaje parpadea con el color del efecto; al congelarse queda completamente teñido.
Respuesta sonora: sonidos diferenciados para hielo, electricidad, fuego, veneno, etc.
Resultado: el efecto es usado y se diferencia por lo que le hace al enemigo.

Personaje fuera del escenario (KO)

Entrada: un personaje cruza el límite del escenario, ya sea por los lados, por una ventana rota o por el techo.
Respuesta visual: durante el lanzamiento permanece visible con una pose que comunica la dirección y la fuerza del impacto. Al cruzar el límite desaparece y se genera un destello en el punto de salida. No se muestra una animación de muerte ni queda un cuerpo en el escenario.
Respuesta sonora: señal breve asociada a su caída o salida del combate.
Resultado: el personaje queda fuera del combate. Si es el jugador, pierde una vida y, tras unos instantes, reaparece cayendo desde arriba con 0 % e invulnerable unos 2 segundos (parpadea mientras dura). Si es un enemigo, da monedas. El último KO del piso se marca con cámara lenta.


## Fricción intencional

¿Qué dificultad forma parte del diseño y qué dificultad es simplemente mala experiencia de usuario?

Dificultad que forma parte del diseño:

Entre más porcentaje tiene un personaje, más lejos sale volando. Esta regla aplica igual para el jugador y los enemigos.

Se pierde una vida al salir de los límites del escenario. El jugador tiene 3 vidas.

No hay mejoras permanentes entre partidas: cada partida empieza desde cero.

La dificultad sube de forma gradual: más enemigos por piso (repartidos en rondas de hasta 4), enemigos más fuertes, drones y más élites a partir del piso 3. Hay picos con el jefe Mr. Big Data cada 50 pisos.

Dificultad que no forma parte del diseño:

Que el combate se sienta "flotado" o injusto.
Combinaciones de controles innecesariamente complejas.
Que no se vea el porcentaje de los personajes en pantalla.
Que las ventanas rotas no se distingan con claridad de las intactas.


## Descubrimiento

¿Cómo sabe el jugador:

- Qué hacer?
- ¿Dónde ir?

Al completar el piso y resolver la elección de boon, el personaje sube solo al siguiente piso. En la tienda, la salida se indica con el aviso "SUBIR".

- ¿Qué puede interactuar?

El jugador elige boons en su menú, recoge los boons que sueltan los élites y, en la tienda, usa el mostrador y la salida.

- Qué ocurrió?
- Por qué ganó o perdió?



¿Qué hacer? 
El HUD muestra el contador de KO del piso (enemigos fuera / total) y el número de piso, que comunican la tarea inmediata: derrotar a los enemigos o al jefe.

¿Dónde ir?
 El jugador sube piso por piso: al limpiar un nivel, el personaje salta al piso de arriba. Hay avisos breves cuando se puede recoger un boon ("AGARRAR") y, en la tienda, para comprar ("COMPRAR") o salir ("SUBIR").

¿Qué puede interactuar?
El jugador elige boons en el menú de boons, recoge boons del suelo y compra en la tienda. 

¿Qué ocurrió?
Los golpes se comunican con congelación breve, destellos, estelas, parpadeos de color y sonidos diferenciados. El porcentaje del jugador y de los enemigos se ve en pantalla; el jefe muestra una barra de vida.

¿Por qué ganó o perdió?

Se pierde una vida al salir disparado del escenario, por una ventana rota, por el techo o por los límites del escenario. Se pierde la partida al perder las 3 vidas: aparece el letrero "GAME!" y después la pantalla de resultados.
No hay condición de victoria: la subida no tiene fin y el objetivo es llegar lo más alto posible.


> **Navegación:** [[00 - Índice]] · ← [[05 - Audio y Música]] · [[02 - UI y Menús]] →
