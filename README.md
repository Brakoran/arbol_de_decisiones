# arbol_de_decisiones

Importa las bibliotecas necesarias: pandas, numpy, matplotlib.pyplot y diversas clases y funciones de scikit-learn para trabajar con árboles de decisión y evaluar modelos.

Carga un conjunto de datos desde un archivo CSV llamado "wine.data" ubicado en "C:\date\Arboles/wine.data" en un DataFrame llamado data.

Muestra las primeras 15 filas del DataFrame data utilizando data.head(15).

Muestra la forma del DataFrame data utilizando data.shape, lo que indica la cantidad de filas y columnas en el conjunto de datos.

Calcula estadísticas descriptivas básicas del DataFrame data utilizando data.describe(), lo que proporciona información como la media, la desviación estándar, el valor mínimo y máximo, entre otros, para cada columna numérica en el conjunto de datos.

Crea un histograma utilizando plt.hist(data.columns). Sin embargo, este código intenta crear un histograma de los nombres de las columnas, lo cual es inusual ya que los histogramas generalmente se utilizan para visualizar distribuciones de datos numéricos. Esto puede no ser útil en este contexto.

Define dos listas: predictors_col y target_col, que representan las columnas que se utilizarán como predictores (características) y la columna que se utilizará como variable objetivo, respectivamente.

Crea dos DataFrames, predictors y target, seleccionando las columnas correspondientes del DataFrame data utilizando las listas predictors_col y target_col.

Divide los datos en conjuntos de entrenamiento (x_train, y_train) y prueba (x_test, y_test) utilizando train_test_split. El 80% de los datos se asignan al conjunto de entrenamiento y el 20% al conjunto de prueba. El parámetro random_state se establece en 13 para garantizar que la división sea reproducible.

Crea un modelo de regresión de árbol de decisión utilizando DecisionTreeRegressor() y lo almacena en la variable arbol.

Ajusta el modelo de regresión de árbol de decisión a los datos de entrenamiento utilizando arbol.fit(x_train, y_train).

Visualiza el árbol de decisión utilizando plot_tree(arbol), lo que muestra la estructura del árbol y cómo se realizan las divisiones basadas en las características.

Realiza predicciones en el conjunto de prueba utilizando arbol.predict(x_test) y almacena las predicciones en la variable predicciones.

Crea una tabla de contingencia utilizando pd.crosstab, que muestra la relación entre los valores reales (y_test) y las predicciones (predicciones). Esto puede ayudar a evaluar el rendimiento del modelo de regresión de árbol de decisión
