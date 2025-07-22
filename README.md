# KNN_TP

El objetivo de este trabajo es realizar un reconocedor de imagenes. Para esto utilizamos
un conjunto de datos llamado Fashion Mnist [2] el cual consiste en imagenes de 10
clases de prendas de ropa (zapatillas, remeras, etc). Al mismo tiempo realizamos un
Analisis de Componentes Principales (PCA, por las siglas en ingles) sobre este conjunto de
datos y observamos si varıa la performance en el reconocimiento utilizando distinta cantidad de
componentes.


En este tp trabajamos con datos de imagenes de 28 × 28 pixeles en escala de
grises. Una forma sencilla de almacenar los datos es tomarlos como vectores fila de dimension
28×28 = 784, es decir vectores xi ∈ R^784. Suponiendo que contamos con N imagenes, entonces
es posible armar una matriz X ∈ R ^(N ×784) que represente todo el conjunto de datos. Veremos
que de las 784 dimensiones hay muchas que pueden ser redundantes o poco informativas y
para esto sera util PCA, permitiendo reducir la dimensionalidad del problema.
La tarea de reconocimiento de imagenes involucro crear un clasificador, el cual toma un
elemento del conjunto de datos y genera una prediccion, en este caso un valor entre 1 y 10
que representa a una de las clases de prendas de ropa. Para armar este clasificador utilizamos
la tecnica de aprendizaje automatico de k-vecinos mas proximos (en ingles, k-nearest
neighbors, KNN).


Una de las principales caracterısticas de un sistema de aprendizaje automatico en base
a datos, es poder optimizar un objetivo a partir de un conjunto de datos de entrenamiento
y poder mantener la performance en datos no vistos durante el entrenamiento. Para evaluar
este escenario, se suele tomar distintos datos para entrenar y medir la performance. Si se
cuenta con un solo conjunto de datos, la practica mas comun es tomar una proporcion de
ellos mayoritaria como conjunto de entrenamiento y el resto dejarlo como conjunto de prueba.
Un paso importante aca, es identificar que criterios son importantes que el conjunto de prueba
cumpla y separar los datos en base a eso.
