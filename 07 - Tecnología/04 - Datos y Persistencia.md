# Datos y Persistencia

## Descripción de la sección

Define qué información necesita conservar el juego y cómo se estructura.

## Datos persistentes

- **Progreso:** no hay progreso permanente entre partidas; cada partida empieza desde cero. El guardado es automático, pero su contenido está por definir.
- **Configuración:** categorías de audio y controles.
- **Inventario:** no persiste. Las monedas y los boons solo duran una partida.
- **Estadísticas:** por definir. Durante la partida se generan el número de nivel alcanzado y los KO totales.
- **Desbloqueos:** ninguno por ahora. Los tres personajes jugables (Niko, Mateo Cruz y Mr. Wobbles) están disponibles desde el inicio.
- **Otros:** por definir.

## Modelo de datos

| Entidad | Datos principales |
|---|---|
| Personaje | Moveset, datos de ataques, peso y susceptibilidad al daño |
| Enemigo | Tipo (normal o élite), susceptibilidad al daño y una sola vida |
| Boon | Tipo (fuego, hielo, curación, pluma o espacio) y nivel (1 a 5) |
| Partida | Personaje elegido, nivel actual, vidas (3), porcentaje de daño, monedas, boons (máximo 3) y KO totales |
| Nivel | Número de nivel, rondas (1 a 3), enemigos, élites, y si tiene tienda, mini-jefe o jefe final |

**Relaciones:**

- Una partida tiene un personaje y hasta 3 boons.
- Una partida recorre niveles, hasta el nivel 100.
- Cada nivel genera sus enemigos, entre normales y élite.
- Los datos de ataques pertenecen a cada personaje.

## Formato

**Formato de guardado:** Por definir

**Ubicación:** Por definir

**Versionado de datos:** Por definir

## Migraciones

Por definir. Como no existe progreso permanente entre partidas, un cambio en la estructura de los datos afectaría únicamente a la configuración y al guardado automático.


> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
