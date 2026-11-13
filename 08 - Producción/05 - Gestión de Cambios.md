# Gestión de Cambios

## Descripción de la sección

El diseño de un videojuego cambia. Esta sección evita que las modificaciones importantes se pierdan o aparezcan sin evaluar sus consecuencias.

Aquí se compara lo que planteaba el GDD inicial (versión 0.4.0, del 2026-10-16) con lo que quedó en el juego entregado (versión 1.0.0, del 2026-11-13), y se explica por qué se hizo cada cambio.

## Solicitud de cambio

**Fecha:** 2026-11-12

**Cambio propuesto:** Reemplazar los 100 pisos con jefe final y pantalla de ¡Victoria! por una subida sin límite de pisos, con Mr. Big Data cada 50 pisos y sin mini-jefes.

**Motivo:** Que el jugador siempre tenga ganas de intentar llegar un poco más alto. Además, construir 100 pisos fijos y un final cerrado habría tomado demasiado tiempo para la entrega.

**Beneficio esperado:** Partidas rejugables sin límite, un solo jefe bien hecho en lugar de mini-jefes que se sentían como élites normales, y menos contenido que construir a mano.

**Costo estimado:** Bajo. Los pisos ya se generaban a partir de arquetipos reutilizables; se ajustaron la ubicación de las tiendas, la aparición del jefe y la pantalla de Resultados.

**Impacto en otros sistemas:** Estructura de niveles, progresión, tiendas, jefe, interfaz (Resultados en lugar de ¡Victoria!), alcance, roadmap y pruebas.

**Decisión:** Aprobado e implementado en el juego.

**Responsable:** Anthony David Duarte Naal.

## Registro

| Fecha | Cambio | Motivo | Impacto | Estado |
|---|---|---|---|---|
| 2026-10-16 | Avanzar de piso con un ascensor que se activa con la tecla E. | Integrar el avance a la estructura del edificio. | Mecánicas, Controles, Niveles y UX. | Reemplazado por el salto al piso de arriba (2026-11-10) |
| 2026-10-16 | Quitar el botón de agarre del moveset. | Simplificar los controles. | Mecánicas y Controles. | Revertido: se mantiene el agarre (2026-11-10) |
| 2026-11-09 | Incluir a Niko, Mateo Cruz y Mr. Wobbles desde el inicio. | Ofrecer tres estilos de combate en la selección inicial. | Personajes, Progresión, UI y Alcance. | Ampliado a cinco personajes (2026-11-11) |
| 2026-11-09 | Incluir 100 pisos de Nuddle y a Big Data como jefe del piso 100. | Completar el recorrido de Nuddle en la primera versión. | Niveles, Alcance, Roadmap y Pruebas. | Reemplazado por la subida sin límite (2026-11-12) |
| 2026-11-09 | Contemplar dos personajes jugables adicionales. | Ampliar las opciones de combate. | Personajes, Alcance y Backlog. | Integrados: Atsuko y Craub (2026-11-11) |
| 2026-11-10 | Mantener el agarre (I / RB) como parte del moveset. | Sin agarres, los enemigos que se cubrían con el escudo eran casi imposibles de vencer. El agarre atraviesa el escudo. | Mecánicas, Controles y Pruebas. | Implementado en el juego |
| 2026-11-10 | Avanzar saltando y rompiendo el techo al terminar el piso, sin ascensor. | Romper el techo se siente mejor y encaja con todo lo demás que se rompe (ventanas y muebles). El ascensor solo hacía esperar al jugador. | Mecánicas, Niveles, Animación, UX y Pruebas. | Implementado en el juego |
| 2026-11-10 | Las ventanas se rompen según la fuerza del lanzamiento (antes, al llegar a 100 % de daño) y se regeneran unos segundos después de que nadie esté afuera (antes, a los 2 s). | Es más justo: la ventana se rompe según qué tan fuerte sale volando el personaje, no por un número. | Mecánicas, Entornos y Pruebas. | Implementado en el juego |
| 2026-11-11 | Incluir a Atsuko y Craub desde el inicio, para un total de cinco personajes. | Cada personaje tiene sus ataques armados por separado, así que agregar dos más fue viable. Ya existían en la historia como personajes para después. | Personajes, Arte, UI, Alcance y Backlog. | Implementado en el juego |
| 2026-11-11 | Pasar de 5 boons con máximo 3 por partida a 16 boons con forma de objetos de oficina, 4 rarezas, 5 niveles y sin límite fijo. | Con solo 3 espacios el jugador se quedaba sin mejoras muy rápido y las partidas se sentían iguales. Más boons hacen que cada partida sea distinta. | Sistemas, Economía, UI y Pruebas. | Implementado en el juego |
| 2026-11-11 | La tienda deja de vender comida y solo vende boons nuevos y mejoras; se quita el tope de 200 monedas. | Todo lo que se compra pasa a ser un boon. La curación depende de boons como el Botiquín, las Vitaminas o el Gato de la suerte. | Economía, Objetos y UI. | Implementado en el juego |
| 2026-11-12 | Subida sin límite de pisos, con Mr. Big Data cada 50 pisos y sin mini-jefes ni pantalla de victoria. | Ver la solicitud de cambio de esta sección. | Niveles, Alcance, Roadmap, UI y Pruebas. | Implementado en el juego |
| 2026-11-12 | Mover las tiendas a los pisos 10, 20, 30, 40, 49, 60… (antes 10, 19, 30, 39…). | Que coincidan con el jefe, que ahora aparece cada 50 pisos. | Niveles y Economía. | Implementado en el juego |
| 2026-11-12 | Pasar de 3 variantes de enemigo (débil, fuerte y demasiado fuerte) a 6 tipos: Guardia, Antidisturbios, Antidisturbios con porra, Guardia pesado, Dron y Dron kamikaze. | Los drones obligan a pelear de otra forma: vuelan, y el kamikaze se lanza contra el jugador y explota. | Enemigos, Arte y Pruebas. | Implementado en el juego |
| 2026-11-12 | Los élites dejan de ser enemigos normales con otro color: pelean mejor, dan el doble de monedas y sueltan el boon que llevan equipado. El Guardia pesado solo aparece como élite. | Que valga la pena enfrentar al enemigo difícil, porque deja un boon como recompensa. | Enemigos, Economía y Sistemas. | Implementado en el juego |
| 2026-11-12 | Reemplazar las 5 secciones fijas de 20 pisos por pisos armados al azar con arquetipos de sala (oficina, juntas, descanso, mantenimiento y servidores), más la Recepción, Café Corp y la oficina ejecutiva. | Cada piso se ve diferente sin tener que construirlos uno por uno. | Niveles, Entornos y Arte. | Implementado en el juego |
| 2026-11-12 | Pasar de 1 a 3 rondas por piso a entre 2 y 16 enemigos por piso, repartidos en rondas de hasta 4. | Que la dificultad suba poco a poco y no de golpe. | Niveles, Progresión y Enemigos. | Implementado en el juego |
| 2026-11-12 | El jefe pasa de 3 fases con KO por porcentaje a una armadura con barra de vida; al 70 %, 40 % y 20 % salta del escenario e invoca guardias. | Una barra de vida se entiende más fácil y evita que el jefe salga del escenario por accidente. | Enemigos, UI y Pruebas. | Implementado en el juego |

## Características agregadas

Elementos que no estaban en el GDD inicial y se agregaron durante el desarrollo:

- Tutorial jugable con Niko, accesible desde el menú principal.
- Pantalla de Resultados con estadísticas y calificación de S a D.
- Parry al soltar el escudo justo antes del golpe.
- Muebles rompibles y techo rompible.
- Anunciador que dice el nombre del personaje elegido.
- Iconos de botones que cambian según el control conectado (teclado, Xbox, PlayStation o Switch).
- Pruebas automáticas en Unity (ver [[02 - Pruebas]]).

## Características recortadas

| Fecha | Característica | Motivo | ¿Se retomará? |
|---|---|---|---|
| 2026-10-16 | Sistema de puntaje inspirado en Balatro | Se sustituyó por la calificación de la pantalla de Resultados (ver [[03 - Registro de Decisiones]]). | No |
| 2026-11-11 | Comida en la tienda (café, sándwich y menú ejecutivo) | Ya no hacía falta: la curación se obtiene con boons. | No |
| 2026-11-11 | Bebida energética como objeto que soltaban los guardias | Se convirtió en un boon de velocidad. | No |
| 2026-11-13 | Almanaque con el trasfondo de los personajes | No alcanzó el tiempo. La historia de los personajes está escrita en [[03 - Personajes]]. | Sí |
| 2026-11-13 | Guardado automático y checkpoints | Cada partida empieza desde cero, así que no era indispensable. | Tal vez |
| 2026-11-13 | Reasignación de controles | No alcanzó el tiempo; los controles quedaron fijos. | Sí |
| 2026-11-13 | Funcionalidad de los menús de Opciones y Créditos | No alcanzó el tiempo. Los botones están en el menú, pero todavía no tienen función. | Sí |
| 2026-11-13 | Otras corporaciones (Bookworm, Nile e Y) y el final narrativo | Era demasiado para el tiempo disponible; la entrega se enfoca en Nuddle. | Sí |
| 2026-11-13 | Versiones para consolas y Steam Deck | Exportar a consolas requiere SDK propietarios. La interfaz ya se adapta al tipo de mando. | Sí |


> **Navegación:** [[00 - Índice]] · ← [[04 - Backlog del Proyecto]] · [[01 - Criterios de Calidad]] →
