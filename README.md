# Analizando_a_Metacritic

Análisis de Prensa de Videojuegos  Autor: Christopher Orea. Admin de TheHappyCookieHour El motivo del presente notebook es análizar a la prensa de videojuegos y abarcar la tan llamada guerra de consolas.   Se intentará evaluar si existe o no preferencia hacia alguna compañía en especial. Por lo útilizaremos análisis de datos, prueba de hipotesís y un poco de ciencia de datos para entender que sucedió entre 2011 y 2019 con respecto a la forma de evaluar los videojuegos de esa época.

Se utilizó el dataset de Metacritic Games de Kaggle. Puedes encontrarlo en la siguiente liga para cargarlo y hacer la prueba de este notebook.

https://www.kaggle.com/skateddu/metacritic-games-stats-20112019

## Número de jugadores por compañías

Estamos intentando explorar los datos y probar la creencia de que solo en Xbox se tienen más juegos para jugar entre más jugadores que Play Station.

Por lo que evaluaremos un Ratio entre total de juegos y cantidad de juegos que puedes jugar a:

*   Múltijugador local
*   Múltijugador en linea
*   Jugar a un solo jugador.


![image](https://user-images.githubusercontent.com/21028835/109438707-b7eff380-79f0-11eb-9ecd-224079c84653.png)
Parece ser que en la mayoría de los juegos que van de 1 hasta 8 jugadores, playstation nutre un catálogo que se enfoca exclusivamente a esto, en mayor medida que Xbox.

Mientras que Xbox nutre su catalogo de juegos de 6 hasta 16 en mayor medida que Playstation.

## Graficando la relación de los datos.

![image](https://user-images.githubusercontent.com/21028835/109438739-d0600e00-79f0-11eb-8d76-73c2e2969306.png)

## Información similar

¿Es la prensa una imagen de lo que los usuarios piensan de la industria?

Vamos a probar si la prensa y las puntiaciones de los usuarios estan relacionadas o son similares

H0: puntiación prensa == puntuación usuarios

HA: puntiación prensa =/= puntuación usuarios

Usaremos Chi cuadrado para evaluar la diferencia entre medias.

### Resultados
Chi2 value= 0.24031609979784996

p-value= 0.8867802701087308

Degrees of freedom= 2

Expected Result = 

[[76.07202852 70.340519]

[70.31508152 65.01731876]

[71.14242102 65.78232387]]

 
El Valor P es de .88 o de 88%. Esto indica que es 88% probable de que H0 sea correcta. 

Nos interesa tener presente que si esta por debajo de .05 o 5%, ya que si esta por debajo de este valor significa que podríamos sospechar que la H0 no satisface los datos y la HA sí.

## Gráfica de Prensa con respecto a compañías

![image](https://user-images.githubusercontent.com/21028835/109438773-eec60980-79f0-11eb-9905-f0b9db4e3cc1.png)

Parece ser que Switch y XONE se relacionan. Comparten rangos similars. Sin embargo Playstation es diferente.

## Gráfica de Puntuaciones de Usuarios con respecto a compañías.

![image](https://user-images.githubusercontent.com/21028835/109438777-f5ed1780-79f0-11eb-9bb3-32073c7908a9.png)

Tanto XBOX como Playstation tienen más amplitud de datos.
Nintendo parece tener un trato especial por parte de los usuarios.

## Diferencias y relaciones entre Público de PS4 y Prensa:

### H0: Calificación Prensa == Calificación Usuarios
### HA: Calificación Prensa =/= Calificación Usuarios

F-score: 223.17208811288273, p-value: 1.2050744184861254e-48

![image](https://user-images.githubusercontent.com/21028835/109438796-1026f580-79f1-11eb-95f4-837265ef141e.png)

Parece que hay grandes diferencias de lo que piensan los usuarios de play a lo que dice la prensa realmente. En este caso son más bajas las notas que dan los usuarios a lo que realmente la prensa dice ser.

## Diferencias y relaciones entre Público de Switch y Prensa:

### H0: Calificación Prensa == Calificación Usuarios
### HA: Calificación Prensa =/= Calificación Usuarios

F-score: 2.616732903648962, p-value: 0.10604229989059531

![image](https://user-images.githubusercontent.com/21028835/109438822-377dc280-79f1-11eb-97e7-804a7d1c9f3d.png)

Con Switch es el caso contrario a Playstation. Estos comparten similitud, solo que los valores más extremos positivos no son puntuados por los usuarios y la prensa sí.

## Diferencias y relaciones entre Público de XONE y Prensa:

### H0: Calificación Prensa == Calificación Usuarios
### HA: Calificación Prensa =/= Calificación Usuarios

F-score: 166.1701235257701, p-value: 3.284521622933438e-36

![image](https://user-images.githubusercontent.com/21028835/109438830-45cbde80-79f1-11eb-8fb2-243c798e2888.png)

Es el mismo caso que PS4. Los usuarios tienden a ver peor de lo que la prensa ve a XONE.

## Prueba de Varianza.

### H0: Las compañías varian de igual medida entre ellas. 

Switch = XONE = PS4

### HA: Las compañías varian diferente
Switch ≠ XONE ≠ PS4

XONE y Switch: F-score: 3.0756516432462715, p-value: 0.07970693408287087

XONE y PS4: F-score: 8.711307247864388, p-value: 0.0031957015012337004

Switch y PS4: F-score: 20.155928277505357, p-value: 7.554222030822733e-06


Existe una relación entre como varian los juegos tanto buenos como malos de Switch y XONE por parte de la prensa.

Si hablamos de PS4, esta se vé muy diferente tanto por parte de XONE como de Switch. Esta estando más distante de Switch que XONE.



## Porcentaje de Juegos Buenos y Porcentaje de Juegos Malos en cada plataforma por total de juegos

Nos interesa saber cual es el rango de puntuaciones para el decil más alto y bajo. 

En este caso probamos saber el 10% más bajo y el 10% más alto e intentamos saber que compañía tiene más juegos en estos rangos con respecto a su catálogo.

Para los juegos mejor puntuados tenemos el siguiente orden para los juegos de catálogo en el 10% mejor puntuado.


1.   XONE con 9.44% 
2.   Switch con 8.56%
3.   PS4 con 6.65

Para los juegos peor puntuados tenemos el siguiente orden para los juegos de catálogo en el 10% mejor puntuado.

(Mientras menor sea el dato, mejor catálogo tienen)


1.   Switch con 6.65% 
2.   XONE con 9.57%
3.   PS4 con 11.20%


## Conclusiones Finales:


### XONE:
Es la que más juegos de su catálogo estan en el 10% mejor puntuado por la prensa y la segunda más separada de lo que se observa con la preferencia de los usuarios y lo que la prensa observa.

La calidad de sus juegos considerados por la prensa se asemejan más a los de Switch. Las pruebas indican que su rendimiento es igual de favorable, a pesar de no ser la opción preferida por el público.


### Switch:
Es la empresa que más apegada esta a lo que ve la prensa y lo que ven los usuarios. 

Es la que más se asemeja a la variación de XBOX. No son tán diferentes.

Es la compañía con menos juegos y la que menos juegos tiene en su catálogo en el 10% peor puntuado por la prensa.

Se podría pensar que es favorecida por la prensa por poner juegos con mayor puntiación que los usuarios. Sin embargo, las pruebas muestran que hay más similitud entre lo que sienten los usuarios y lo que la prensa observa.



#### PS4: 
A pesar de tener a PS4 como una compañía con muchos juegos, tiene mayoría en el 10% de los peores puntuados.

Es el que más alejado esta entre lo que dice la prensa y lo que los usuarios perciben.

Es el que está más disperso de las tres compañías, no comparte ni la misma variación. Hay datos suficientes para poder asumir que podría haber sido favorecida por la prensa durante la época del 2011 y 2019.

Créditos: Christopher Orea.
christopheroreaalegre@gmail.com
