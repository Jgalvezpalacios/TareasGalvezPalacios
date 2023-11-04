
# Muchos datos de "Bienestar Digital"
---
![Coraline's Dad](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/0%20work%20work.gif
 "Trabajando hasta tarde")
Para la recolección de datos busqué datos en mi vida que pudiese recolectar y tuvieran significado. Trate primero con la cantidad de veces que mi gato me pedía comida, pero no dio resultados porque no siempre estaba yo ahí (y porque lo olvide). Pensé también en la cantidad de pastillas que tomo, pero la cantidad se mantiene fija y tomar más o menos pastillas tendría consecuencias para mi salud. Pase a métodos de recolección de datos más precisos como el reloj inteligente. La aplicación parecía funcionar bien, confiaba plenamente en mi reloj de origen chino (AliExpress), hasta que el día de la entrega me di cuenta de que los datos sobre mi ritmo cardiaco y horas de sueño no quedaron guardados, dejándome solo con la "cantidad de pasos que di"(información que no reflejaba la realidad).

En medio de mi desesperación y buscando en mi teléfono di con una aplicación llamada "bienestar digital y control parental", en donde finalmente encontre datos; muchos, muchos datos...
![Bienestar digital](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/1%20Bienestar%20digital.jpeg
 "Aplicación Bienestar digital")

## Los datos
---
La aplicación tenía mucha información respecto a mis hábitos con el celular, pero me llamo la atención estos datos:
- Aplicaciones abiertas.
- Tiempo en la aplicación.
- Fecha.
![Datos csv](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/0%20basedatos.png
 "Contenido CSV")


A primera vista parecía simple, solo tomar los nombres de las aplicaciones, registrar el tiempo y las veces que las había abierto ese día, pero mi plan tenía un fallo fundamental: uso más aplicaciones de las que creo en el celular.
Comencé registrando los datos por día en un Excel, labor que solo me tomo una hora (40 minutos buscando como descargar los datos y 20 minutos transcribiéndolos a un Excel).
Todo esto me dejo con cinco columnas:
1. Aplicación
1. Fecha
1. Tiempo
1. Aperturas
1. Minutos

## Primer intento de gráfico
---
Tenía cuatro variables que graficar y busque distintas formas de hacer. Mi primera idea fue utilizar la librería Seaborn, con un gráfico de burbuja, donde, utilizara el eje "x" para manejar las aperturas, el eje "y" para la fecha, el radio del círculo para el tiempo en la aplicación y etiquetas de colores para los nombres de las aplicaciones.

El resultado fue un gráfico bastante desproporcional, que mostraba la información pero no era del todo legible.

![Grafico de burbujas](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/2%20primer%20intento.png "Primer intento")

## Intentos fallidos con Altair y plotly
---

Continúe mis pruebas con la librería Altair y Plotly, el primero no me funciono, trate de utilizarlo en un Google notebook, pero no me reconocía la librería. Por otra parte, trate don Plotly utilizando uno de los ejemplos, pero los deseche luego de un rato.


Aquí algunos ejemplos que no borre:
![Grafico de burbujas](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/3%20fallido%202.png "Primer intento")
![Grafico de burbujas](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/3%20fallido%203.png "Primer intento")
![Grafico de burbujas](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/3%20fallido.png "Primer intento")

## Los gráficos finales
---


Mis múltiples intentos fallidos por una gráfica decente me llevaron a insistir con Plotly. Revisando la documentación encontré algunas visualizaciones que parecían interesantes terminando en la construcción de cuatro gráficos distintos:
1. Gráfico de burbujas
1. Gráfico de barras seccionados
1. Gráfico de barras con horas totales por aplicación
1. Gráfico de líneas con aperturas totales por aplicación


![Grafico de burbujas final](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/Grafico%204.png "Grafico de burbujas")
![Gráfico de barras seccionados ](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/Grafico%205.png "Gráfico de barras seccionados")
![Gráfico de barras con horas totales por aplicación y lineas con cantidad de aperturas](https://github.com/Jgalvezpalacios/TareasGalvezPalacios/blob/main/Tareas/Tarea%204/Imagenes/Grafico%206.png "Gráfico de barras con horas totales por aplicación y lineas con cantidad de aperturas")

## Información obtenida con los datos

Establecí una relación entre el uso de una aplicación y la cantidad de veces que las abría. Mi hipótesis era la siguiente: las aplicaciones que más abro en al día serán las que más tiempo de uso tendrán (relación directamente proporcional). 
Al ver los datos en crudo, a primera vista parecía ser cierto, pero una vez graficado se pueden detectar algunas anomalías. Este es el caso de AFK Arena, Chess y Vampire Survival, que pese a tener una baja cantidad de aperturas, registraban tiempos mayores a las dejas.
Otras conclusiones obtenidas son: 
1. La cantidad de datos que se pueden obtener a través de las aplicaciones son muchas y presentan un potencial riesgo a nuestra privacidad como usuarios.
1. Los mayores tiempos corresponden a redes sociales (Instagram y WhatsApp) y este tiempo varía dependiendo del día (semana y fin de semana).

1. Debo dejar de comprar cosas por AliExpress (maldito reloj) y temu, el cual sufrió una gran filtración de datos. (ahora, alguien en algún lugar del mundo sabe que paso una hora en promedio en AFK arena...)

Adjunto el Google Collab en la carpeta de la entrega con el archivo CSV con los datos. La demora en la entrega se produjo porque soy olvidadizo y no lo envíe hasta hoy, pero si puedo tener algo distinto a un 1.5 seré feliz.