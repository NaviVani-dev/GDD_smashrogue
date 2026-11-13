	# UI y Menús

## Descripción de la sección

Define la estructura funcional de las interfaces y menús.

## Mapa de navegación

```text
Pantalla de inicio ("PULSA CUALQUIER BOTÓN")
└── Menú principal
    ├── Jugar
    │   └── Selección de personaje
    │       └── Cuenta regresiva
    │           └── Jugando
    │               ├── Menú de boons
    │               ├── Tienda
    │               ├── Pausa
    │               └── GAME! (derrota)
    │                   └── Resultados
    ├── Tutorial
    ├── Opciones (sin función por ahora)
    ├── Créditos (sin función por ahora)
    ├── Salir
    └── Mundo debug
```

## Pantallas


**Pantalla de inicio**

Propósito: Presentar el logo del juego.

Elementos: Logo animado y el aviso "PULSA CUALQUIER BOTÓN".

Acciones disponibles: Pulsar cualquier botón del teclado, del mando o del ratón.

Transiciones: Pulsar un botón → Menú principal.


**Menú principal**

Propósito: Dar acceso a las opciones principales.

Elementos: JUGAR, TUTORIAL, OPCIONES, CRÉDITOS y SALIR, más el botón "MUNDO DEBUG" en la esquina inferior derecha.

Acciones disponibles: Jugar, entrar al tutorial, entrar al mundo debug y salir del juego. Opciones y Créditos todavía no tienen función.

Estados: Por definir.

Transiciones:

Jugar → Selección de personaje.
Tutorial → Escena de tutorial.
Mundo debug → Escena de pruebas.
Salir → Cierra el juego, sin confirmación.
Derrota → GAME! → Resultados → Reintentar o Menú principal.


**Selección de personaje**

Propósito: Elegir entre los protagonistas disponibles.

Elementos: Título "ELIGE A TU LUCHADOR" y una tarjeta por cada personaje: Niko, Mateo Cruz, Atsuko, Mr. Wobbles y Craub, todos disponibles desde el inicio. Se muestra el nombre y el modelo 3D del personaje seleccionado.

Acciones disponibles: Elegir personaje (suena la voz del anunciador con su nombre), confirmar con la franja "START" y volver.

Estados: Sin elegir; personaje elegido con la franja "START" visible.

Transiciones: Elegir personaje → START → Cuenta regresiva. Volver → Menú principal.

**Menú de boons**

Propósito: Elegir un boon o una mejora para personalizar la partida.

Elementos: 3 opciones al azar, con la descripción de sus efectos. Cada opción puede ser un boon nuevo o la mejora de uno que el jugador ya tiene. No hay límite de boons equipados. Las opciones y sus efectos pasan a ser el foco principal de la interfaz.

Acciones disponibles: Seleccionar una carta.

Estados: Si no hay nada que ofrecer (todo al máximo), se omite el menú y el personaje sube al siguiente piso.

Transiciones:

Último enemigo del piso fuera → Menú de boons, si hay opciones disponibles.
Derrotar al jefe → Menú de boons, si hay opciones disponibles.
Elegir boon → Celebración breve → Salto al siguiente piso.
Sin opciones disponibles → Salto al siguiente piso.

**Tienda**

Propósito: Permitir comprar boons nuevos y mejoras de boons con las monedas de la partida.

Elementos: Tendero con diálogos, mostrador con el aviso "COMPRAR", salida con el aviso "SUBIR", saldo disponible, 4 productos y sus precios.

Acciones disponibles: Acercarse al mostrador y abrir la tienda, consultar productos, comprar, cerrar la tienda y salir por la salida.

Estados: Compra disponible si el saldo alcanza; compra bloqueada por saldo insuficiente, por producto agotado o porque el jugador ya tiene ese boon. Si ya no queda nada que comprar, el tendero lo avisa y no abre la tienda. Después de una compra, el saldo se actualiza tanto en la tienda como en el HUD.

Transiciones: Salida ("SUBIR") → Salto al siguiente piso.

**Pausa**

Propósito: Detener la partida temporalmente.

Elementos: CONTINUAR, OPCIONES y VOLVER AL INICIO.

Acciones disponibles: Continuar y volver al inicio. Opciones todavía no tiene función. No se puede pausar con el menú de boons o la tienda abiertos.

Transiciones: Esc / Start → Jugando. Volver al inicio → Menú principal, sin confirmación.

**Resultados**

Propósito: Mostrar el resumen de la partida al perder las 3 vidas.

Elementos: Modelo del personaje y los datos de piso alcanzado, KOs, monedas ganadas, boons (suma de niveles) y tiempo, más una calificación de S a D.

Acciones disponibles: REINTENTAR y MENÚ.

Transiciones: Reintentar → Nueva partida con el mismo personaje. Menú → Menú principal.

## Confirmaciones

Por ahora no se pide confirmación al volver al inicio desde la pausa ni al salir del juego.


> **Navegación:** [[00 - Índice]] · ← [[01 - UX y Flujo del Jugador]] · [[03 - Accesibilidad]] →
