# Datos y Persistencia

## Descripción de la sección

Define qué información necesita conservar el juego y cómo se estructura.

## Datos persistentes

- **Progreso:** no hay progreso permanente entre partidas; cada partida empieza desde cero. El guardado es automático y solo conserva la configuración. La partida en curso no se guarda.
- **Configuración:** categorías de audio, video, controles y accesibilidad.
- **Inventario:** no persiste. Las monedas y los boons solo duran una partida.
- **Estadísticas:** no se guardan. Durante la partida se generan el número de nivel alcanzado y los KO totales, que solo se muestran al terminar la partida.
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

**Formato de guardado:** Archivo JSON local con la configuración.

**Ubicación:** Carpeta de datos persistentes de Unity, en el equipo del jugador.

**Versionado de datos:** El archivo guarda un número de versión.

## Migraciones

Como no existe progreso permanente entre partidas, un cambio en la estructura de los datos solo afecta a la configuración. Si la versión del archivo no coincide con la del juego, se restablecen los valores predeterminados.


> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
