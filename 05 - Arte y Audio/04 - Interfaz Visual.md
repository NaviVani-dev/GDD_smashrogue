# Interfaz Visual

## Descripción de la sección

Documenta la información que el juego muestra al jugador y las reglas visuales de la interfaz.

## HUD

Elementos:

- Porcentaje de daño
Indicador numérico que aumenta al recibir golpes.

- Vidas restantes
Indicador independiente del porcentaje de daño. El jugador comienza con tres vidas y pierde una cada vez que sale de los límites del escenario.

- Energía
No aplica: el juego no tiene un sistema de energía.

- Munición
No aplica: los protagonistas no usan munición.

- Objetivo
Debe comunicar la tarea inmediata: derrotar al grupo de enemigos, avanzar o enfrentar al jefe.

- Mapa
No aplica: cada piso es una sola arena, sin recorrido entre zonas, por lo que no hay mapa ni minimapa.

- Recursos
Contador discreto de las monedas disponibles durante la partida, representado mediante un icono y una cantidad numérica. Se actualiza al obtener monedas o realizar compras. Debe ser legible sin competir visualmente con el porcentaje de daño y las vidas restantes.

- Indicadores contextuales
Avisos breves cuando haya una elección de mejora o una transición disponible.

## Jerarquía visual

¿Qué información debe verse primero, segundo y tercero?

1. **Información inmediata:** indicador de daño del personaje y avisos que afecten su supervivencia.
2. **Estado del encuentro:** objetivo actual, avance y situación del jefe cuando corresponda.
3. **Información complementaria:** boons, detalles de mejoras y puntaje si se implementa.
4. El contador de monedas tendrá menor prioridad visual que el porcentaje de daño y las vidas restantes.

Durante la elección de un boon, las opciones y sus efectos pasan a ser el foco principal de la interfaz.
## Estados

Documenta estados normales, advertencias, daño, éxito, error y bloqueo.

- **Normal:** HUD con el porcentaje de daño de todos los personajes, las vidas restantes, el objetivo y el contador de monedas.
- **Advertencia:** avisos que afectan la supervivencia del jugador. Los enemigos élite muestran su porcentaje en color dorado.
- **Daño:** el indicador de porcentaje aumenta al recibir golpes y el personaje golpeado muestra un destello rojo.
- **Éxito:** al completar el piso aparece el aviso de la elección de mejora o de la transición disponible, y el ascensor se muestra con luz verde.
- **Error:** la tienda indica claramente cuándo el saldo es insuficiente.
- **Bloqueo:** el ascensor permanece con las puertas cerradas y luz roja durante el combate, y la compra queda bloqueada si el saldo no alcanza.
## Convenciones

**Tipografía:**
Sans serif gruesa y redondeada para los números (porcentaje, vidas y monedas), legible a primera vista durante el combate. Sans serif limpia de peso regular para las descripciones de los boons y los textos de la tienda. Ambas con estilo anime y sin adornos.

**Iconografía:**
Iconos planos con contorno grueso, en el mismo estilo cel-shading del juego. Cada boon tiene una silueta propia: llama para Fuego, copo de nieve para Hielo, cruz para Curación, pluma para Pluma y planeta para Espacio. Las monedas y las vidas usan iconos fijos junto a su número. Utilizar formas simples y consistentes para representar boons y estados. Los iconos deben distinguirse también por su silueta, acompañados de texto cuando sea necesario.

**Tamaños mínimos:**
A 1280 × 720, el porcentaje de daño es el número más grande del HUD y ningún texto es más pequeño que el contador de monedas. Las medidas exactas se ajustan mediante pruebas a las resoluciones objetivo. La información esencial debe leerse sin ampliar la interfaz.

**Contraste:**
Los textos e indicadores deben distinguirse sobre fondos claros y oscuros. El color se acompañará de formas, símbolos o texto para comunicar estados.

**Animaciones:**
El porcentaje "salta" brevemente al subir y se muestra en dorado en los enemigos élite. Las cartas del menú de boons entran rápido y se agrandan al seleccionarlas. Los avisos (piso completado, ascensor disponible y saldo insuficiente) aparecen y desaparecen en menos de un segundo. Se evitan efectos prolongados que retrasen las decisiones.
## Pantallas

- Menú principal
Acceso a Jugar, Configuración y el almanaque con el trasfondo de cada personaje. Estructura visual por definir.

- Selección de personaje
Elección entre Niko, Mateo Cruz y Mr. Wobbles, disponibles desde el inicio. Presentación y datos por definir.

- Pausa
Continuar, Configuración y Abandonar partida. Abandonar la partida pide confirmación y regresa al menú principal.

- Configuración
Ajustes de audio, video, controles y accesibilidad, y opción para restablecer los valores predeterminados.

- Seleccion de boon
Opciones de mejora y descripción de sus efectos. La propuesta contempla selección por teclado o mouse.

- Inventario
No aplica: no hay un sistema de inventario. Puede evaluarse una consulta de boons sin asumir un sistema de objetos.

- Tienda
Muestra las monedas disponibles, los productos y sus precios. Debe indicar claramente cuándo el saldo es insuficiente y actualizarlo después de cada compra.

- Mapa
No aplica: cada piso es una sola arena, sin recorrido entre zonas.

- Victoria
Pantalla de ¡Victoria! tras derrotar a Big Data en el piso 100. Al continuar, se muestran los créditos y después el menú principal. Información de la pantalla por definir.

- Derrota
Resultado al perder la partida. Opciones y reglas de reinicio por definir.

> **Navegación:** [[00 - Índice]] · ← [[03 - Entornos]] · [[05 - Audio y Música]] →
