# UX y Flujo del Jugador

## Descripción de la sección

UX (experiencia de usuario) describe qué tan comprensible, cómoda y coherente resulta la interacción con el videojuego.

## Flujo principal

```text
Elegir personaje → Combatir las rondas del piso → Elegir boon o mejora, si hay opciones → Ascensor habilitado → Interactuar con el ascensor → Subir al siguiente piso → Tienda o encuentro correspondiente → Jefe final en el piso 100 → Victoria o derrota
```

## Primeros minutos

El jugador elige a su personaje; no se puede cambiar a mitad de partida. Una animación breve muestra cómo se abren las puertas del ascensor y el personaje sale a la primera arena, sin diálogos ni explicación del lore. Al terminar la entrada, comienza la cuenta regresiva de 3, 2, 1, ¡GO! y los enemigos caen al escenario. Los primeros niveles tienen una sola ronda de 3 o 4 enemigos débiles.

Lo que el jugador descubre y aprende:

Moverse, saltar y usar ataques básicos.
Entender el porcentaje: entre más daño, más lejos sale volando un enemigo.
Usar las ventanas: lanzar enemigos contra ellas para romperlas y sacarlos.
Usar ataques fuertes y habilidades en todas direcciones.
Elegir y combinar boons de forma estratégica.
Administrar monedas y vida en las tiendas.

Al limpiar el primer nivel se abre el menú de boons. Después de elegir una mejora, se habilita el ascensor de la arena. El jugador se acerca, identifica el aviso de interacción y lo activa para subir al siguiente piso.

## Retroalimentación

Para cada acción importante define:

**Entrada → Respuesta visual → Respuesta sonora → Resultado**


Golpe conectado

Entrada: un ataque conecta con un personaje.
Respuesta visual: congelación breve del golpe, destello rojo y vibración del personaje golpeado. 
Respuesta sonora: respuesta sonora diferenciada que confirma que el personaje fue golpeado.
Resultado: se suma porcentaje a quien recibe el golpe.

Lanzamiento fuerte

Entrada: un personaje sale volando por el golpe recibido.
Respuesta visual: destello y estela de color detrás del personaje.
Respuesta sonora: por definir.
Resultado: entre más porcentaje tiene, más lejos sale volando.

Estado alterado

Entrada: un golpe activa el efecto de un boon.
Respuesta visual: el personaje parpadea con el color del efecto.
Respuesta sonora: sonidos diferenciados para hielo, electricidad, fuego, veneno, etc.
Resultado: el efecto es usado y se diferencia por lo que le hace al enemigo.

Personaje fuera del escenario (KO)

Entrada: un personaje cruza el límite del escenario.
Respuesta visual: durante el lanzamiento permanece visible con una pose que comunica la dirección y la fuerza del impacto. Al cruzar el límite desaparece y se genera un destello en el punto de salida. No se muestra una animación de muerte ni queda un cuerpo en el escenario.
Respuesta sonora: señal breve asociada a su caída o salida del combate.
Resultado: el personaje queda fuera del combate. Si es el jugador, pierde una vida y reaparece en una plataforma temporal, con 0% e invulnerable por unos instantes. Si es un enemigo, da monedas.


## Fricción intencional

¿Qué dificultad forma parte del diseño y qué dificultad es simplemente mala experiencia de usuario?

Dificultad que forma parte del diseño:

Entre más porcentaje tiene un personaje, más lejos sale volando. Esta regla aplica igual para el jugador y los enemigos.

Se pierde una vida al salir de los límites del escenario. El jugador tiene 3 vidas.

No hay mejoras permanentes entre partidas: cada partida empieza desde cero.

La dificultad sube de forma gradual: más rondas por nivel, enemigos más fuertes y más élites. Hay picos con un mini-jefe cada 20 niveles.

Dificultad que no forma parte del diseño:

Que el combate se sienta "flotado" o injusto.
Combinaciones de controles innecesariamente complejas.
Que no se vea el porcentaje de todos los personajes en pantalla.
Que las ventanas rotas no se distingan con claridad de las intactas.


## Descubrimiento

¿Cómo sabe el jugador:

- Qué hacer?
- ¿Dónde ir?

Al completar el piso y resolver la elección de boon, el ascensor se identifica con una luz verde. El jugador se acerca e interactúa con él para avanzar.

- ¿Qué puede interactuar?

El jugador elige boons en su menú, compra en la tienda y activa el ascensor cuando está disponible.

- Qué ocurrió?
- Por qué ganó o perdió?



¿Qué hacer? 
El indicador de objetivo comunica la tarea inmediata: derrotar al grupo de enemigos, avanzar o enfrentar al jefe.

¿Dónde ir?
 El jugador sube piso por piso: al limpiar un nivel, el personaje salta al piso de arriba. Hay avisos breves cuando hay una elección de mejora o una transición disponible.

¿Qué puede interactuar?
El jugador elige boons en el menú de boons y compra en la tienda. 

¿Qué ocurrió?
Los golpes se comunican con congelación breve, destellos, estelas, parpadeos de color y sonidos diferenciados. El porcentaje de todos los personajes siempre debe verse en pantalla.

¿Por qué ganó o perdió?

Se pierde una vida al salir disparado del escenario, por una ventana rota o por los límites del escenario. Se pierde la partida al perder las 3 vidas.
Se gana al derrotar al jefe final en el nivel 100. Aparece una pantalla de ¡Victoria! y la partida termina.


> **Navegación:** [[00 - Índice]] · ← [[05 - Audio y Música]] · [[02 - UI y Menús]] →
