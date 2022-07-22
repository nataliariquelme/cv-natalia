---
title: 1. Python para el análisis de datos de Wes McKinney - Preeliminares.
subtitle: Proyecto de traducción voluntaria.

# Summary for listings and search engines
summary: Este libro se ocupa de las tuercas y los tornillos de la manipulación, el procesamiento, la limpieza y el procesamiento de datos en Python.

# Link this post with a project
projects: []

# Date published
date: '2022-07-21T00:00:00Z'

# Date updated
lastmod: '2022-07-21T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Python**](https://www.goodreads.com/book/show/14744694-python-for-data-analysis)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - Wes McKinney

tags:
  - Academic
  - Data Science
  - Programación
---

# Python para analisis de datos

## Capítulo 1: Pre-eliminares

### ¿De qué se trata este libro?

Este libro se ocupa de las tuercas y los tornillos de la manipulación, el procesamiento, la limpieza y el procesamiento de datos en Python. También es una introducción práctica y moderna a la computación científica en Python, adaptada a las aplicaciones de uso intensivo de datos. Este es un libro sobre las partes del lenguaje Python y las bibliotecas que necesitará para resolver eficazmente un amplio conjunto de problemas de análisis de datos. Este libro no es una exposición de métodos analíticos utilizando Python como lenguaje de implementación.


Cuando digo "datos", ¿a qué me refiero exactamente? El enfoque principal es el de los datos estructurados, un término deliberadamente vago que engloba muchas formas comunes de datos, como:

- Arreglos multidimensionales (matrices).
- Datos tabulares o de hoja de cálculo en los que cada columna puede ser de un tipo diferente (cadena, numérico, fecha u otro). Esto incluye la mayoría de los tipos de datos que suelen almacenados en bases de datos relacionales o archivos de texto delimitados por tabulaciones o comas.
- Múltiples tablas de datos interrelacionadas por columnas clave (lo que serían claves primarias o claves externas para un usuario de SQL).
- Series temporales espaciadas de manera uniforme o irregular.


Esta no es en absoluto una lista completa. Aunque no siempre sea obvio, un gran porcentaje de conjuntos de datos puede transformarse en una forma estructurada que sea más adecuada para el análisis y la modelización. Si no, puede ser posible extraer características de un conjunto de datos en una forma estructurada. Por ejemplo, una colección de artículos de noticias podría transformarse en una tabla de frecuencias de palabras que luego podría utilizarse para realizar un análisis de sentimientos.

La mayoría de los usuarios de programas como hojas de cálculo como Microsoft Excel  no serán ajenos a este tipo de datos.


### ¿Por qué Python para analisis de datos?

Para muchas personas (yo mismo entre ellas), es fácil enamorarse del lenguaje Python. Desde su primera aparición en 1991, Python se ha convertido en uno de los
junto con Perl, Ruby y otros se han hecho especialmente populares en los últimos años para construir sitios web utilizando sus numerosos
frameworks web, como Rails (Ruby) y Django (Python). Estos lenguajes suelen llamarse lenguajes de scripting ya que pueden ser utilizados para escribir pequeños programas rápidos
o scripts. No me gusta el término "lenguaje de scripting" ya que conlleva una connotación de que no pueden usarse para construir software de misión crítica. Entre los lenguajes interpretados
Python se distingue por su amplia y activa comunidad de computación científica. La adopción de Python para la computación científica, tanto en aplicaciones industriales como en la investigación académica ha aumentado significativamente desde principios de la década de 2000.

Para el análisis de datos, la computación interactiva y exploratoria y la visualización de datos, Python inevitablemente se comparará con muchos otros lenguajes de programación comerciales y de código abierto, como R, MATLAB, SAS, Stata y otros, SAS, Stata y otros. En los últimos años, la mejora del soporte de las bibliotecas de Python (principalmente pandas) lo ha convertido en una fuerte alternativa para las tareas de manipulación de datos. En combinación con la fuerza de Python en la programación de propósito general, es una excelente opción como
para construir aplicaciones centradas en los datos.

### Python as Glue

Parte del éxito de Python como plataforma de computación científica es la facilidad para integrar código C++ y FORTRAN. La mayoría de los entornos informáticos modernos comparten un conjunto similar de librerías FORTRAN y C heredadas para hacer álgebra lineal, optimización, integración transformaciones rápidas de Fourier y otros algoritmos similares. La misma historia es válida para muchas empresas y laboratorios nacionales que han utilizado Python para pegar 30 años de años de software heredado.

La mayoría de los programas consisten en pequeñas porciones de código en las que se pasa la mayor parte del tiempo, con grandes cantidades de "código cola" que no se ejecuta a menudo. En muchos casos, el tiempo de ejecución del código de cola es insignificante; el esfuerzo se invierte de forma más fructífera en optimizar los los cuellos de botella computacionales, a veces trasladando el código a un lenguaje de nivel inferior como C.

En los últimos años, el proyecto Cython (http://cython.org) se ha convertido en una de las formas preferidas tanto para crear extensiones compiladas rápidas para Python como para interactuar con código C y C++.

# Solving the "two lenguage problem"

En muchas organizaciones, es habitual investigar, crear prototipos y probar nuevas ideas utilizando un lenguaje informático más específico, como MATLAB o R, para luego trasladar esas ideas para formar parte de un sistema de producción más amplio escrito, por ejemplo, en Java, C# o C++. Lo que gente está descubriendo cada vez más que Python es un lenguaje adecuado no sólo para hacer investigación y creación de prototipos, sino también para construir los sistemas de producción. Creo que cada vez más empresas seguirán este camino, ya que a menudo hay importantes beneficios organizativos al tener tanto científicos como tecnólogos utilizando el mismo conjunto de herramientas de programación.


# Why not Python?

Aunque Python es un entorno excelente para construir aplicaciones científicas de cálculo intensivo y para construir la mayoría de los sistemas de propósito general, hay una serie de usos para los que Python puede ser menos adecuado. 

Como Python es un lenguaje de programación interpretado, en general la mayor parte del código Python se ejecuta sustancialmente más lento que el código escrito en un lenguaje compilado como Java o C++. Como tiempo del programador es normalmente más valioso que el tiempo de la CPU, muchos están contentos de hacer esta compensación. 

Sin embargo, en una aplicación con requisitos de latencia muy bajos (por ejemplo, un sistema de comercio de alta frecuencia), el tiempo dedicado a programar en un lenguaje de bajo nivel, y menor productividad, como C++, para lograr el máximo rendimiento posible
puede ser un tiempo bien empleado.



Python no es un lenguaje ideal para aplicaciones altamente concurrentes y multihilo, particularmente aplicaciones con muchos hilos ligados a la CPU. La razón es que tiene lo que se conoce como bloqueo global del intérprete (GIL), un mecanismo que impide que el intérprete ejecute más de una instrucción de código de bytes de Python a la vez. Las razones técnicas de por qué existe el GIL están más allá del alcance de este libro, pero al momento de escribir esto, no parece probable que el GIL desaparezca pronto. Si bien es cierto que en muchas aplicaciones de procesamiento de big data, puede ser necesario un clúster de ordenadores para procesar un conjunto de datos en un tiempo razonable, todavía hay situaciones en las que es deseable un sistema multihilo de un solo proceso.

Esto no quiere decir que Python no pueda ejecutar código paralelo verdaderamente multihilo; simplemente, ese código no puede ejecutarse en un único proceso de Python. Por ejemplo, el proyecto Cython se integra fácilmente con OpenMP, un marco de trabajo en C para la computación paralela, con el fin de paralelizar los bucles y así acelerar significativamente los algoritmos numéricos.

# Essential Python Libraries

Para aquellos que estén menos familiarizados con el ecosistema científico de Python y las bibliotecas utilizadas a lo largo del libro, presento el siguiente resumen de cada biblioteca.


## NumPy

NumPy, abreviatura de Numerical Python, es el paquete fundacional para la computación científica en Python. La mayor parte de este libro se basará en NumPy y en las bibliotecas construidas sobre NumPy. Proporciona, entre otras cosas:

- Un objeto de array multidimensional rápido y eficiente ndarray.
- Funciones para realizar cálculos a nivel de elementos con matrices u operaciones matemáticas entre matrices.
- Herramientas para leer y escribir en el disco conjuntos de datos basados en matrices.
- Operaciones de álgebra lineal, transformación de Fourier y generación de números aleatorios.
- Herramientas para integrar la conexión de código C, C++ y Fortran a Python.


Más allá de las capacidades de procesamiento rápido de matrices que NumPy añade a Python, uno de sus propósitos primarios con respecto al análisis de datos es como el contenedor primario de datos que se pasan entre algoritmos. Para los datos numéricos, las matrices de NumPy son una forma mucho mejor de almacenar y manipular datos que las otras estructuras de datos incorporadas en Python. Además, las bibliotecas escritas en un lenguaje de bajo nivel, como C o Fortran, pueden operar con los datos almacenados en una matriz NumPy sin copiar ningún dato.

## pandas

pandas proporciona estructuras ricas de datos y funciones diseñadas para hacer que el trabajo con datos estructurados de forma rápida, fácil y expresiva. Es, como verás, uno de los ingredientes críticos que permiten a Python ser un entorno de análisis de datos potente y productivo. El objeto principal de pandas que se utilizará en este libro es el DataFrame, una estructura de datos tabular bidimensional orientada a columnas y filas:

![dataframe1.png](C:\Users\natal\Desktop\dataframe1.png)

pandas combina las características de alto rendimiento de NumPy con las de manipulación de datos de las hojas de cálculo y las bases de datos relacionales (como como SQL). Proporciona una sofisticada funcionalidad de indexación para facilitar la remodelaciónm de datos, realizar agregaciones y seleccionar subgrupos de datos, herramienta que utilizaremos en este libro.

Para los usuarios del sector financiero, pandas ofrece una rica funcionalidad de series temporales de alto rendimiento y herramientas muy adecuadas para trabajar con datos financieros. De hecho, inicialmente diseñé pandas como una herramienta ideal para aplicaciones de análisis de datos financieros.


Para los usuarios del lenguaje R para la computación estadística, el nombre de DataFrame les resultará familiar, ya que el objeto fue nombrado como el objeto similar al  data.frame de R. Sin embargo, no son lo mismo; el data.frame en R es esencialmente un subconjunto de la proporcionada por el DataFrame de pandas. Aunque este es un libro sobre Python, ocasionalmente de vez en cuando haré comparaciones con R, ya que es uno de los entornos de análisis de datos de código abierto y será familiar para muchos lectores.

 El propio nombre de pandas deriva de datos de panel, un término de econometría para conjuntos de datos estructurados multidimensionales, y del análisis de datos de Python.

## matplotlib

matplotlib es la biblioteca más popular de Python para producir gráficos y otras visualizaciones de datos en 2D. Fue creada originalmente por John D. Hunter (JDH) y ahora es mantenida por un gran equipo de desarrolladores. Es muy adecuada para crear gráficos adecuados para su publicación. Se integra bien con IPython (véase más adelante), proporcionando así un cómodo entorno interactivo para trazar y explorar los datos. Los gráficos también son interactivos; puede acercarse a una sección del gráfico y desplazarse por él mediante la barra de herramientas de la ventana.

## IPython

IPython es el componente del conjunto de herramientas científicas estándar de Python que une todo. Proporciona un entorno robusto y productivo para la computación interactiva y exploratoria. Es un shell de Python mejorado diseñado para acelerar la escritura, pruebas y depuración de código Python. Es especialmente útil para trabajar de forma interactiva con datos y visualizarlos con matplotlib. IPython suele estar involucrado en la la mayoría de mi trabajo en Python, incluyendo la ejecución, depuración y prueba de código.

Además del shell estándar de IPython basado en el terminal, el proyecto también proporciona:

- Un cuaderno HTML tipo Mathematica para conectarse a IPython a través de un navegador web (más adelante).
- Una consola GUI basada en el marco Qt con trazado en línea, edición multilínea y resaltado de sintaxis.
- Una infraestructura para la computación interactiva paralela y distribuida.

Dedicaré un capítulo a IPython y a cómo sacar el máximo provecho de sus características. Recomiendo encarecidamente su uso mientras se trabaja en este libro.

## SciPy

SciPy es una colección de paquetes que abordan una serie de problemas estándar en la computación científica. He aquí una muestra de los paquetes incluidos:

- scipy.integrate: rutinas de integración numérica y solucionadores de ecuaciones diferenciales
- scipy.linalg: rutinas de álgebra lineal y descomposición de matrices que van más allá de las proporcionadas en numpy.linalg.
- scipy.optimize: optimizadores de funciones (minimizadores) y algoritmos de búsqueda de raíces
- scipy.signal: herramientas de procesamiento de señales
- scipy.sparse: matrices dispersas y solucionadores de sistemas lineales dispersos
- scipy.special: envoltura de SPECFUN, una biblioteca Fortran que implementa muchas funciones matemáticas comunes, como la función gamma
- scipy.stats: distribuciones de probabilidad continuas y discretas estándar (funciones de densidad, muestreadores, funciones de distribución continua), varias pruebas estadísticas y más estadísticas descriptivas
- scipy.weave: herramienta para utilizar código C++ en línea para acelerar los cálculos de matrices.

Juntos, NumPy y SciPy forman un reemplazo computacional razonablemente completo para gran parte de MATLAB junto con algunas de sus cajas de herramientas complementarias.


## Python 2 and python 3

La comunidad de Python se encuentra actualmente en una prolongada transición de la serie de intérpretes Python 2 a la serie Python 3. Hasta la aparición de Python 3.0, todo el código de Python era compatible hacia atrás. La comunidad decidió que, para hacer avanzar el lenguaje, eran necesarios ciertos cambios incompatibles hacia atrás.

Estoy escribiendo este libro con Python 2.7 como base, ya que la mayoría de la comunidad científica comunidad científica de Python aún no ha hecho la transición a Python 3. La buena noticia es que, con
con unas pocas excepciones, no debería tener problemas para seguir el libro si si está usando Python 3.2.

## Integrate Development Environments (IDEs)

Cuando me preguntan por mi entorno de desarrollo estándar, casi siempre digo "IPython más un editor de texto". Normalmente escribo un programa y pruebo y depuro de forma iterativa cada pieza del mismo en IPython. También es útil poder jugar con los datos de forma interactiva y verificar visualmente que un conjunto particular de manipulaciones de datos está haciendo lo correcto. Bibliotecas como pandas y NumPy están diseñadas para ser fáciles de usar en el shell.


Sin embargo, algunos seguirán prefiriendo trabajar en un IDE en lugar de un editor de texto. Éstos proporcionan proporcionan muchas características agradables de "inteligencia de código" como completar o sacar rápidamente la documentación asociada a funciones y clases. Aquí hay algunas que puedes explorar:

- Eclipse con el plugin PyDev.
- Herramientas de Python para Visual Studio (para usuarios de Windows).
- PyCharm.
- Spyder.
- Komodo IDE.

## Comunity and Conferences

Aparte de una búsqueda en Internet, las listas de correo científico de Python suelen ser útiles y responder a las preguntas. Algunas de las que se pueden consultar son

- pydata: una lista de Google Group para preguntas relacionadas con Python para el análisis de datos y pandas.
- pystatsmodels: para preguntas relacionadas con statsmodels o pandas.
- numpy-discussion: para preguntas relacionadas con NumPy.
- scipy-user: para preguntas generales sobre SciPy o Python científico.

Deliberadamente no publiqué las URLs de estos sitios en caso de que cambien. Se pueden localizar fácilmente a través de la búsqueda en Internet.

Cada año se celebran en todo el mundo numerosas conferencias para programadores de Python. PyCon y EuroPython son las dos principales conferencias generales de Python en Estados Unidos y Europa, respectivamente. SciPy y EuroSciPy son conferencias de Python orientadas a la ciencia donde es probable que encuentre muchos "pájaros de un plumaje" si se involucra más con con el uso de Python para el análisis de datos después de leer este libro.

## Navigating this book

Si nunca has programado en Python antes, puede que quieras empezar por el final del libro, donde he puesto un tutorial condensado sobre la sintaxis de Python, las características del lenguaje y las estructuras de datos incorporadas como tuplas, listas y diccionarios. Estas cosas son consideradas como conocimientos previos para el resto del libro.

El libro comienza introduciendo el entorno IPython. A continuación, doy una breve introducción a las características clave de NumPy, dejando el uso más avanzado de NumPy para para otro capítulo al final del libro. A continuación, introduzco pandas y dedico el resto del libro a temas de análisis de datos aplicando pandas, NumPy y matplotlib (para la visualización). He estructurado el material de la forma más incremental posible, aunque ocasionalmente hay algún cruce menor entre capítulos.
Los archivos de datos y el material relacionado con cada capítulo están alojados en un repositorio git en GitHub:

http://github.com/pydata/pydata-book

Te animo a que descargues los datos y los utilices para reproducir los ejemplos de código del libro y experimentar con las herramientas presentadas en cada capítulo. Aceptaré con gusto contribuciones, scripts, cuadernos de IPython o cualquier otro material que desee aportar a al repositorio del libro para que todos lo disfruten.


## Code examples

La mayoría de los ejemplos de código en el libro se muestran con la entrada y la salida tal y como aparecerían ejecutado en el shell de IPython.

![inout1.png](C:\Users\natal\Desktop\inout1.png)

En ocasiones, para mayor claridad, se mostrarán varios ejemplos de código uno al lado del otro. Estos deben leerlos de izquierda a derecha y ejecutarlos por separado.



![inout2.png](C:\Users\natal\Desktop\inout2.png)

## Data for examples

Los conjuntos de datos para los ejemplos de cada capítulo están alojados en un repositorio en GitHub: http: //github.com/pydata/pydata-book. Puede descargar estos datos utilizando el programa de línea de comandos de control de revisiones git o descargando un archivo zip del repositorio desde el sitio web. desde el sitio web.

He hecho todo lo posible para asegurarme de que contiene todo lo necesario para reproducir los ejemplos, pero es posible que haya cometido algunos errores u omisiones. Si es así, por favor, envíame un correo electrónico: wesmckinn@gmail.com

## Import conventions

La comunidad de Python ha adoptado una serie de convenciones de nomenclatura para los módulos de uso común:

![nomen.png](C:\Users\natal\Desktop\nomen.png)

Esto significa que cuando veas np.arange, esto es una referencia a la función arange en NumPy. Esto se hace porque se considera una mala práctica en el desarrollo de software en Python importar todo (from numpy import *) de un paquete grande como NumPy.

## Jargon

Utilizaré algunos términos comunes tanto a la programación como a la ciencia de los datos que quizá no no estés familiarizado con ellos. Por lo tanto, aquí hay algunas definiciones breves:

*Munge/Munging/Wrangling*

Describe el proceso general de manipulación de datos no estructurados y/o desordenados en en una forma estructurada o limpia. La palabra se ha colado en la jerga de muchos hackers de datos modernos. Munge rima con "lunge".

*Pseudocódigo*

Descripción de un algoritmo o de un proceso que adopta una forma parecida a la del código.

*Syntactic sugar*

Sintaxis de programación que no añade nuevas características, sino que hace algo más más conveniente o más fácil de escribir.



