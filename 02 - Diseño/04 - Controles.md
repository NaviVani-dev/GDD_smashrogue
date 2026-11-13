# Controles

## Descripción de la sección

Define la relación entre las acciones del jugador y las entradas físicas del dispositivo.

El juego se controla con **teclado y gamepad**, con un esquema inspirado en **MultiVersus**. No usa mouse ni controles táctiles durante el combate.

## Mapa de controles

| Acción                        | Teclado                              | Mouse | Control (Xbox / PlayStation) | Táctil |
| ------------------------------ | ------------------------------------ | ----- | ---------------------------- | ------- |
| Mover                          | W A S D                              | —    | Stick izquierdo              | —      |
| Caminar lento                  | Shift + dirección                   | —    | Inclinar poco el stick       | —      |
| Ataque básico                 | J (+ dirección)                     | —    | B / ○ (+ dirección)        | —      |
| Habilidad (especial)           | K (+ dirección)                     | —    | X / □ (+ dirección)        | —      |
| Ataque fuerte (smash)          | Flechas                              | —    | Stick derecho                | —      |
| Saltar / doble salto           | Espacio (o W)                        | —    | A / ✕                       | —      |
| Escudo                         | L                                    | —    | Gatillos (LT / RT) o Y / △  | —      |
| Esquive / rodar                | L + dirección                       | —    | Escudo + dirección          | —      |
| Agarrar                        | I (o L + J)                          | —    | RB / R1                      | —      |
| Recoger boon de un élite      | J                                    | —    | B / ○                       | —      |
| Elegir boon                    | Navegar y Enter                      | Clic  | Navegar y A / ✕             | —      |
| Cafetería: comprar / subir    | I (junto al mostrador o a la salida) | —    | RB / R1                      | —      |
| Menú / pausa                  | Esc                                  | —    | Start / Options              | —      |
| Resultados: reintentar o menú | Navegar y Enter                      | Clic  | Navegar y A / ✕             | —      |

> [!warning] ⚠️ Diferencia con el prototipo
> El diseño original no tenía agarres y usaba un ascensor (tecla E). En la versión final **sí hay agarres** (sirven para romper escudos) y **no hay ascensor**: el personaje pasa al siguiente piso saltando a través del techo de forma automática..

## Principios de control

- Los controles deben ser consistentes.
- Las acciones críticas deben ser fáciles de identificar.
- Debe existir retroalimentación visual, sonora o háptica cuando corresponda.
- Evitar combinaciones innecesariamente complejas.
- Un mismo botón cambia de ataque según la dirección, como en Smash: pocas teclas, muchos movimientos.

## Reasignación

El jugador **no puede reasignar** los controles.

## Entrada y retroalimentación

* **Golpe conectado:** congelación breve (hitlag), destello rojo y vibración del personaje golpeado.
* **Lanzamiento fuerte:** estela de color detrás del personaje.
* **Carga de ataque fuerte:** el personaje parpadea en amarillo.
* **Parry:** destello azul.
* **Estado alterado:** el personaje parpadea con el color del efecto (naranja = quemadura, azul = hielo).
* **Último KO del nivel:** cámara lenta.
* **Indicaciones en pantalla:** los avisos (COMPRAR, SUBIR, AGARRAR) muestran el icono del botón según el dispositivo que se esté usando (teclado, Xbox, PlayStation o Switch).
* **Paso al siguiente piso:** el personaje salta, rompe el techo con cámara lenta y aterriza en el piso de arriba.

> **Navegación:** [[00 - Índice]] · ← [[03 - Sistemas]] · [[05 - Progresión]] →
