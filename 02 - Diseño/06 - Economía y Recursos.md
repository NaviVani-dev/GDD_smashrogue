# Economía y Recursos

## Descripción de la sección

Documenta cualquier recurso cuantificable: dinero, vida, energía, munición, experiencia, materiales, tiempo, puntos, etc.

## Recursos

| Recurso                | Obtención                                                         | Uso                                               | Límite                    | Pérdida                                                                                                       |
| ---------------------- | ----------------------------------------------------------------- | ------------------------------------------------- | ------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **Porcentaje de daño** | Sube al recibir golpes                                            | Determina qué tan lejos sale volando el personaje | 0% – 999%                 | Se reinicia a 0% al perder una vida. Puede reducirse mediante comida, bebida energética o el boon de curación |
| **Vidas**              | 3 al iniciar la partida                                           | Seguir jugando después de salir del escenario     | 3                         | Se pierde una al salir del escenario                                                                          |
| **Monedas**            | Al derrotar enemigos: cantidad aleatoria **de 0 a 5** por enemigo | Comprar en la tienda                              | 200                       | Se pierden al terminar la partida                                                                             |
| **Boons**              | Uno al terminar cada nivel                                        | Mejorar el combate                                | 3 boons, nivel 5 cada uno | Se pierden al terminar la partida                                                                             |

## Fuentes y sumideros

**Fuentes:**
- Monedas por cada enemigo derrotado.
- Bebida energética: probabilidad de que la suelte un Guardia Débil al ser derrotado.
- Un boon (o una mejora) por cada nivel completado.

**Sumideros:**
- **Tienda** (niveles 10, 19, 30, 39, 50, 59, 70, 79, 90 y 99):
  - **Comida:** cura (reduce el porcentaje).
  - **Mejoras de boons.**

**Comida de la tienda:**

| Producto | Efecto | Precio |
|---|---|---|
| Café de máquina | Porcentaje restante = porcentaje actual × 0.80 (−20%) | 15 monedas |
| Sándwich de la cafetería | Porcentaje restante = porcentaje actual × 0.60 (−40%) | 30 monedas |
| Menú ejecutivo | Deja el porcentaje en 0% | 60 monedas |

**Mejoras de boons:**

| Mejora | Precio |
|---|---|
| Nivel 1 → 2 | 25 monedas |
| Nivel 2 → 3 | 40 monedas |
| Nivel 3 → 4 | 60 monedas |
| Nivel 4 → 5 | 80 monedas |

## Reglas

- Las monedas solo sirven dentro de la partida actual.
- Hay **tienda cada 10 niveles**, excepto cuando el siguiente nivel tiene un mini-jefe o el jefe final: en ese caso, la tienda aparece **un nivel antes** para que el jugador se prepare. Las tiendas quedan en los niveles **10, 19, 30, 39, 50, 59, 70, 79, 90 y 99**.
- Los enemigos sueltan una cantidad aleatoria de monedas, **entre 0 y 5**: algunos no sueltan nada.
- El jugador puede tener un máximo de **200 monedas**. Las monedas que se obtienen al llegar al límite se pierden.
- La bebida energética la sueltan los Guardias Débiles y no se vende en la tienda. Se consume automáticamente al pasar por encima de ella y reduce un 30% del porcentaje de daño acumulado: porcentaje restante = porcentaje actual × 0.70.

> [!note] Puntaje
> El sistema de puntaje inspirado en Balatro **queda descartado por ahora**.

## Balance

¿Qué comportamiento queremos incentivar?
- Pelear de forma agresiva y sacar enemigos del escenario.
- Decidir entre curarse o fortalecer los boons.

¿Qué comportamiento queremos evitar?
- Esconderse detrás del escudo todo el tiempo.
- Acumular tantas monedas que la tienda deje de ser una decisión.


> **Navegación:** [[00 - Índice]] · ← [[05 - Progresión]] · [[07 - Reglas y Estados del Juego]] →
