# Segundo parcial DISEÑO DE INTERFAZ Y EXPERIENCIA DE USUARIO (UX/UI) – FIDAE 2026

## 1. Objetivo del sitio web

El propósito fundamental de la plataforma web offline para la Feria Internacional del Aire y del Espacio *(FIDAE 2026)* es consolidar un ecosistema digital centralizado que funcione de manera óptima en entornos locales, garantizando la difusión institucional del evento como tambien la accesibilidad de la información.

+ Los objetivos estratégicos del sitio se desglosan en tres pilares técnico
	* **Difusión y Posicionamiento Sectorial:** Actuar como el vector principal de comunicación visual de la feria, proyectando una identidad corporativa aeroespacial sólida y profesional mediante la exposición de expositores y evetos o actividades del mismo.
	
	* **Accesibilidad Eficiente del Cronograma:** Proveer una consulta ágil, intuitiva y jerarquizada de las exhibiciones aéreas, conferencias comerciales y demostraciones, asegurando que el usuario local acceda a la planificación horaria sin fricciones ni dependencias de conectividad externa.
	
	* **Simulación Transaccional de Tickets:** Implementar un flujo de conversión simulado mediante componentes de formularios interactivos para la adquisición de pases y boletos de ingreso, validando la lógica frontend y reduciendo la carga cognitiva del usuario en la experiencia pre-evento.
	
## 2. Bechmarjing Competitivo

Para validar el maquetado y las decisiones de diseño del proyecto, se realizó un análisis comparativo simulado frente al estándar de la industria, tomando como referencia el sitio institucional histórico de la **FIDAE** y estructuras homólogas como la **Feria Aeroespacial México (FAMEX).**

| Variables de Diseño / UX | Estandar real del sector (Sitios oficiales) | Interfaz propuesta en el repositorio (FIDAE 2026) |
| ------------ | ------------ | ------------ |
| **Arquitectura tecnológic**a | Dependencia crítica de scripts de servidores externos (CDNs), APIs dinámicas y bases de datos en la nube. | Arquitectura estática *offline* basada en HTML5, CSS y el framework Bootstrap cargado de manera estrictamente local. 
| **Navegación e Interfaz** | Menús masivos (Megamenús) con múltiples niveles que sobrecargan al usuario no corporativo.| Estructura simplificada de navegación lineal de cuatro páginas principales orientada al flujo de de información mas rápida y de facil acceso.
| **Rendimiento Local** | Latencia variable y degradación total de la UI en caso de pérdida de conectividad a internet. | Tiempo de respuesta inmediato e inmunidad a la pérdida de red gracias a activos locales precomprimidos.
| **Inclusión Transaccional** | Redirección a pasarelas bancarias externas complejas y formularios multi-paso extensos. | Simulación directa en una sola pantalla (*Ticket.html*) mediante una interfaz limpia y estructurada por secciones visuales.

### Buenas Prácticas Adoptadas en el Maquetado:
+ **Autonomía Tecnológica Absoluta:** Al integrar las hojas de estilo de Bootstrap de forma local (`/css/bootstrap.min.css`), el diseño responsive y el sistema de grillas operan de forma óptima sin peticiones HTTP externas.

+ **Estandarización de Componentes:** Uso coherente de la biblioteca de componentes nativos del framework (Cards, Navbars, Buttons) que garantizan una consistencia visual unificada a lo largo de todas las pantallas, reduciendo el esfuerzo de desarrollo y diseño.

+ **Estructura Semántica Limpia:** Separación estricta entre la semántica del documento (HTML5) y la presentación visual, asegurando un mantenimiento ágil del código de la interfaz aeroespacial.

## 3. Arquitectura de la Información
La organización, estructuración y jerarquización del contenido se diseñaron para minimizar el número de clics requeridos para completar las tareas críticas del usuario. La navegación utiliza un modelo plano y directo compuesto por 4 nodos principales que se enlazan de forma transversal a través de un menú de navegación global superior

### Detalle de las Páginas Principales:
+ **Home (`Home.html`):** Actúa como el hub de entrada y la página de aterrizaje (landing page). Presenta la propuesta de valor de la FIDAE 2026, un resumen visual de alto impacto (Hero Section) con estética aeronáutica y accesos directos hacia las secciones críticas del sitio.

+ **Excibitions (`Excibitions.html`):** Sección dedicada a la visualización de los pabellones, aeronaves en exposición y empresas participantes. El contenido está estructurado visualmente mediante una cuadrícula de tarjetas (Cards) de Bootstrap que segmenta la información técnica y de entretenimiento.

+ **Calendar (`Calendar.html`):** Pantalla operativa y funcional del cronograma. Organiza los bloques horarios de los espectáculos aéreos, conferencias aeroespaciales y demostraciones de vuelo mediante tablas estructuradas cronológicamente, permitiendo al usuario planificar su jornada cronometrada.

+ **Ticket (`Ticket.html`):** Sección que contiene el formulario interactivo de reserva y simulación de compra de boletos. Está diseñado en una zona de foco único para maximizar la tasa de la tarea de registro.

#### Niveles de Navegación:
+ **Nivel 1 (Navegación Global):** Accesible desde cualquier pantalla mediante un elemento `navbar` principal de Bootstrap en el encabezado. Contiene los enlaces directos a: Inicio, Exhibiciones, Cronograma y Tickets.

**Nivel 2 (Navegación Contextual/Interna):** Enlaces internos integrados en botones de llamada a la acción (`btn-primary`) que dirigen dinámicamente al usuario desde la descripción de una exhibición o banner en la *Home* directamente hacia el formulario de *Tickets* o el *Calendar*, agilizando el flujo de conversión del usuario.


## 4. Arquetipo de Persona
Para guiar las decisiones estéticas, de usabilidad y de diseño de interfaces del proyecto, se estructuró el siguiente perfil que representa el segmento de audiencia objetivo principal: 


### Perfil de Usuario Tipo: Alejandro Torres 
+ **Datos Demográficos:** * Edad: 28 años.
	* **Ocupación:** Ingeniero en Sistemas y Entusiasta de la Aviación Civil y Militar.
	* **Ocupación:** Ingeniero en Sistemas y Entusiasta de la Aviación Civil y Militar.

+ **Objetivos y Motivaciones al ingresar a la Web:**
	* Localizar con precisión quirúrgica los horarios específicos de las pasadas de los jets de combate y las demostraciones de acrobacias aéreas para planificar su llegada a la base aérea.
	
	* Conocer de antemano la distribución de las aeronaves en la muestra estática para optimizar su recorrido fotográfico.
	 
	* Simular el proceso de cotización y reserva de entradas comerciales para entender los precios por categoría (General, Niño, Profesional) y requisitos de acceso.

+ **Frustraciones y Puntos de Dolor en Sitios Competidores:**
	* Sitios web sobrecargados de banners institucionales irrelevantes que ocultan los horarios de los vuelos.
	
	* Interfaces que sufren caídas de rendimiento o errores de carga de archivos CSS debido a la saturación de las redes de telefonía móvil dentro del predio de la feria.
	
	* Formularios de compra excesivamente largos que exigen crear una cuenta antes de mostrar los valores reales de las entradas.
	

### Justificación de Decisiones de Diseño Tomadas para este Arquetipo:

1. **La sección *Calendar.html*** utiliza un maquetado limpio y tabular: Esto permite que un usuario orientado a datos y tiempos como Alejandro encuentre instantáneamente la hora exacta del bloque de vuelo que le interesa sin navegar por bloques densos de texto.

2. **Implementación de Arquitectura Local Offline**: Al optimizar los estilos CSS y componentes de Bootstrap localmente, se garantiza que si Alejandro consulta la interfaz desde un dispositivo móvil en un entorno simulado de baja conectividad dentro del evento, la interfaz responderá de forma imediata

3. **Formulario unificado en *Ticket.html*:** Se eliminó la fricción de registros obligatorios previos; el usuario respondiendo a su frustración frente a flujos burocráticos.


## 5. Leyes y Estándares de UX Utilizados
El diseño de la interfaz del proyecto FIDAE 2026 fundamenta la disposición de sus componentes visuales de la experiencia de usuario, garantizando un entorno digital predecible y de baja fricción:


**Ley de Hick (Tiempo de Toma de Decisiones)**

+ **Aplicación en el sitio:** En la pantalla simulada de boletos (`ticket.html`), el formulario de contacto y selección, está fragmentado visualmente mediante divisiones claras, agrupando los campos de datos personales. Se restringen los campos estrictamente a los necesarios para la simulación (Nombre, Apellido, Correo, País proveniente).

+ **Justificación técnica:** El tiempo que se tarda en tomar una decisión aumenta con el número y la complejidad de las opciones. Al delimitar el formulario al mínimo número de campos a completar y ordenarlo de forma lineal, se reduce exponencialmente la carga cognitiva del usuario, agilizando el flujo operativo de registro.


**Ley de Tesler (Ley de la Conservación de la Complejidad)**

+ **Aplicación en el sitio:** En el módulo (`ticket.html`), la complejidad de una reserva de entradas aeronáuticas (cálculo de categorías, impuestos y procesamiento) ha sido asumida por el diseño de la interfaz y la lógica interna del frontend. Al usuario solo se le presentan selectores preconfigurados (inputs tipo select y text) que ocultan la lógica interna, eliminando la necesidad de ingresar datos redundantes o realizar cálculos manuales de tarifas según el tipo de región.

+ **Justificación técnica:** Esta ley establece que todo sistema posee una cantidad de complejidad inherente que no puede ser reducida, por lo que la única opción es decidir si la asume el sistema o el usuario. En esta interfaz, la complejidad ha sido absorbida por completo por la estructura del maquetado y los componentes de Bootstrap, permitiendo al usuario realizar una simulación fluida sin lidiar con la fricción del procesamiento de datos complejo.


**Ley de Fitts (Accesibilidad y Objetivos de Clic)**

+ **Aplicación en el sitio:** Los botones de llamada a la acción (CTA) críticos —tales como el botón de confirmación en el formulario de compra (`ticket.html`) y los botones de redirección hacia el cronograma en la Home— han sido dimensionados de forma prioritaria utilizando las clases de escalado de Bootstrap (`.btn-lg`, `.w-100` o bloques de botones expandidos). Además, se ha implementado un margen de separación visual respecto a otros elementos interactivos del layout.

+ **Justificación técnica:** Al incrementar el área de clic (tamaño del botón) y reducir la distancia de navegación visual mediante una ubicación estratégica dentro del flujo de lectura del usuario, se minimiza el índice de error de selección, optimizando la usabilidad especialmente en dispositivos móviles donde la precisión táctil es variable.


## 6. Aclaraciones finales

### Tecnologías utilizadas en el proyecto

![Imagen de Bootstrap](https://imgs.search.brave.com/Ng0kWrY_-Bh69ZhLGdPPJlCwOcqbTmmBCHOx330Y1-0/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9hc3Nl/dHMuc3RpY2twbmcu/Y29tL3RodW1icy82/MmE3NjQ5MmJkNzNh/NGFmNWM1ZDRmYjku/cG5n)

![Imagen de HTML](https://imgs.search.brave.com/oKXoHBVXV696CEPzdUCZH9Kn9b75Sas6F-A6x3d1T30/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9jZG4u/aWNvbnNjb3V0LmNv/bS9pY29uL2ZyZWUv/cG5nLTI1Ni9mcmVl/LWh0bWwtaWNvbi1z/dmctZG93bmxvYWQt/cG5nLTIyNTk5NS5w/bmc_Zj13ZWJwJnc9/MTI4)

![Imagen de CSS](https://imgs.search.brave.com/Q4nNbOIjaTbklhrSQR2UzwWEzfXNQCcXmcZfieIXe9E/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly8xMDAw/bWFyY2FzLm5ldC93/cC1jb250ZW50L3Vw/bG9hZHMvMjAyMS8w/Mi9DU1MtTG9nby01/MDB4MjgzLnBuZw)
