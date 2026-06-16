---
layout: page
title: "Drones con instinto de supervivencia: cómo la robótica de bajo costo está aprendiendo a ver sin GPS"
published: false
---

<iframe width="100%" height="450" src="https://www.youtube.com/embed/eo8WHMkEv20?si=E72O-OoP2nn9gCHI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="100%" height="450"
src="https://www.youtube.com/embed/eo8WHMkEv20"
title="YouTube video player"
frameborder="0"
allowfullscreen>
</iframe>

Imagine un escenario devastador: un sismo de gran magnitud ha sacudido la ciudad y un edificio antiguo presenta daños estructurales graves. Enviar a un equipo de rescatistas al interior para inspeccionar grietas y muros es una sentencia de riesgo incalculable.

En ese momento crítico, los drones parecen la solución ideal, pero al cruzar el umbral de la puerta, se enfrentan a un "muro tecnológico" invisible: la pérdida de la señal GPS. Sin conexión satelital, los drones convencionales pierden su sentido de ubicación global y se vuelven "ciegos" para la navegación autónoma.

Históricamente, resolver este problema ha requerido equipar a las máquinas con sensores láser LiDAR y procesadores de alto rendimiento, lo que incrementa drásticamente el peso y el costo del equipo. Ante este panorama, surge una pregunta que desafía el statu quo de la industria: ¿Es posible que un dron navegue en el caos de un edificio colapsado usando solo una cámara barata y matemáticas inteligentes?

### Algoritmos: El nuevo "acero" de la robótica accesible

La robótica avanzada suele asociarse con presupuestos de ciencia ficción, pero la investigación liderada por expertos en México está demostrando que es posible "hacer más con menos".

Al utilizar drones comerciales estándar, como el Parrot Bebop 2 —equipado únicamente con una cámara frontal básica—, los investigadores han trasladado la complejidad del hardware al software. Este enfoque representa un acto de democratización tecnológica sin precedentes. La verdadera magia ocurre fuera del dron: todo el procesamiento de datos se realiza de forma inalámbrica a través de una computadora portátil común.

Al eliminar la necesidad de un superordenador a bordo o sensores militares costosos, se abre la puerta para que instituciones de protección civil en países en vías de desarrollo tengan acceso a herramientas de inspección autónoma de alto nivel. El avance en algoritmos matemáticos puede suplir la necesidad de hardware costoso, transformando un equipo comercial en una herramienta capaz de proteger vidas humanas.

### Reflejos contra mapas: La rebelión del visual servoing

La robótica clásica es, a menudo, ineficiente por exceso de precaución: intenta que las máquinas escaneen su entorno para crear mapas tridimensionales perfectos, un proceso que devora energía y tiempo. Sin embargo, este desarrollo propone un cambio de paradigma: el "control visual" (visual servoing).

En lugar de construir un mapa pesado, el dron utiliza la imagen 2D de su cámara para ajustar sus motores en tiempo real. Es, en esencia, dotar al robot de reflejos. Piense en cómo camina usted por un pasillo: no necesita calcular conscientemente la distancia exacta en centímetros hasta una caja en el suelo ni trazar un mapa mental trigonométrico; sus ojos detectan el obstáculo y sus piernas reaccionan para rodearlo mientras su mirada permanece fija en la salida.

El dron hace exactamente lo mismo: reconoce rasgos visuales y ajusta su trayectoria para que lo que ve coincida con su "imagen objetivo".

<br>

> 🎧 **¿PREFIERES ESCUCHAR ESTA HISTORIA?** [**DALE PLAY A NUESTRO PODCAST AQUÍ**](https://youtu.be/5IyC9q6n5Q0?si=FJgLBElnh1HzwY1Y)

<br>

### Supervivencia programada: Las tres leyes del instinto robótico

Para evitar que el procesador se sature ante la impredecibilidad del mundo real, se ha implementado un esquema de control jerárquico. Este sistema prioriza las tareas siguiendo una lógica biológica de supervivencia, donde lo más importante es mantener la integridad del equipo:

1. **Prevención de colisiones:** Es la prioridad absoluta. Si la cámara detecta que un objeto se acerca a un límite crítico, el algoritmo interrumpe cualquier orden para priorizar la evasión.
2. **Visibilidad:** El dron debe asegurar que no perderá de vista su meta. Si al esquivar un objeto el objetivo está por salir del encuadre, el dron rota su cámara para no perder el horizonte visual.
3. **Avance hacia la meta:** Es el objetivo final, pero solo se ejecuta si las dos reglas anteriores (no chocar y no perder el rumbo) están garantizadas.

Este enfoque es mucho más eficiente que el procesamiento de datos puro, permitiendo que el robot "sobreviva" a entornos complejos con una fracción de la potencia computacional tradicional.

![Infografía Resumen](https://drcarlostoroarcila.github.io/recursos/ojos-en-el-aire/infografia_vertical.png)

### Del laboratorio al mundo real: El baile entre columnas

La validez de estas ecuaciones se puso a prueba en un entorno de "fuego real" con obstáculos físicos. Durante los experimentos, se colocaron columnas invasoras en la trayectoria de un Parrot Bebop 2.

Los resultados confirmaron la agilidad del sistema: al detectar una columna en su camino, el dron redujo suavemente su velocidad frontal y aumentó su velocidad lateral para deslizarse con agilidad por un costado, rodeando el obstáculo sin detenerse. Un aspecto clave para lograr este vuelo fluido fue el uso de retroalimentación anticipada (feed-forward). Cuando el camino está despejado, este componente permite que el dron se desplace con mayor rapidez y naturalidad, optimizando el tiempo de llegada al destino sin sacrificar la seguridad de la misión.

### Tecnología con rostro humano: Rescate y Protección Civil en México

Este avance no es solo un logro académico; es una respuesta directa a problemas nacionales de seguridad e inspección. En un país como México, donde los presupuestos para emergencias suelen ser limitados, la capacidad de explorar edificios siniestrados o naves industriales utilizando drones comprados en tiendas de electrónica tiene un valor incalculable.

Permite que las brigadas de Protección Civil locales, que a menudo carecen de equipos de grado militar, cuenten con aliados autónomos para misiones de alto riesgo. La apropiación social de este conocimiento es el fin último de la innovación: convertir la tecnología de punta en una herramienta de seguridad pública accesible para todos. "La investigación científica cobra su verdadero valor cuando demuestra tener la capacidad de mejorar nuestra sociedad".

### Conclusión y Reflexión Final

La transición de drones que dependen de satélites a robots que "entienden" visualmente su entorno marca un hito en la robótica accesible. Hemos pasado de máquinas que requieren mapas perfectos a sistemas que operan con instinto y reflejos, demostrando que la inteligencia matemática es, a menudo, más poderosa que el hardware más caro.

¿Estamos listos para un futuro donde los primeros en entrar a una zona de desastre no sean humanos, sino una flota de robots autónomos de bajo costo trabajando codo a codo con nuestras brigadas de rescate? La tecnología ya está aquí; el siguiente paso es verla volar allí donde más se necesita salvar una vida.

---

## 📚 Recursos Académicos Descargables
* 📥 [Descargar Presentación de Diapositivas (PDF)](https://drcarlostoroarcila.github.io/recursos/ojos-en-el-aire/presentacion.pdf)
* 🗺️ [Descargar Mapa Mental de Estudio (PNG)](https://drcarlostoroarcila.github.io/recursos/ojos-en-el-aire/mapa_mental.png)
* 📊 [Descargar Infografía Panorámica (PNG)](https://drcarlostoroarcila.github.io/recursos/ojos-en-el-aire/infografia_horizontal.png)

---

**🔬 Acerca de esta investigación:**
Esta entrada de blog está basada en la investigación original revisada por pares y publicada en la revista científica internacional *Control Engineering Practice* ([Haz clic aquí para leer el artículo JCR completo](https://doi.org/10.1016/j.conengprac.2023.105493)). Un artículo extendido de divulgación científica se encuentra actualmente en revisión por el comité editorial de la revista *CienciaCierta* de la UAdeC. Esta labor de divulgación es parte del esfuerzo por el Acceso Universal al Conocimiento, con el apoyo del SECIHTI (antes CONACYT) y la Universidad Autónoma de Coahuila.
