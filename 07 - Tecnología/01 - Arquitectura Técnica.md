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
Sistemas de combate, enemigos y progresión
  ↓
Datos de la partida
  ↓
Presentación visual, audio, animaciones y UI
```

## Componentes principales

| Componente                      | Responsabilidad                                                                                                         | Dependencias                                           |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| Sistema de entrada              | Detectar las acciones del jugador, como moverse, saltar, atacar y agarrar                                               | Sistema de Input de Unity                              |
| Controlador del jugador         | Interpretar las entradas y controlar el movimiento y las acciones del personaje seleccionado: Niko, Mateo Cruz, Atsuko, Mr. Wobbles o Craub | Sistema de entrada, física y componentes del personaje |
| Sistema de combate              | Administrar ataques, agarres, daño, retroceso, y lanzamiento de personajes y enemigos                                   | Personajes, hitboxes, física y datos de ataques        |
| Sistema de niveles y progresión | Administrar las rondas de enemigos, el salto entre pisos (rompiendo el techo) y el inicio de combate contra el jefe     | Sistema de enemigos y estado de la partida             |
| Escenario                       | Administrar la plataforma tipo pilar, las ventanas y paredes rompibles, el techo rompible y los límites del escenario             | Combate                                                |
| IA de enemigos                  | Controlar a los enemigos normales y élite: guardias, antidisturbios, guardias pesados, drones y drones kamikaze         | Combate y niveles                                      |
| Sistema de boons                | Ofrecer y aplicar los boons y sus mejoras durante la partida, y los boons que sueltan los élites                        | Combate y estados alterados                            |
| Estados alterados               | Aplicar quemadura, congelación, lentitud, veneno y enamorado                                                       | Combate                                                |
| Economía y tienda               | Administrar las monedas, la tendera y la venta de boons nuevos y mejoras de boons                                       | Niveles y boons                                        |
| Jefes                           | Controlar a Mr. Big Data, que aparece cada 50 pisos                                                                     | Combate, IA y niveles                                  |
| Tutorial                        | Enseñar los controles básicos en una escena propia                                                                      | Combate y entrada                                      |
| Mundo debug                     | Probar personajes, enemigos y boons en una escena de pruebas                                                            | Todos los sistemas                                     |
| Interfaz (HUD)                  | Mostrar porcentajes, vidas, piso, contador de KO del piso, monedas, boons equipados, avisos de interacción, barra del jefe y menú de boons | Todos los sistemas                                     |

## Comunicación

¿Cómo intercambian información los sistemas?

Los componentes intercambiarán información mediante llamadas a métodos y referencias directas cuando sea necesario. Se buscará mantener una comunicación sencilla para facilitar el desarrollo y evitar dependencias innecesarias.

Por ejemplo, cuando Niko ataque a un enemigo, el sistema de combate comprobará el impacto, aplicará el daño y actualizará su porcentaje. Cuando se eliminen todos los enemigos de un piso, el sistema de progresión ofrecerá el menú de boons y después hará saltar al personaje al siguiente piso.

## Principios técnicos

- **Prioridad a la jugabilidad:** desarrollar primero el movimiento, los ataques y las colisiones antes de agregar elementos secundarios.
    
- **Pruebas frecuentes:** comprobar cada mecánica conforme se implemente para detectar errores a tiempo.
- **Optimización progresiva:** mantener un rendimiento estable y optimizar únicamente cuando se identifiquen problemas.


> **Navegación:** [[00 - Índice]] · ← [[04 - Guardado y Configuración]] · [[02 - Motor y Herramientas]] →
