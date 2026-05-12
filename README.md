# 

# **AEE. UD06. Auditoría ASG y Refactorización Sostenible**

# Sostenibilidad Aplicada a los Sectores Productivos

**Alumno:** Guillermo Eugui Sánchez  
**Alumno:** José Luis Segura Fernandez  
**Profesor:** Willman Acosta Lugo 

## Fase 1: Inventario y Dimensión Ambiental (A)

Para evaluar el consumo energético y la huella de carbono de la web actual de *Kebab Cavaleri*, se ha utilizado la herramienta Website Carbon Calculator.

* Y ha resultado en que la página obtiene una calificación energética de F (la más baja por encima de la media). ![\imagenesaAnalisis\][Captura de pantalla 2026-05-12 115307.png]  
* El análisis revela que esta web es más contaminante "dirtier" que el 88% de todas las páginas web a nivel global. Esto indica un consumo de recursos y una emisión de CO2 por visita extremadamente altos para una web que, en esencia, es puramente informativa.

Al analizar el código y la carga de la página, hemos identificado los 3 principales responsables del peso excesivo de la web:

1. Se está cargando una imagen de fondo altísima resolución a pantalla completa directamente desde el CSS, ni se comprime, ni utiliza formatos de generación más optimizados y obliga al navegador a descargar megabytes de datos innecesarios en cada visita.  
2. La imagen principal del contenido (`doner_kebab.jpg`), se renderiza a un tamaño de 1200px de ancho sin utilizar el atributo `loading="lazy"`, entonces la imagen se descarga completamente de golpe al abrir la página, independientemente de si el usuario hace scroll para verla o no.  
3. En el `<head>` de la web se están importando librerías enteras y muy pesadas: `jQuery`, `jQuery UI`, `Bootstrap` y `FontAwesome`. El problema es que el código no utiliza ninguna de las funcionalidades complejas de estas herramientas; la web está maquetada con un HTML y CSS en línea muy básico. Es un peso muerto que el dispositivo del usuario tiene que descargar y procesar en vano.

   

## Fase 2: Dimensión Social y Equidad (S)

## Fase 3: Dimensión de Gobernanza y Ética (G)

## Fase 4: Propuesta de Refactorización (Green Coding)

