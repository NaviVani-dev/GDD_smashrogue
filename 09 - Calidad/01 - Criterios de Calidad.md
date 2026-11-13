# Criterios de Calidad

## Descripción de la sección

Define qué significa que una característica esté correctamente terminada.

## Calidad funcional

- [ ]  **Combate:** cada golpe suma porcentaje a quien lo recibe, y el retroceso crece con el porcentaje. Un enemigo con mucho porcentaje sale volando visiblemente más lejos que uno con poco.
- [ ]  **KO y vidas:** salir de los límites del escenario (por una ventana o pared rota, o al caer por el borde de la plataforma) siempre cuenta como KO. El jugador pierde una vida, reaparece cayendo desde arriba con 0 % e invulnerable unos instantes, y pierde la partida al perder la tercera vida.
- [ ]  **Ventanas:** una ventana intacta funciona como pared, se rompe con un golpe muy fuerte, se regenera después de unos segundos y se repara al cambiar de piso. Las paredes de las salas cerradas funcionan igual.
- [ ]  **Defensa:** el escudo se desgasta y, al romperse, aturde al personaje. El parry y el esquive funcionan en el suelo y en el aire, según corresponda.
- [ ]  **Moveset:** cada combinación de botón y dirección produce el ataque documentado para los cinco personajes iniciales. El agarre (I / RB) atrapa al rival y permite atacarlo y lanzarlo.
- [ ]  **Boons:** se ofrecen 3 opciones, que pueden ser boons nuevos o mejoras; no hay límite de boons equipados; ningún boon pasa del nivel 5; si no hay opciones, el menú se omite.
- [ ]  **Estructura de la partida:** las tiendas aparecen cada 10 pisos y en el piso anterior a cada jefe (10, 20, 30, 40, 49, 60, 70, 80, 90, 99…); Mr. Big Data aparece cada 50 pisos (50, 100, 150…).
- [ ]  **Avance:** el personaje solo sube al siguiente piso después de limpiar todas las rondas del piso y resolver la elección de boon. En la tienda, sube al usar la salida.
- [ ]  **Fin de partida:** perder las 3 vidas muestra el letrero "GAME!" y después la pantalla de resultados. No hay condición de victoria: la subida no tiene fin.
- [ ]  **Sin progreso permanente:** una partida nueva empieza con 0 monedas, sin boons, con 3 vidas y en el piso 1.

## Calidad de experiencia

- [ ] **Objetivo claro:** el jugador sabe en todo momento si debe pelear, elegir un boon, recoger un boon o comprar en la tienda.
- [ ]  **Lectura del combate:** el porcentaje del jugador y de los enemigos es visible en todo momento; la vida del jefe se ve en su barra.
- [ ]  **Sensación de impacto:** cada golpe conectado tiene congelación breve (hitlag), destello y respuesta sonora. Los lanzamientos fuertes dejan estela. El último KO del nivel se marca con cámara lenta.
- [ ]  **Ventanas legibles:** una ventana rota se distingue de una intacta a primera vista, sin depender solo del color.
- [ ]  **Controles:** un jugador nuevo puede moverse, saltar y atacar en el primer piso sin leer instrucciones externas.
- [ ]  **Dificultad coherente:** los primeros pisos son claramente más fáciles que los posteriores, y Mr. Big Data es un pico de dificultad reconocible.
- [ ]  **Decisiones con sentido:** en la tienda, el jugador duda entre comprar un boon nuevo y mejorar uno que ya tiene; no compra siempre lo mismo.
- [ ]  **Ritmo:** la historia nunca interrumpe el combate. Los descansos (menú de boons, salto entre pisos y tienda) son breves.

## Calidad técnica

- [ ] **Rendimiento:** 60 FPS estables a 1920×1080 en un equipo con los requisitos recomendados, incluso con el máximo de enemigos y efectos de boons en pantalla.
- [ ]  **Rendimiento mínimo:** el juego es jugable a 1280×720 en un equipo con los requisitos mínimos, sin caídas sostenidas por debajo de 30 FPS.
- [ ]  **Carga:** menos de 10 segundos para entrar a la partida en condiciones normales.
- [ ]  **Memoria:** hasta 4 GB de RAM durante la ejecución, sin crecimiento sostenido entre el piso 1 y el piso 100 (sin fugas de memoria).
- [ ]  **Estabilidad:** se puede jugar del piso 1 al piso 100 sin cierres inesperados ni bloqueos.
- [ ]  **Entrada:** el juego funciona igual con teclado y con mando, y detecta el mando conectado sin reiniciar.
- [ ]  **Sin dependencias rotas:** la compilación de PC no muestra errores en consola, referencias perdidas ni assets faltantes.
## Definición de terminado

Una característica se considera terminada cuando:

Funciona según lo documentado en el GDD y cumple su criterio de aceptación.
Se probó con teclado y con mando, en la compilación de PC y no solo en el editor de Unity.
Se probó con Niko, Mateo Cruz, Atsuko, Mr. Wobbles y Craub cuando la característica afecta al combate.
No tiene bugs abiertos de severidad crítica o alta.


> **Navegación:** [[00 - Índice]] · ← [[05 - Gestión de Cambios]] · [[02 - Pruebas]] →
