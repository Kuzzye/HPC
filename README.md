<p align="center">
<FONT FACE="times new roman" SIZE=5>
<br>
<img src="https://res-5.cloudinary.com/crunchbase-production/image/upload/c_lpad,h_256,w_256,f_auto,q_auto:eco/v1455514364/pim02bzqvgz0hibsra41.png"
width="200" height="200">
</img>
<br>
<i><b>Docente:</b></i> John Corredor, PhD.
<br>
<i><b>Asignatura:</b></i> HPC Introducción 
<br>
<i><b>Estudiantes:</b></i><br>Kevin Fabian Chepe Astudillo
<br>
<i><b>Tema:</b></i> Parcial Final
<br>
23/11/22
<br>
</FONT>
</p>

__Resumen:__ 

Esta práctica tiene como fin el poder replicar las técnicas aprendidas en clase para implementar regresión lineal, el desarrollo se llevará a cabo de manera manual desde Qt utilizando lenguaje de programación C++ y desde Google Collaboratory haciendo uso de módulos como Sklearn utilizando el lenguaje de programación Python

__Introducción:__

El planteamiento de un conjunto de datos de prueba tomado de Kaggle que recoge los ingresos por ventas generadas con respecto a los costes de la publicidad en múltiples canales como la radio, la televisión y los periódicos, para llevar a cabo el experimento de aplicar regresión lineal sobre dos lenguajes de programación diferentes.

__Objetivos:__

* __Modelar las predicciones basadas en la Regresión Lineal__

 - Seleccionar un dataset.
- Hacer una análitica de datos sobre el dataset seleccionado
- Modelar usando la regresión lineal usando: Python,  Scikit-Learn
- Modelar usando la regresión lineal usando: C++
- Comparar los modelos

__Ejecución:__

Para el modelo de Python en Google Collab se utilizaron los módulos:

* __Sk-learn:__ para la creación del modelo, la separación de los datos, las métricas de rendimiento
* __Pandas:__ Para manejar el dataset y convertirlo a una variable manejable
* __Numpy:__ Para realizar operaciones aritméticas.
* __Matplotlib y Seaborn:__ Para graficar.

Se importó el dataset desde un repositorio de github y se trabajó con el módulo de pandas para poder trabajarlo de manera adecuada, se procedió a hacer un análisis de los datos y generar gráficas de matrices de dispersión y correlación con matplotlib y seaborn para ver qué tan relacionadas están unas columnas con otras, se halló el promedio y desviación estándar de todas las columnas para posterior su comparación y se procedió a dividir el conjunto de datos en datos de entrenamiento y datos de prueba con el módulo Sklearn para su uso, se aplicó regresión lineal y halló que cual fue su rendimiento con la métrica R2.

Para el modelo de C++ en Qt se hizo de manera algo manual apoyándose de herramientas como:

* __Eigen:__ Para facilitar el uso de matrices en c++
* Módulos heredados de C como Vector, list.
* __fstream:__ para manejar el dataset.

En este modelo se creó un proyecto en el cual se crearon diferentes clase como lo son:

* __ClassExtraction:__ Donde se crearon funciones para abrir el dataset csv, para convertir el dataset a matrices trabajables desde eigen, sacar la normalización, el promedio, la desviación estándar y hacer la separación de datos simulando un traintestsplit de python.

* __LinearRegression:__ Donde se crearon funciones como: de costo, gradiente descendiente y la métrica de rendimiento R2

__Comparativa:__

Qt - C++
![imagen](https://user-images.githubusercontent.com/79543099/203247297-a6a5df62-4302-4897-8376-72d23b08ef64.png)

Collab - Python
![imagen](https://user-images.githubusercontent.com/79543099/203247427-b641154f-e78a-4472-9086-a7bf23061c85.png)


__Analisis:__

* Como se puede apreciar en los resultados de las métricas de rendimiento de cada uno de los modelos, el modelo de C++ es un poco más preciso que el de Python, pero aun así son resultados bastante buenos los dos muy similares.

__Conclusiones:__

* Del dataset seleccionado se puede concluir que es un dataset muy simple pero muy práctico para casos en los que se tenga que aplicar regresión lineal ya que no presenta variaciones grandes,
* El rendimiento es demasiado bueno, al ser un dataset algo pequeño puede que no tenga los suficientes datos para determinar una regresión lineal óptima.
* No se encontraron muchos datos atípicos lo cual quiere decir que es un caso perfecto para la aplicación de modelos como la regresión lineal.
* No hubo ni un solo dato vacío ni errado, lo que quiere decir que es un dataset enfocado a la experimentación.
* Los valores hallados del promedio y la desviación estándar entre los dos modelos son muy cercanos, dando a entender que el modelo manual está bien hecho, y el desfase es probablemente por cómo maneja los tipos de datos el lenguaje utilizado en cuestión.
* La mayor correlación se presenta entre la variable TV y ventas esto debido a que el mercado de televisores es bastante estable y las ventas siempre siguen un promedio.
* Aunque el proceso para realizar regresión lineal fue mucho más sencillo en Python ya que tiene módulos específicos que se encargan de esta, se pierde un poco de rendimiento ya que el ajuste de datos está generado en un estándar y no puede ser retocado como si se puede en el modelo de C++.

