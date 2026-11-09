# Jugabilidad

## Descripción de la sección

La jugabilidad explica **qué hace el jugador, qué recibe a cambio y cómo evoluciona la experiencia**.

## Bucle principal de juego

Describe el ciclo que se repite durante la experiencia.

**Ejemplo conceptual:**

`Explorar → Encontrar desafío → Resolver → Obtener recompensa → Mejorar → Explorar`

**Bucle del proyecto:**
 Rift es un roguelike de combate de plataformas al estilo Smash Bros. El jugador sube piso por piso un rascacielos corporativo, peleando contra oleadas de enemigos y construyendo su personaje con boons hasta llegar al jefe.

`Elegir personaje → Pelear contra una o varias rondas de enemigos → Elegir o mejorar un boon, si hay opciones disponibles → Activar el ascensor → Subir al siguiente piso → Tienda cuando corresponda → Continuar los encuentros → Jefe final en el piso 100 → Victoria o derrota → Nueva partida`

Cada **nivel** es un piso del rascacielos. Al completar todas sus rondas, el jugador elige un boon o una mejora, si hay opciones disponibles. Después se habilita el ascensor, ubicado dentro de la misma arena. El jugador se acerca y lo activa mediante una interacción para subir al siguiente piso. No se necesita una tarjeta de acceso.

## Acciones principales del jugador

| Acción | Propósito | Resultado |
|---|---|---|
| Atacar (básicos, habilidades y ataques fuertes en todas direcciones) | Subir el porcentaje de daño de los enemigos | Entre más porcentaje, más lejos salen volando |
| Sacar enemigos del escenario | Derrotarlos (KO) | Al eliminar a todos, se limpia el nivel |
| Escudo y esquive | Evitar el daño propio | Mantener tu porcentaje bajo para no salir volando |
| Moverse y saltar (doble salto) | Posicionarse y volver al escenario | Sobrevivir y alcanzar a los enemigos |
| Elegir boons | Personalizar el estilo de pelea | Cada partida se juega diferente |
| Comprar en la tienda | Curarse o mejorar boons | Llegar más lejos en la partida |

## Experiencia segundo a segundo

La partida comienza con una animación breve: las puertas del ascensor se abren y el personaje seleccionado sale a la primera arena. Después aparece la cuenta regresiva **3, 2, 1, ¡GO!** y los enemigos caen al escenario. El jugador se mueve, combina ataques básicos, habilidades y ataques fuertes, se cubre con el escudo o esquiva, y busca subir el porcentaje de los enemigos hasta lanzarlos por las ventanas del edificio.

## Experiencia minuto a minuto

1. Limpiar las rondas de enemigos del nivel (de 1 a 3 rondas, según la altura).
2. Elegir uno de los boons o mejoras disponibles. Si no quedan opciones, se omite esta elección.
3. Acercarse al ascensor habilitado e interactuar con él para subir al siguiente piso mediante una transición breve.
4. Visitar una tienda para curarse o mejorar boons con las monedas obtenidas. Hay **tienda cada 10 niveles**, excepto cuando el siguiente nivel tiene un mini-jefe o el jefe final: en ese caso, la tienda aparece **un nivel antes** para que el jugador se prepare. Las tiendas quedan en los niveles **10, 19, 30, 39, 50, 59, 70, 79, 90 y 99**.
5. Cada **20 niveles**, enfrentar a un **mini-jefe**: un **enemigo élite**.
6. En el **nivel 100**, la cima del edificio, enfrentar al **jefe final**.

## Experiencia a largo plazo

Cada partida es diferente gracias a las combinaciones de boons, la aparición aleatoria de enemigos élite y la elección entre Niko, Mateo Cruz y Mr. Wobbles. El jugador quiere volver para probar otras combinaciones, dominar el combate y llegar más lejos.

## Condición de victoria

Derrotar al **jefe final** en el **nivel 100** (en la entrega, Big Data Nuddleman). Aparece una pantalla de **¡Victoria!**, como en Hades, y **la partida termina ahí**.

## Condición de derrota

Perder las **3 vidas**. Se pierde una vida al salir disparado del escenario (por una ventana rota o por los límites del escenario). En la historia, el personaje escapa en paracaídas y regresa a La Coladera. **La Coladera no es un lugar jugable:** solo existe en el lore. Lo único jugable son las oficinas; todo lo demás es interfaz (UI).

## Ritmo

- **Acción:** la mayor parte del tiempo. Peleas cortas e intensas en cada piso.
- **Desafío:** sube de forma gradual: más rondas por nivel, enemigos más fuertes y más élites. Hay picos con un mini-jefe cada 20 niveles y el jefe final en el nivel 100.
- **Recompensa:** después de cada nivel (boon) y en cada tienda.
- **Descanso:** breve, en el menú de boons, antes de activar el ascensor, durante la transición entre pisos y en las tiendas.
- **Historia:** solo en las tiendas (NPC) y en el almanaque del menú. Nunca interrumpe el combate.
- **Exploración:** no hay.

## Principios de interacción

- Entre más porcentaje tiene un personaje, más lejos sale volando. Esta regla aplica igual para el jugador y los enemigos.
- Siempre debe verse el porcentaje de todos los personajes en pantalla.
- Los golpes deben sentirse: congelación breve del golpe (hitlag), destello y estela al salir volando.
- El último KO de cada nivel se marca con cámara lenta.
- Las ventanas rotas deben distinguirse con claridad de las que están intactas.


> **Navegación:** [[00 - Índice]] · ← [[04 - Pilares de Diseño]] · [[02 - Mecánicas]] →
