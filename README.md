EJERCICIO 1: EXPLORACIÓN Y LIMPIEZA
El csv Customer Flight Activity está en el dataframe llamado: df_activity_flight. 

Tiene 405.624 filas y 10 columnas. Los nombres de las columnas son: 'Loyalty Number', 'Year', 'Month', 'Flights Booked', 'Flights with Companions', 'Total Flights', 'Distance', 'Points Accumulated', 'Points Redeemed', 'Dollar Cost Points Redeemed'.

Este csv tiene un 0,46% de filas duplicadas, en concreto 1.864 filas de 405.624.

Respecto a los valores nulos, no tiene ninguno.

El csv Customer Loyalty History está en el dataframe llamado: df_activity_loyalty.
Tiene 16.737 filas y 16 columas. Los nombres de las columnas son: 'Loyalty Number', 'Country', 'Province', 'City', 'Postal Code', 'Gender', 'Education', 'Salary', 'Marital Status', 'Loyalty Card', 'CLV', 'Enrollment Type', 'Enrollment Year', 'Enrollment Month', 'Cancellation Year', 'Cancellation Month'.
Este csv no tiene ningún valor duplicado pero si tiene 4.238 valores nulos en salario (un 25,32%), 14.670 en Cancellation Year (un 87,65%) y la misma cantidad en Cancellation Month.

Elimino los duplicados de Flight para limpiar más el data frame.

Uno los dos data frame analizados y sin duplicados creando uno común llamado df_union
df_union tiene 403.760 filas y 25 columnas siendo el nombre de estas: 'Loyalty Number', 'Year', 'Month', 'Flights Booked', 'Flights with Companions', 'Total Flights', 'Distance', 'Points Accumulated', 'Points Redeemed', 'Dollar Cost Points Redeemed', 'Country', 'Province', 'City', 'Postal Code', 'Gender', 'Education', 'Salary', 'Marital Status', 'Loyalty Card', 'CLV', 'Enrollment Type', 'Enrollment Year', 'Enrollment Month', 'Cancellation Year', 'Cancellation Month'.

Limpieza de datos: Para hacerlo visualmente más cómodo, modifico los nombres de las columnas a minúscula con la función lower. Además, el espacio entre las palabras compuestas, las cambio por _.

También observo que en ‘Cancellation Year’ y ‘Cancellation Month’ tiene un punto detrás del año y del mes, lo modifico reemplazando el . por un espacio. Esto me ha generado problema porque eran valores tipo float y con un lower y un replace se ha quedado solucionado.

Como no limpié los duplicados en el Data Frame de Flight, en el Data Frame de Union siguen habiendo los mismos duplicados, un 0,46%.

Observo que hay valores negativos en Salary e interpreto que es por un error en la incorporación por lo que cambio los valores negativos a positivos.
También, observo que hay relación entre la educación y el tipo de educación. Todos los que pertenecen en ‘Education’ a ‘College’ tienen valores nulos en ‘Salary’. Dichos valores los reemplazo con 0 para quitar los nulos.

Otra modificación para la limpieza de datos con el fin de que se pueda visualizar mejor, creo dos columnas nuevas llamadas ‘cancellation_month_year’ y ‘enrollment_month_year’ con el fin de unificar, por un lado, ‘cancellation_month’ y ‘cancellation_year’, y,por otro, ‘enrollment_month’ y ‘enrollment_year’.

Una vez realizada la limpieza, calculo diversas frecuencias tales como porcentajes, moda y nulos de todas las columnas del Data Frame.

Posteriormente, realizo una correlación entre variables numéricas y realizo dos gráficos para visualizar mejor los resultados.

EJERCICIO 2: VISUALIZACIÓN

 He realizado distintos gráficos tales como Lineplot, Scatterplot, Barplot, Pieplot y Pivot.plot

