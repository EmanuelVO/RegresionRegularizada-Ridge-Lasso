# RegresionRegularizada-Ridge-Lasso

1. Considere la base de datos siguiente: FuelConsumptionCo2.xlsx

2. Elimine las columnas de tipo categórico de la base de datos y verifique que no existan datos nulos que deban ser eliminados de manera previa al análisis.

Se eliminaron las columnas 'MODELYEAR', 'MAKE', 'MODEL', 'VEHICLECLASS', 'TRANSMISSION', 'FUELTYPE'.

3. Realice un análisis de regresión múltiple para pronosticar la variable “CO2 EMISSIONS” con las variables remanentes. Obtenga los indicadores de bondad de ajuste correspondientes (R cuadrada, Error medio absoluto, etc.). Utilice los coeficientes resultantes y pronostique la primera observación de la base de prueba. ¿Coincide su resultado con aquel obtenido con la instrucción “predict”? Explique.

Intercepto:  388.74250128235667
Coeficientes: -116.50352944,  111.94245879,  -28.55294687,  -57.30206895,  329.02984369,  -281.56796432

Pronóstico de la primera observación de la base de prueba: -6588.970957818888

Pronóstico obtenido con la instrucción “predict”: 242.05056484

Valor de R2:  0.9101041999638888
Error absoluto medio:  7.582278595997424
Error cuadratico medio:  311.19797055029375
Raiz del error cuadratico medio:  17.64080413559126

Explicación: a veces, al sacar manualmente los valores de valores_x, el orden puede no coincidir exactamente con el orden de los coeficientes, especialmente si el modelo fue entrenado con un DataFrame que tiene columnas ordenadas alfabéticamente o si tu subconjunto de prueba fue manipulado. Seguramente hay una desalineación en el orden de las variables o en el preprocesamiento. Lo más recomendable es usar .predict() siempre que puedas, ya que así evitas errores manuales y aprovechas todo el pipeline del modelo.

4. Repita el ejercicio 3 pero aplicando un modelo de regresión Ridge mediante el valor de Alpha óptimo.

Valor de R2:  0.9127388477539915
Error absoluto medio:  7.450651668123023
Error cuadratico medio:  302.07744383975273
Raiz del error cuadratico medio:  17.38037525025719

5. Repita el ejercicio 3 pero aplicando un modelo de regresión Lasso mediante el valor de Alpha óptimo.

Valor de R2:  0.9067951896584938
Error absoluto medio:  7.453202795795379
Error cuadratico medio:  322.65298058585995
Raiz del error cuadratico medio:  17.962543822795812

6. ¿Cuál de los 3 modelos de regresión resultó ser el mejor? Explique a detalle.

El modelo de regresión Ridge obtuvo los mejores resultados de acuerdo con los indicadores de bondad de ajuste mostrados en el punto 4.
