# Enemigos y NPC

## Descripción de la sección

Documenta las entidades controladas por el juego y su comportamiento.

## Plantilla de enemigo

### Nombre: Guardia Débil

**Rol de combate: Enemigo básico de patrullaje / Corto a medio alcance**

**Comportamiento: Patrulla de rutina. En solitario es fácil de derrotar, pero intenta agruparse para abrumar al jugador**

**Porcentaje de daño: Comienza en 0% y aumenta al recibir golpes. Cuanto mayor sea, mayor será el retroceso recibido**

**Vidas: 1. Queda eliminado al salir de los límites del escenario**

**Susceptibilidad al daño: ×2.0 (×1.2 si es élite)**

**Resistencia al lanzamiento: Por definir durante el balance**

**Daño: Bajo**

**Defensas: Ninguna**

**Velocidad: Media**

**Rango de detección: Corto/Medio**

**Ataques: Golpe rápido con porra antidisturbios**

**Debilidades: Poca resistencia física**

**Recompensa: Monedas (de 0 a 5) y probabilidad de soltar una bebida energética**

**Estados de IA:** 

```text
Patrullar → Detectar → Perseguir → Atacar
                  ↓
                Perder objetivo → Buscar
```



### Nombre: Guardia Pesado

**Rol de combate: Tanque pesado / Fuerza bruta**

**Comportamiento: Disfruta el enfrentamiento físico. Persigue implacablemente e intenta arrinconar al jugador**

**Porcentaje de daño: Comienza en 0% y aumenta al recibir golpes. Cuanto mayor sea, mayor será el retroceso recibido**

**Vidas: 1. Queda eliminado al salir de los límites del escenario**

**Susceptibilidad al daño: ×2.0 (×1.2 si es élite)**

**Resistencia al lanzamiento: Por definir durante el balance**

**Daño: Alto**

**Defensas: Alta inmunidad a los empujones directos, porta placas de protección livianas y guantes reforzados**

**Velocidad: Baja**

**Rango de detección: Medio**

**Ataques: Puñetazos demoledores beneficiados por la amplitud y alcance de sus brazos**

**Debilidades: uñetazos demoledores beneficiados por la amplitud y alcance de sus brazos**

**Recompensa: Multiplicador alto de puntuación**

**Estados de IA:**

```
Patrullar → Detectar → Embestir → Atacar pesado
```

## Enemigos

Los enemigos cambian según la compañía, pero **cada compañía tiene siempre tres variantes**. Pueden ser humanos o robots, según la empresa. Entre empresas, el moveset es prácticamente el mismo; lo que cambia es la apariencia y el estilo.

| Variante                   | Descripción                                                                                                            |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Débil**           | Enemigo básico, aparece en grandes cantidades.                                                                         |
| **Fuerte**           | Enemigo más resistente y peligroso. En Nuddle: **guardias muy musculosos**, que aparentan ser demasiado fuertes. |
| **Demasiado fuerte** | El enemigo más difícil antes del jefe.                                                                                |

> [!note] ✏️ Alcance de la entrega
> Por ahora solo se desarrollarán los enemigos de **Nuddle**. El jefe, Big Data Nuddleman, también usa robots, armaduras robóticas e invoca guardias (ver [[03 - Personajes]]). La variante débil de Nuddle es el Guardia Débil y la variante fuerte es el Guardia Pesado. Falta por definir la variante demasiado fuerte.

## Plantilla de NPC

**Nombre:** NPC de la tienda (trabajador genérico de la compañía, sin nombre propio, que cambia según el piso)

**Función:** Trabajador de la compañía (programador, gente de marketing, etc.) que apoya la causa de la resistencia.

**Ubicación:** Tiendas de los pisos 10, 19, 30, 39, 50, 59, 70, 79, 90 y 99.

**Interacción:** Conversación opcional durante la visita a la tienda.

**Diálogos:**

**Condiciones:** El jugador llega a un piso con tienda.

**Recompensas / información:** Comenta un poco sobre la historia y el mundo.

> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →
