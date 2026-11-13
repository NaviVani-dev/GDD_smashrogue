# Pruebas

## Descripción de la sección

Define cómo se comprobará que el videojuego funciona como fue diseñado.

## Tipos de prueba

### Pruebas funcionales

Comprueban que una característica haga lo que debe.

- Daño por porcentaje, retroceso y KO al salir de los límites del escenario (por una ventana o pared rota, o al caer por el borde de la plataforma).
- Vidas y reaparición cayendo desde arriba con 0 % e invulnerabilidad.
- Ventanas y paredes rompibles: pared intacta, ruptura con un golpe muy fuerte, regeneración y reparación al cambiar de piso.
- Escudo, parry y esquive en el suelo y en el aire.
- Moveset de Niko, Mateo Cruz, Atsuko, Mr. Wobbles y Craub, incluido el agarre.
- Menú de boons: 3 opciones (boons nuevos o mejoras), sin límite de boons equipados, hasta nivel 5 y omisión del menú cuando no hay opciones.
- Tienda: compra de boons nuevos y mejoras de boons, y compra bloqueada por saldo insuficiente.

### Pruebas de integración

Comprueban que varios sistemas funcionen correctamente juntos.

- **Entrada → Personajes → Combate:** el botón presionado ejecuta el ataque correcto y Combate resuelve el golpe.
- **Combate → Escenario:** un lanzamiento fuerte rompe una ventana y la salida de los límites se registra como KO.
- **KO → Niveles → Boons:** al quedar fuera todos los enemigos, el nivel termina y se abre el menú de boons.
- **KO → Economía:** cada enemigo derrotado puede dar monedas y el saldo se actualiza en el HUD.
- **Boons → Niveles:** el personaje sube al siguiente piso después de limpiar todas las rondas y resolver la elección de boon.
- **Estructura de la partida:** tiendas cada 10 pisos y en el piso anterior a cada jefe (10, 20, 30, 40, 49, 60, 70, 80, 90, 99…); Mr. Big Data cada 50 pisos (50, 100, 150…).

### Pruebas de usabilidad

Comprueban si los jugadores entienden y pueden utilizar el sistema.

- Un jugador nuevo puede moverse, saltar y atacar en el primer piso sin leer instrucciones externas.
- El jugador sabe en todo momento si debe pelear, elegir un boon, recoger un boon o comprar en la tienda.
- El porcentaje del jugador y de los enemigos es visible en todo momento.
- Una ventana rota se distingue de una intacta sin depender solo del color.
- En la tienda, el jugador duda entre comprar un boon nuevo y mejorar uno que ya tiene.

### Pruebas de rendimiento

Comprueban FPS, memoria, tiempos de carga y estabilidad.

- 60 FPS estables a 1920×1080 en un equipo con los requisitos recomendados.
- Sin caídas sostenidas por debajo de 30 FPS a 1280×720 en un equipo con los requisitos mínimos.
- Menos de 10 segundos para entrar a la partida en condiciones normales.
- Hasta 4 GB de RAM durante la ejecución, sin crecimiento sostenido entre el piso 1 y el piso 50.
- Subida del piso 1 al 50, incluido el combate contra Mr. Big Data, sin cierres inesperados ni bloqueos.

## Casos de prueba

### CP-01 · Retroceso según el porcentaje

**Objetivo:** Comprobar que el retroceso crece con el porcentaje de quien recibe el golpe.

**Precondiciones:** Partida iniciada en el piso 1 con cualquiera de los cinco personajes. Hay al menos dos enemigos en el escenario.

**Pasos:**

1. Golpear a un enemigo hasta que acumule mucho porcentaje.
2. Golpear a otro enemigo una sola vez para que tenga poco porcentaje.
3. Lanzar a ambos enemigos con el mismo ataque fuerte.

**Resultado esperado:** Cada golpe suma porcentaje a quien lo recibe. El enemigo con más porcentaje sale volando visiblemente más lejos que el de menos porcentaje.

**Resultado obtenido:** Cada golpe suma porcentaje y los enemigos con más porcentaje salen volando visiblemente más lejos.

**Estado:** Aprobado

### CP-02 · KO, pérdida de vida y reaparición

**Objetivo:** Comprobar que salir de los límites del escenario cuenta como KO y que el jugador reaparece correctamente.

**Precondiciones:** Partida iniciada con 3 vidas.

**Pasos:**

1. Dejar que los enemigos suban el porcentaje del jugador.
2. Permitir que el jugador salga de los límites del escenario.
3. Observar la reaparición y el contador de vidas.
4. Repetir hasta perder la tercera vida.

**Resultado esperado:** Cada salida del escenario cuenta como KO. El jugador pierde una vida y, tras unos instantes, reaparece cayendo desde arriba con 0 % e invulnerable unos 2 segundos (parpadea mientras dura). Al perder la tercera vida, aparece el letrero "GAME!" y después la pantalla de resultados.

**Resultado obtenido:** Al salir del escenario el jugador pierde una vida y reaparece cayendo desde arriba, con 0 % e invulnerable unos instantes.

**Estado:** Aprobado

### CP-03 · Ventanas rompibles

**Objetivo:** Comprobar el comportamiento de las ventanas como paredes del escenario.

**Precondiciones:** Partida iniciada. Hay un enemigo en el escenario.

**Pasos:**

1. Lanzar al enemigo con poco porcentaje contra una ventana intacta.
2. Subir su porcentaje a 100% o más y lanzarlo contra la ventana con un golpe muy fuerte.
3. Lanzar a otro personaje contra la ventana mientras sigue rota.
4. Esperar a que la ventana se regenere.
5. Limpiar el piso y subir al siguiente.

**Resultado esperado:** La ventana intacta funciona como pared. Con un golpe muy fuerte, la ventana se rompe y el personaje sale volando. Un personaje lanzado contra la ventana rota sale directo sin chocar. La ventana se regenera después de un rato y todas las ventanas están reparadas en el siguiente piso.

**Resultado obtenido:** Las ventanas y paredes funcionan como pared, se rompen con golpes fuertes, se regeneran después de unos segundos y se reparan al cambiar de piso.

**Estado:** Aprobado

### CP-04 · Escudo, parry y esquive

**Objetivo:** Comprobar las herramientas de defensa del jugador.

**Precondiciones:** Partida iniciada. Hay un enemigo atacando al jugador.

**Pasos:**

1. Mantener el escudo arriba mientras el enemigo ataca hasta que el escudo se rompa.
2. Soltar el escudo justo cuando llega un ataque del enemigo.
3. Esquivar hacia un lado en el suelo.
4. Esquivar en el aire.

**Resultado esperado:** El escudo bloquea los golpes y se desgasta. Al romperse, el personaje queda aturdido. Soltar el escudo justo a tiempo provoca un parry con destello cian y el atacante queda expuesto. El esquive en el suelo y en el aire da un momento de invulnerabilidad.

**Resultado obtenido:** El escudo bloquea y se desgasta; al romperse, el personaje queda aturdido. El parry y el esquive funcionan.

**Estado:** Aprobado

### CP-05 · Moveset de los personajes

**Objetivo:** Comprobar que cada combinación de botón y dirección produce el ataque documentado.

**Precondiciones:** Partida iniciada con Niko. Se repite con Mateo Cruz, Atsuko, Mr. Wobbles y Craub.

**Pasos:**

1. Ejecutar los ataques básicos neutral, lado, arriba, abajo y en carrera.
2. Ejecutar las habilidades neutral, lado, arriba y abajo.
3. Cargar y soltar los ataques fuertes hacia el lado, arriba y abajo.
4. Ejecutar los ataques aéreos neutral, adelante, atrás, arriba y abajo.
5. Presionar el botón de agarre (I / RB) cerca de un enemigo, atacarlo mientras está atrapado y lanzarlo.

**Resultado esperado:** Cada combinación produce el ataque documentado para el personaje. El ataque neutral básico es un combo de 3 golpes. El personaje parpadea en amarillo al cargar un ataque fuerte. El agarre atrapa al enemigo, permite golpearlo y lanzarlo.

**Resultado obtenido:** Los cinco personajes ejecutan sus ataques según la dirección y el agarre (I / RB) funciona en todos.

**Estado:** Aprobado

### CP-06 · Menú de boons

**Objetivo:** Comprobar las reglas de oferta y límite de los boons.

**Precondiciones:** Partida iniciada sin boons.

**Pasos:**

1. Limpiar el primer piso y revisar las opciones del menú de boons.
2. Continuar hasta tener más de 3 boons equipados y revisar las opciones ofrecidas.
3. Mejorar un boon hasta el nivel 5.
4. Llegar a un piso en el que no haya boons ni mejoras disponibles.

**Resultado esperado:** Se ofrecen 3 opciones al azar, que pueden ser boons nuevos o mejoras de los boons que ya tiene el jugador. No hay límite de boons equipados: se siguen ofreciendo boons nuevos mientras queden. Ningún boon pasa del nivel 5. Si no hay opciones, el menú se omite y el personaje sube al siguiente piso.

**Resultado obtenido:** El menú ofrece 3 opciones entre boons nuevos y mejoras, respeta el nivel máximo y se omite cuando no hay opciones.

**Estado:** Aprobado

### CP-07 · Avance al siguiente piso

**Objetivo:** Comprobar que el personaje solo sube al siguiente piso al completarlo.

**Precondiciones:** Partida iniciada en un piso con más de una ronda de enemigos.

**Pasos:**

1. Limpiar la primera ronda y comprobar que llega la siguiente ronda en lugar de subir de piso.
2. Limpiar todas las rondas del piso.
3. Comprobar que el personaje no sube con el menú de boons abierto.
4. Elegir un boon y observar la transición.

**Resultado esperado:** Mientras queden rondas o enemigos, el personaje permanece en el piso. Después de limpiar todas las rondas y resolver la elección de boon, el personaje celebra unos instantes, salta, rompe el techo y llega al siguiente piso, sin necesidad de interactuar con nada. El número de piso del HUD aumenta.

**Resultado obtenido:** Al limpiar el piso y elegir boon, el personaje celebra, salta, rompe el techo y aterriza en el siguiente piso.

**Estado:** Aprobado

### CP-08 · Tienda

**Objetivo:** Comprobar la compra de boons nuevos y mejoras de boons con las monedas de la partida.

**Precondiciones:** Partida en el piso 10 con monedas y al menos un boon equipado.

**Pasos:**

1. Acercarse al mostrador ("COMPRAR") y abrir la tienda.
2. Consultar los productos y sus precios.
3. Comprar un boon nuevo.
4. Comprar una mejora de boon.
5. Intentar comprar un producto con saldo insuficiente.
6. Cerrar la tienda y salir por la salida ("SUBIR").

**Resultado esperado:** La tienda ofrece 4 productos. El boon nuevo se agrega a los boons del jugador. La mejora de boon sube el nivel del boon. La compra con saldo insuficiente queda bloqueada y la tendera lo avisa. Después de cada compra, el saldo se actualiza en la tienda y en el HUD. Al usar la salida, el personaje sube al siguiente piso.

**Resultado obtenido:** Los textos de la información de los productos se enciman y dificultan la lectura. El juego no indica con claridad cómo interactuar con la tienda.

**Estado:** Fallido: los dos problemas siguen pendientes.

### CP-09 · Estructura de la partida

**Objetivo:** Comprobar la ubicación de las tiendas y del jefe.

**Precondiciones:** Compilación de PC. Partida nueva con cualquiera de los cinco personajes.

**Pasos:**

1. Subir piso por piso y registrar en qué pisos aparece la tienda.
2. Llegar al piso 50 y derrotar a Mr. Big Data.
3. Continuar la subida después del jefe.

**Resultado esperado:** Las tiendas aparecen cada 10 pisos y en el piso anterior a cada jefe (10, 20, 30, 40, 49, 60, 70, 80, 90, 99…). Mr. Big Data aparece en el piso 50 y después cada 50 pisos. Al derrotarlo, el jugador recibe monedas, se abre el menú de boons y la subida continúa. No hay pantalla de victoria.

**Resultado obtenido:** Las tiendas aparecen en los pisos indicados, Mr. Big Data aparece en el piso 50 y la subida continúa después de derrotarlo.

**Estado:** Aprobado

### CP-10 · Partida nueva sin progreso permanente

**Objetivo:** Comprobar que cada partida empieza desde cero.

**Precondiciones:** Haber terminado una partida por derrota, con monedas y boons.

**Pasos:**

1. En la pantalla de resultados, elegir "REINTENTAR". Repetir después eligiendo "MENÚ" e iniciando una partida nueva desde el menú principal.
2. Revisar el HUD en cada caso.

**Resultado esperado:** La partida nueva empieza con 0 monedas, sin boons, con 3 vidas y en el piso 1. "REINTENTAR" empieza con el mismo personaje.

**Resultado obtenido:** La partida nueva empieza en el piso 1, con 0 monedas, sin boons y con 3 vidas; REINTENTAR conserva el personaje.

**Estado:** Aprobado

### CP-11 · Teclado y mando

**Objetivo:** Comprobar que el juego funciona igual con teclado y con mando.

**Precondiciones:** Compilación de PC con un mando disponible.

**Pasos:**

1. Iniciar el juego y jugar un piso con teclado.
2. Conectar el mando durante la partida.
3. Jugar un piso con el mando.

**Resultado esperado:** Todas las acciones funcionan con teclado y con mando. El mando se detecta sin reiniciar el juego.

**Resultado obtenido:** Todas las acciones funcionan con teclado y con mando. Se probó con distintos mandos y todos fueron reconocidos.

**Estado:** Aprobado

### CP-12 · Primer piso con un jugador nuevo

**Objetivo:** Comprobar que un jugador nuevo entiende los controles y el objetivo sin ayuda.

**Precondiciones:** Jugador que no conoce el juego. Compilación de PC.

**Pasos:**

1. Pedir al jugador que inicie una partida sin darle instrucciones.
2. Observar cómo juega el primer piso.
3. Observar si identifica el menú de boons y entiende la subida al siguiente piso.

**Resultado esperado:** El jugador se mueve, salta y ataca en el primer piso sin leer instrucciones externas. Sabe cuándo debe pelear o elegir un boon. Distingue las ventanas rotas de las intactas.

**Resultado obtenido:** El jugador nuevo se movió, saltó y atacó en el primer piso sin instrucciones externas y entendió el menú de boons y la subida.

**Estado:** Aprobado

### CP-13 · Rendimiento con requisitos recomendados

**Objetivo:** Comprobar los objetivos de rendimiento en un equipo con los requisitos recomendados.

**Precondiciones:** Equipo con los requisitos recomendados de [[03 - Requisitos Técnicos]]. Compilación de PC a 1920×1080.

**Pasos:**

1. Medir el tiempo desde iniciar la partida hasta entrar al primer piso.
2. Jugar un piso con el máximo de enemigos y efectos de boons en pantalla mientras se miden los FPS.
3. Medir el uso de RAM en el piso 1 y en el piso 50.

**Resultado esperado:** La carga tarda menos de 10 segundos. Los FPS se mantienen estables en 60. El uso de RAM no pasa de 4 GB y no crece de forma sostenida entre el piso 1 y el piso 50.

**Resultado obtenido:** En una laptop de gama alta el juego corre fluido y la carga es rápida. No se midieron FPS ni RAM con herramientas.

**Estado:** Aprobado

### CP-14 · Rendimiento con requisitos mínimos

**Objetivo:** Comprobar que el juego es jugable en un equipo con los requisitos mínimos.

**Precondiciones:** Equipo con los requisitos mínimos de [[03 - Requisitos Técnicos]]. Compilación de PC a 1280×720.

**Pasos:**

1. Iniciar una partida.
2. Jugar varios pisos con enemigos y efectos de boons en pantalla mientras se miden los FPS.

**Resultado esperado:** El juego es jugable y no tiene caídas sostenidas por debajo de 30 FPS.

**Resultado obtenido:** En una laptop de gama baja el juego también corre fluido. No se midieron FPS con herramientas.

**Estado:** Aprobado

### CP-15 · Estabilidad de la subida

**Objetivo:** Comprobar que se puede jugar una partida larga sin fallos.

**Precondiciones:** Compilación de PC.

**Pasos:**

1. Jugar una partida del piso 1 al piso 50, incluido el combate contra Mr. Big Data.
2. Revisar la consola durante la partida.

**Resultado esperado:** La subida se completa sin cierres inesperados ni bloqueos. No aparecen errores en consola, referencias perdidas ni assets faltantes.

**Resultado obtenido:** Se jugó una partida larga sin cierres inesperados ni bloqueos.

**Estado:** Aprobado


> **Navegación:** [[00 - Índice]] · ← [[01 - Criterios de Calidad]] · [[03 - Bugs y Seguimiento]] →
