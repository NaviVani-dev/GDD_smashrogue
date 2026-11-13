# Entornos

## Descripción de la sección

Define la estética y necesidades visuales de escenarios, fondos, objetos y elementos ambientales.

## Zonas

| Zona | Estilo | Elementos | Función |
| --- | --- | --- | --- |
| La Recepción (piso 1) | Vestíbulo corporativo con mostrador de recepción. | Mostrador, mobiliario de recepción, ventanas y la calle visible afuera del edificio. | Primer piso de combate. |
| Oficina | Área de trabajo con escritorios. | Divisiones de cubículos, libreros, impresoras, plantas, garrafón de agua, pizarrón, ventanas y plataformas flotantes. | Encuentros contra grupos de enemigos. |
| Sala de juntas | Sala de reuniones. | Mesa de juntas, sillas, pantalla de proyector, pizarrones, sofá, ventanas y plataformas flotantes. | Encuentros contra grupos de enemigos. |
| Sala de descanso | Zona de convivencia. | Sofás, puffs, futbolito, mesa de ping-pong, máquina arcade, televisión, máquina expendedora, ventanas y plataformas flotantes. | Encuentros contra grupos de enemigos. |
| Mantenimiento | Cuarto de servicio con muros de ladrillo y piso de concreto. | Generador, casilleros, escaleras, extintores y plataformas flotantes. Sin ventanas. | Encuentros contra grupos de enemigos. |
| Sala de servidores | Espacio oscuro con iluminación azul. | Racks de servidores con luces azules y rojas y plataformas flotantes. Sin ventanas. | Encuentros contra grupos de enemigos. |
| Café Corp | Cafetería dentro del edificio. | Mostrador del tendero, letrero "CAFÉ CORP" y salida. | Tienda. |
| Oficina ejecutiva | Espacio de autoridad corporativa con iluminación cálida. | Libreros, logotipo y letrero "NUDDLE". | Enfrentamiento con Mr. Big Data, cada 50 pisos. |

No hay secciones de ambientación: el escenario de los pisos de combate se elige al azar y se mantiene en bloques de 3 pisos (ver [[01 - Estructura del Contenido]]). Durante los primeros 12 pisos, la iluminación se vuelve poco a poco más tenue.

## Modularidad

¿Qué elementos pueden reutilizarse?

Los entornos se construyen con piezas reutilizables de paredes, suelos, techos, ventanas, puertas y mobiliario. Esto permite mantener consistencia y producir distintas distribuciones sin crear todos los elementos desde cero.

Las variaciones se obtienen mediante la colocación de objetos, iluminación y composición del espacio. Los elementos decorativos deben distinguirse de las superficies transitables.

Parte del mobiliario se puede tirar o romper durante el combate (sillas, plantas, escritorios, libreros, impresoras, máquinas expendedoras, etc.), y algunos muebles sirven como superficies sobre las que se puede estar.

## Iluminación

Describe iluminación global, fuentes de luz y cambios durante el juego.

La iluminación debe separar visualmente a los personajes del fondo y destacar las zonas de combate. Las ventanas y luminarias de techo funcionan como fuentes reconocibles dentro de las oficinas.

Se utilizará una jerarquía de luz principal, ambiental y de acento para orientar la atención y conservar la profundidad del escenario. La paleta y el contraste deben permitir reconocer a los enemigos grises incluso dentro de espacios de tonos neutros. Cada tipo de sala tiene su propio tono de luz: la sala de servidores es oscura y azulada, mantenimiento es más gris y la oficina ejecutiva es cálida.
## Efectos visuales

- Partículas 
Polvo al correr, saltar, girar y aterrizar; cristales al romperse las ventanas; escombros de paredes, techo y muebles; restos de drones; y confeti de los ataques de Mr. Wobbles. Su presencia debe apoyar la acción sin saturar la pantalla.

- Clima
No aplica: lo único jugable son las arenas dentro de las oficinas, por lo que no hay un sistema de clima.

- Humo
Humo detrás de los personajes que salen volando y vapor en algunos impactos. No es una mecánica.

- Fuego
Vinculado al boon de fuego y a los ataques de fuego de Craub. No implica incendios o propagación por el escenario.

- Agua
No aplica: no tiene una función jugable ni ambiental.

- Magia / energía
Representación de hielo, electricidad y veneno mediante el color del personaje afectado (ver [[01 - Dirección de Arte]]). Los drones disparan un láser y el dron kamikaze explota.

- Impactos
Destellos blancos localizados en el contacto de los golpes. El personaje golpeado muestra un destello blanco, los lanzamientos fuertes dejan una estela naranja y, al salir del escenario, se genera un destello en el punto de salida.

## Recursos requeridos

Lista los modelos, sprites, texturas, materiales y efectos necesarios.

- Plataformas flotantes con lámpara (de 1 a 3 por sala).
- Ventanas rompibles con estado intacto y roto, que se distingan con claridad.
- Techo rompible, que se rompe al subir de piso y al lanzar a alguien contra él.
- Fachada y calle visibles desde La Recepción.
- Piezas modulares de paredes, suelos, techos, ventanas, puertas y mobiliario de oficina (escritorios, sillas, luminarias, libreros, sofás, racks y más), muchas de ellas rompibles.
- Mostrador y tendero de Café Corp.
- Efectos de impacto, estela de lanzamiento, destello de salida del escenario, polvo, humo, cristales, escombros y efectos de los boons.

> **Navegación:** [[00 - Índice]] · ← [[02 - Personajes y Animación]] · [[04 - Interfaz Visual]] →
