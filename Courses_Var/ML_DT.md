# `MACHINE` LEARNING PARA DATA SCIENCE

## APRENDIZAJE NO SUPERVIZADO

Descrobe la estructura de un conjunto de datos sin etiquetar por  lo que solo soran datos de salida.

### APRENDIZAJE Y BATCH

-   No aprenden de manera incremental por lo que para predicciones solo es para casos en concreto.

-   Funciona en sistomas que no roquieren conjuntos muy grandes ni adaptarse muy rapido

-   Es sencillo 

-   Muy restringido para problemas con pocos recursos como smartphone

### APRENDIZAJE ONLINE

-   Se caracterizan por ser incremental mediante el consumo incremental de mini batches

-   Solucion ideal para sistemas que reciben datos continuamente y requieren adaptarse 

-   Es capas de lidiar con conjuntos de datos que no entren en una maquina

-   Son suceptibles a errores si hay datos de baja calidad y en caso de que pase esto debemos empezar de un check point



## APRENDIZAJE BASADOS EN INTANCIAS Y EN MODELOS

-   El sistema aprende y generaliza para intentar en nuevos modelos

-   Se requiere **media de similitud**

## REGRESION LINEAL

-   Aprendizaje **supervizado** | conjunto de datos etiquetados

-   Aprendizaje **basado en modelos** | contruye una funcion de hipotesis

-   Se corresponde con un **modelo lineal**

-   Realiza predicciones computando una **suma ponderada de las caracteristicas de entrada** y sumandole una constante conocida como *bias*

-   Intenta predecir **valores continuos** | rangos amplios 

    

Conjunto de datos de entrenamiento (dataframe)

| Incidente | Numero Sistemas Afectados (*x*)\| features | Coste en Euros \| target value |
| --------- | ------------------------------------------ | ------------------------------ |
| i1        | 1000                                       | 2000                           |
| i2        | 2000                                       | 4000                           |
| i3        | 1200                                       | 23000                          |

>   *x* = variables de entrada
>
>   *y* = variables de salida
>
>   (*x,y*) = ejemplos de entrenamiento



### CONSTRUCCION DE MODELOS

-   Buscar los parametros **??0** y **??1** que generen la hipotesis (h**??**(*x*)) que se adapte al conjunto de datos de entrenamiento (*x,y*)

-   Se minimiza una funcion de coste (j(**??**)) para obtener los parametros **??0** y **??1** optimos
-   Se ajustara entre el valor real y la predicciones al entrenar un algoritmo de machine learning

>   h**??**(*x*) = funcion de hipotesis
>
>   j(**??**) = funcion de error



### FUNCION DE COSTE

Los algoritmos para predecir los valores estos van a recorrer los ejemplos de los datos de entrenamiento se ajustara entre la prediccion y el resultado que debera de predecir por diferencia del error con la funcion de coste J(??) o de error

La funcion basado en error de cuadrados o error cuadratico 

>   J(??)= 1/2 ??^m^~i=1~ (h??^(x^^(i)^)-y^(i)^)^2^
>
>   m = longitud de ejemplos de conjunto de datos
>
>   y^(i)^= Variable de salida para cada uno de los ejemplos de nuestro conjunto de datos de entrenamiento | y^1^ ,y^2^ ,Y^...^
>
>   h??^(x^^(i)^)= La funcion de hipotesis de la regresion lineal | valor de prediccion | h??(x^1^)= ??~0~ +??~1~ X1 | Funcion hipotesis 
>
>   ??= Valor que le damos, punto de partida y eje lineal de proyeccion (??^0^,??^1^)
>
>   J(??)= Error global de prediccion

Toma el valor que predice la funcion hipotesis para unos parametros *??~0~ y ??~1~* determinados y le resta el valor que deberia estar prediciendo y lo eleva al cuadrado. Esto para que no de un valor negativo

Para minimizar el error usa otra funcion llamada *Funcion de optimizacion* gracias a la funcion de error



### FUNCION DE OPTIMIZACION : *Gradient Descent*

Es ena funcion para reducir el error entre el pronostico y la realidad, y se basa en algo que se denomina gradiante que nos identifica como modificando los valores de entrada de una funcion varia el *output* de esa funcion

 Gradiente = Pendiente = Derivada de la funcion

>   $d/d~x~J(x) = 2(x-3)$???
>
>   x= x-?? d/d~x~J(x)
>
>   ??= Learning rate | velocidad con la que nos aproximamos a un punto minimo 
>
>   d= Derivada 

```
x=8-(1/2*10)=3 | x=8
x=3-(1/2*0)=3  | x=3
```

-   ?? Es el rango que nosotros elegimos para ir ajustando el valor
-   x el un valor inicial a eleccion
-   Si el valor final de iteracion se repite significa que el valor de hipotesis y el real son ideticos 

> h~??~^(x)^=g(??~0~+??~1~X~1~+??~2~X~2~) --> se basa en la pendiente -> ajustar ??~0~,??~1~ y ??~2~
>
> parametro = parametro - ?? ^dJ^/~dparametro~
>
> ?? = Margen de aprendizaje, velocidad con la que se va a acercar a un optimo global
>
> d =  Derivada parcial

Primero vamos a inicializar de un modo aleatorio y posteriormente actualizarlo

> ??~0~ = ??~0~ - ?? ^dj^/~d??~~0~ = ??~0~ - ?? * (h??(x) - y)
>
> ??~1~ = ??~1~ - ?? ^dj^/~d??~~1~ = ??~1~ - ?? *(x~1~ (h??(x) - y))
>
> ??~2~ = ??~2~ - ?? ^dj^/~d??~~2~ = ??~2~ - ?? *(x~2~ (h??(x) - y))

### 5 12 
