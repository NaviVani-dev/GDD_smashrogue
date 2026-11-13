# Interfaz Visual

## Descripción de la sección

Documenta la información que el juego muestra al jugador y las reglas visuales de la interfaz.

## HUD

Elementos:

- Porcentaje de daño
Indicador numérico con un decimal (por ejemplo, "45.3%") que aumenta al recibir golpes. Aparece junto al nombre del personaje. Los enemigos muestran su porcentaje (sin decimales) flotando sobre su cabeza.

- Vidas restantes
Indicador independiente del porcentaje de daño, con iconos del personaje. El jugador comienza con tres vidas y pierde una cada vez que sale de los límites del escenario.

- Energía
No aplica: el juego no tiene un sistema de energía.

- Munición
No aplica: los protagonistas no usan munición.

- Objetivo
Contador de KO del piso ("KO x/y": enemigos eliminados sobre el total, contando las rondas que faltan) y número de piso ("PISO x").

- Mapa
No aplica: cada piso es una sola arena, sin recorrido entre zonas, por lo que no hay mapa ni minimapa.

- Recursos
Contador discreto de las monedas disponibles durante la partida, representado mediante un icono y una cantidad numérica. Al ganar monedas aparece un "+x" que sube y se desvanece. Debe ser legible sin competir visualmente con el porcentaje de daño y las vidas restantes.

- Boons equipados
Iconos de los boons del jugador con su nivel.

- Barra del jefe
Barra de vida de Mr. Big Data, con su nombre y título, durante el enfrentamiento.

- Indicadores contextuales
Una marca que rebota sobre la cabeza del jugador; avisos con el botón correspondiente para recoger un boon ("AGARRAR") y, en la tienda, para comprar ("COMPRAR") o salir ("SUBIR"); flechas que señalan los boons en el suelo, también desde el borde de la pantalla.

## Jerarquía visual

¿Qué información debe verse primero, segundo y tercero?

1. **Información inmediata:** indicador de daño del personaje y avisos que afecten su supervivencia.
2. **Estado del encuentro:** contador de KO del piso, número de piso y barra del jefe cuando corresponda.
3. **Información complementaria:** boons y detalles de mejoras.
4. El contador de monedas tendrá menor prioridad visual que el porcentaje de daño y las vidas restantes.

Durante la elección de un boon, las opciones y sus efectos pasan a ser el foco principal de la interfaz.
## Estados

Documenta estados normales, advertencias, daño, éxito, error y bloqueo.

- **Normal:** HUD con el porcentaje de daño del jugador y de los enemigos, las vidas restantes, el contador de KO, el piso, los boons y el contador de monedas.
- **Advertencia:** el porcentaje cambia de color según el daño (crema, amarillo, naranja, rojo y carmesí). Los enemigos élite muestran su porcentaje en color cian.
- **Daño:** el indicador de porcentaje aumenta y tiembla al recibir golpes, y el personaje golpeado muestra un destello blanco.
- **Éxito:** al completar el piso aparece el menú de boons y, al elegir uno, el personaje celebra y sube al siguiente piso. Al perder las 3 vidas aparece el letrero "GAME!".
- **Error:** en la tienda, el tendero avisa con un diálogo cuando el saldo es insuficiente, el producto está agotado o el jugador ya tiene ese boon.
- **Bloqueo:** la compra queda bloqueada si el saldo no alcanza.
## Convenciones

**Tipografía:**
Barlow Condensed, una sans serif condensada, en pesos Bold, SemiBold, ExtraBold Italic y Black Italic. Los números (porcentaje, vidas y monedas) usan los pesos más gruesos para leerse a primera vista durante el combate.

**Iconografía:**
Iconos en el mismo estilo del juego. Cada boon se representa con un objeto de oficina: encendedor, extintor, regleta, café, caja de chocolates, reloj, botiquín, frasco de vitaminas, caja de cartón, bebida energética, zapatillas, mancuerna, casco, cerdito, cáscara de plátano y gato de la suerte. Las monedas y las vidas usan iconos fijos junto a su número. Los avisos muestran el icono del botón según el control que se esté usando (teclado, Xbox, PlayStation o Switch). Los iconos deben distinguirse también por su silueta, acompañados de texto cuando sea necesario.

**Tamaños mínimos:**
A 1280 × 720, el porcentaje de daño es el número más grande del HUD y ningún texto es más pequeño que el contador de monedas. Las medidas exactas se ajustan mediante pruebas a las resoluciones objetivo. La información esencial debe leerse sin ampliar la interfaz.

**Contraste:**
Los textos e indicadores deben distinguirse sobre fondos claros y oscuros. El color se acompañará de formas, símbolos o texto para comunicar estados.

**Animaciones:**
El porcentaje "salta" y tiembla brevemente al subir. Las cartas del menú de boons entran rápido y se agrandan al seleccionarlas. Los menús entran deslizándose y las transiciones entre pantallas usan efectos de diamantes y fragmentos. Se evitan efectos prolongados que retrasen las decisiones.
## Pantallas

- Pantalla de inicio
Logo animado, con letras que caen y rebotan, y el aviso "PULSA CUALQUIER BOTÓN".

- Menú principal
JUGAR, TUTORIAL, OPCIONES, CRÉDITOS y SALIR, más el botón "MUNDO DEBUG". Opciones y Créditos todavía no tienen función.

- Selección de personaje
"ELIGE A TU LUCHADOR": una tarjeta por personaje (Niko, Mateo Cruz, Atsuko, Mr. Wobbles y Craub), el nombre y el modelo 3D del seleccionado, la voz del anunciador al elegir y la franja "START" para confirmar.

- Pausa
CONTINUAR, OPCIONES (sin función por ahora) y VOLVER AL INICIO. Volver al inicio regresa al menú principal sin pedir confirmación.

- Configuración
No aplica por ahora: el menú de Opciones todavía no tiene función.

- Seleccion de boon
3 cartas. Cada una muestra el icono y el nombre del boon, si es "NUEVO" o una mejora ("NV 1 » 2"), su etiqueta (por ejemplo, la rareza) y la descripción del efecto.

- Inventario
No aplica: no hay un sistema de inventario. Los boons equipados se ven en el HUD.

- Tienda
Muestra las monedas disponibles, 4 productos y sus precios. El tendero indica cuándo el saldo es insuficiente y el saldo se actualiza después de cada compra.

- Mapa
No aplica: cada piso es una sola arena, sin recorrido entre zonas.

- Victoria
No aplica: el juego no tiene condición de victoria.

- Derrota
Al perder las 3 vidas aparece el letrero "GAME!" y después la pantalla de resultados: el personaje con su animación de victoria, el piso alcanzado, los KOs, las monedas ganadas, los boons (suma de niveles), el tiempo y una calificación de S a D, con las opciones "REINTENTAR" y "MENÚ".

> **Navegación:** [[00 - Índice]] · ← [[03 - Entornos]] · [[05 - Audio y Música]] →
