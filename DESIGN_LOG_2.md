# Actividad 2: Arquitectura de Información y el "Lienzo" del Mapa

## Decisiones de diseño

Para crear el mapa, se utilizó la librería de OpenStreetMap, pero se le indicó a Gemini que utilizara una capa diferente, ya que la que viene por estandar está un poco saturada de iconos y no es agradable para el usuario. Se busca enfocar toda su atención solo en los restaurantes y no en otros comercios. Además, los marcadores también tienen estos colores de Foody.

* Capa del Mapa: Se utilizó CartoDB Voyager. Es una alternativa excelente a la capa estándar de OSM y a Tracestrack (que a veces requiere API key). Es extremadamente limpia, usa colores pasteles que combinan perfecto con Foody, y resalta las calles y puntos de interés sin saturar la vista con iconos innecesarios.

* Ubicación: Centrado exactamente en Plaza Río Tijuana.

* UX Móvil: Se colocaron los controles del zoom en la parte inferior derecha para que sean de fácil acceso para usuarios móvil.

* Estilo: Se conservó la paleta de colores de Foody para diseñar el header y los botones del mapa.

## Prompts de Gemini Canvas

* "Ahora quiero que crees un archivo aparte, pero manteniendo el la paleta de colores de Foody. Esta nueva página sólo será un mapa con las siguientes características:
Genera un archivo HTML que incluya la librería Leaflet.js (vía CDN) y Tailwind CSS. Crea un contenedor div 'map' que ocupe el 100% del ancho y 500px de alto (o 'h-screen'). Inicializa el mapa centrado en Tijuana, para ser exactos cerca de plaza río con un tilelayer de OpenStreetMap. Asegúrate de que los botones de zoom estén en una posición fácil de alcanzar y que sea responsivo en dispositivos móviles. Quiero que la capa del mapa no sea la estandar porque viene con muchos iconos y leyendas, mejor usa una como tracestrack topo que solo marca los estacionamientos y se ve más limpio."
