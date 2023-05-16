# Diseño e implementación básica de un DSL para enseñar a programar a niños
El mundo profesional de los ITC está lleno de retos interesantísimos, y uno relativamente común es el de aprender nuevos lenguajes de programación, o incluso diseñar nuevos lenguajes. En algunas ocasiones, hay necesidades tan específicas, que demandan un lenguaje de dominio específico o DSL (Domain Specific Language). Un DSL es un lenguaje de programación con un nivel superior de abstracción optimizado para una clase específica de problemas. Un DSL usa los conceptos y reglas de su campo o dominio, y normalmente es menos complejo que un lenguaje de propósito general como los que típicamente utilizamos.

Imagina que has sido contratado por una escuela que desea utilizar un DSL y tendrás sólo estas semanas del primer período para diseñarlo e implementar algunos elementos del mismo.

El dominio del lenguaje para esta escuela es el manejo de un robot virtual que dibuja en pantalla, es decir, se desea trabajar con un lenguaje de programación que permita representar los comandos que se le pueden dar a este robot para que haga dibujos. 

Ante este reto, tendrás que diseñar ágilmente un DSL relacionado con la representación de este robot para implementar un sencillo analizador y ejecutor de programas escritos en este DSL.

## Descripcion
La necesidad de este lenguaje no es una novedad. En los años 70's surgió la propuesta de un lenguaje con este propósito: el lenguaje LOGO. Este lenguaje NO es un DSL, pues en realidad es un lenguaje de propósto general con funcionalidades muy potentes que analizarás en la situación problema #3. Curiosamente, la popularidad de LOGO se dió en los años 80's y 90's, precisamente con una aplicación especifica, al proveer un ambiente gráfico, con una "tortuga" que se podría programar para que ejecutara dibujos en pantalla, entre otras cosas. Esto permitió impulsar la idea de que los niños y niñas podían formarse en el pensamiento lógico y computacional desde pequeños, y en la actualidad, se le sigue dando mantenimiento a esta idea. En la siguiente página podrás encontrar una breve referencia a la historia de este lenguaje: https://el.media.mit.edu/logo-foundation/what_is_logo/history.html.Links to an external site. Revisa también el tutorial de inicio que se muestra en esta misma referencia: https://el.media.mit.edu/logo-foundation/what_is_logo/logo_primer.htmlLinks to an external site.. Inspírate un poco en esta página en la que se puede practicar el uso del lenguaje con algunos retos: https://www.transum.org/Software/Logo/Links to an external site.

La escuela que te ha contratado te solicita que implementes en Python o el lenguaje de tu preferencia, un analizador y ejecutor del DSL equivalente al lenguaje del manejo de la tortuga que pudiste observar en las referencias anteriores. El diseño del lenguaje que realices deberá manejar las instrucciones en español, y estará limitado a los siguientes comandos básicos:
* Mover hacia adelante o hacia atrás.
* Girar a la izquierda o derecha.
* Levantar o bajar la pluma.
* Cambiar de color la pluma.
* Limpiar la pantalla.
* Llevar al centro de la pantalla el robot.
* Repetir un número específico de veces los comandos indicados.

El programa que realices, además de analizar el uso correcto del léxico del minilenguaje, deberá ejecutar el código de entrada con los dibujos correspondientes a los comandos identificados con acciones del robot. El análisis del léxico deberá implementarse utilizando la librería de manejo de expresiones regulares que tenga el lenguaje en que implementes (ej. módulo re si utilizas Python). Añade también el reconocimiento de la sintaxis básica del lenguaje implementando el parser con el método de descenso recursivo.

El programa que implementes deberá tener una interfase en la cual el usuario dará el nombre de un archivo que contiene el código en el minilenguaje de comandos para el robot el cuál será analizado y ejecutado. Se recomienda usar como pruebas, los retos que se muestran en la lección 1 del tutorial de esta página: https://www.transum.org/Software/Logo/Links to an external site. pero utilizando el lenguaje el léxico y la sintaxis que hayas diseñado.

## Especificaciones de la entrega
Como resultado de tu proceso de solución a esta situación problema, deberás entregar lo siguiente:

* Un documento identificado con una portada adecuada y que contenga lo siguiente:
  * Una lista con los elementos del léxico del lenguaje, incluyendo para cada uno su expresión regular que lo representa utilizando la notación básica.
  * El diseño de un autómata determinístico que modele el proceso de análisis del léxico del lenguaje según la técnica aprendida en el curso. Este autómata NO se implementará, pero su diseño es una práctica importante.
  * El diseño de los diagramas de sintaxis y la gramática BNF que modelen la sintaxis del lenguaje que utiliza los lexemas previamente diseñados. 
  * El código implementado, documentado con los comentarios convenientes para entenderlo.
  * Las entradas (inputs) con las que se probó el programa, describiendo si funcionaron o no.
  * Un breve comentario sobre la experiencia de aprendizaje y los resultados obtenidos.
* Un video de no más de 5 minutos, en los que muestres la ejecución de tu programa con pruebas significativas, explicando los elementos principales del mismo y haciendo comentarios respecto a tu proceso de solución y tus aprendizajes.
