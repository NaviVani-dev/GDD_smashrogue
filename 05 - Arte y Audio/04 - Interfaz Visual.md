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
No hay un sistema de energía confirmado.

- Munición
No se ha definido munición para los protagonistas.

- Objetivo
Debe comunicar la tarea inmediata: derrotar al grupo de enemigos, avanzar o enfrentar al jefe.

- Mapa
No se ha confirmado un mapa o minimapa.

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
**Por definir**
## Convenciones

**Tipografía:**
Por definir. Debe resultar legible en textos breves, números y descripciones de habilidades.

**Iconografía:**
Por definir. Utilizar formas simples y consistentes para representar boons y estados. Los iconos deben distinguirse también por su silueta, acompañados de texto cuando sea necesario.

**Tamaños mínimos:**
Por definir mediante pruebas a las resoluciones objetivo. La información esencial debe leerse sin ampliar la interfaz.

**Contraste:**
Los textos e indicadores deben distinguirse sobre fondos claros y oscuros. El color se acompañará de formas, símbolos o texto para comunicar estados.

**Animaciones:**
Por definir transiciones breves para selección, confirmación y avisos, evitando efectos prolongados que retrasen las decisiones.
## Pantallas

- Menú principal
Acceso a las opciones principales. Estructura por definir.

- Selección de personaje
Elección entre los protagonistas disponibles; presentación y datos por definir.

- Pausa
Opciones durante la partida. Comportamiento por definir.

- Configuración
Ajustes disponibles; categorías por definir.

- Seleccion de boon
Opciones de mejora y descripción de sus efectos. La propuesta contempla selección por teclado o mouse.

- Inventario
No se ha confirmado un inventario. Puede evaluarse una consulta de boons sin asumir un sistema de objetos.

- Tienda
Muestra las monedas disponibles, los productos y sus precios. Debe indicar claramente cuándo el saldo es insuficiente y actualizarlo después de cada compra.

- Mapa
No confirmado.

- Victoria
Resultado tras superar el contenido correspondiente. Información por definir.

- Derrota
Resultado al perder la partida. Opciones y reglas de reinicio por definir.

> **Navegación:** [[00 - Índice]] · ← [[03 - Entornos]] · [[05 - Audio y Música]] →
