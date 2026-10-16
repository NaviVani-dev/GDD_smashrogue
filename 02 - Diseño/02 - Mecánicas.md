# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

## Plantilla de mecánica

### Nombre de la mecánica

**Propósito:**  
¿Qué aporta a la experiencia?

**Activación:**  
¿Qué debe hacer el jugador?

**Reglas:**  
¿Qué puede y qué no puede ocurrir?

**Entrada:**  
¿Qué botón, gesto o acción la activa?

**Estado inicial:**

**Estado final:**

**Recursos utilizados:**

**Recompensa:**

**Penalización:**

**Interacciones con otras mecánicas:**

**Casos límite:**  
¿Qué ocurre en situaciones poco comunes?

## Mecánicas principales

### Mecánica 01 - Movimiento y salto

Propósito: Es la base del posicionamiento. Moverse bien es la diferencia entre ganar o perder la partida.

Activación: El jugador se mueve horizontalmente y salta.

Reglas:

Movimiento horizontal sobre el escenario.
Un salto desde el suelo y un salto aéreo adicional.
El salto aéreo se recupera al tocar el suelo.
Mientras el personaje está en estado de aturdimiento o siendo empujado, no controla su movimiento.

Entrada: A / D mover · Espacio saltar · 

Estado inicial: En el suelo, sin movimiento.

Estado final: En movimiento, en el aire o de regreso en el suelo.

Recursos utilizados: Salto aéreo.

Recompensa: Evitar ataques y acercarse a los enemigos para golpearlos.

Penalización: Caer fuera del escenario provoca la derrota de la partida.

Interacciones con otras mecánicas: por definir

Casos límite:

Recibir un golpe no consume el salto aéreo.
Usar el salto aéreo estando ya fuera del límite visible del escenario aún es válido hasta salir por completo de la zona de peligro.

### Mecánica 02 - Ataque básico


Propósito: Golpe rápido y constante; es la herramienta principal para acumular daño y generar combos.

Activación: El jugador presiona el botón de ataque.

Reglas:

Cadena de hasta 3 golpes seguidos.
El ataque aplica daño acumulado (%) y un empuje pequeño al enemigo.
Entrada: por definir
Estado inicial: Personaje libre sin movimiento
Estado final: Fin de la animación de ataque.
Recursos utilizados: Ninguno
Recompensa: Daño acumulado en el enemigo, puntos y aumento del combo.
Penalización: Fallar el golpe deja al personaje vulnerable durante la recuperación
Interacciones con otras mecánicas: por definir
Casos límite:
Si el enemigo es lanzado fuera del escenario a mitad de un combo, el combo termina y suma el punto de KO.



### Mecánica 03 - Habilidad especial




Propósito: Ataque más potente que da identidad a cada personaje y que los boons modifican de forma notable.

Activación: El jugador presiona el botón de habilidad.

Reglas:

Tiene un periodo de enfriamiento.
Aplica mayor empuje y/o un efecto de control sobre los enemigos.
Cada personaje tiene una habilidad especial propia.

Entrada: por definir

Estado inicial: Habilidad disponible.

Estado final: Habilidad en enfriamiento.

Recursos utilizados: Enfriamiento de la habilidad.

Recompensa: Gran empuje, control de grupo o efecto de estado.

Penalización: Durante el enfriamiento, el jugador no la tiene disponible; si falla, queda vulnerable.

Interacciones con otras mecánicas: por definir

Casos límite:

Intentar usarla en enfriamiento: respuesta visual/sonora de "no disponible".
La pausa y la pantalla de selección de boon congelan el enfriamiento.

## Mecánicas secundarias

Lista las mecánicas que complementan la experiencia pero no constituyen el núcleo.


> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
