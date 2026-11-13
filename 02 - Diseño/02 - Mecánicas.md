# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

## Plantilla de mecánica

### Nombre de la mecánica

**Propósito:**
¿Qué aporta a la experiencia?

**Activación:**
¿Qué debe hacer el jugador?

**Reglas:**
¿Qué puede y qué no puede ocurrir?

**Entrada:**
¿Qué botón, gesto o acción la activa?

**Estado inicial:**

**Estado final:**

**Recursos utilizados:**

**Recompensa:**

**Penalización:**

**Interacciones con otras mecánicas:**

**Casos límite:**
¿Qué ocurre en situaciones poco comunes?

## Mecánicas principales

### Mecánica 01 — Daño por porcentaje y KO

**Propósito:** Es el corazón del combate, igual que en Smash. El jugador no "baja vida": sube el porcentaje del enemigo hasta poder sacarlo del escenario.

**Activación:** Golpear a un personaje.

**Reglas:**

* Cada golpe suma porcentaje a quien lo recibe (máximo 999%).
* Entre más porcentaje, mayor es el retroceso (knockback) y más lejos sale volando.
* Un personaje queda fuera (KO) al salir de los límites del escenario: por una ventana o pared rota, o al caer por el borde de la plataforma.
* Los **enemigos reciben el daño multiplicado por su susceptibilidad**. Los enemigos normales empiezan en ×2.0 y los élites en ×1.2; el multiplicador baja un poco cada 4 pisos (mínimo ×1.4 y ×0.8). Los personajes jugables reciben el daño sin multiplicador (×1.0).
* El jugador tiene  **3 vidas** ; los enemigos, una.
* **Peso** de los personajes jugables (entre más peso, menos lejos salen volando): Niko 94, Mateo 108, Mr. Wobbles 98, Atsuko 100 y Craub 75.

**Entrada:** Cualquier ataque.

**Estado inicial:** 0%.

**Estado final:** KO al salir del escenario. El jugador reaparece en 0% si le quedan vidas.

**Recursos utilizados:** Vidas del jugador.

**Recompensa:** Monedas por cada enemigo derrotado.

**Penalización:** Perder una vida.

**Interacciones con otras mecánicas:** Ventanas rompibles y boons (por ejemplo, Encendedor, Extintor criogénico, Mancuerna, Casco de obra, Botiquín y Gato de la suerte).

**Casos límite:** Si el último enemigo y el jugador salen al mismo tiempo, se aplican las dos cosas: el piso se completa y el jugador pierde una vida. Si era su última vida, la partida termina (perder tiene prioridad). El boon Gato de la suerte puede evitar ese KO.

### Mecánica 02 — Moveset estilo Smash

**Propósito:** Dar profundidad al combate con controles simples.

**Activación:** Botón de ataque o habilidad combinado con una dirección.

**Reglas:**

* **Ataques básicos** en todas direcciones: neutral (combo de 3 golpes), lado, arriba, abajo y ataque en carrera.
* **Habilidades** (especiales) en todas direcciones: neutral, lado, arriba (recuperación) y abajo.
* **Ataques fuertes** (smash) hacia el lado, arriba y abajo, que se pueden **cargar** hasta 1 s para hacer hasta 40 % más de daño.
* **Ataques aéreos** en el aire: neutral, adelante, atrás, arriba y abajo.
* **Agarres:** el personaje puede agarrar a un enemigo (botón de agarre, o escudo + ataque) y lanzarlo en una dirección. Los agarres atraviesan el escudo.
* Cada personaje tiene su propio moveset: Niko pelea con los puños, Mateo utiliza principalmente patadas de taekwondo y Mr. Wobbles combate con objetos de payaso (globos explosivos, etc.), Atsuko pelea con una motosierra y Craub ataca con sus garras.

**Entrada:** Teclado: ataque básico J, habilidad K, ataque fuerte con las flechas, agarre con I (o L + J). Mando: ataque básico B / ○, habilidad X / □, ataque fuerte con el stick derecho, agarre con RB / R1. Ver [[04 - Controles]].

**Estado inicial:** Personaje en reposo, sin ataque en curso.

**Estado final:** El ataque termina y el personaje vuelve a reposo.

**Recursos utilizados:** Ninguno: el juego no tiene sistema de energía ni munición.

**Recompensa:** El enemigo recibe porcentaje y retroceso, lo que facilita sacarlo del escenario (ver Mecánica 01).

**Penalización:** Un parry deja expuesto al atacante durante 14 cuadros extra (ver Mecánica 03).

**Interacciones con otras mecánicas:** Los boons modifican los efectos de los ataques (ver Mecánica 05). Los agarres se combinan con el escudo (ver Mecánica 03).

**Casos límite:** Un ataque fuerte cargado al máximo (1 s) hace hasta 40 % más de daño. Los guardias comunes no agarran, así que solo los antidisturbios y los pesados pueden hacerlo (ver [[03 - Enemigos y NPC]]).

### Mecánica 03 — Defensa: escudo y esquive

**Propósito:** Dar al jugador herramientas para no recibir daño.

**Activación:** Mantener el botón de escudo. Para esquivar, escudo más dirección.

**Reglas:**

- El **escudo** bloquea golpes, pero se desgasta: tiene 50 de vida y aguanta unos 5.5 s levantado. Si se rompe, el personaje queda aturdido 6.7 s.
- Soltar el escudo justo cuando llega un golpe provoca un **parry** (ventana de 5 cuadros, a 60 cuadros por segundo): el atacante queda expuesto y congelado 14 cuadros extra.
- **Esquive** en el suelo (rodar a un lado) y en el aire (esquive aéreo), con un momento de invulnerabilidad.

**Entrada:** Teclado: escudo con L, esquive con L + dirección. Mando: escudo con gatillos (LT / RT) o Y / △, esquive con escudo + dirección. Ver [[04 - Controles]].

**Estado inicial:** Escudo bajado, con 50 de vida.

**Estado final:** Escudo bajado con la vida que le quede, o escudo roto con el personaje aturdido 6.7 s.

**Recursos utilizados:** Vida del escudo (50).

**Recompensa:** Parry: el atacante queda expuesto y congelado 14 cuadros extra. Esquive: un momento de invulnerabilidad.

**Penalización:** Abusar del escudo provoca que se rompa, con el aturdimiento que eso conlleva.

**Interacciones con otras mecánicas:** Los agarres atraviesan el escudo (Mecánica 02). Los antidisturbios se defienden con un contraataque que agarra al atacante (ver [[03 - Enemigos y NPC]]).

**Casos límite:** El esquive solo da invulnerabilidad durante un momento; un agarre ignora el escudo.

### Mecánica 04 — Ventanas rompibles

**Propósito:** Convierte los edificios en parte del combate y conecta la mecánica de KO con la historia (los personajes salen por las ventanas).

**Activación:** Un personaje choca contra una ventana o pared lateral a suficiente velocidad (un lanzamiento fuerte).

**Reglas:**

- El escenario es una **plataforma flotante tipo pilar** dentro de un piso de oficina, con **ventanas** como paredes laterales.
- Una ventana intacta funciona como pared.
- Si un personaje choca contra ella a suficiente velocidad (un lanzamiento fuerte), la ventana se rompe y el personaje sale volando. Como la velocidad depende del porcentaje, en la práctica solo se rompe con personajes muy dañados.
- La ventana rota **se queda abierta** mientras haya alguien fuera y se regenera unos **5 segundos** después.
- En las salas cerradas sin ventanas (Mantenimiento y Sala de servidores), las paredes laterales funcionan igual: se rompen igual que las ventanas, cuando un personaje choca contra ellas a suficiente velocidad (un lanzamiento fuerte); el hueco queda abierto mientras haya alguien fuera y se regeneran unos 5 segundos después.
- Al pasar al siguiente nivel, todas las ventanas y paredes se reparan.

**Entrada:** No aplica: es una reacción del escenario ante un lanzamiento.

**Estado inicial:** Ventana o pared intacta, que funciona como pared.

**Estado final:** Ventana o pared rota y abierta mientras haya alguien fuera; se regenera unos 5 s después, o se repara al cambiar de piso.

**Recursos utilizados:** No aplica.

**Recompensa:** Sacar al enemigo del escenario por la abertura (KO, ver Mecánica 01).

**Penalización:** Si el jugador sale por la abertura, pierde una vida (ver Mecánica 01).

**Interacciones con otras mecánicas:** KO (Mecánica 01) y regla global 5 de [[07 - Reglas y Estados del Juego]].

**Casos límite:** Si un personaje es lanzado contra una ventana o pared rota, sale directo sin chocar.

### Mecánica 05 — Boons

**Propósito:** Personalizar cada partida (pilar de Unicidad).

**Activación:** Al terminar cada piso, al derrotar a un enemigo élite (suelta su boon), al romper un mueble (5 % de probabilidad) y comprándolos en la cafetería.

**Reglas:**

* Se ofrecen **3 opciones** al azar y el jugador elige una. Cada opción puede ser un boon nuevo o una mejora de uno que ya tiene.
* **No hay un límite fijo de boons.** Entre más boons tiene el jugador, menos probable es que se le ofrezcan nuevos y más probable que se le ofrezcan mejoras (la probabilidad de un boon nuevo baja de 100 % a 75 %, 56 %… con cada boon que ya tiene).
* Cada boon tiene una **rareza** (Común, Raro, Épico o Legendario). Cada boon nuevo sale común el 49.8 % de las veces, raro el 32.3 %, épico el 11.9 % y legendario el 6 %.
* Cada boon tiene  **hasta 5 niveles** .
* Si quedan menos de 3 opciones disponibles, se muestran solo las que quedan (1 o 2 cartas).
* Si no hay nada que ofrecer (todo al máximo), se omite el menú de boons y se pasa al siguiente piso. Con 16 boons de 5 niveles hay 80 mejoras posibles, así que esto solo pasa en partidas muy largas.

**Entrada:** Seleccionar una carta en el menú de boons (Navegar y Enter; A / ✕ en mando). Recoger un boon del suelo con el botón de ataque. Comprar en la tienda con COMPRAR (ver [[04 - Controles]]).

**Estado inicial:** El boon no está equipado, o está equipado con su nivel actual.

**Estado final:** El boon queda equipado en su nivel nuevo (1 a 5).

**Recursos utilizados:** Elegir un boon del menú no cuesta recurso. Comprarlo en la cafetería cuesta monedas (ver [[06 - Economía y Recursos]]).

**Recompensa:** El efecto del boon durante el resto de la partida (ver tabla).

**Penalización:** No hay penalización durante la partida. Los boons se pierden al terminar la partida (regla global 7 de [[07 - Reglas y Estados del Juego]]).

**Interacciones con otras mecánicas:** La tienda también vende mejoras de boons. Los boons de élite no pueden ser Caja de chocolates, Reloj de pared, Botiquín, Caja de cartón, Cerdito hucha ni Gato de la suerte (ver Mecánica 06).

**Casos límite:** Si quedan menos de 3 opciones, se muestran 1 o 2 cartas. Si todo está al máximo, se omite el menú. Caja de cartón: mientras el jugador está escondido, ningún enemigo lo detecta (ver [[03 - Enemigos y NPC]]).

> [!note] ✏️ Lista de boons
> Lista de boons implementados (16) Los boons son objetos de oficina, en línea con la sátira corporativa del juego.
>
> | Boon                  | Elemento/tipo | Rareza     | Efecto (nivel 1 → nivel 5)                                                                               |
> | --------------------- | ------------- | ---------- | -------------------------------------------------------------------------------------------------------- |
> | Encendedor            | Fuego         | Común      | Tus golpes queman: de 1.5 %/s durante 3.25 s a 2.5 %/s durante 3.75 s                                      |
> | Extintor criogénico   | Hielo         | Raro       | Probabilidad de congelar con ataques normales: de 15 % (0.95 s) a 25 % (1.25 s); el siguiente golpe rompe el hielo con +50 % de knockback |
> | Regleta sobrecargada  | Electricidad  | Raro       | Tus especiales sueltan un rayo que salta a enemigos cercanos: de 1 enemigo con 4 % a 2 enemigos con 6 %   |
> | Café de la oficina    | Veneno        | Épico      | Tus golpes envenenan: el enemigo hace de 25 % menos daño (4.5 s) a 35 % menos (5.5 s) y contagia a quien toque |
> | Caja de chocolates    | Amor          | Legendario | Probabilidad de enamorar al enemigo para que pelee a tu lado: de 8 % (5 s) a 12 % (7 s)                   |
> | Reloj de pared        | Lentitud      | Épico      | Cada KO ralentiza al resto de los enemigos: del 55 % de su velocidad (3 s) al 45 % (4 s)                  |
> | Botiquín              | Curación      | Común      | Al limpiar un piso te curas de 28 % a 44 % del porcentaje                                                 |
> | Frasco de vitaminas   | Regeneración  | Raro       | Si no te golpean en 3 s, te curas de 0.6 %/s a 1.2 %/s                                                    |
> | Caja de cartón        | Sigilo        | Legendario | Agáchate 1 s para esconderte: ningún enemigo te detecta de 2.5 s a 3.5 s (se recarga en 6 s)              |
> | Bebida energética     | Velocidad     | Común      | Te mueves y atacas de 8 % a 16 % más rápido                                                               |
> | Zapatillas deportivas | Salto         | Común      | De 1 salto extra en el aire a 2 saltos extra con 12 % más de altura                                       |
> | Mancuerna             | Fuerza        | Raro       | Tus golpes lanzan de 8 % a 18 % más lejos                                                                 |
> | Casco de obra         | Defensa       | Raro       | Recibes de 8 % a 16 % menos knockback                                                                     |
> | Cerdito hucha         | Monedas       | Común      | Cada KO suelta de 30 % a 70 % más monedas y nunca 0                                                       |
> | Cáscara de plátano    | Trampa        | Épico      | Al esquivar dejas una cáscara: quien la pisa resbala y recibe de 4 % a 6 % (dos cáscaras a la vez en nivel 5) |
> | Gato de la suerte     | Rescate       | Legendario | Te salva de un KO por sala (dos en nivel 5) y te cura de 40 % a 60 % del daño                             |
>

**Reglas extra de los boons:**

- El hielo solo funciona con ataques normales, y un enemigo congelado no se puede volver a congelar en 2.5 s.
- La electricidad solo funciona con habilidades; el rayo se recarga en 0.5 s.
- La probabilidad de enamorar es la mitad contra élites y no funciona contra el jefe.
- La Caja de cartón se activa agachándose 1 s; mientras dura, los enemigos no detectan al jugador.

### Mecánica 06 — Enemigos élite

**Propósito:** Sorprender al jugador y aumentar la dificultad poco a poco.

**Activación:** Aparece en el piso con probabilidad: 15 % por piso desde el piso 3, y cada 25 pisos se suma otra oportunidad.

**Reglas:**

* Un élite es un **Guardia pesado** con **borde dorado**, su **porcentaje en color cian** y el icono del boon que lleva.
* Es más fuerte (recibe menos daño) y más inteligente (su IA tiene un nivel más que los enemigos normales del piso).
* **Lleva un boon** : al ser derrotado lo suelta y el jugador puede recogerlo con el botón de ataque. También da el doble de monedas. El boon es de nivel 1 hasta el piso 24, de nivel 2 desde el piso 25 y sube un nivel cada 25 pisos, hasta el 5. Los élites nunca llevan Caja de chocolates, Reloj de pared, Botiquín, Caja de cartón, Cerdito hucha ni Gato de la suerte.
* Puede aparecer a partir del piso 3. En cada piso hay una oportunidad del 15% de que aparezca uno, y cada 25 pisos se suma otra oportunidad, así que más arriba pueden aparecer varios.
* **No hay mini-jefes cada 20 pisos** : los picos de dificultad son los élites y Mr. Big Data cada 50 pisos.

**Entrada:** Recoger su boon con el botón de ataque (J en teclado; B / ○ en mando).

**Estado inicial:** Élite en el escenario, con su boon equipado.

**Estado final:** Derrotado: suelta su boon en el suelo. Si no se recoge en 10 segundos, el boon desaparece.

**Recursos utilizados:** No aplica.

**Recompensa:** El doble de monedas (0 a 20) y el boon que lleva.

**Penalización:** No aplica para el jugador. El boon se pierde si no se recoge en 10 segundos.

**Interacciones con otras mecánicas:** Boons (Mecánica 05) y Objetos ([[04 - Objetos y Coleccionables]]). En los pisos del jefe, los guardias pesados que invoca Mr. Big Data también son élites.

**Casos límite:** El nivel del boon depende del piso (ver Reglas). El piso no se da por terminado mientras queden boons en el suelo.

## Mecánicas secundarias

### Doble salto y recuperación

**Propósito:** Permitir volver al escenario tras un lanzamiento.

**Activación:** Pulsar salto en el aire (Espacio o W; A / ✕ en mando). La recuperación se activa con la habilidad hacia arriba (K + arriba).

**Reglas:** El personaje tiene doble salto. Zapatillas deportivas añade saltos extra y altura (Mecánica 05).

**Entrada:** Ver [[04 - Controles]].

**Estado inicial:** Personaje en el aire, con saltos disponibles.

**Estado final:** Personaje en el aire sin saltos, o de vuelta en el escenario.

**Recursos utilizados:** No aplica.

**Recompensa:** Volver al escenario y seguir peleando.

**Penalización:** Si el personaje sale del escenario, pierde una vida (Mecánica 01).

**Interacciones con otras mecánicas:** Zapatillas deportivas (Mecánica 05). Agarrarse al borde (se detalla abajo).

**Casos límite:** Por definir: el GDD no indica qué pasa si la recuperación choca con el borde.

### Caminar lento

**Propósito:** Permitir moverse con más control, por ejemplo para posicionarse.

**Activación:** Mantener Shift mientras se mueve (teclado), o inclinar poco el stick (mando).

**Reglas:** Reduce la velocidad de movimiento respecto al movimiento normal. La cantidad exacta de reducción está por definir.

**Entrada:** Shift + dirección (teclado); inclinar poco el stick izquierdo (mando).

**Estado inicial:** Personaje moviéndose a velocidad normal.

**Estado final:** Personaje moviéndose a velocidad reducida, o de vuelta a velocidad normal al soltar Shift.

**Recursos utilizados:** No aplica.

**Recompensa:** Más control del movimiento.

**Penalización:** No aplica.

**Interacciones con otras mecánicas:** Ninguna definida.

**Casos límite:** Por definir.

### Cámara lenta

**Propósito:** Marcar momentos importantes del piso.

**Activación:** El último KO de cada nivel, el salto entre pisos y el fin de la partida.

**Reglas:** El tiempo se ralentiza durante la transición o el KO marcado.

**Entrada:** No aplica: es automática.

**Estado inicial:** Juego a velocidad normal.

**Estado final:** Juego a velocidad normal al terminar la transición o el KO.

**Recursos utilizados:** No aplica.

**Recompensa:** Dar énfasis visual al momento.

**Penalización:** No aplica.

**Interacciones con otras mecánicas:** Salto entre pisos y Fin de la partida (ver [[07 - Reglas y Estados del Juego]]).

**Casos límite:** Por definir: la duración exacta no está indicada.

### Salto entre pisos

**Propósito:** Avanzar al siguiente piso sin ascensor.

**Activación:** Terminar el piso y resolver la elección de boon, si hay opciones.

**Reglas:** El personaje salta, rompe el techo y aterriza en el siguiente piso, con cámara lenta. En la cafetería, el jugador sube usando la salida (SUBIR).

**Entrada:** Automática; en la cafetería, agarrar en la salida (I; RB / R1 en mando).

**Estado inicial:** Piso completado.

**Estado final:** Personaje en el piso de arriba.

**Recursos utilizados:** No aplica.

**Recompensa:** Avanzar en la subida.

**Penalización:** No aplica.

**Interacciones con otras mecánicas:** Menú de boons (Mecánica 05) y Cafetería.

**Casos límite:** Si no hay boons disponibles, se pasa directo al siguiente piso.

### Cuenta regresiva

**Propósito:** Preparar al jugador antes de empezar la partida.

**Activación:** Iniciar una partida o reintentar.

**Reglas:** La cuenta 3, 2, 1, MAKE 'EM FALL mientras los enemigos entran al escenario.

**Entrada:** No aplica.

**Estado inicial:** Partida recién iniciada.

**Estado final:** Partida en curso.

**Recursos utilizados:** No aplica.

**Recompensa:** No aplica.

**Penalización:** No aplica.

**Interacciones con otras mecánicas:** Selección de personaje y Reintentar (ver [[07 - Reglas y Estados del Juego]]).

**Casos límite:** No aplica.

### Agarrarse al borde

**Propósito:** Permitir recuperarse tras un lanzamiento.

**Activación:** El personaje llega al borde del escenario al recuperarse.

**Reglas:** Por definir: el GDD solo indica que el personaje se agarra al borde al recuperarse.

**Entrada:** Por definir.

**Estado inicial:** Personaje en el aire, cerca del borde.

**Estado final:** Personaje sobre el escenario.

**Recursos utilizados:** No aplica.

**Recompensa:** Volver al escenario.

**Penalización:** Por definir.

**Interacciones con otras mecánicas:** Doble salto y recuperación (ver arriba).

**Casos límite:** Por definir.

### Muebles rompibles

**Propósito:** Dar al escenario elementos que el jugador puede destruir durante el combate.

**Activación:** Golpear el mueble.

**Reglas:** Algunos muebles se pueden tirar o romper durante el combate (sillas, plantas, escritorios, libreros, impresoras, máquinas expendedoras, etc.), y otros sirven como plataforma (ver [[03 - Entornos]]).

**Entrada:** Ataque sobre el mueble.

**Estado inicial:** Mueble intacto.

**Estado final:** Mueble roto.

**Recursos utilizados:** No aplica.

**Recompensa:** 5 % de probabilidad de que caiga un boon (ver Mecánica 05).

**Penalización:** No aplica.

**Interacciones con otras mecánicas:** Boons (Mecánica 05).

**Casos límite:** Por definir: el GDD no indica si el mueble roto deja restos en el escenario.

> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
