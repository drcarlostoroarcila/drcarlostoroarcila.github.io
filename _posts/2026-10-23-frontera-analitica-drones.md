---
layout: default
title: "Evasión Reactiva de Obstáculos en Drones mediante Fronteras Analíticas"
date: 2026-10-23 10:00:00 -0600
published: true
---

# Evasión reactiva de obstáculos en el control visual de drones (UAV): un enfoque de frontera de seguridad analítica
**Dr. Carlos A. Toro-Arcila | Publicado el 23 de octubre de 2026**

[⬅️ Volver a la página principal](https://drcarlostoroarcila.github.io/)

<br>

<div style="text-align: justify;" markdown="1">

> 🎥 **¿QUIERES VER LA EXPLICACIÓN EN ESPAÑOL?** [**HAZ CLIC AQUÍ PARA VER EL VIDEO EN YOUTUBE**](https://youtu.be/jiW2qZTwKH4)

<br>

> 💻 **¿BUSCAS LAS PRUEBAS TÉCNICAS EN EL SIMULADOR?** [**VER VIDEO SUPLEMENTARIO EN COPPELIASIM (INGLÉS)**](https://youtu.be/jTn9dnSvutU)

<br>

La navegación autónoma de vehículos aéreos no tripulados (UAV) en entornos sin señal GPS depende frecuentemente del control visual basado en imagen (IBVS). Sin embargo, esta técnica presenta una vulnerabilidad fundamental: requiere que el objetivo visual se mantenga dentro del campo de visión (FOV) de la cámara. Si el objetivo se pierde de vista debido a una maniobra brusca al esquivar un obstáculo, la misión de control visual fracasa.

En esta entrada presento los fundamentos matemáticos y los resultados de simulación de mi más reciente artículo de investigación, publicado en la revista científica *International Journal of Aeronautical and Space Sciences* (Springer). En este trabajo, desarrollé y validé una frontera de seguridad geométrica analítica diseñada para superar las limitaciones operativas de los métodos reactivos clásicos.

### El problema de la resintonización manual en métodos clásicos

Tradicionalmente, la evasión reactiva de obstáculos se aborda mediante algoritmos como los campos potenciales artificiales (APF). Aunque funcionales en teoría, estos métodos operan mediante márgenes de seguridad estáticos o heurísticos.

Su principal limitación operativa es que **exigen resintonización manual**: cada vez que cambia alguna variable del entorno (como el diámetro del obstáculo), se modifica el hardware (un lente con distinto campo de visión) o se alterna la tarea de navegación principal, un operador humano debe intervenir y recalibrar manualmente las ganancias matemáticas del controlador. Además, al emplear márgenes heurísticos, suelen reaccionar con rodeos excesivos que empujan al objetivo fuera del campo de visión de la cámara.

### La contribución científica: Ecuación analítica de 3 parámetros

Para eliminar esta dependencia operativa, formulé una **frontera de seguridad geométrica analítica** que calcula en línea (en tiempo real) la distancia mínima exacta a la cual el dron debe iniciar su maniobra de evasión frente a un obstáculo estático.

La eficiencia computacional de esta ecuación radica en que no requiere recalibración manual y depende exclusivamente de tres parámetros:
1. **El radio físico del vehículo aéreo** (valor fijo y conocido).
2. **El ángulo del campo de visión de la cámara / FOV** (valor fijo y conocido).
3. **El radio del obstáculo** (estimado y actualizado en línea mediante el sensor de profundidad).

<br>

> 🎧 **¿PREFIERES ESCUCHAR EL ANÁLISIS EN AUDIO?** [**DALE PLAY AL EPISODIO 4 DEL PODCAST AQUÍ**](https://youtu.be/70hlYz532gs)

<br>

### Independencia operativa y consecuencia cinemática favorable

Al fundamentarse en relaciones geométricas directas entre las dimensiones físicas de los agentes y los límites ópticos del sensor, la formulación requiere sintonizarse una única vez. A través de un análisis paramétrico riguroso, comprobé que el sistema actúa como una capa de seguridad modular e independiente en tres niveles:
* **Independiente del hardware óptico:** Se adapta de forma autónoma a cámaras teleobjetivo (45°), sensores de profundidad estándar (69°) y lentes gran angular (110°).
* **Independiente de las dimensiones del entorno:** Ajusta dinámicamente la frontera de seguridad ante obstáculos de distinto radio.
* **Independiente de la tarea primaria:** Al proyectar la tarea secundaria en el espacio nulo del obstáculo mediante una función de activación continuamente diferenciable, opera con estabilidad tanto en seguimiento visual (IBVS) como en control de pose basado en coordenadas.

Respecto a la visibilidad del objetivo, es importante precisar desde el punto de vista de la teoría de control que mantener el objetivo en pantalla no se impone como una restricción rígida ni como una tarea dedicada. Más bien, al calcular la desviación lateral *estrictamente necesaria* para librar el obstáculo, el controlador evita maniobras evasivas exageradas; como **consecuencia geométrica directa y favorable** de esta trayectoria ajustada, se reduce significativamente el riesgo de perder de vista el objetivo principal.

![Resumen Gráfico Frontera Analítica](https://drcarlostoroarcila.github.io/recursos/frontera-analitica/infografia_vertical.png)

### Validación mediante simulaciones dinámicas de alta fidelidad

El marco teórico —respaldado por análisis de estabilidad de Lyapunov y conjuntos positivamente invariantes a nivel cinemático— fue evaluado mediante **simulaciones dinámicas de alta fidelidad** bajo una arquitectura *Software-in-the-Loop (SITL)* en el motor físico CoppeliaSim. 

Implementado íntegramente en C++ con OpenCV sobre un equipo de cómputo comercial, el algoritmo completo (incluyendo el filtrado espacial de nube de puntos 3D y la proyección en el espacio nulo) requirió un tiempo de ejecución de apenas **1.5 a 6.0 milisegundos por iteración**, consumiendo como máximo el 12% del ciclo de control de 50 ms. Estos resultados en simulación confirman su viabilidad computacional y establecen un marco cinemático confiable como base metodológica previa a su futura integración experimental en plataformas físicas.

---

## 📚 Recursos académicos descargables
* 📥 [Descargar Presentación Académica (PDF)](https://drcarlostoroarcila.github.io/recursos/frontera-analitica/presentacion.pdf)
* 🗺️ [Descargar Mapa Mental de la Metodología (PNG)](https://drcarlostoroarcila.github.io/recursos/frontera-analitica/mapa_mental.png)
* 📊 [Descargar Resumen Gráfico Panorámico (PNG)](https://drcarlostoroarcila.github.io/recursos/frontera-analitica/infografia_horizontal.png)

---

**🔬 Autoría y Publicación Científica:**
La propiedad intelectual, la formulación matemática y la arquitectura de simulación expuestas en este trabajo son de la autoría exclusiva del **Dr. Carlos A. Toro-Arcila** (Profesor-Investigador en la Facultad de Ingeniería de la Universidad Autónoma de Coahuila, UAdeC). 

La investigación original revisada por pares se encuentra publicada en la revista internacional *International Journal of Aeronautical and Space Sciences* (Springer):
* 📖 [**Leer el artículo JCR completo sin costo (Enlace oficial Springer SharedIt)**](https://rdcu.be/UvGg8WctMYha)
* 🔗 [**Enlace DOI oficial**](https://doi.org/10.1007/s42405-026-01310-8)

*Nota de Transparencia Tecnológica (SNII):* La investigación científica, las demostraciones matemáticas y el código de simulación son de completa autoría intelectual del Dr. Carlos A. Toro-Arcila. Con fines de comunicación pública de la ciencia, la maquetación de los recursos gráficos y audiovisuales complementarios contó con la asistencia de herramientas de Inteligencia Artificial bajo la estricta supervisión, edición y curaduría técnica del autor.

</div>

<br>
[⬅️ Volver a la página principal](https://drcarlostoroarcila.github.io/)
<br><hr><br>

### 💬 Déjame tu opinión o dudas técnicas sobre esta investigación:

<!-- Contenedor Giscus -->
<div class="giscus"></div>
<script src="https://giscus.app/client.js"
        data-repo="drcarlostoroarcila/drcarlostoroarcila.github.io"
        data-repo-id="R_kgDOS7uaRg"
        data-category="Announcements"
        data-category-id="DIC_kwDOS7uaRs4C_Rkp"
        data-mapping="title"
        data-strict="0"
        data-reactions-enabled="1"
        data-emit-metadata="0"
        data-input-position="top"
        data-theme="light"
        data-lang="es"
        crossorigin="anonymous"
        async>
</script>

<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-HD8EZRESGW"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-HD8EZRESGW');
</script>
