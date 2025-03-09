# Proyecto de ciencia de datos aplicada (Capstone) del Certificado Profesional en Ciencia de Datos de IBM
El proyecto tuvo como objetivo el predecir si la primera etapa del Falcon 9 aterrizará con éxito. 
## Contexto
SpaceX anuncia lanzamientos de cohetes Falcon 9 en su sitio web con un costo de 62 millones de dólares; otros proveedores cuestan más de 165 millones de dólares cada uno; gran parte de los ahorros se deben a que SpaceX puede reutilizar la primera etapa. Por lo tanto, si se puede determinar si la primera etapa aterrizará, se puede determinar el costo de un lanzamiento. Esta información se puede utilizar si una empresa alternativa desea presentar una oferta contra SpaceX para el lanzamiento de un cohete. La mayoría de los aterrizajes fallidos están planificados. Space X realiza un aterrizaje controlado en los océanos.
## Fase 1:
Para esta fase se inició con la recopilación de los datos a partir de la API de Space X utilizando la solicitud GET. Posteriormente se realiza la manipulación y el análisis de los datos utilizando los métodos como replace para los valores faltantes utilizando la media de los datos existentes. En esta fase de recopilaron y se aseguraró que los datos estén en el formato correcto desde una API. 
## Fase 2:
En esta fase del proyecto se realizó un raspado web para recopilar los registros históricos del lanzamiento del Falcon 9 de una página de Wikipedia titulada Lista de lanzamientos de Falcon 9 y Falcon Heavy: https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches
Se extrajo una tabla HTML de los registros de lanzamientos, posteriormente la tabla se transformó en un marco de datos de Pandas para realizar su análisis.
## Fase 3:
Esta fase consistió en la manipulación de los datos y posteriormente se realizó el análisis exploratorio (EDA) para encontrar patrones en los datos y determinar las etiquetas para entrenar los modelos de aprendizaje automático supervisados. Se genera el dataframe que lee el archivo CSV y posteriormente realizamos algunas determinaciones para las columnas; Lauchsite, orbit, outcome. Determinando la cantidad que se repite cada uno de sus datos utilizando el método .value_counts(). Posteriormente se generan las etiquetas de clase 0 y 1 para lanzamientos fallidos y exitosos respectívamente y se genera la columna correspondiente en el marco de datos, "Class". Por último se determina la media o tasa de éxito para esta columna, de la cual se concluye que más de la mitad (66%) de los lanzamientos se han realizado de forma exitosa.
## Fase 4:
En esta fase se realizan consultas SQL en el archivo CSV Conjunto de datos de SpaceX. Se inicia proporcionando el comando %load_ext sql para poder realizar consultas SQL en el cuaderno de Jupyter, después de cargar las librerías necesarias se conecta con la base de datos a través del comando %sql sqlite:///my_data1.db. Se eliminaron las filas con que contenían datos en blanco y posteriormente se generó la tabla SPACEXTBL para realizar las consultas en esta. Se relizando cosultas buscando la fehca del primer lanzamiento exitoso, la carga total de los propulsores de la NASA, etc. Adicional a esto, se realizaron búsquedas más complejas que requierieron el uso de agrupaciones y subconsultas.
## Fase 5:

## Fase 6: 

## Fase 7:
