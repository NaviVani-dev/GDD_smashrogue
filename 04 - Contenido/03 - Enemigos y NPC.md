# Enemigos y NPC

## Descripción de la sección

Documenta las entidades controladas por el juego y su comportamiento.

## Reglas comunes de los enemigos

- **Porcentaje de daño:** comienza en 0 % y aumenta al recibir golpes. Cuanto mayor sea, mayor será el retroceso recibido.
- **Vidas:** 1. Quedan eliminados al salir de los límites del escenario.
- **Susceptibilidad al daño:** ×2.0 en los primeros pisos y baja 0.1 cada 4 pisos, hasta ×1.4. Los élites empiezan en ×1.2 y bajan 0.05 cada 4 pisos, hasta ×0.8.
- **Recompensa:** de 0 a 10 monedas por enemigo (las cantidades bajas son las más probables). Los élites dan el doble y sueltan el boon que llevan equipado, que el jugador puede recoger.
- **Élites:** se distinguen por un borde dorado y su porcentaje en color cian. Llevan un boon equipado y tienen una IA más hábil. Pueden aparecer a partir del piso 3, excepto en los pisos del jefe.
- **IA:** no patrullan. Desde que entran al escenario van hacia el jugador, atacan, usan habilidades, se cubren con el escudo y, si pueden, agarran. Su nivel de habilidad (1 a 9) sube con los pisos: reaccionan más rápido, se quedan quietos menos veces y se defienden más.

**Estados de IA (enemigos de a pie):**

```text
Entrada al escenario → Acercarse al jugador → Atacar / Habilidad / Agarrar
                              ↓
                      Cubrirse con el escudo
```

## Plantilla de enemigo

### Nombre: Guardia

**Rol de combate: Enemigo básico / Corto a medio alcance**

**Comportamiento: Es el enemigo más común. En solitario es fácil de derrotar, pero aparece en grupo para abrumar al jugador**

**Porcentaje de daño: Comienza en 0% y aumenta al recibir golpes. Cuanto mayor sea, mayor será el retroceso recibido**

**Vidas: 1. Queda eliminado al salir de los límites del escenario**

**Susceptibilidad al daño: ×2.0 en los primeros pisos, hasta ×1.4 (×1.2 a ×0.8 si es élite)**

**Resistencia al lanzamiento: Peso medio (85)**

**Daño: Bajo**

**Defensas: Escudo**

**Velocidad: Media**

**Rango de detección: No aplica: siempre sabe dónde está el jugador**

**Ataques: Combo de 3 golpes, golpes y patadas, ataques fuertes y un disparo con pistola a media distancia. No agarra**

**Debilidades: Poca resistencia física y no puede agarrar**

**Recompensa: De 0 a 10 monedas (el doble si es élite)**

**Aparición: Desde el piso 1**



### Nombre: Antidisturbios

**Rol de combate: Enemigo medio / Cuerpo a cuerpo y agarres**

**Comportamiento: Busca el contacto cercano para golpear y agarrar al jugador**

**Porcentaje de daño: Comienza en 0% y aumenta al recibir golpes. Cuanto mayor sea, mayor será el retroceso recibido**

**Vidas: 1. Queda eliminado al salir de los límites del escenario**

**Susceptibilidad al daño: ×2.0 en los primeros pisos, hasta ×1.4 (×1.2 a ×0.8 si es élite)**

**Resistencia al lanzamiento: Peso alto (98)**

**Daño: Por definir durante el balance**

**Defensas: Escudo y un contraataque que agarra al atacante**

**Velocidad: Media**

**Rango de detección: No aplica: siempre sabe dónde está el jugador**

**Ataques: Combo de golpes, patada explosiva, gancho ascendente, suplex, agarres y lanzamientos**

**Debilidades: No tiene ataques a distancia**

**Recompensa: De 0 a 10 monedas (el doble si es élite)**

**Aparición: Desde el piso 2, cada vez con más frecuencia**



### Nombre: Antidisturbios con porra

**Rol de combate: Enemigo medio / Medio alcance con arma**

**Comportamiento: Usa la porra para golpear desde más lejos que un guardia y castiga los ataques con contraataques**

**Porcentaje de daño: Comienza en 0% y aumenta al recibir golpes. Cuanto mayor sea, mayor será el retroceso recibido**

**Vidas: 1. Queda eliminado al salir de los límites del escenario**

**Susceptibilidad al daño: ×2.0 en los primeros pisos, hasta ×1.4 (×1.2 a ×0.8 si es élite)**

**Resistencia al lanzamiento: Peso alto (100)**

**Daño: Por definir durante el balance**

**Defensas: Escudo y contraataque con la porra**

**Velocidad: Media-baja**

**Rango de detección: No aplica: siempre sabe dónde está el jugador**

**Ataques: Combo con porra, estocada, giro con la porra, contraataque, agarres y lanzamientos**

**Debilidades: Es más lento que el guardia y el antidisturbios**

**Recompensa: De 0 a 10 monedas (el doble si es élite)**

**Aparición: Desde el piso 2, cada vez con más frecuencia**



### Nombre: Guardia Pesado

**Rol de combate: Tanque pesado / Fuerza bruta**

**Comportamiento: Disfruta el enfrentamiento físico. Persigue implacablemente e intenta arrinconar al jugador. En los pisos normales solo aparece como élite; también puede salir en las oleadas que invoca el jefe**

**Porcentaje de daño: Comienza en 0% y aumenta al recibir golpes. Cuanto mayor sea, mayor será el retroceso recibido**

**Vidas: 1. Queda eliminado al salir de los límites del escenario**

**Susceptibilidad al daño: ×1.2 en los primeros pisos, hasta ×0.8 (siempre es élite)**

**Resistencia al lanzamiento: Es el enemigo más pesado (116)**

**Daño: Alto**

**Defensas: Escudo y un contraataque ("venganza") que devuelve el golpe recibido**

**Velocidad: Baja: es el enemigo más lento del juego**

**Rango de detección: No aplica: siempre sabe dónde está el jugador**

**Ataques: Lariats, golpe cruzado, golpes demoledores, agarres y lanzamientos**

**Debilidades: Es el enemigo más lento (camina a la mitad de velocidad que un guardia), así que se le puede rodear y alejar con facilidad**

**Recompensa: De 0 a 20 monedas (doble por ser élite) y el boon que lleva equipado**

**Aparición: Desde el piso 3, solo como élite**



### Nombre: Dron

**Rol de combate: Enemigo volador / Ataque a distancia**

**Comportamiento: Vuela a cierta altura, mantiene la distancia con el jugador y le dispara un láser después de cargarlo**

**Porcentaje de daño: Comienza en 0% y aumenta al recibir golpes. Al llegar a 100 % se rompe y cae destruido**

**Vidas: 1. Queda eliminado al romperse o al salir de los límites del escenario**

**Susceptibilidad al daño: ×2.0 en los primeros pisos, hasta ×1.4**

**Resistencia al lanzamiento: Peso bajo (80)**

**Daño: Por definir durante el balance**

**Defensas: Ninguna**

**Velocidad: Media**

**Rango de detección: Largo: dispara desde lejos**

**Ataques: Láser cargado**

**Debilidades: Se rompe al llegar a 100 % y es ligero**

**Recompensa: De 0 a 10 monedas**

**Aparición: Desde el piso 2. Máximo 3 drones por piso**



### Nombre: Dron kamikaze

**Rol de combate: Enemigo volador / Embestida explosiva**

**Comportamiento: Vuela hacia el jugador, se arma (su luz parpadea), se lanza contra él y explota**

**Porcentaje de daño: Comienza en 0% y aumenta al recibir golpes. Al llegar a 100 % se rompe y cae destruido**

**Vidas: 1. Queda eliminado al romperse, al explotar o al salir de los límites del escenario**

**Susceptibilidad al daño: ×2.0 en los primeros pisos, hasta ×1.4**

**Resistencia al lanzamiento: Peso bajo (80)**

**Daño: Por definir durante el balance**

**Defensas: Ninguna**

**Velocidad: Alta al lanzarse**

**Rango de detección: Medio**

**Ataques: Embestida y explosión**

**Debilidades: Avisa antes de lanzarse; se rompe al llegar a 100 %**

**Recompensa: De 0 a 10 monedas**

**Aparición: Desde el piso 3, como parte de los drones del piso**

## Enemigos

Los enemigos cambian según la compañía. Pueden ser humanos o robots, según la empresa. Entre empresas, el moveset es prácticamente el mismo; lo que cambia es la apariencia y el estilo.

| Enemigo de Nuddle | Variante | Descripción |
| --- | --- | --- |
| **Guardia** | Débil | Enemigo básico, aparece en grandes cantidades. |
| **Antidisturbios** | Media | Pelea cuerpo a cuerpo y agarra. |
| **Antidisturbios con porra** | Media | Pelea con porra y contraataques. |
| **Guardia pesado** | Fuerte | **Guardia muy musculoso**, que aparenta ser demasiado fuerte. En los pisos normales solo aparece como élite. |
| **Dron** | Robot | Vuela y dispara un láser a distancia. |
| **Dron kamikaze** | Robot | Se lanza contra el jugador y explota. |

> [!note] ✏️ Alcance de la entrega
> Por ahora solo se desarrollan los enemigos de **Nuddle**. El jefe, Mr. Big Data, aparece cada 50 pisos, tiene una barra de vida en lugar de porcentaje y, durante el combate, invoca oleadas de guardias, antidisturbios, guardias pesados y drones (ver [[03 - Personajes]]). Al derrotarlo, el jugador recibe monedas.

## Plantilla de NPC

**Nombre:** Tendero de Café Corp (siempre es el mismo personaje)

**Función:** Atiende la tienda Café Corp, donde se venden boons nuevos y mejoras de boons.

**Ubicación:** Tiendas cada 10 pisos y en el piso anterior a cada jefe: 10, 20, 30, 40, 49, 60, 70, 80, 90, 99…

**Interacción:** Habla solo, con globos de texto, cuando el jugador se acerca al mostrador. Al usar el mostrador ("COMPRAR") se abre la tienda.

**Diálogos:** Frases cortas y humorísticas sobre su trabajo, su cansancio y su jefe. Tiene frases para saludar, abrir la tienda, ver un producto, agradecer una compra, avisar que no alcanza el dinero, que un producto está agotado o que ya no queda nada, despedirse y cuando el jugador se va rompiendo el techo.

**Condiciones:** El jugador llega a un piso con tienda.

**Recompensas / información:** Sus diálogos no cuentan la historia; solo dan ambiente y humor.

> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →
