# Dirección de Arte

## Descripción de la sección

Define la identidad visual del videojuego y las reglas que deben seguir los recursos gráficos.

## Identidad visual

**Estilo:**
Estética de anime y animación de acción indie, con personajes expresivos y un acabado visual limpio y sombreado plano tipo cel-shading. 

El juego se presenta en **2.5D**, con desplazamiento lateral y escenarios que muestran profundidad. Su mundo corresponde a un futuro cercano de apariencia moderna, compuesto por oficinas, vestíbulos, pasillos y otros espacios empresariales reconocibles.

**Referencias:**
![[WhatsApp Image 2026-10-16 at 12.29.57 PM.jpeg|366]]
![[20261016_070750.jpg.jpeg]]

**Sensación buscada:**
Acción enérgica, rebeldía y determinación. Los protagonistas deben ser el foco de las escenas de combate, los enemigos deben comunicar oposición y amenaza mediante su silueta, equipo y diferencia de tamaño.

**Nivel de realismo:**
Caricaturesco y estilizado, con anatomía simplificada y expresiva.

**Formas predominantes:**
Combinación de curvas y ángulos. Las curvas se usan en rostros, anatomía, cabello y prendas; los ángulos definen articulaciones, pliegues, protecciones y equipo. Los enemigos se distinguen por su silueta: tamaño, anchura, postura y equipamiento.

**Iluminación:**
El acabado gráfico utiliza sombras sólidas de bordes nítidos. Se evitan degradados como recursos de sombreado.

**Materiales:**
El juego usa shaders propios de sombreado plano tipo cel-shading (por ejemplo, `SpriteToon` y el material "toon"). Además, tiene activo un filtro de render llamado "Pixel Art": la imagen se dibuja a baja resolución (270 píxeles de alto) y después se agranda, con los colores reducidos a 11 niveles y contornos automáticos en los bordes de los modelos, lo que da un aspecto de pixel art.
## Paleta de color

**Colores principales:**
Azul noche y morados (violeta y morado grafiti) para fondos y menús, con crema y amarillo para el texto.

**Colores secundarios:**
Naranja, rojo y carmesí.

**Colores para información jugable:**
- **Blanco:** destello del personaje golpeado y destellos localizados en el contacto de los golpes.
- **Rojo:** pulso del personaje con 100 %, 125 % y 150 % o más de daño, y escudo del jugador.
- **Amarillo:** parpadeo al cargar un ataque fuerte y parpadeo del estado de electricidad.
- **Cian:** destello del parry y número de porcentaje de los enemigos élite.
- **Azul claro:** estado de congelación (el personaje queda teñido por completo) y escudo de los enemigos.
- **Morado:** parpadeo del estado de lentitud.
- **Naranja:** parpadeo del estado de quemadura y estela de los lanzamientos fuertes.
- **Verde:** parpadeo del estado de veneno.
- **Rosa:** parpadeo del estado de enamorado.
- **Dorado:** borde de los enemigos élite.
- **Rareza de los boons:** gris lila (común), azul (rara), morado (épica) y ámbar (legendaria).
- **Porcentaje de daño:** el número cambia de color según el daño: crema en 0 %, amarillo en 50 %, naranja en 100 %, rojo en 150 % y carmesí en 300 %.

El color se acompaña de formas, símbolos o texto para comunicar estados.

## Reglas visuales

1. **Mantener una estética anime coherente.**  
    Todos los personajes deben compartir un tratamiento consistente de línea, sombreado y simplificación anatómica. Los ojos expresivos, los rasgos faciales definidos y el cabello organizado en mechones forman parte del lenguaje visual común.
    
2. **Respetar la individualidad de cada protagonista.**  
    Cada personaje debe distinguirse mediante su silueta, complexión, facciones, peinado, vestimenta, accesorios y actitud. La variedad debe expresar su personalidad y su estilo de combate, conservando la coherencia gráfica del conjunto.
    
3. **Conservar la jerarquía del trazo.**  
    Los contornos exteriores tendrán mayor peso visual que los detalles internos. Las líneas deben ser limpias y definidas, con un grosor adecuado para reconocer al personaje durante el juego. Las facciones, los pliegues y los accesorios utilizarán líneas más finas para evitar una apariencia sobrecargada.
    
4. **Construir el volumen mediante formas y sombras claras.**  
    El sombreado tipo _cel-shading_ debe utilizar bloques de luz y sombra que permitan comprender el volumen. Se evitarán las texturas fotográficas, la musculatura excesivamente detallada y los efectos difuminados que dificulten la lectura. Los brillos de ojos, cabello y materiales deberán mantener un tratamiento estilizado y consistente.
    
5. **Combinar curvas y ángulos con intención.**  
    Las curvas pueden utilizarse en rostros, anatomía, cabello y prendas, mientras que los ángulos ayudan a definir articulaciones, pliegues, protecciones y equipo. Las formas deben responder al diseño de cada personaje y conservar una construcción clara, sin exigir que toda la anatomía sea angular.
    
6. **Simplificar el cabello en mechones reconocibles.**  
    El cabello se organizará en masas y mechones definidos que describan su volumen, dirección y textura. Cada peinado tendrá una silueta propia. Se evitará dibujar cabellos individuales en exceso o añadir detalles que desaparezcan a la escala de juego.
    
7. **Mantener proporciones y anatomía consistentes.**  
    La altura, el tamaño de la cabeza, la longitud de las extremidades y la complexión deben conservarse entre vistas y poses de un mismo personaje. Las manos y el calzado deben adaptarse a la perspectiva y al movimiento. Las proporciones concretas se establecerán en las hojas de personaje, permitiendo diferencias entre protagonistas y enemigos.
    
8. **Comunicar la identidad corporativa mediante uniformidad.**  
    Los enemigos tendrán una apariencia anime rígida y ordenada, con repetición de uniformes, protecciones y elementos de equipo. Su paleta será gris casi monocromática para expresar frialdad, despersonalización y pertenencia a una organización opresiva.
    
9. **Diferenciar los tipos de enemigo mediante su silueta.**  
    Los guardias débiles, medios y pesados deben reconocerse por su tamaño, anchura, postura y equipamiento. La uniformidad corporativa debe permitir identificar claramente cada amenaza, incluso cuando los enemigos compartan colores similares.
    
10. **Utilizar el color con una jerarquía clara.**  
    Los protagonistas tendrán identidades cromáticas propias. En cada escena se utilizarán hasta tres colores dominantes, acompañados de neutros y acentos controlados. Este límite se refiere a la composición general y permite conservar los colores particulares de personajes, efectos e información jugable.
    
11. **Priorizar la lectura del combate.**  
    La composición, el contraste y la iluminación deben destacar al personaje jugable y las amenazas inmediatas. Los detalles del fondo y los efectos visuales deben permitir reconocer las poses, la dirección de los ataques y los puntos de contacto.

## Referencias

Añade enlaces o imágenes dentro de la carpeta del proyecto.

- Imágenes de referencia de la sección **Identidad visual**.
- Imágenes de personajes: [[Poster_promocional.png]], [[Mr_Wobbles.png]], [[Atsuko.png]] y [[Craub.png]].
- Estética anime y cel-shading en [[02 - Referencias e Inspiración]].


> **Navegación:** [[00 - Índice]] · ← [[05 - Misiones y Desafíos]] · [[02 - Personajes y Animación]] →
