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
- Cada golpe suma porcentaje a quien lo recibe (máximo 999%).
- Entre más porcentaje, mayor es el retroceso (knockback) y más lejos sale volando.
- Un personaje queda fuera (KO) al salir de los límites del escenario.
- Los **enemigos son más susceptibles al daño** que el jugador: reciben más porcentaje por golpe *(prototipo: enemigos normales ×2.0, élites ×1.2)*.
- El jugador tiene **3 vidas**; los enemigos, una.

**Entrada:** Cualquier ataque.

**Estado inicial:** 0%.

**Estado final:** KO al salir del escenario. El jugador reaparece en 0% si le quedan vidas.

**Recursos utilizados:** Vidas del jugador.

**Recompensa:** Monedas por cada enemigo derrotado.

**Penalización:** Perder una vida.

**Interacciones con otras mecánicas:** Ventanas rompibles, boons (fuego, hielo, curación), comida de la tienda (reduce el porcentaje).

**Casos límite:** Si el último enemigo y el jugador salen al mismo tiempo *(por definir)*.

### Mecánica 02 — Moveset estilo Smash

**Propósito:** Dar profundidad al combate con controles simples.

**Activación:** Botón de ataque o habilidad combinado con una dirección.

**Reglas:**
- **Ataques básicos** en todas direcciones: neutral (combo de 3 golpes), lado, arriba, abajo y ataque en carrera.
- **Habilidades** (especiales) en todas direcciones: neutral, lado, arriba (recuperación) y abajo.
- **Ataques fuertes** (smash) hacia el lado, arriba y abajo, que se pueden **cargar**.
- **Ataques aéreos** en el aire: neutral, adelante, atrás, arriba y abajo.
- **No hay agarres.**
- Cada personaje tiene su propio moveset: Niko pelea con los puños y Mr. Wobbles con objetos de payaso (globos explosivos, etc.).

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
- Si un personaje choca contra ella con un golpe muy fuerte, la ventana se rompe y el personaje sale volando *(prototipo: con 100% o más de daño)*.
- La ventana rota **se queda abierta un rato** y luego se regenera *(prototipo: 2 segundos)*.
- Al pasar al siguiente nivel, todas las ventanas se reparan.

**Casos límite:** Si un personaje es lanzado contra una ventana rota, sale directo sin chocar.

### Mecánica 05 — Boons

**Propósito:** Personalizar cada partida (pilar de Unicidad).

**Activación:** Al terminar cada nivel.

**Reglas:**
- Se ofrecen **3 boons** al azar y el jugador elige uno.
- El jugador puede tener un máximo de **3 boons** *(prototipo; diseño original: 3 o 4)*.
- Con los espacios llenos, solo se ofrecen **mejoras** de los boons que ya tiene.
- Cada boon tiene **hasta 5 niveles**.
- Si no hay nada que ofrecer (todo al máximo), se pasa directo al siguiente nivel.

**Entrada:** Seleccionar una carta en el menú de boons.

**Interacciones con otras mecánicas:** La tienda también vende mejoras de boons.

> [!note] Lista de boons
> Los boons de la idea original (hielo, electricidad, amor, veneno, fuego, velocidad, regeneración, curación, lentitud, fantasma) son **ejemplos**. El prototipo actual implementa:
>
> | Boon | Efecto |
> |---|---|
> | Fuego | Los golpes queman: daño constante por unos segundos |
> | Hielo | Los golpes congelan: el enemigo se mueve más lento |
> | Curación | Probabilidad al golpear de reducir tu propio porcentaje |
> | Pluma | Saltos extra y saltos aéreos más altos |
> | Espacio | Gravedad baja: caes más lento |

### Mecánica 06 — Enemigos élite

**Propósito:** Sorprender al jugador y aumentar la dificultad poco a poco.

**Reglas:**
- Un élite es un enemigo normal, pero con su **porcentaje en color dorado**.
- Es un poco más fuerte (recibe menos daño) y más inteligente (reacciona más rápido y casi nunca se queda quieto).
- Los **mini-jefes** (cada 20 niveles) son enemigos élite, para no complicar el desarrollo.
- Mientras más alto es el nivel, mayor es la probabilidad de que aparezcan élites *(prototipo: 2% en el nivel 1, ~25% cerca del nivel 7; después pueden aparecer varios por ronda)*.

## Mecánicas secundarias

- **Doble salto** y recuperación con la habilidad hacia arriba.
- **Caminar lento** con un modificador.
- **Cámara lenta** en el último KO de cada nivel.
- **Salto entre pisos:** animación de transición al siguiente nivel.
- **Cuenta regresiva** al iniciar la partida.


> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
