# Criterios de Calidad

## Descripción de la sección

Define qué significa que una característica esté correctamente terminada.

## Calidad funcional

- [ ]  **Combate:** cada golpe suma porcentaje a quien lo recibe, y el retroceso crece con el porcentaje. Un enemigo con mucho porcentaje sale volando visiblemente más lejos que uno con poco.
- [ ]  **KO y vidas:** salir de los límites del escenario siempre cuenta como KO. El jugador pierde una vida, reaparece en una plataforma temporal con 0% e invulnerable unos instantes, y pierde la partida al perder la tercera vida.
- [ ]  **Ventanas:** una ventana intacta funciona como pared, se rompe con un golpe muy fuerte, se regenera después de un rato y se repara al cambiar de piso.
- [ ]  **Defensa:** el escudo se desgasta y, al romperse, aturde al personaje. El parry y el esquive funcionan en el suelo y en el aire, según corresponda.
- [ ]  **Moveset:** cada combinación de botón y dirección produce el ataque documentado para los tres personajes iniciales. No existe ningún agarre.
- [ ]  **Boons:** se ofrecen 3 opciones; con 3 boons equipados solo se ofrecen mejoras; ningún boon pasa del nivel 5; si no hay opciones, el menú se omite.
- [ ]  **Estructura de la partida:** las tiendas aparecen solo en los pisos 10, 19, 30, 39, 50, 59, 70, 79, 90 y 99; los mini-jefes, en los pisos 20, 40, 60 y 80; el jefe final, en el piso 100.
- [ ]  **Avance:** el ascensor solo se habilita después de limpiar todas las rondas del piso y resolver la elección de boon.
- [ ]  **Fin de partida:** derrotar a Big Data en el piso 100 lleva a la pantalla de ¡Victoria! sin otro ascenso. Perder las 3 vidas lleva a la pantalla de derrota.
- [ ]  **Sin progreso permanente:** una partida nueva empieza con 0 monedas, sin boons, con 3 vidas y en el piso 1.

## Calidad de experiencia

- [ ] **Objetivo claro:** el jugador sabe en todo momento si debe pelear, elegir un boon o ir al ascensor.
- [ ]  **Lectura del combate:** el porcentaje de **todos** los personajes en pantalla es visible en todo momento.
- [ ]  **Sensación de impacto:** cada golpe conectado tiene congelación breve (hitlag), destello y respuesta sonora. Los lanzamientos fuertes dejan estela. El último KO del nivel se marca con cámara lenta.
- [ ]  **Ventanas legibles:** una ventana rota se distingue de una intacta a primera vista, sin depender solo del color.
- [ ]  **Ascensor legible:** el estado bloqueado o disponible del ascensor se entiende sin depender solo del color rojo o verde.
- [ ]  **Controles:** un jugador nuevo puede moverse, saltar y atacar en el primer piso sin leer instrucciones externas.
- [ ]  **Dificultad coherente:** los primeros pisos son claramente más fáciles que los posteriores, y los mini-jefes y el jefe final son picos de dificultad reconocibles.
- [ ]  **Decisiones con sentido:** en la tienda, el jugador duda entre curarse y mejorar un boon; no compra siempre lo mismo.
- [ ]  **Ritmo:** la historia nunca interrumpe el combate. Los descansos (menú de boons, ascensor y tienda) son breves.

## Calidad técnica

- [ ] **Rendimiento:** 60 FPS estables a 1920×1080 en un equipo con los requisitos recomendados, incluso con el máximo de enemigos y efectos de boons en pantalla.
- [ ]  **Rendimiento mínimo:** el juego es jugable a 1280×720 en un equipo con los requisitos mínimos, sin caídas sostenidas por debajo de 30 FPS.
- [ ]  **Carga:** menos de 10 segundos para entrar a la partida en condiciones normales.
- [ ]  **Memoria:** hasta 4 GB de RAM durante la ejecución, sin crecimiento sostenido entre el piso 1 y el piso 100 (sin fugas de memoria).
- [ ]  **Estabilidad:** se puede completar un recorrido del piso 1 al 100 sin cierres inesperados ni bloqueos.
- [ ]  **Entrada:** el juego funciona igual con teclado y con mando, y detecta el mando conectado sin reiniciar.
- [ ]  **Guardado estable:** la configuración se conserva al cerrar y abrir el juego. Lo que guarde la partida se validará cuando se defina en [[04 - Guardado y Configuración]] (backlog P08).
- [ ]  **Sin dependencias rotas:** la compilación de PC no muestra errores en consola, referencias perdidas ni assets faltantes.
## Definición de terminado

Una característica se considera terminada cuando:

Funciona según lo documentado en el GDD y cumple su criterio de aceptación.
Se probó con teclado y con mando, en la compilación de PC y no solo en el editor de Unity.
Se probó con Niko, Mateo Cruz y Mr. Wobbles cuando la característica afecta al combate.
No tiene bugs abiertos de severidad crítica o alta.


> **Navegación:** [[00 - Índice]] · ← [[05 - Gestión de Cambios]] · [[02 - Pruebas]] →
