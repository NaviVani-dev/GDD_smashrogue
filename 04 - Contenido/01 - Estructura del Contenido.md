# Estructura del Contenido

## Descripción de la sección

Organiza el contenido del videojuego en unidades manejables: mundos, capítulos, zonas, niveles, misiones y desafíos.

## Estructura

```text
Juego
├── Mundo / Capítulo 1: Lobby y Oficinas Bajas
│   ├── Nivel 1.1: El Filtro de Recepción
│   ├── Nivel 1.2: Laberinto de Cubículos
│   └── Jefe / Evento: Jefe de Seguridad del Lobby
├── Mundo / Capítulo 2: Sector Privado (I+D y Archivos)
│   ├── Nivel 2.1: Servidores de Datos
│   ├── Nivel 2.2: Laboratorios de Pruebas
|   └── Jefe / Evento: Jefe de Seguridad mas pesado
└── Final: La Oficina del Director (La cima del rascacielos)
```

## Cantidad estimada

| Tipo     |          Cantidad |
| -------- | ----------------: |
| Mundos   |             2 o 3 |
| Niveles  | 6 (dos por mundo) |
| Misiones |       Sin definir |
| Enemigos |                 5 |
| Jefes    |             1 o 2 |
| NPC      |             1 o 2 |
| Objetos  |                 2 |

## Dependencias

¿Qué contenido debe existir antes de otro?

* **Dirección de Arte y Modelado:** Todos los *assets* principales (personajes principales y los 5 tipos de enemigos) deben estar modelados y texturizados en su estilo 2.5D *low-poly* con *flat shading* antes de integrarlos a los *prefabs* de los niveles.
* **Mecánicas Base:** El sistema de combate debe estar programado y pulido antes de balancear la dificultad del Capítulo 1.
* **Flujo de Niveles:** Los nibeles debe estar completamente ensamblado y probado como nivel tutorial antes de comenzar la producción de los entornos de cada uno.

Navegación:[[00 - Índice]] · ← [[04 - Diálogos y Narrativa]] · [[02 - Niveles]] →
