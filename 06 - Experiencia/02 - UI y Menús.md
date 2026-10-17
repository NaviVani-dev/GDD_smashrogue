	# UI y Menús

## Descripción de la sección

Define la estructura funcional de las interfaces y menús.

## Mapa de navegación

```text
Menú principal
├── Jugar
│   └── Selección de personaje
│       └── Cuenta regresiva
│           └── Jugando
│               ├── Menú de boons
│               ├── Tienda
│               ├── Pausa
│               ├── Victoria
│               └── Derrota
└── Configuración
```

## Pantallas


**Menú principal**

Propósito: Dar acceso a las opciones principales.

Elementos: Estructura por definir.

Acciones disponibles: Jugar.

Estados: Por definir.

Transiciones:

Jugar → Selección de personaje.
Victoria / Derrota → Continuar → Menú principal.


**Selección de personaje**

Propósito: Elegir entre los protagonistas disponibles.

Elementos: Presentación y datos por definir.

Acciones disponibles: Elegir personaje.

Estados: Por definir.

Transiciones: Elegir personaje → Cuenta regresiva.

**Menú de boons**

Propósito: Elegir un boon o una mejora para personalizar la partida.

Elementos: 3 boons ofrecidos al azar, con la descripción de sus efectos. Con los espacios llenos, solo se ofrecen mejoras de los boons que ya tiene el jugador. Las opciones y sus efectos pasan a ser el foco principal de la interfaz.

Acciones disponibles: Seleccionar una carta.

Estados: Si no hay nada que ofrecer (todo al máximo), se pasa directo al siguiente nivel.

Transiciones:

Último enemigo del nivel fuera → Menú de boons (si hay boons o mejoras disponibles).
Derrotar al mini-jefe → Menú de boons.
Elegir boon → Transición de nivel.

## Confirmaciones

Las confirmaciones de acciones destructivas o irreversibles están por definir.


> **Navegación:** [[00 - Índice]] · ← [[01 - UX y Flujo del Jugador]] · [[03 - Accesibilidad]] →
