# Datos y Persistencia

## Descripción de la sección

Define qué información necesita conservar el juego y cómo se estructura.

## Datos persistentes

- **Progreso:** no hay progreso permanente entre partidas; cada partida empieza desde cero. La partida en curso no se guarda.
- **Configuración:** no se guarda; por ahora el juego no tiene opciones de configuración.
- **Inventario:** no persiste. Las monedas y los boons solo duran una partida.
- **Estadísticas:** no se guardan. Durante la partida se generan el piso alcanzado, los KO totales, las monedas ganadas, la suma de niveles de boons y el tiempo, que solo se muestran en la pantalla de resultados junto con una calificación de S a D.
- **Desbloqueos:** ninguno por ahora. Los cinco personajes jugables (Niko, Mateo Cruz, Atsuko, Mr. Wobbles y Craub) están disponibles desde el inicio.
- **Otros:** ninguno.

## Modelo de datos

| Entidad | Datos principales |
|---|---|
| Personaje | Moveset, datos de ataques, peso y susceptibilidad al daño |
| Enemigo | Tipo (guardia, antidisturbios, antidisturbios con porra, guardia pesado, dron o dron kamikaze), si es élite, susceptibilidad al daño, nivel de la IA y una sola vida |
| Jefe | Mr. Big Data, con barra de vida y fases |
| Boon | Tipo (Encendedor, Extintor criogénico, Regleta sobrecargada, Café de la oficina, Caja de chocolates, Reloj de pared, Botiquín, Frasco de vitaminas, Caja de cartón, Bebida energética, Zapatillas deportivas, Mancuerna, Casco de obra, Cerdito hucha, Cáscara de plátano o Gato de la suerte), rareza (común, rara, épica o legendaria) y nivel (1 a 5) |
| Partida | Personaje elegido, piso actual, vidas (3), porcentaje de daño, monedas, boons (sin límite), KO totales y tiempo |
| Nivel | Número de piso, rondas (de hasta 4 enemigos cada una), enemigos, élites, y si tiene tienda o jefe |

**Relaciones:**

- Una partida tiene un personaje y cualquier cantidad de boons.
- Una partida recorre pisos sin límite, hasta que el jugador pierde las 3 vidas.
- Cada nivel genera sus enemigos, entre normales y élite.
- Los datos de ataques pertenecen a cada personaje.

## Formato

**Formato de guardado:** No aplica: el juego no guarda datos.

**Ubicación:** No aplica.

**Versionado de datos:** No aplica.

## Migraciones

No aplica: no existe progreso permanente ni configuración guardada.


> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
