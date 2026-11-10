	# UI y Menús

## Descripción de la sección

Define la estructura funcional de las interfaces y menús.

## Mapa de navegación

```text
Menú principal
├── Jugar
│   └── Selección de personaje
|       ├── Entrada inicial por el ascensor
│       └── Cuenta regresiva
│           └── Jugando
│               ├── Menú de boons
│               ├── Tienda
│               ├── Pausa
│               ├── Victoria
│               │   └── Créditos
│               └── Derrota
└── Configuración
```

## Pantallas


**Menú principal**

Propósito: Dar acceso a las opciones principales.

Elementos: Jugar, Configuración y almanaque con el trasfondo de cada personaje. Estructura visual por definir.

Acciones disponibles: Jugar, entrar a Configuración y consultar el almanaque.

Estados: Por definir.

Transiciones:

Jugar → Selección de personaje.
Derrotar al jefe final → Victoria → Créditos → Menú principal.
Derrota → Continuar → Menú principal.


**Selección de personaje**

Propósito: Elegir entre los protagonistas disponibles.

Elementos: Niko, Mateo Cruz y Mr. Wobbles, disponibles desde el inicio. Presentación y datos por definir.

Acciones disponibles: Elegir personaje.

Estados: Por definir.

Transiciones: Elegir personaje → Entrada inicial por el ascensor → Cuenta regresiva.

**Menú de boons**

Propósito: Elegir un boon o una mejora para personalizar la partida.

Elementos: 3 boons ofrecidos al azar, con la descripción de sus efectos. Con los espacios llenos, solo se ofrecen mejoras de los boons que ya tiene el jugador. Las opciones y sus efectos pasan a ser el foco principal de la interfaz.

Acciones disponibles: Seleccionar una carta.

Estados: Si no hay nada que ofrecer (todo al máximo), se omite el menú y se habilita el ascensor.

Transiciones:

Último enemigo del nivel fuera → Menú de boons, si hay opciones disponibles.
Derrotar al mini-jefe → Menú de boons, si hay opciones disponibles.
Elegir boon → Ascensor disponible → Interactuar con el ascensor → Transición de nivel.
Sin opciones disponibles → Ascensor disponible.

**Tienda**

Propósito: Permitir comprar comida y mejoras de boons con las monedas de la partida.

Elementos: Saldo disponible, productos, precios y opción para salir de la tienda.

Acciones disponibles: Consultar productos, comprar y salir.

Estados: Compra disponible si el saldo alcanza; compra bloqueada por saldo insuficiente. Después de una compra, el saldo se actualiza tanto en la tienda como en el HUD.

Transiciones: Salir de la tienda → Continuar con el flujo del piso correspondiente.

**Pausa**

Propósito: Detener la partida temporalmente.

Elementos: Continuar, Configuración y Abandonar partida.

Acciones disponibles: Continuar, entrar a Configuración y abandonar la partida.

Transiciones: Esc / Start → Jugando. Abandonar partida → Confirmación → Menú principal.

## Confirmaciones

Se pide confirmación al abandonar la partida (la partida se pierde porque no se guarda), al restablecer la configuración y al salir del juego.


> **Navegación:** [[00 - Índice]] · ← [[01 - UX y Flujo del Jugador]] · [[03 - Accesibilidad]] →
