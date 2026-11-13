# Sistemas del Juego

## Descripción de la sección

Los sistemas son conjuntos de reglas y componentes que trabajan juntos: combate, inventario, IA, diálogo, progresión, economía, misiones, etc.

## Inventario de sistemas

| Sistema              | Propósito                                                               | Dependencias               | Estado                               |
| -------------------- | ------------------------------------------------------------------------ | -------------------------- | ------------------------------------ |
| Combate              | Daño por porcentaje, knockback, escudo, parry, esquive, agarres, hitlag | Personajes, Escenario      | Implementado                         |
| Personajes (Fighter) | Movimiento, saltos y moveset de cada personaje                           | Entrada, Combate           | Implementado (5 personajes jugables) |
| Escenario            | Pisos de oficina generados, ventanas y muebles rompibles, límites       | Combate                    | Implementado                         |
| Niveles y oleadas    | Generar los enemigos y las rondas de cada piso                           | IA, Escenario              | Implementado                         |
| IA de enemigos       | Controlar a guardias, antidisturbios, drones y élites (9 niveles de IA) | Combate, Niveles           | Implementado                         |
| Boons                | Mejoras de la partida                                                    | Combate, Estados alterados | Implementado (16 boons)              |
| Estados alterados    | Quemadura, congelación, veneno, lentitud, enamorado y otros             | Combate                    | Implementado                         |
| Economía y tienda   | Monedas y cafetería que vende boons y mejoras                           | Niveles, Boons             | Implementado                         |
| Jefes                | Mr. Big Data cada 50 pisos, con barra de vida propia                     | Combate, IA, Niveles       | Implementado                         |
| Interfaz (HUD)       | Porcentajes, vidas, piso, monedas, boons y menú de boons                | Todos                      | Implementado                         |
| Tutorial             | Escena guiada con Niko que enseña los controles paso a paso             | Combate, Interfaz          | Implementado                         |

## Plantilla de sistema

### Combate

**Objetivo:** Resolver los golpes entre personajes al estilo Smash.

**Entradas:** Ataques activos (hitboxes) y cuerpos de los personajes (hurtboxes).

**Procesamiento / reglas:** Si un golpe toca a un personaje del otro equipo: si tiene el escudo arriba, se bloquea (o se hace parry si fue a tiempo); si no, se suma el daño multiplicado por su susceptibilidad y se calcula el retroceso según su porcentaje y su peso.

**Salidas:** Porcentaje nuevo, dirección y fuerza del lanzamiento, tiempo de aturdimiento.

**Estados posibles:** Normal, daño leve, daño fuerte, aturdido (escudo roto), expuesto (parry), derribado, agarrado y fuera del escenario (KO).

**Dependencias:** Personajes, Escenario.

**Interacciones:** Boons de golpe (Encendedor, Extintor criogénico, Café de la oficina, Caja de chocolates), Estados alterados, ventanas rompibles (Escenario).

**Datos que necesita:** Porcentaje de cada personaje, peso, susceptibilidad al daño, tipo de ataque (básico, habilidad, fuerte, aéreo o agarre) y dirección.

**Datos que genera:** Porcentaje nuevo, vector de lanzamiento, tiempo de aturdimiento y evento de KO.

**Riesgos:** Que el combate se sienta "flotado" o injusto. Ajustar con pruebas de sensación.

**Criterios de aceptación:** Un enemigo con mucho porcentaje sale volando visiblemente más lejos que uno con poco.

### Personajes (Fighter)

**Objetivo:** Controlar el movimiento, los saltos y el moveset de cada personaje jugable.

**Entradas:** Acciones del jugador (mover, saltar, atacar, habilidad, ataque fuerte, escudo, esquive y agarre), según [[04 - Controles]].

**Procesamiento / reglas:** Cada personaje ejecuta su propio moveset según botón y dirección (ver [[03 - Personajes]]). Doble salto, caminar lento y recuperación con la habilidad hacia arriba (ver [[02 - Mecánicas]]). Peso y susceptibilidad según el personaje: el jugador recibe el daño sin multiplicador (×1.0).

**Salidas:** Ataque, habilidad, agarre, esquive o salto ejecutado, con su animación (ver [[02 - Personajes y Animación]]).

**Estados posibles:** Reposo, caminar, caminar lento, correr, saltar, caer, escudo, atacando, esquivando, agarrando, daño, derrota y victoria.

**Dependencias:** Entrada, Combate.

**Interacciones:** Combate (golpes y lanzamientos), Boons de movimiento (Bebida energética, Zapatillas deportivas, Mancuerna, Casco de obra), Escenario (ventanas y muebles).

**Datos que necesita:** Moveset del personaje, peso, susceptibilidad (×1.0), tres vidas y porcentaje actual.

**Datos que genera:** Acciones y hitboxes para Combate, vidas restantes y porcentaje de daño.

**Riesgos:** Cada personaje tiene su propio moveset; un error en uno no se detecta si solo se prueba con Niko.

**Criterios de aceptación:** Cada combinación de botón y dirección produce el ataque documentado para los cinco personajes iniciales (ver [[01 - Criterios de Calidad]]).

### Escenario

**Objetivo:** Administrar los pisos de oficina, las ventanas y paredes rompibles, el techo y los límites del escenario.

**Entradas:** Número de piso, arquetipo del piso (ver [[01 - Estructura del Contenido]]) y golpes sobre ventanas, paredes o muebles.

**Procesamiento / reglas:** El arquetipo de los pisos de combate se elige al azar y se mantiene en bloques de 3 pisos. Una ventana intacta funciona como pared y se rompe con un lanzamiento fuerte; se regenera unos 5 s después y se repara al cambiar de piso. Las paredes de Mantenimiento y Sala de servidores se comportan igual. El techo se rompe al subir de piso. Los límites del escenario generan el KO.

**Salidas:** Límites del escenario que generan KO, geometría del piso, muebles rotos que pueden soltar boons.

**Estados posibles:** Ventana intacta, ventana rota (abierta mientras haya alguien fuera), ventana en regeneración y ventana reparada al cambiar de piso.

**Dependencias:** Combate.

**Interacciones:** Combate (lanzamientos y KO), Niveles (arquetipos), Boons (5 % de probabilidad al romper un mueble).

**Datos que necesita:** Arquetipo del piso, posición de ventanas, paredes, plataformas y muebles.

**Datos que genera:** Eventos de KO por límite y muebles rotos.

**Riesgos:** El rendimiento depende de la complejidad de los escenarios (ver [[03 - Requisitos Técnicos]]).

**Criterios de aceptación:** La ventana intacta funciona como pared, se rompe con un golpe muy fuerte, se regenera y se repara al cambiar de piso (ver [[04 - Criterios de Aceptación]]).

### Niveles y oleadas

**Objetivo:** Decidir qué enemigos aparecen en cada nivel.

**Entradas:** Número de piso, ronda actual y enemigos derrotados.

**Procesamiento / reglas:**

- Pisos 1 y 2: 2 enemigos. Desde el piso 3, 3 enemigos, y uno más cada 4 pisos, hasta un máximo de 16.
- Los enemigos se reparten en rondas de hasta 4, una justo después de otra. Por eso los pisos altos tienen varias rondas.
- Tipos de enemigo según la altura: guardias comunes desde el inicio; antidisturbios (con puños o con porra) y drones desde el piso 2; drones kamikaze desde el piso 3 (máximo 3 drones por piso).
- Cada 4 pisos los enemigos reciben un poco menos de daño y su IA sube de nivel (reacciona más rápido y se cubre más).
- Élites desde el piso 3 (ver [[02 - Mecánicas]]).
- Hay cafetería cada 10 pisos y un piso antes de cada jefe (10, 20, 30, 40, 49, 60, 70, 80, 90, 99…).
- Cada 50 pisos aparece Mr. Big Data. Al vencerlo, el jugador cobra 60 monedas y sigue subiendo.

**Salidas:** Rondas de enemigos del piso, fin del piso (todos fuera) y apertura del menú de boons o salto al siguiente piso.

**Estados posibles:** Jugando (ronda), piso limpio, menú de boons, salto al siguiente piso, cafetería y combate contra el jefe.

**Dependencias:** IA de enemigos, Escenario.

**Interacciones:** Boons (menú al terminar el piso), Economía (monedas por enemigo y cafetería), Jefes (cada 50 pisos).

**Datos que necesita:** Número de piso, probabilidad de élite (15 % por piso desde el piso 3, más una oportunidad cada 25 pisos), tipos de enemigo permitidos según el piso.

**Datos que genera:** Número de piso, KO totales, monedas ganadas, boons y tiempo (se muestran en la pantalla de Resultados).

**Riesgos:** Pisos altos con demasiadas rondas pueden volver el combate injusto. Revisar con pruebas de dificultad.

**Criterios de aceptación:** Los primeros pisos son claramente más fáciles que los posteriores, y Mr. Big Data es un pico reconocible (ver [[01 - Criterios de Calidad]]).

### IA de enemigos

**Objetivo:** Controlar a guardias, antidisturbios, drones, drones kamikaze y élites.

**Entradas:** Posición del jugador, estado de la ronda y nivel de IA del piso.

**Procesamiento / reglas:** Los enemigos no patrullan. Desde que entran al escenario van hacia el jugador, atacan, usan habilidades, se cubren con el escudo y, si pueden, agarran. El nivel de IA va de 1 a 8 (élites y jefe llegan a 9) y sube cada 4 pisos. Los drones mantienen la distancia y disparan un láser cargado; los drones kamikaze se arman, se lanzan y explotan.

**Salidas:** Ataques, habilidades, escudo, agarres, láser y embestida.

**Estados posibles:** Entrada al escenario, acercarse al jugador, atacar o usar habilidad o agarre, cubrirse con el escudo y, en los drones, mantener distancia o armarse.

**Dependencias:** Combate, Niveles.

**Interacciones:** Caja de cartón (ningún enemigo detecta al jugador mientras está escondido), Estados alterados (los enemigos pueden quemarse, congelarse o enamorarse), Jefe (invoca oleadas de guardias, antidisturbios, guardias pesados y drones).

**Datos que necesita:** Nivel de IA, tipo de enemigo, si es élite y posición del jugador.

**Datos que genera:** Ataques al jugador, KO del enemigo y monedas o boon al morir.

**Riesgos:** Una IA que reacciona demasiado rápido en los pisos altos puede volver el combate injusto.

**Criterios de aceptación:** El nivel de IA sube cada 4 pisos, de 1 a 8, y los élites y el jefe llegan a 9 (ver [[03 - Enemigos y NPC]]).

### Boons

**Objetivo:** Ofrecer y aplicar mejoras durante la partida.

**Entradas:** Fin de piso, élites derrotados, muebles rotos y compras en la cafetería.

**Procesamiento / reglas:** Al limpiar un nivel se ofrecen 3 opciones al azar entre boons nuevos y mejoras de los que ya tiene, ponderadas por rareza. No hay límite fijo de boons; cada uno llega hasta el nivel 5. Los élites también sueltan un boon, al romper un mueble hay un 5 % de probabilidad de que caiga uno y la cafetería los vende.

**Salidas:** Boons equipados con su nivel, y efectos aplicados a combate, movimiento o eventos.

**Estados posibles:** Ofrecido en el menú, equipado (nivel 1 a 5) y mejorado al máximo (nivel 5).

**Dependencias:** Combate, Estados alterados.

**Interacciones:** Los boons de golpe (Encendedor, Extintor, Café, Chocolates) se activan al conectar un ataque; los de estadística (Bebida energética, Zapatillas, Mancuerna, Casco) cambian los atributos del personaje; otros reaccionan a eventos (KO, esquive, limpiar la sala).

**Datos que necesita:** Rareza, nivel actual, lista de boons equipados y piso.

**Datos que genera:** Boons equipados, niveles y monedas gastadas en la cafetería.

**Riesgos:** Combinaciones de boons demasiado fuertes o inútiles, que afectan la variedad de las partidas.

**Criterios de aceptación:** Se ofrecen 3 opciones, no hay límite de boons equipados, ningún boon pasa del nivel 5, y si no hay opciones el menú se omite (ver [[04 - Criterios de Aceptación]]).

### Estados alterados

**Objetivo:** Aplicar efectos temporales de quemadura, congelación, veneno, lentitud y enamorado.

**Entradas:** Golpes con boons que aplican efectos (Encendedor, Extintor criogénico, Café de la oficina, Reloj de pared, Caja de chocolates, Regleta sobrecargada).

**Procesamiento / reglas:** Cada efecto tiene probabilidad y duración según su nivel (ver tabla de boons en [[02 - Mecánicas]]). El hielo solo funciona con ataques normales y el enemigo congelado no se puede volver a congelar en 2.5 s. La electricidad solo funciona con habilidades y el rayo se recarga en 0.5 s. La probabilidad de enamorar es la mitad contra élites y no funciona contra el jefe.

**Salidas:** Daño por tiempo (quemadura), congelación, reducción de daño (veneno), lentitud y enamoramiento, que hace que el enemigo pelee a favor del jugador.

**Estados posibles:** Quemado, congelado, envenenado, ralentizado y enamorado.

**Dependencias:** Combate.

**Interacciones:** Combate, Boons, Interfaz (color y parpadeo por estado, según [[01 - Dirección de Arte]]).

**Datos que necesita:** Boon y nivel, duración, probabilidad y tipo de enemigo (élite o jefe).

**Datos que genera:** Efecto activo con su duración y eventos de congelación rota.

**Riesgos:** Varios efectos acumulados pueden ser difíciles de leer si no se distinguen por color y forma.

**Criterios de aceptación:** El personaje parpadea con el color del efecto y, al congelarse, queda completamente teñido (ver [[01 - UX y Flujo del Jugador]]).

### Economía y tienda

**Objetivo:** Administrar las monedas y la cafetería que vende boons nuevos y mejoras.

**Entradas:** Monedas de enemigos derrotados, 60 monedas al vencer a Mr. Big Data y compras del jugador.

**Procesamiento / reglas:** Los enemigos sueltan de 0 a 10 monedas (los élites, el doble). La cafetería aparece cada 10 pisos y un piso antes de cada jefe, y ofrece 4 productos al azar. Los precios dependen de la rareza (boon nuevo) o del nivel (mejora). Cada producto se puede comprar una vez por visita. Si el saldo no alcanza, la compra queda bloqueada.

**Salidas:** Boon nuevo o mejora comprados, saldo actualizado y diálogo de la tendera.

**Estados posibles:** Tienda cerrada, tienda abierta, compra disponible, compra bloqueada (saldo insuficiente o producto agotado) y sin productos.

**Dependencias:** Niveles, Boons.

**Interacciones:** Boons (productos), Interfaz (saldo en el HUD), Audio (sonido al ganar monedas y al comprar).

**Datos que necesita:** Monedas actuales, precios por rareza y nivel, lista de productos del piso.

**Datos que genera:** Saldo actualizado y boons nuevos o mejorados.

**Riesgos:** Acumular monedas puede hacer que la tienda deje de ser una decisión (ver [[06 - Economía y Recursos]]).

**Criterios de aceptación:** Si el saldo no alcanza, la compra queda bloqueada; si se compra, el saldo se actualiza en la tienda y en el HUD (ver [[04 - Criterios de Aceptación]]).

### Jefes

**Objetivo:** Controlar a Mr. Big Data, que aparece cada 50 pisos.

**Entradas:** Piso múltiplo de 50 y golpes sobre su barra de vida.

**Procesamiento / reglas:** Su barra de vida tiene 450 puntos y se derrota bajándola a cero, sin sacarlo del escenario. Al bajar al 70 %, 40 % y 20 % cambia de fase: salta fuera del escenario, invoca una oleada de guardias, antidisturbios, guardias pesados y drones, y lanza misiles desde lejos. Al derrotarlo, la armadura explota, se cobran 60 monedas y se abre el menú de boons. No hay pantalla de victoria.

**Salidas:** Barra de vida en el HUD, oleadas invocadas, monedas y menú de boons.

**Estados posibles:** Normal, cambio de fase (enfurecido) y derrotado (armadura explotada).

**Dependencias:** Combate, IA de enemigos, Niveles.

**Interacciones:** Niveles (Oficina ejecutiva, cada 50 pisos), Boons (Caja de chocolates no funciona contra el jefe), Economía (60 monedas).

**Datos que necesita:** Vida del jefe (450), umbrales de fase (70 %, 40 %, 20 %) y piso actual.

**Datos que genera:** Monedas ganadas, menú de boons y avance al siguiente piso.

**Riesgos:** El jefe debe ser un pico de dificultad reconocible sin volverse injusto.

**Criterios de aceptación:** Al derrotar a Mr. Big Data se cobran monedas, se abre el menú de boons y la subida continúa (ver [[04 - Criterios de Aceptación]]).

### Interfaz (HUD)

**Objetivo:** Mostrar la información de la partida durante el combate.

**Entradas:** Porcentajes, vidas, KO del piso, piso actual, monedas, boons equipados y estado del jefe.

**Procesamiento / reglas:** El porcentaje del jugador se muestra con un decimal y el de los enemigos sin decimales. Las vidas se muestran con iconos. El contador "KO x/y" y "PISO x" muestran el avance del piso. Las monedas tienen menor prioridad visual que el porcentaje y las vidas. Los avisos (AGARRAR, COMPRAR, SUBIR) aparecen según el contexto.

**Salidas:** Elementos visibles en pantalla y su estado (normal, advertencia, daño, éxito, error o bloqueo).

**Estados posibles:** Normal, advertencia, daño, éxito, error y bloqueo (ver [[04 - Interfaz Visual]]).

**Dependencias:** Todos los sistemas.

**Interacciones:** Combate (porcentajes), Economía (saldo), Jefes (barra de vida).

**Datos que necesita:** Porcentajes, vidas, KO, piso, monedas, boons equipados y barra del jefe.

**Datos que genera:** Ninguno: el HUD solo muestra información y no guarda datos.

**Riesgos:** La información debe ser legible en 1280 × 720 sin que las monedas compitan con el porcentaje.

**Criterios de aceptación:** El porcentaje del jugador y de los enemigos es visible en todo momento y la vida del jefe se ve en su barra (ver [[01 - Criterios de Calidad]]).

### Tutorial

**Objetivo:** Enseñar los controles básicos a través de una escena guiada con Niko.

**Entradas:** Acciones del jugador en cada paso: movimiento, ataques, smash, especiales, escudo, esquive, agarres, KO y boons.

**Procesamiento / reglas:** Los pasos se completan en orden. Cada paso avanza cuando el jugador cumple la acción pedida. Desde la pausa se puede salir del tutorial sin terminarlo.

**Salidas:** Jugador con los controles practicados y regreso al menú principal al completar todos los pasos.

**Estados posibles:** Paso en curso, completado y abandonado (desde la pausa).

**Dependencias:** Combate, Interfaz.

**Interacciones:** Pausa (Volver al inicio sale del tutorial), Combate, Interfaz (avisos).

**Datos que necesita:** Paso actual y acciones completadas.

**Datos que genera:** Paso completado y tutorial terminado.

**Riesgos:** Pasos que no avanzan por fallos de la IA o del conteo de golpes.

**Criterios de aceptación:** Completar todos los pasos regresa al menú principal, y un jugador nuevo puede moverse, saltar y atacar sin instrucciones externas (ver [[01 - Criterios de Calidad]]).

## Relaciones entre sistemas

- **Entrada → Personajes → Combate:** el jugador presiona un botón, el personaje ejecuta un ataque y Combate resuelve el golpe.
- **Combate → Escenario:** un lanzamiento fuerte rompe una ventana. Si el personaje sale de los límites, Escenario avisa del KO.
- **KO → Niveles → Boons:** cuando todos los enemigos están fuera, el piso termina y se abre el menú de boons. Si el KO fue de un élite, suelta su boon.
- **KO → Economía:** cada enemigo derrotado da monedas.
- **Niveles → IA:** el nivel define cuántos enemigos hay, cuántos son élite y qué tan inteligentes son.

> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
