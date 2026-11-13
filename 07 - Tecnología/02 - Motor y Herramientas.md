# Motor y Herramientas

## Descripción de la sección

Documenta las herramientas utilizadas para crear el videojuego y por qué fueron seleccionadas.

## Motor

**Motor:** Unity 

**Versión:** 6.6 

**Renderizado:** 2.5D

**Física:** Física del motor

**Sistema de entrada:** Input System de Unity

## Lenguajes

| Lenguaje | Uso                                                                                  |
| -------- | ------------------------------------------------------------------------------------ |
| C#       | Scripts del juego: combate, mejoras (boons), comportamiento de enemigos y progresión |

## Herramientas

| Herramienta     | Propósito                                      | Versión     |
| --------------- | ---------------------------------------------- | ----------- |
| UNITY           | MOTOR DEL JUEGO                                | 6.6         |
| BLENDER         | Modelar y animar elementos 3D                  | Por definir |
| Adobe Photoshop | Sprites, fondos e interfaz                     |             |
| Github          | Control de versiones y trabajo en equipo       |             |
| Discord         | Comunicación del equipo y comunidad de testers |             |
| itch.io         | Venta, distribución y actualizaciones          |             |
| Obsidian        | Redacción y mantenimiento del GDD              |             |

## Dependencias

Input System de Unity.

## Convenciones del proyecto

Control de versiones: GitHub.

- **Ramas:** `main` solo contiene versiones estables; `develop` integra el trabajo del equipo; cada tarea tiene su propia rama, `feature/nombre-de-la-tarea` o `fix/nombre-del-bug`.
- **Commits:** en español y en imperativo, describiendo el cambio. Ejemplos: "Agrega el menú de pausa" o "Corrige la regeneración de ventanas".

Nomenclatura: se sigue la sección Convenciones de nombres del Glosario.

- **Estructura de carpetas:** `Assets/_Project/` con las carpetas `Scripts`, `Prefabs`, `Scenes`, `Art`, `Audio`, `UI` y `Data`.
- **Formato de assets:** FBX para modelos, PNG para texturas y sprites, WAV para la música y OGG para los efectos y las voces.
- **Convenciones de código (C#):** PascalCase para clases y métodos, camelCase para variables y `_camelCase` para campos privados. Un script por clase.


> **Navegación:** [[00 - Índice]] · ← [[01 - Arquitectura Técnica]] · [[03 - Requisitos Técnicos]] →
