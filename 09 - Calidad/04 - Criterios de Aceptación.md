# Criterios de Aceptación

## Descripción de la sección

Los criterios de aceptación permiten decidir objetivamente si una característica está lista.

## Características

### Daño por porcentaje y retroceso

**Dado que:** hay dos enemigos en el escenario, uno con mucho porcentaje y otro con poco.

**Cuando:** el jugador los golpea con el mismo ataque.

**Entonces:** cada golpe suma porcentaje a quien lo recibe y el enemigo con más porcentaje sale volando visiblemente más lejos.

### Combate base

**Dado que:** hay una arena con un personaje jugable y un guardia.

**Cuando:** el jugador saca al guardia de la arena.

**Entonces:** la oleada termina por KO. Si el jugador sufre un KO, pierde una vida y reaparece si le quedan vidas.

### Reaparición

**Dado que:** el jugador tiene más de una vida.

**Cuando:** sale de los límites del escenario.

**Entonces:** pierde una vida y reaparece en una plataforma temporal, con 0% e invulnerable unos instantes.

### Ventanas rompibles

**Dado que:** una ventana está intacta.

**Cuando:** un personaje choca contra ella con un golpe muy fuerte.

**Entonces:** la ventana se rompe y el personaje sale volando. La ventana se regenera después de un rato y se repara al cambiar de piso.

### Defensa

**Dado que:** el jugador tiene el escudo arriba.

**Cuando:** recibe golpes hasta que el escudo se desgasta por completo.

**Entonces:** el escudo se rompe y el personaje queda aturdido. Si bloquea justo a tiempo, se produce un parry y el atacante queda expuesto.

### Moveset

**Dado que:** el jugador eligió a Niko, Mateo Cruz o Mr. Wobbles.

**Cuando:** combina el botón de ataque, habilidad o ataque fuerte con una dirección.

**Entonces:** se produce el ataque documentado para ese personaje y no existe ningún agarre.

### Boons

**Dado que:** el jugador limpió todas las rondas del piso.

**Cuando:** se abre el menú de boons.

**Entonces:** se ofrecen 3 opciones. Con 3 boons equipados, solo se ofrecen mejoras. Ningún boon pasa del nivel 5. Si no hay opciones, el menú se omite.

### Ascensor

**Dado que:** el jugador está en un piso con enemigos.

**Cuando:** limpia todas las rondas y resuelve la elección de boon.

**Entonces:** el ascensor se habilita con luz verde y, al interactuar con él, el jugador sube al siguiente piso. Antes de eso, el ascensor permanece cerrado con luz roja.

### Tienda

**Dado que:** el jugador llega a un piso con tienda y tiene monedas.

**Cuando:** compra comida o una mejora de boon.

**Entonces:** la comida reduce su porcentaje o el boon sube de nivel, y el saldo se actualiza en la tienda y en el HUD. Si el saldo no alcanza, la compra queda bloqueada.

### Victoria

**Dado que:** el jugador llegó al piso 100.

**Cuando:** derrota a Big Data.

**Entonces:** aparece la pantalla de ¡Victoria!, sin otro ascenso, y la partida termina.

### Derrota

**Dado que:** el jugador tiene una sola vida.

**Cuando:** sale de los límites del escenario.

**Entonces:** aparece la pantalla de derrota y la partida termina.

### Partida nueva

**Dado que:** terminó una partida anterior.

**Cuando:** el jugador inicia una partida nueva.

**Entonces:** empieza con 0 monedas, sin boons, con 3 vidas y en el piso 1.

## Criterios del proyecto

- [ ] El bucle principal funciona: elegir personaje, limpiar las rondas del piso, elegir boon, activar el ascensor y subir del piso 1 al piso 100 con cualquiera de los tres personajes iniciales.
- [ ] Las condiciones de victoria y derrota funcionan: derrotar a Big Data en el piso 100 lleva a la pantalla de ¡Victoria! y perder las 3 vidas lleva a la pantalla de derrota.
- [ ] La configuración se conserva al cerrar y abrir el juego. 
- [ ] Los sistemas principales están integrados: combate, ventanas, boons, monedas, tienda, HUD, ascensor, mini-jefes de los pisos 20, 40, 60 y 80, y Big Data en el piso 100.
- [ ] Las pruebas críticas están aprobadas: los casos y el recorrido completo en la compilación de PC con teclado y mando.
- [ ] El rendimiento cumple el objetivo definido: 60 FPS a 1920×1080 con los requisitos recomendados, carga de menos de 10 segundos y hasta 4 GB de RAM.
- [ ] No existen errores bloqueantes conocidos ni bugs abiertos de severidad crítica o alta.


> **Navegación:** [[00 - Índice]] · ← [[03 - Bugs y Seguimiento]] · [[01 - Glosario]] →
