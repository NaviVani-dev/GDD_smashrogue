# Arquitectura Técnica

## Descripción de la sección

Explica cómo está construido técnicamente el videojuego y cómo se comunican sus componentes.

## Arquitectura

El videojuego se desarrollará en **Unity utilizando C#**. Su arquitectura se organizará en capas que separen la entrada del jugador, el control de los personajes, la lógica de juego, los sistemas generales, los datos y la presentación visual.

```text
Entrada del jugador
  ↓
Controladores de personajes
  ↓
Lógica de juego
  ↓
Sistemas de combate , enemigos y progresion
  ↓
Datos / Persistencia
  ↓
Presentación visual, audio, animaciones y UI
```

## Componentes principales

| Componente                      | Responsabilidad                                                                               | Dependencias                                           |
| ------------------------------- | --------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| sistema de entrada              | Detectar las acciones del jugador, como moverse, saltar y atacar                              | Sistema de Input de Unity                              |
| Controlador del jugador         | Interpretar las entradas y controlar el movimiento y las acciones de Niko o Mr. Wobbles       | Sistema de entrada, fisica y componentes del personaje |
| Sistema de combate              | Administrar ataques, daño, retroceso, y lanzamiento de personajes y enemigos                  | Personajes, hitboxes, física y datos de ataques        |
| sistema de niveles y progresion | administrar oleadas de enemigos , el avance entre pisos y el inicio de combate contra el jefe | sistema de enemigos y estado de la partida             |

## Comunicación

¿Cómo intercambian información los sistemas?

Los componentes intercambiarán información mediante llamadas a métodos y referencias directas cuando sea necesario. Se buscará mantener una comunicación sencilla para facilitar el desarrollo y evitar dependencias innecesarias.

Por ejemplo, cuando Niko ataque a un enemigo, el sistema de combate comprobará el impacto, aplicará el daño y actualizará la salud. Cuando se eliminen todos los enemigos de un piso, el sistema de progresión permitirá avanzar al siguiente encuentro.

## Principios técnicos

- **Prioridad a la jugabilidad:** desarrollar primero el movimiento, los ataques y las colisiones antes de agregar elementos secundarios.
    
- **Pruebas frecuentes:** comprobar cada mecánica conforme se implemente para detectar errores a tiempo.
- **Optimización progresiva:** mantener un rendimiento estable y optimizar únicamente cuando se identifiquen problemas.


> **Navegación:** [[00 - Índice]] · ← [[04 - Guardado y Configuración]] · [[02 - Motor y Herramientas]] →
