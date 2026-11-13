# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

> [!info] Valores del prototipo
> Los números marcados como *(prototipo)* vienen del proyecto de Unity actual y pueden ajustarse durante el balance.

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
* Un personaje queda fuera (KO) al salir de los límites del escenario.
* Los **enemigos son más susceptibles al daño** que el jugador: reciben más porcentaje por golpe. Los enemigos normales empiezan en ×2.0 y los élites en ×1.2; el multiplicador baja un poco cada 4 pisos (mínimo ×1.4 y ×0.8).
* El jugador tiene  **3 vidas** ; los enemigos, una.

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
* **Ataques fuertes** (smash) hacia el lado, arriba y abajo, que se pueden  **cargar** .
* **Ataques aéreos** en el aire: neutral, adelante, atrás, arriba y abajo.
* **Agarres:** el personaje puede agarrar a un enemigo (botón de agarre, o escudo + ataque) y lanzarlo en una dirección. Los agarres atraviesan el escudo.
* Cada personaje tiene su propio moveset: Niko pelea con los puños, Mateo utiliza principalmente patadas de taekwondo y Mr. Wobbles combate con objetos de payaso (globos explosivos, etc.).

**Entrada:** Ver [[04 - Controles]].

**Interacciones con otras mecánicas:** Los boons modifican los efectos de los ataques.

### Mecánica 03 — Defensa: escudo y esquive

**Propósito:** Dar al jugador herramientas para no recibir daño.

**Reglas:**

- El **escudo** bloquea golpes, pero se desgasta. Si se rompe, el personaje queda aturdido.
- Bloquear justo a tiempo provoca un **parry**: el atacante queda expuesto.
- **Esquive** en el suelo (rodar a un lado) y en el aire (esquive aéreo), con un momento de invulnerabilidad.

**Entrada:** Botón de escudo (más dirección para esquivar).

**Penalización:** Abusar del escudo provoca que se rompa.

### Mecánica 04 — Ventanas rompibles

**Propósito:** Convierte los edificios en parte del combate y conecta la mecánica de KO con la historia (los personajes salen por las ventanas).

**Reglas:**

- El escenario es una **plataforma flotante tipo pilar** dentro de un piso de oficina, con **ventanas** como paredes laterales.
- Una ventana intacta funciona como pared.

* Si un personaje choca contra ella a suficiente velocidad (un lanzamiento fuerte), la ventana se rompe y el personaje sale volando. Como la velocidad depende del porcentaje, en la práctica solo se rompe con personajes muy dañados.
* La ventana rota **se queda abierta** mientras haya alguien fuera y se regenera unos **5 segundos** después.

- Al pasar al siguiente nivel, todas las ventanas se reparan.

**Casos límite:** Si un personaje es lanzado contra una ventana rota, sale directo sin chocar.

### Mecánica 05 — Boons

**Propósito:** Personalizar cada partida (pilar de Unicidad).

**Activación:** Al terminar cada piso, al derrotar a un enemigo élite (suelta su boon) y comprándolos en la cafetería.

**Reglas:**

* Se ofrecen **3 opciones** al azar y el jugador elige una. Cada opción puede ser un boon nuevo o una mejora de uno que ya tiene.
* **No hay un límite fijo de boons.** Entre más boons tiene el jugador, menos probable es que se le ofrezcan nuevos y más probable que se le ofrezcan mejoras.
* Cada boon tiene una **rareza** (Común, Raro, Épico o Legendario). Los raros salen con menos frecuencia.
* Cada boon tiene  **hasta 5 niveles** .
* Si quedan menos de 3 opciones disponibles, se muestran solo las que quedan (1 o 2 cartas).
* Si no hay nada que ofrecer (todo al máximo), se omite el menú de boons y se pasa al siguiente piso. Con 16 boons de 5 niveles hay 80 mejoras posibles, así que esto solo pasa en partidas muy largas.

**Entrada:** Seleccionar una carta en el menú de boons.

**Interacciones con otras mecánicas:** La tienda también vende mejoras de boons.

> [!note] ✏️ Lista de boons
> Lista de boons implementados (16) Los boons son objetos de oficina, en línea con la sátira corporativa del juego.
>
> | Boon                  | Elemento/tipo | Rareza     | Efecto                                                                                                 |
> | --------------------- | ------------- | ---------- | ------------------------------------------------------------------------------------------------------ |
> | Encendedor            | Fuego         | Común     | Tus golpes queman: suman porcentaje por segundo durante unos segundos                                  |
> | Extintor criogénico  | Hielo         | Raro       | Probabilidad de congelar con ataques normales; el siguiente golpe rompe el hielo con +50% de knockback |
> | Regleta sobrecargada  | Electricidad  | Raro       | Tus especiales sueltan un rayo que salta a enemigos cercanos                                           |
> | Café de la oficina   | Veneno        | Épico     | Tus golpes envenenan: el enemigo hace menos daño y contagia a quien toque                             |
> | Caja de chocolates    | Amor          | Legendario | Probabilidad de enamorar al enemigo: pelea a tu lado unos segundos                                     |
> | Reloj de pared        | Lentitud      | Épico     | Cada KO ralentiza al resto de los enemigos                                                             |
> | Botiquín             | Curación     | Común     | Al limpiar una sala te curas parte del porcentaje                                                      |
> | Frasco de vitaminas   | Regeneración | Raro       | Si no te golpean en 3 s, te curas poco a poco                                                          |
> | Caja de cartón       | Sigilo        | Legendario | Agáchate 1s para esconderte: los enemigos no te ven                                                   |
> | Bebida energética    | Velocidad     | Común     | Te mueves y atacas más rápido                                                                        |
> | Zapatillas deportivas | Salto         | Común     | Saltos extra en el aire y saltos aéreos más altos                                                    |
> | Mancuerna             | Fuerza        | Raro       | Tus golpes lanzan más lejos                                                                           |
> | Casco de obra         | Defensa       | Raro       | Recibes menos knockback                                                                                |
> | Cerdito hucha         | Monedas       | Común     | Cada KO suelta más monedas y nunca 0                                                                  |
> | Cáscara de plátano  | Trampa        | Épico     | Al esquivar dejas una cáscara: quien la pisa resbala y recibe daño                                   |
> | Gato de la suerte     | Rescate       | Legendario | Te salva de un KO por sala (dos en nivel 5) y te cura                                                  |
>

### Mecánica 06 — Enemigos élite

**Propósito:** Sorprender al jugador y aumentar la dificultad poco a poco.

**Reglas:**

* Un élite es un **Guardia pesado** con su **porcentaje en color dorado** y el icono del boon que lleva.
* Es más fuerte (recibe menos daño) y más inteligente (su IA tiene un nivel más que los enemigos normales del piso).
* **Lleva un boon** : al ser derrotado lo suelta y el jugador puede recogerlo con el botón de ataque. También da el doble de monedas.
* Puede aparecer a partir del piso 3. En cada piso hay una oportunidad del 15% de que aparezca uno, y cada 25 pisos se suma otra oportunidad, así que más arriba pueden aparecer varios.
* **No hay mini-jefes cada 20 pisos** : los picos de dificultad son los élites y Mr. Big Data cada 50 pisos.

## Mecánicas secundarias

* **Doble salto** y recuperación con la habilidad hacia arriba.
* **Caminar lento** con un modificador.
* **Cámara lenta** en el último KO de cada nivel.
* **Salto entre pisos:** el personaje salta, rompe el techo y aterriza en el siguiente piso, con cámara lenta.
* **Cuenta regresiva** al iniciar la partida.
* **Agarrarse al borde** del escenario al recuperarse.
* **Muebles rompibles:** algunos objetos de la oficina se pueden golpear y destruir.

> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
