# trabajo_econometria_7 de Eliut  y Manuel Diaz#

Modelo Logit.
•	Probabilidad de tener ganancias o pérdidas de capital de una acción en la BMV.
o	Y = Gana o pierde valor una acción.
o	X1 = Razón ganancia/capital (nivel de endeudamiento).
o	X2 = Número de acciones de esa empresa en circulación. (tengo dudas de donde sacar datos de esta…)
o	X3 = Rendimientos históricos de la bolsa (BMV).
o	X4 = Riesgo país.
o	X5 = Rendimientos históricos de la acción.
o	X6 = Tasa impositiva histórica aplicable
Tarea.
Hacemos una correcta predicción si el resultado del modelo (al momento de darle números a las variables explicativas) es acorde con la observación. Para el caso del modelo probit, esto sucede si (yi, ȳi) son las siguientes combinaciones (1,1) y (0,0). 
1.	¿Qué es el APE?
Los coeficientes dan señales sobre el efecto parcial de cada variable explicativa en la probabilidad dada como respuesta.
Para obtener las magnitudes de los efectos parciales de cada b en el modelo, es bueno tener un único escalar que multiplique a cada beta, generalmente se reemplaza cada variable explicativa x con sus respectivos promedios. La idea es que al multiplicarlos con las betas, obtenemos el efecto parcial de xi para la unidad promedio de la muestra. Por lo tanto, si a la idea anterior la multiplicamos por un escalar, se obtiene el PEA. Este método no funciona cuando metemos variables dicotómicas (el promedio no representa a la muestra) o si las variables continuas no son lineales.
Otra opción es promediar el efecto parcial individual a lo largo de cada muestra. Esto nos lleva al APE. Que es (para el caso continuo) la multiplicación de las bj con el promedio de la suma del intercepto con la multiplicación de la bi con su muestra (xi) correspondiente utilizando una de las formas funcionales, ya sea la normal (caso probit) o la sigmoide (caso logit). El término bj sirve, para este caso, como un escalar. El resultado es un efecto parcial ya que todas las variables explicativas diferentes de xi se mantienen fijas
Los dos escalares pueden ser diferentes porque en el último se usa el promedio de la función no-lineal en lugar de la función no lineal del promedio. Cabe mencionar que si usamos variables discretas como explicativas ambos métodos no funcionan.
2.	Odd Ratio.
Un odd es la probabilidad de que suceda un evento, dividido por la probabilidad de que no suceda. Se interpreta como la cantidad de veces que algo pueda suceder sobre la cantidad de veces que no suceda.  Un Odd ratio es una medida que se utiliza cuando queremos ver la relación, fortaleza y dirección de una posible asociación entre 2 variables.
Entre dos variables, un odd ratio, es el cociente del odd de la primera entre el odd de la segunda, siendo la variable a explicar la del numerador y la explicativa la del denominador.
3.	Pseudo R2.
Para este tipo de modelos existen varias Pseudo R2. Para McFadden esta se obtiene usando: 1 menos el cociente de la función logarítmica de probabilidad (verosimilitud) del modelo estimado entre la función logarítmica de probabilidad del mismo modelo con una sola variable. Si las covarianzas no sirven entonces la R2 será 0. También podemos estimarla obteniendo el cuadrado de la correlación entre las observaciones (yi) y las estimaciones (ŷi). En general, mide el grado de mejora en el ajuste del modelo de probabilidad con respecto al modelo sin predictores. 
4.	Prediction in sample vs. out of sample.
Un pronóstico dentro de la muestra utiliza el subconjunto de datos disponibles para pronosticar valores dentro de la misma muestra, para después compararlos con resultados conocidos.
Por otro lado, un pronóstico fuera de la muestra utiliza los datos muestrales para pronosticar una observación que no forma parte o está fuera de la muestra.
5.	Tercer método para definir qué valores son 0 y 1.
Una medida de la bondad de ajuste, para este tipo de modelos, es el “Percent Correctly Predicted” (porcentaje correctamente predicho). El libro describe tres posibles formas.
La tercera consiste en: elegir el límite tal que la fracción de éxitos (obtenidos por el modelo) en la muestra sea el mismo o este muy cerca del número de éxitos observados. Buscar valores t, entre 0 y 1, tal que si definimos yi estimada = 1 cuando G (b0+b1X) ≥ t, entonces la sumatoria de las yi estimadas será aproximadamente igual a la sumatoria de las yi observadas 

