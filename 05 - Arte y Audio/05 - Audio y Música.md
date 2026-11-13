# Audio y Música

## Descripción de la sección

Define la identidad sonora y cómo el audio comunica información al jugador.

## Música

**Estilo:**
Temas de 136 a 138 BPM que acompañan la energía del combate y la tensión del enfrentamiento contra las corporaciones. El tema de la tienda es lo-fi. Las influencias visuales del proyecto no determinan automáticamente el género musical.

**Instrumentación:**
No aplica: la música no fue compuesta por el equipo. Se tomó de un recurso externo (ver [[#Origen de los recursos de audio]]).

**Temas principales:**
- Menú principal.
- Combate en Nuddle.
- Tienda (Café Corp).
- Tutorial.

Cada tema tiene una introducción y una parte que se repite en bucle. No hay temas propios para el jefe, la victoria, la derrota ni las transiciones: el enfrentamiento con el jefe usa la música de combate y, al perder, la música se apaga y suena un golpe fuerte.

**Música dinámica:** Sí
La música cambia a la de la tienda en los pisos con tienda y vuelve a la de combate al salir. Mientras está abierto el menú de boons, la música se escucha apagada, como "bajo el agua". Al cambiar de pantalla, la música se desvanece.
## Efectos de sonido

| Evento              | Sonido                                                              | Propósito                                    |
| ------------------- | ------------------------------------------------------------------- | -------------------------------------------- |
| Desplazamiento      | Pasos acordes con el personaje.                                     | Dar presencia física al personaje.           |
| Salto y aterrizaje  | Sonidos breves de movimiento y contacto.                            | Reforzar la lectura del desplazamiento.      |
| Daño recibido       | Respuesta sonora diferenciada según el tipo de golpe (puñetazo, patada, corte, golpe pesado). | Confirmar que el personaje fue golpeado.     |
| Lanzamiento         | Sonido de lanzamiento según la fuerza del golpe.                    | Reforzar la fuerza del impacto.              |
| Escudo              | Sonidos al activar, bloquear, hacer parry y romper el escudo.       | Comunicar el estado de la defensa.           |
| Enemigo derrotado   | Señal breve asociada a su caída o salida del combate.               | Confirmar la derrota.                        |
| Boons               | Sonidos diferenciados para hielo, electricidad, fuego, veneno, etc. | Identificar la activación de efectos.        |
| Selección de mejora | Navegación, confirmación y un sonido de subida de nivel al elegir el boon. | Comunicar la elección del jugador.           |
| Monedas y compras   | Sonido al ganar monedas y al comprar en la tienda.                  | Confirmar la economía de la partida.         |
| Ventanas, paredes y techo | Sonidos de cristal y escombros al romperse.                         | Confirmar la ruptura del escenario.          |
| Público             | Ovación, aplausos y decepción que reaccionan al combate.            | Dar ambiente y energía al combate.           |
| Interfaz            | Movimiento del cursor, confirmación, regreso e inicio.              | Dar respuesta a las acciones en menús.       |

No hay sonidos de ambiente de oficina.

## Audio espacial

Sí, de forma sencilla: los sonidos del combate se escuchan más a la izquierda o a la derecha según dónde ocurran en la pantalla.

## Voz

**Narración:**
No hay narrador durante la partida. En la selección de personaje, una voz de anunciador dice el nombre del personaje elegido.

**Diálogos hablados:**
No hay diálogos hablados. Los personajes solo tienen sonidos de esfuerzo y de golpe. Los diálogos de las tiendas se presentan como texto.

**Idiomas:**
Español
## Mezcla

Define prioridades, volumen relativo y comportamiento de la música ante eventos importantes.

Priorizar las señales que afectan al jugador, seguidas de los impactos y acciones principales. La música debe acompañar el ritmo del combate sin ocultar información importante.

Se deberá controlar la acumulación de sonidos cuando varios enemigos ataquen o reciban daño al mismo tiempo. La música suena a 0.5 de volumen base (0.3 en la tienda), los sonidos de los enemigos suenan al 60 % y se reproducen hasta 28 sonidos al mismo tiempo. Por ahora no hay ajustes separados de volumen para música, efectos y voces.

## Origen de los recursos de audio

El equipo no creó audio propio: toda la música, los efectos de sonido y las voces se tomaron de un recurso externo. El equipo solo los seleccionó, los integró en Unity y ajustó su mezcla.

| Recurso | Uso en el juego | Origen | Licencia o uso |
|---|---|---|---|
| Música | Menú principal, combate, tienda (Café Corp) y tutorial | Externo: archivo del código fuente de *Super Smash Flash* (2006), [codeberg.org/SmashFlashDevs/SuperSmashFlash](https://codeberg.org/SmashFlashDevs/SuperSmashFlash) | El repositorio no declara una licencia y aclara que no está afiliado con Nintendo. Se usa solo con fines escolares, sin fines de lucro. |
| Efectos de sonido | Golpes, lanzamientos, escudo, boons, ventanas, monedas, público e interfaz | Externo: mismo repositorio | Igual que la música. |
| Voces | Anunciador de la selección de personaje y sonidos de esfuerzo y golpe | Externo: mismo repositorio | Igual que la música. |

> [!warning] ⚠️ Derechos de autor
> Estos recursos no pertenecen al equipo. Para publicar o vender el juego habría que reemplazarlos por audio propio o con licencia libre.

> **Navegación:** [[00 - Índice]] · ← [[04 - Interfaz Visual]] · [[01 - UX y Flujo del Jugador]] →
