# Pruebas

## Descripción de la sección

Define cómo se comprobará que el videojuego funciona como fue diseñado.

## Tipos de prueba

### Pruebas funcionales

Comprueban que una característica haga lo que debe.

- Daño por porcentaje, retroceso y KO al salir de los límites del escenario.
- Vidas y reaparición en una plataforma temporal con 0% e invulnerabilidad.
- Ventanas rompibles: pared intacta, ruptura con un golpe muy fuerte, regeneración y reparación al cambiar de piso.
- Escudo, parry y esquive en el suelo y en el aire.
- Moveset de Niko, Mateo Cruz y Mr. Wobbles, sin agarres.
- Menú de boons: 3 opciones, máximo 3 boons, hasta nivel 5 y omisión del menú cuando no hay opciones.
- Tienda: compra de comida y mejoras de boons, y compra bloqueada por saldo insuficiente.

### Pruebas de integración

Comprueban que varios sistemas funcionen correctamente juntos.

- **Entrada → Personajes → Combate:** el botón presionado ejecuta el ataque correcto y Combate resuelve el golpe.
- **Combate → Escenario:** un lanzamiento fuerte rompe una ventana y la salida de los límites se registra como KO.
- **KO → Niveles → Boons:** al quedar fuera todos los enemigos, el nivel termina y se abre el menú de boons.
- **KO → Economía:** cada enemigo derrotado da monedas y el saldo se actualiza en el HUD.
- **Boons → Ascensor → Niveles:** el ascensor se habilita después de limpiar todas las rondas y resolver la elección de boon.
- **Estructura de la partida:** tiendas en los pisos 10, 19, 30, 39, 50, 59, 70, 79, 90 y 99; mini-jefes en los pisos 20, 40, 60 y 80; Big Data en el piso 100.

### Pruebas de usabilidad

Comprueban si los jugadores entienden y pueden utilizar el sistema.

- Un jugador nuevo puede moverse, saltar y atacar en el primer piso sin leer instrucciones externas.
- El jugador sabe en todo momento si debe pelear, elegir un boon o ir al ascensor.
- El porcentaje de todos los personajes en pantalla es visible en todo momento.
- Una ventana rota se distingue de una intacta y el estado del ascensor se entiende sin depender solo del color.
- En la tienda, el jugador duda entre curarse y mejorar un boon.

### Pruebas de rendimiento

Comprueban FPS, memoria, tiempos de carga y estabilidad.

- 60 FPS estables a 1920×1080 en un equipo con los requisitos recomendados.
- Sin caídas sostenidas por debajo de 30 FPS a 1280×720 en un equipo con los requisitos mínimos.
- Menos de 10 segundos para entrar a la partida en condiciones normales.
- Hasta 4 GB de RAM durante la ejecución, sin crecimiento sostenido entre el piso 1 y el piso 100.
- Recorrido del piso 1 al 100 sin cierres inesperados ni bloqueos.

## Casos de prueba

### CP-01 · Retroceso según el porcentaje

**Objetivo:** Comprobar que el retroceso crece con el porcentaje de quien recibe el golpe.

**Precondiciones:** Partida iniciada en el piso 1 con cualquiera de los tres personajes. Hay al menos dos enemigos en el escenario.

**Pasos:**

1. Golpear a un enemigo hasta que acumule mucho porcentaje.
2. Golpear a otro enemigo una sola vez para que tenga poco porcentaje.
3. Lanzar a ambos enemigos con el mismo ataque fuerte.

**Resultado esperado:** Cada golpe suma porcentaje a quien lo recibe. El enemigo con más porcentaje sale volando visiblemente más lejos que el de menos porcentaje.

**Resultado obtenido:**

**Estado:**

### CP-02 · KO, pérdida de vida y reaparición

**Objetivo:** Comprobar que salir de los límites del escenario cuenta como KO y que el jugador reaparece correctamente.

**Precondiciones:** Partida iniciada con 3 vidas.

**Pasos:**

1. Dejar que los enemigos suban el porcentaje del jugador.
2. Permitir que el jugador salga de los límites del escenario.
3. Observar la reaparición y el contador de vidas.
4. Repetir hasta perder la tercera vida.

**Resultado esperado:** Cada salida del escenario cuenta como KO. El jugador pierde una vida, reaparece en una plataforma temporal con 0% e invulnerable unos instantes. Al perder la tercera vida, se muestra la pantalla de derrota.

**Resultado obtenido:**

**Estado:**

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

**Resultado obtenido:**

**Estado:**

### CP-04 · Escudo, parry y esquive

**Objetivo:** Comprobar las herramientas de defensa del jugador.

**Precondiciones:** Partida iniciada. Hay un enemigo atacando al jugador.

**Pasos:**

1. Mantener el escudo arriba mientras el enemigo ataca hasta que el escudo se rompa.
2. Bloquear justo a tiempo un ataque del enemigo.
3. Esquivar hacia un lado en el suelo.
4. Esquivar en el aire.

**Resultado esperado:** El escudo bloquea los golpes y se desgasta. Al romperse, el personaje queda aturdido. Bloquear justo a tiempo provoca un parry con destello azul y el atacante queda expuesto. El esquive en el suelo y en el aire da un momento de invulnerabilidad.

**Resultado obtenido:**

**Estado:**

### CP-05 · Moveset de los personajes

**Objetivo:** Comprobar que cada combinación de botón y dirección produce el ataque documentado.

**Precondiciones:** Partida iniciada con Niko. Se repite con Mateo Cruz y con Mr. Wobbles.

**Pasos:**

1. Ejecutar los ataques básicos neutral, lado, arriba, abajo y en carrera.
2. Ejecutar las habilidades neutral, lado, arriba y abajo.
3. Cargar y soltar los ataques fuertes hacia el lado, arriba y abajo.
4. Ejecutar los ataques aéreos neutral, adelante, atrás, arriba y abajo.
5. Presionar el botón de agarre del prototipo (I / RB).

**Resultado esperado:** Cada combinación produce el ataque documentado para el personaje. El ataque neutral básico es un combo de 3 golpes. El personaje parpadea en amarillo al cargar un ataque fuerte. No existe ningún agarre.

**Resultado obtenido:**

**Estado:**

### CP-06 · Menú de boons

**Objetivo:** Comprobar las reglas de oferta y límite de los boons.

**Precondiciones:** Partida iniciada sin boons.

**Pasos:**

1. Limpiar el primer piso y revisar las opciones del menú de boons.
2. Continuar hasta tener 3 boons equipados y revisar las opciones ofrecidas.
3. Mejorar un boon hasta el nivel 5.
4. Llegar a un piso en el que no haya boons ni mejoras disponibles.

**Resultado esperado:** Se ofrecen 3 opciones al azar. Con 3 boons equipados, solo se ofrecen mejoras de los boons que ya tiene el jugador. Ningún boon pasa del nivel 5. Si no hay opciones, el menú se omite y se habilita el ascensor.

**Resultado obtenido:**

**Estado:**

### CP-07 · Avance por ascensor

**Objetivo:** Comprobar que el ascensor solo se habilita al completar el piso.

**Precondiciones:** Partida iniciada en un piso con más de una ronda de enemigos.

**Pasos:**

1. Acercarse al ascensor e intentar interactuar con él durante el combate.
2. Limpiar todas las rondas del piso.
3. Intentar interactuar con el ascensor con el menú de boons abierto.
4. Elegir un boon, acercarse al ascensor e interactuar con él.

**Resultado esperado:** Durante el combate, el ascensor tiene las puertas cerradas y luz roja, y no se puede activar. Después de limpiar todas las rondas y resolver la elección de boon, muestra luz verde y el aviso del botón de interacción al acercarse. Al activarlo, las puertas se cierran, cambia el indicador de piso y se abren en el siguiente nivel.

**Resultado obtenido:**

**Estado:**

### CP-08 · Tienda

**Objetivo:** Comprobar la compra de comida y mejoras de boons con las monedas de la partida.

**Precondiciones:** Partida en el piso 10 con monedas y al menos un boon equipado.

**Pasos:**

1. Consultar los productos y sus precios.
2. Comprar comida con porcentaje acumulado.
3. Comprar una mejora de boon.
4. Intentar comprar un producto con saldo insuficiente.
5. Salir de la tienda.

**Resultado esperado:** La comida reduce el porcentaje. La mejora de boon sube el nivel del boon. La compra con saldo insuficiente queda bloqueada. Después de cada compra, el saldo se actualiza en la tienda y en el HUD. Al salir, continúa el flujo del piso correspondiente.

**Resultado obtenido:**

**Estado:**

### CP-09 · Estructura de la partida y victoria

**Objetivo:** Comprobar la ubicación de tiendas, mini-jefes y jefe final, y la condición de victoria.

**Precondiciones:** Compilación de PC. Partida nueva con cualquiera de los tres personajes.

**Pasos:**

1. Subir piso por piso y registrar en qué pisos aparece la tienda.
2. Registrar en qué pisos aparece un mini-jefe.
3. Llegar al piso 100 y derrotar a Big Data.

**Resultado esperado:** Las tiendas aparecen solo en los pisos 10, 19, 30, 39, 50, 59, 70, 79, 90 y 99. Los mini-jefes aparecen en los pisos 20, 40, 60 y 80. Al derrotar a Big Data en el piso 100, aparece la pantalla de ¡Victoria! sin otro ascenso ni elección de boon. Al continuar, se muestran los créditos y después el menú principal.

**Resultado obtenido:**

**Estado:**

### CP-10 · Partida nueva sin progreso permanente

**Objetivo:** Comprobar que cada partida empieza desde cero.

**Precondiciones:** Haber terminado una partida, por victoria o por derrota, con monedas y boons.

**Pasos:**

1. Continuar desde la pantalla de victoria, pasando por los créditos, o desde la pantalla de derrota hasta el menú principal.
2. Iniciar una partida nueva.
3. Revisar el HUD.

**Resultado esperado:** La partida nueva empieza con 0 monedas, sin boons, con 3 vidas y en el piso 1.

**Resultado obtenido:**

**Estado:**

### CP-11 · Teclado y mando

**Objetivo:** Comprobar que el juego funciona igual con teclado y con mando.

**Precondiciones:** Compilación de PC con un mando disponible.

**Pasos:**

1. Iniciar el juego y jugar un piso con teclado.
2. Conectar el mando durante la partida.
3. Jugar un piso con el mando.

**Resultado esperado:** Todas las acciones funcionan con teclado y con mando. El mando se detecta sin reiniciar el juego.

**Resultado obtenido:**

**Estado:**

### CP-12 · Primer piso con un jugador nuevo

**Objetivo:** Comprobar que un jugador nuevo entiende los controles y el objetivo sin ayuda.

**Precondiciones:** Jugador que no conoce el juego. Compilación de PC.

**Pasos:**

1. Pedir al jugador que inicie una partida sin darle instrucciones.
2. Observar cómo juega el primer piso.
3. Observar si identifica el menú de boons y el ascensor habilitado.

**Resultado esperado:** El jugador se mueve, salta y ataca en el primer piso sin leer instrucciones externas. Sabe cuándo debe pelear, elegir un boon o ir al ascensor. Distingue las ventanas rotas de las intactas y el estado del ascensor.

**Resultado obtenido:**

**Estado:**

### CP-13 · Rendimiento con requisitos recomendados

**Objetivo:** Comprobar los objetivos de rendimiento en un equipo con los requisitos recomendados.

**Precondiciones:** Equipo con los requisitos recomendados de [[03 - Requisitos Técnicos]]. Compilación de PC a 1920×1080.

**Pasos:**

1. Medir el tiempo desde iniciar la partida hasta entrar al primer piso.
2. Jugar un piso con el máximo de enemigos y efectos de boons en pantalla mientras se miden los FPS.
3. Medir el uso de RAM en el piso 1 y en el piso 100.

**Resultado esperado:** La carga tarda menos de 10 segundos. Los FPS se mantienen estables en 60. El uso de RAM no pasa de 4 GB y no crece de forma sostenida entre el piso 1 y el piso 100.

**Resultado obtenido:**

**Estado:**

### CP-14 · Rendimiento con requisitos mínimos

**Objetivo:** Comprobar que el juego es jugable en un equipo con los requisitos mínimos.

**Precondiciones:** Equipo con los requisitos mínimos de [[03 - Requisitos Técnicos]]. Compilación de PC a 1280×720.

**Pasos:**

1. Iniciar una partida.
2. Jugar varios pisos con enemigos y efectos de boons en pantalla mientras se miden los FPS.

**Resultado esperado:** El juego es jugable y no tiene caídas sostenidas por debajo de 30 FPS.

**Resultado obtenido:**

**Estado:**

### CP-15 · Estabilidad del recorrido completo

**Objetivo:** Comprobar que se puede completar la partida sin fallos.

**Precondiciones:** Compilación de PC.

**Pasos:**

1. Jugar una partida completa del piso 1 al 100.
2. Revisar la consola durante la partida.
3. Cerrar el juego, volver a abrirlo y revisar la configuración.

**Resultado esperado:** El recorrido se completa sin cierres inesperados ni bloqueos. No aparecen errores en consola, referencias perdidas ni assets faltantes. La configuración se conserva al cerrar y abrir el juego.

**Resultado obtenido:**

**Estado:**


> **Navegación:** [[00 - Índice]] · ← [[01 - Criterios de Calidad]] · [[03 - Bugs y Seguimiento]] →
