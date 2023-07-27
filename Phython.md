
- Python es un lenguaje de programación interpretado, de alto nivel, de propósito general y de código abierto. Fue creado a finales de la década de 1980 por Guido van Rossum y se ha vuelto extremadamente popular debido a su enfoque en la legibilidad del código y su facilidad de aprendizaje.

Algunas de las características distintivas de Python son: 
1. **Legibilidad del código:**  Python enfatiza la claridad y la simplicidad del código, lo que facilita su lectura y comprensión, lo que a su vez promueve la colaboración entre desarrolladores. 
2. **Sintaxis clara y sencilla:**  La sintaxis de Python es intuitiva y cercana al lenguaje natural, lo que facilita el desarrollo rápido y la escritura de programas concisos. 
3. **Versátil y de propósito general:**  Python se puede utilizar para una amplia variedad de tareas, desde desarrollo web y científico hasta automatización, inteligencia artificial y análisis de datos. 
4. **Orientado a objetos:**  Python admite la programación orientada a objetos, lo que permite organizar el código en clases y objetos para reutilización y modularidad. 
5. **Interpretado e interactivo:**  Python es un lenguaje interpretado, lo que significa que el código se ejecuta línea por línea en lugar de ser compilado previamente. Esto permite una mayor flexibilidad y facilidad en el desarrollo. Además, Python también ofrece un modo interactivo que permite probar fragmentos de código de manera inmediata. 
6. **Amplia comunidad y bibliotecas:**  Python cuenta con una comunidad activa y numerosas bibliotecas que facilitan el desarrollo de diversas aplicaciones y resuelven una amplia gama de problemas, lo que lo convierte en una opción popular para muchos proyectos.



Ejercicios:



```Python
print ("hola mundo")

def multiply_by_two(x):
    """This function multiplies
        an input number by 2"""
    return x * 2

help(multiply_by_two)
#muestra la informacion de ayuda de la funcion

def apply_func_twice(func, arg):
    """This function applies 'func' twice to 'arg'"""
    return func(func(arg))

def add_five(x):
    return x + 5 

print(apply_func_twice(add_five, 10))

def greet(person):
    return f"Hello, {person}!"

def repeat(func, times, arg):
    for _ in range(times):
        print(func(arg))

repeat(greet, 3 ,"OpenIA")

import random
signs = ['Libra', 'Aries', 'Cancer', 'Tauro']
forecast  = ['Encontraras el amor', 'Perderas a una persona importante', 'Ganaras un juego', 'Te van a robar hoy']

def horoscope():
  signs_ingresados = input("Ingresa tu signo: ")
horoscope()
print(random.choice(forecast))


num = 5
factorial = 1
while num > 0:
  factorial *= num
  num -= 1

print(factorial)


s = " Hello, Mars!"
print(s.lower())
print(s.upper())
print(s.split(", "))


planets =[
    'Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune'
]

planet_initials = {
    planet: planet[0]
    for planet in planets
}
print(planet_initials)

```


TAREA FINAL:

Realizar un sorteo donde se muestre el numero ganador de la lotería y que el animal escogido del sorteo puede conseguir otro boleto de forma gratuita  

```Python
import random

aniamls  = ['Perro', 'Gato', 'Delfin', 'Tiburon', 'Jirafa']

numbers = [1, 2, 3, 4]

  
def lottery():

    lottery = input("Ingresar su numero de loteria: ")

lottery()

tamano_lista = 4

rango_minimo = 1

rango_maximo = 4

  
lista_aleatoria = [random.randint(rango_minimo, rango_maximo) for _ in range(tamano_lista)]

  
if lottery == lista_aleatoria:

    print("Ganaste la loteria")

else:

  print("Lo sentimos esta es la lista de numeros de loteria que ganaron: ", lista_aleatoria)

  
def animal():

    animal = input("Ingrese su Animal: ")

animal()

  
lista_animal =

  
if animal == lista_animal:

     print("Ganaste otro boleto")

else:

     print("Lo sentimos el animal ganador es: ", random.choice(aniamls))

```



![[Pasted image 20230727010753.png]]

El programa a realizar se basara en la probabilidad que un pasajero del Titanic pueda o pudo sobrevivir a este gran desastre: 

```python
##########LIBRERÍAS A UTILIZAR########## #Se importan la librerias a utilizar import numpy as np import pandas as pd from sklearn.model_selection import train_test_split from sklearn.linear_model import LogisticRegression from sklearn.svm import SVC from sklearn.neighbors import KNeighborsClassifier 


##########IMPORTANDO LA DATA########## #Se guardan los datos en un archivo para 

siempre tenerlos disponibles dir_test = '/Users/devgh/OneDrive/Instituto/Cursos/test.csv' dir_train = '/Users/devgh/OneDrive/Instituto/Cursos/train.csv' 
#Importar los datos de los archivos .csv almacenados 
df_test = pd.read_csv(dir_test) df_train = pd.read_csv(dir_train) print(df_test.head()) print(df_train.head()) 
##########ENTENDIMIENTO DE LA DATA########## 
#Verifico la cantidad de datos que hay en los dataset 
print('Cantidad de datos:') print(df_train.shape) print(df_test.shape) 
#Verifico el tipo de datos contenida en ambos dataset 
print('Tipos de datos:') print(df_train.info()) print(df_test.info()) 
#Verifico los datos faltantes de los dataset 
print('Datos faltantes:') print(pd.isnull(df_train).sum()) print(pd.isnull(df_test).sum()) 
#Verifico las estadísticas del dataset 
print('Estadísticas del dataset:') print(df_train.describe()) print(df_test.describe()) 
##########PREPROCESAMIENTO DE LA DATA########## 
#Cambio los datos de sexos en números 
df_train['Sex'].replace(['female','male'],[0,1],inplace=True) df_test['Sex'].replace(['female','male'],[0,1],inplace=True) 
#Cambio los datos de embarque en números
df_train['Embarked'].replace(['Q','S', 'C'],[0,1,2],inplace=True) df_test['Embarked'].replace(['Q','S', 'C'],[0,1,2],inplace=True) 
#Reemplazo los datos faltantes en la edad por la media de esta columna 
print(df_train["Age"].mean()) print(df_test["Age"].mean()) promedio = 30 df_train['Age'] = df_train['Age'].replace(np.nan, promedio) df_test['Age'] = df_test['Age'].replace(np.nan, promedio) 
#Creo varios grupos de acuerdo a bandas de las edades #
Bandas: 0-8, 9-15, 16-18, 19-25, 26-40, 41-60, 61-100 bins = [0, 8, 15, 18, 25, 40, 60, 100] names = ['1', '2', '3', '4', '5', '6', '7'] 
df_train['Age'] = pd.cut(df_train['Age'], bins, labels = names) df_test['Age'] = pd.cut(df_test['Age'], bins, labels = names) 
#Se elimina la columna de "Cabin" ya que tiene muchos datos perdidos 
df_train.drop(['Cabin'], axis = 1, inplace=True) df_test.drop(['Cabin'], axis = 1, inplace=True) 
#Elimino las columnas que considero que no son necesarias para el analisis 
df_train = df_train.drop(['PassengerId','Name','Ticket'], axis=1) df_test = df_test.drop(['Name','Ticket'], axis=1) 
#Se elimina las filas con los datos perdidos 
df_train.dropna(axis=0, how='any', inplace=True) df_test.dropna(axis=0, how='any', inplace=True) 
#Verifico los datos 
print(pd.isnull(df_train).sum()) print(pd.isnull(df_test).sum()) print(df_train.shape) print(df_test.shape) print(df_test.head()) print(df_train.head()) 
##########APLICACIÓN DE ALGORITMOS DE MACHINE LEARNING########## 
#Separo la columna con la información de los sobrevivientes 
X = np.array(df_train.drop(['Survived'], 1)) y = np.array(df_train['Survived']) #Separo los datos de "train" en entrenamiento y prueba para probar los algoritmos 
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2) ##Regresión logística 
logreg= LogisticRegression() logreg.fit(X_train, y_train) Y_pred = logreg.predict(X_test) print('Precisión Regresión Logística:') print(logreg.score(X_train, y_train)) 
##Support Vector Machines 
svc = SVC() svc.fit(X_train, y_train) Y_pred = svc.predict(X_test) print('Precisión Soporte de Vectores:') print(svc.score(X_train, y_train)) 
##K neighbors 
knn = KNeighborsClassifier(n_neighbors = 3) knn.fit(X_train, y_train) Y_pred = knn.predict(X_test) print('Precisión Vecinos más Cercanos:') print(knn.score(X_train, y_train)) 
##########PREDICCIÓN UTILIZANDO LOS MODELOS########## 
ids = df_test['PassengerId'] df_test['Age'] = df_test['Age'].astype(float) ###Regresión logística 
prediccion_logreg = logreg.predict(df_test.drop('PassengerId', axis=1)) out_logreg = pd.DataFrame({ 'PassengerId' : ids, 'Survived': prediccion_logreg }) print('Predicción Regresión Logística:') print(out_logreg.head()) 
##Support Vector Machines
prediccion_svc = svc.predict(df_test.drop('PassengerId', axis=1)) out_svc = pd.DataFrame({ 'PassengerId' : ids, 'Survived': prediccion_svc }) print('Predicción Soporte de Vectores:') print(out_svc.head()) 
##
K neighbors rediccion_knn = knn.predict(df_test.drop('PassengerId', axis=1)) out_knn = pd.DataFrame({ 'PassengerId' : ids, 'Survived': prediccion_knn }) print('Predicción Vecinos más Cercanos:') print(out_knn.head())

