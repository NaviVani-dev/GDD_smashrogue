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

### Nombre

**Objetivo:**

**Entradas:**

**Procesamiento / reglas:**

**Salidas:**

**Estados posibles:**

**Dependencias:**

**Interacciones:**

**Datos que necesita:**

**Datos que genera:**

**Riesgos:**

**Criterios de aceptación:**

### Combate

**Objetivo:** Resolver los golpes entre personajes al estilo Smash.

**Entradas:** Ataques activos (hitboxes) y cuerpos de los personajes (hurtboxes).

**Procesamiento / reglas:** Si un golpe toca a un personaje del otro equipo: si tiene el escudo arriba, se bloquea (o se hace parry si fue a tiempo); si no, se suma el daño multiplicado por su susceptibilidad y se calcula el retroceso según su porcentaje y su peso.

**Salidas:** Porcentaje nuevo, dirección y fuerza del lanzamiento, tiempo de aturdimiento.

**Riesgos:** Que el combate se sienta "flotado" o injusto. Ajustar con pruebas de sensación.

**Criterios de aceptación:** Un enemigo con mucho porcentaje sale volando visiblemente más lejos que uno con poco.

### Niveles y oleadas

**Objetivo:** Decidir qué enemigos aparecen en cada nivel.

**Procesamiento / reglas:**

- Pisos 1 y 2: 2 enemigos. Desde el piso 3, 3 enemigos, y uno más cada 4 pisos, hasta un máximo de 16.
- Los enemigos se reparten en rondas de hasta 4, una justo después de otra. Por eso los pisos altos tienen varias rondas.
- Tipos de enemigo según la altura: guardias comunes desde el inicio; antidisturbios (con puños o con porra) y drones desde el piso 2; drones kamikaze desde el piso 3 (máximo 3 drones por piso).
- Cada 4 pisos los enemigos reciben un poco menos de daño y su IA sube de nivel (reacciona más rápido y se cubre más).
- Élites desde el piso 3 (ver [[02 - Mecánicas]]).
- Hay cafetería cada 10 pisos y un piso antes de cada jefe (10, 20, 30, 40, 49, 60, 70, 80, 90, 99…).
- Cada 50 pisos aparece Mr. Big Data. Al vencerlo, el jugador cobra 60 monedas y sigue subiendo.

**Datos que genera:** Número de piso, KO totales, monedas ganadas, boons y tiempo (se muestran en la pantalla de Resultados).

### Boons

**Objetivo:** Ofrecer y aplicar mejoras durante la partida.

**Procesamiento / reglas:** Al limpiar un nivel se ofrecen 3 opciones al azar entre boons nuevos y mejoras de los que ya tiene, ponderadas por rareza. No hay límite fijo de boons; cada uno llega hasta el nivel 5. Los élites también sueltan un boon y la cafetería los vende.

**Interacciones:** Los boons de golpe (Encendedor, Extintor, Café, Chocolates) se activan al conectar un ataque; los de estadística (Bebida energética, Zapatillas, Mancuerna, Casco) cambian los atributos del personaje; otros reaccionan a eventos (KO, esquive, limpiar la sala).

## Relaciones entre sistemas

- **Entrada → Personajes → Combate:** el jugador presiona un botón, el personaje ejecuta un ataque y Combate resuelve el golpe.
- **Combate → Escenario:** un lanzamiento fuerte rompe una ventana. Si el personaje sale de los límites, Escenario avisa del KO.
- **KO → Niveles → Boons:** cuando todos los enemigos están fuera, el piso termina y se abre el menú de boons. Si el KO fue de un élite, suelta su boon.
- **KO → Economía:** cada enemigo derrotado da monedas.
- **Niveles → IA:** el nivel define cuántos enemigos hay, cuántos son élite y qué tan inteligentes son.

> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
