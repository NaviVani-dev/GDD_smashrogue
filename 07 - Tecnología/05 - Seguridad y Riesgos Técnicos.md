# Seguridad y Riesgos Técnicos

## Descripción de la sección

Documenta riesgos técnicos y medidas para reducir fallos, pérdida de datos o abuso de sistemas.

## Riesgos

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| El combate se siente "flotado" o injusto | Media | Alta | Pruebas de sensación y ajuste de los valores del prototipo |
| Rendimiento insuficiente en equipos de gama media y baja, por la complejidad de los escenarios, los efectos visuales y la cantidad de enemigos simultáneos | Media | Alta | Optimización progresiva, pruebas en equipos de distintas capacidades y ajuste de los requisitos técnicos |
| El juego no tiene guardado ni opciones de configuración | Alta | Media | Definir si se agregan antes de la versión de entrega |
| Conflictos de código entre los 5 integrantes del equipo | Media | Media | Control de versiones en GitHub y pruebas frecuentes de cada mecánica |

## Datos sensibles

El juego no contempla cuentas, estadísticas en línea ni datos personales. Por ahora no guarda ningún dato en el equipo del jugador.

## Multijugador

No aplica. Es un juego de un jugador y no requiere conexión a internet, por lo que no hay autenticación, validación, autoridad del servidor, comunicación en red ni protección contra manipulación que documentar.

## Recuperación

No aplica para datos guardados, porque el juego no guarda nada. Al no requerir conexión, no existe el caso de pérdida de conexión.


> **Navegación:** [[00 - Índice]] · ← [[04 - Datos y Persistencia]] · [[01 - Alcance]] →
