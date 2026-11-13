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

**Entonces:** pierde una vida y, tras unos instantes, reaparece cayendo desde arriba con 0 % e invulnerable unos 2 segundos.

### Ventanas rompibles

**Dado que:** una ventana (o una pared de una sala cerrada) está intacta.

**Cuando:** un personaje choca contra ella con un golpe muy fuerte.

**Entonces:** la ventana se rompe y el personaje sale volando. La ventana se regenera después de un rato y se repara al cambiar de piso.

### Defensa

**Dado que:** el jugador tiene el escudo arriba.

**Cuando:** recibe golpes hasta que el escudo se desgasta por completo.

**Entonces:** el escudo se rompe y el personaje queda aturdido. Si suelta el escudo justo cuando llega un golpe, se produce un parry y el atacante queda expuesto.

### Moveset

**Dado que:** el jugador eligió a Niko, Mateo Cruz, Atsuko, Mr. Wobbles o Craub.

**Cuando:** combina el botón de ataque, habilidad, ataque fuerte o agarre con una dirección.

**Entonces:** se produce el ataque documentado para ese personaje. El agarre atrapa al rival y permite golpearlo y lanzarlo.

### Boons

**Dado que:** el jugador limpió todas las rondas del piso.

**Cuando:** se abre el menú de boons.

**Entonces:** se ofrecen 3 opciones, que pueden ser boons nuevos o mejoras. No hay límite de boons equipados. Ningún boon pasa del nivel 5. Si no hay opciones, el menú se omite.

### Avance al siguiente piso

**Dado que:** el jugador está en un piso con enemigos.

**Cuando:** limpia todas las rondas y resuelve la elección de boon.

**Entonces:** el personaje celebra unos instantes, salta, rompe el techo y sube al siguiente piso, sin interactuar con nada. Antes de eso, permanece en el piso.

### Tienda

**Dado que:** el jugador llega a un piso con tienda y tiene monedas.

**Cuando:** compra un boon nuevo o una mejora de boon.

**Entonces:** el boon nuevo se agrega a sus boons o el boon sube de nivel, y el saldo se actualiza en la tienda y en el HUD. Si el saldo no alcanza, la compra queda bloqueada.

### Jefe

**Dado que:** el jugador llegó al piso 50 (o a cualquier múltiplo de 50).

**Cuando:** derrota a Mr. Big Data.

**Entonces:** recibe monedas, se abre el menú de boons y la subida continúa. No hay pantalla de victoria.

### Derrota

**Dado que:** el jugador tiene una sola vida.

**Cuando:** sale de los límites del escenario.

**Entonces:** aparece el letrero "GAME!", la partida termina y se muestra la pantalla de resultados con las opciones "REINTENTAR" y "MENÚ".

### Partida nueva

**Dado que:** terminó una partida anterior.

**Cuando:** el jugador inicia una partida nueva.

**Entonces:** empieza con 0 monedas, sin boons, con 3 vidas y en el piso 1.

## Criterios del proyecto

- [ ] El bucle principal funciona: elegir personaje, limpiar las rondas del piso, elegir boon y subir piso por piso con cualquiera de los cinco personajes iniciales.
- [ ] La condición de derrota funciona: perder las 3 vidas lleva al letrero "GAME!" y a la pantalla de resultados.
- [ ] Los sistemas principales están integrados: combate, agarres, ventanas, boons, monedas, tienda, HUD, salto entre pisos y Mr. Big Data cada 50 pisos.
- [ ] Las pruebas críticas están aprobadas: los casos de prueba y la subida del piso 1 al 100 en la compilación de PC con teclado y mando.
- [ ] El rendimiento cumple el objetivo definido: 60 FPS a 1920×1080 con los requisitos recomendados, carga de menos de 10 segundos y hasta 4 GB de RAM.
- [ ] No existen errores bloqueantes conocidos ni bugs abiertos de severidad crítica o alta.


> **Navegación:** [[00 - Índice]] · ← [[03 - Bugs y Seguimiento]] · [[01 - Glosario]] →
