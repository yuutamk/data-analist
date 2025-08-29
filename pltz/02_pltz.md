# 
Manipulación de Dimensiones en Arrays NumPy para Ciencia de Datos
¿Cómo manejar las dimensiones en NumPy?
Las dimensiones en NumPy transforman tu manera de trabajar con datos. Entender cómo manejar y manipular datos en múltiples dimensiones es crucial para cualquier científico de datos, pues permite abordar problemas complejos con mayor eficiencia y precisión. En este artículo, aprenderás a trabajar con diferentes dimensiones en NumPy, desde un simple valor escalar hasta complejos sensores multidimensionales, explorando ejemplos prácticos y métodos matemáticos útiles.

¿Qué es un escalar en NumPy?
Un escalar en NumPy es el equivalente a un valor simple o único, representado como una dimensión cero. Por ejemplo, si estás interesado en la temperatura de tu ciudad en un día cualquiera, este dato sería un escalar. Imagina que queremos representar la temperatura de un día determinado, un valor simple de 42 grados:

import numpy as np

escalar = np.array(42)
print(escalar)  # Salida: 42
print(type(escalar))  # Salida: <class 'numpy.ndarray'>
¿Cómo crear un vector?
Pues bien, si lo que deseas es almacenar datos de toda una semana, entonces necesitas un vector. Un vector es una secuencia ordenada y se representa como una dimensión uno en NumPy:

vector = np.array([30, 29, 42, 35, 33, 36, 42])
print(vector)
El vector anterior representa una lista de temperaturas durante una semana, cada valor corresponde a un día diferente.

¿Cómo se trabaja con matrices en NumPy?
Las matrices en NumPy se utilizan cuando trabajamos con dos dimensiones, lo cual es común en datos tabulares o imágenes. Almacenar y acceder a datos organizados en filas y columnas puede ser muy eficiente:

matriz = np.array([
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
])
print(matriz)
Una matriz, como la del ejemplo, puede facilitar la representación de píxeles de una imagen o productos vendidos mes a mes en un conjunto de datos de ventas.

¿Qué es un tensor y cómo se representa?
Un tensor es una extensión de matrices a más dimensiones, utilizado para representar estructuras de datos más complejas, como imágenes en 3D en las que se trabaja con los canales RGB:

tensor = np.array([
    [
        [1, 2], [3, 4]
    ],
    [
        [5, 6], [7, 8]
    ]
])
print(tensor)
Un tensor de tres dimensiones como este puede manejar cantidades impresionantes de datos, ideal para proyectos avanzados de aprendizaje automático.

¿Cuáles son las formas de crear arrays en NumPy?
NumPy ofrece diversas formas para crear arrays, cada una adaptándose a situaciones específicas:

Conversión desde otras estructuras de Python, como listas y tuplas.
Funciones de creación, como np.zeros para matrices de ceros.
Replicación, unión o mutación de arrays existentes.
Lectura de arrays desde disco, en formatos estándar o personalizados.
Creación desde bytes crudos usando cadenas o buffers.
Funciones especiales de bibliotecas de álgebra lineal.
Veamos un ejemplo usando arange:

rango = np.arange(10)
print(rango)  # Salida: [0 1 2 3 4 5 6 7 8 9]
Y la creación de una matriz identidad:

identidad = np.eye(3)
print(identidad)
¿Qué otras funciones matemáticas puedo utilizar con NumPy?
NumPy ofrece varias funciones matemáticas avanzadas, como diag para crear matrices diagonales y random para generar matrices con valores aleatorios:

diagonal = np.diag([1, 2, 3, 4])
print(diagonal)

aleatoria = np.random.rand(2, 3)
print(aleatoria)
Estos métodos sirven para aplicaciones que van desde álgebra lineal hasta simulaciones estocásticas. Te recomiendo explorar más sobre métodos numéricos y álgebra lineal para sacar el máximo provecho de NumPy.

¡Conviértete en un experto! Practica estos conceptos, explora nuevas funciones y siempre mantente curioso. NumPy es una herramienta poderosa para el manejo de datos y tus habilidades seguirán creciendo con cada desafío. ¡Adelante!