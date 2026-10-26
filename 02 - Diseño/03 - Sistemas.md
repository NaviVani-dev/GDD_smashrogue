# Sistemas del Juego

## Descripción de la sección

Los sistemas son conjuntos de reglas y componentes que trabajan juntos: combate, inventario, IA, diálogo, progresión, economía, misiones, etc.

## Inventario de sistemas

| Sistema              | Propósito                                                                    | Dependencias               | Estado                                    |
| -------------------- | ---------------------------------------------------------------------------- | -------------------------- | ----------------------------------------- |
| Combate              | Daño por porcentaje, knockback, escudo, esquive, hitlag                      | Personajes, Escenario      | Prototipo funcional                       |
| Personajes (Fighter) | Movimiento, saltos y moveset de cada personaje                               | Entrada, Combate           | Prototipo funcional (personaje de prueba) |
| Escenario            | Plataforma tipo pilar, ventanas rompibles, límites                           | Combate                    | Prototipo funcional                       |
| Niveles y oleadas    | Generar las rondas de enemigos de cada nivel                                 | IA, Escenario              | Prototipo: 1 ronda por nivel              |
| IA de enemigos       | Controlar a los enemigos normales y élite                                    | Combate, Niveles           | Prototipo funcional                       |
| Boons                | Mejoras de la partida                                                        | Combate, Estados alterados | Prototipo funcional (5 boons)             |
| Estados alterados    | Quemadura, lentitud y otros efectos temporales                               | Combate                    | Prototipo funcional                       |
| Economía y tienda    | Monedas, comida y mejoras                                                    | Niveles, Boons             | Por implementar                           |
| Jefes                | Mini-jefe (enemigo élite) cada 20 niveles y jefe final (CEO) en el nivel 100 | Combate, IA, Niveles       | Por implementar                           |
| Interfaz (HUD)       | Porcentajes, vidas, nivel, contador de monedas y menú de boons               | Todos                      | Prototipo funcional                       |

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
- Primeros niveles: **1 ronda de 3 o 4 enemigos**.
- Al subir, aparecen **más rondas por nivel**, una justo después de otra, con un **máximo de 3 rondas**.
- Los enemigos se vuelven más fuertes poco a poco y aumenta la probabilidad de élites.
- Hay **tienda cada 10 niveles**, excepto cuando el siguiente nivel tiene un mini-jefe o el jefe final: en ese caso, la tienda aparece **un nivel antes** para que el jugador se prepare. Las tiendas quedan en los niveles **10, 19, 30, 39, 50, 59, 70, 79, 90 y 99**.
- Cada **20 niveles** aparece un **mini-jefe**, que es un enemigo élite.
- En el **nivel 100** aparece el **jefe final**. Al vencerlo, la partida termina.

**Datos que genera:** Número de nivel, KO totales.

### Boons

**Objetivo:** Ofrecer y aplicar mejoras durante la partida.

**Procesamiento / reglas:** Al limpiar un nivel se ofrecen 3 opciones al azar entre boons nuevos (si hay espacio) y mejoras de los que ya tiene. Máximo 3 boons, hasta nivel 5 cada uno.

**Interacciones:** Los boons de golpe (fuego, hielo, curación) se activan al conectar un ataque; los de estadística (pluma, espacio) cambian el movimiento del personaje.

## Relaciones entre sistemas

- **Entrada → Personajes → Combate:** el jugador presiona un botón, el personaje ejecuta un ataque y Combate resuelve el golpe.
- **Combate → Escenario:** un lanzamiento fuerte rompe una ventana. Si el personaje sale de los límites, Escenario avisa del KO.
- **KO → Niveles → Boons:** cuando todos los enemigos están fuera, el nivel termina y se abre el menú de boons.
- **KO → Economía:** cada enemigo derrotado da monedas.
- **Niveles → IA:** el nivel define cuántos enemigos hay, cuántos son élite y qué tan inteligentes son.


> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
