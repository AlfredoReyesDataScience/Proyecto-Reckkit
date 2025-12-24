# Proyecto Reckkit
El objetivo del proyecto es poder tratar datos de ventas reales de la empresa Reckkit México con el fin de poder predecir resultados futuros.

<img width="500" height="326" alt="image" src="https://github.com/user-attachments/assets/2d5f8d56-377d-43d2-b3f6-384adcc9e370" />
# Limpieza de datos
Se nos proporcionó una serie de archivos Excel y CSV con datos para poder procesarlos, con el fin de terminar haciendo únicamente una sola base de datos limpia y lista para  hacer modelos
<img width="1685" height="801" alt="image" src="https://github.com/user-attachments/assets/503b4e9d-d857-445c-8ab0-9b379b3b4566" />

# Análisis Exploratorio
Una vez los datos están listos, empezamos realizando un análisis exploratorio con el fin de conocer un poco más a lo que nos estamos enfrentando. Para esto realizamos una serie de gráficos en Python.

<img width="537" height="380" alt="image" src="https://github.com/user-attachments/assets/f1651b93-a548-46f7-812f-d803141fd816" />
<img width="521" height="550" alt="image" src="https://github.com/user-attachments/assets/50dd69b3-36af-46c8-aa44-c6f0c59d1eef" />

<img width="501" height="540" alt="image" src="https://github.com/user-attachments/assets/ddea5c38-535e-4921-a407-d0f96a9fca05" />
<img width="534" height="393" alt="image" src="https://github.com/user-attachments/assets/99d04ced-185e-43a4-99ed-b86f0c931e5d" />
<img width="543" height="387" alt="image" src="https://github.com/user-attachments/assets/b02b5b9e-7dc5-4e9d-a1a8-7798b897fb90" />

# Implementación de K-MEANS con la marca Vanish
En esta parte, realizamos un código para aplicar técnicas de clustering para identificar segmentos clave en los que la marca Vanish tiene presencia.

<img width="807" height="472" alt="image" src="https://github.com/user-attachments/assets/228cef3a-cec1-4c27-ae15-8b361514303e" />

# Filtración de datos para implementar primera parte del modelo K-MEANS
Usamos los datos relevantes para generar nuestra base de entrenamiento, transformando la columna “Región” que es una categórica a una con la que se pueda trabajar con la función get_dummies, y posteriormente, aplicamos la función de StandardScaler para que todos los valores tengan la misma escala y sea más fácil el modelado, usando K desde 2 a 98

<img width="921" height="514" alt="image" src="https://github.com/user-attachments/assets/06fb3edc-f96f-4c4c-8861-d0c36ab1d97c" />

# Determinación de K óptimo 
Posteriormente, vemos cuál es el mejor K y generamos nuevamente el modelo con el cluster óptimo, no sin antes graficar nuestras K obtenidas en el paso anterior, en este caso, el número de K óptimo es 5.
<img width="682" height="544" alt="image" src="https://github.com/user-attachments/assets/740b1df3-b524-42ca-9ae7-b9f2d13edf8f" />

Copia de Vanish para K óptimo
Aquí guardamos en un dataframe añadiendo una columna con el Cluster óptimo al cuál pertenece cada renglón
<img width="920" height="530" alt="image" src="https://github.com/user-attachments/assets/3a452f3e-22fa-4793-831d-09e42b1f0872" />

Gráfico de dispersión de Clusters

<img width="1162" height="544" alt="image" src="https://github.com/user-attachments/assets/1d2773a4-6ad4-4ff6-a6cd-517a77f07481" />

Gráfico de Tamaño de Clusters 
En este gráfico de barras, podemos observar que el mayor número de observaciones lo tuvo el cluster 1

<img width="822" height="479" alt="image" src="https://github.com/user-attachments/assets/cf835fe5-11d9-4014-ae70-e0678428be78" />

# Implementación de Base de Datos en SQL

Primero que nada, cambiamos los archivos .xslx a .csv para que sea más sencillo crear las tablas en SSMS. Creamos nuestra base de datos de la siguiente manera:
Damos clic derecho en bases de datos>Nueva base de datos 
<img width="659" height="533" alt="image" src="https://github.com/user-attachments/assets/f92add79-2c21-4ea2-ab4a-02bb9cfd5b54" />
Al entrar en la parte como se muestra en la primer imagen, se crea la base de datos y para cargar los archivos, es dar clicderecho en nuestra base de datos recién creada, damos clic en Tareas>Importar archivo plano
<img width="651" height="617" alt="image" src="https://github.com/user-attachments/assets/1b86906e-196a-4ebd-8eee-d192c92a774a" />

<img width="881" height="688" alt="image" src="https://github.com/user-attachments/assets/b65a5de7-0f94-4d60-b1b1-1ea0868764f8" />

Se abre una ventana como la primer imagen y posteriormente le damos en examinar para cargar nuestros archivos.

<img width="666" height="601" alt="image" src="https://github.com/user-attachments/assets/021bc0d4-6026-466c-b794-51a90fa9c3bc" />

<img width="466" height="339" alt="image" src="https://github.com/user-attachments/assets/94bbb4e6-3bd4-4620-9a79-6c18b7865fa3" />

Ahora si, podemos empezar con nuestros Querys que sean necesarios.

<img width="1505" height="803" alt="image" src="https://github.com/user-attachments/assets/98f21b00-6eef-48c2-bc8e-b013ddaa4d93" />

Realización de Gráficos en Power BI
Posteriormente, se conectó nuestra BD de SQL con Power BI para hacer gráficos dinámicos, empezando por ventas generales.

<img width="967" height="557" alt="image" src="https://github.com/user-attachments/assets/2dbb1877-71de-4ae3-be40-f3ffda618551" />

Ventas por Segmento  y promedios semanales
<img width="773" height="420" alt="image" src="https://github.com/user-attachments/assets/e65b1f99-5dc2-4a18-be19-7f248f267873" />
<img width="773" height="420" alt="image" src="https://github.com/user-attachments/assets/ae168001-1544-4bcd-8b1e-60def6856205" />

Ventas por clasificación, marca y descripción
<img width="970" height="563" alt="image" src="https://github.com/user-attachments/assets/b9c5976a-96a6-4ea2-80be-54706edd1131" />

# Modelado ARIMA para Lysol y Vanish
Filtramos las marcas deseadas para nuestra serie de tiempo, haremos un análisis ARIMA ya que creo que es lo más apropiado debido a la gran cantidad de variables no relevantes que existen dentro de nuestos datos, como lo son el Item_code, Manufacturer, Item, etc.

<img width="798" height="582" alt="image" src="https://github.com/user-attachments/assets/6f6efbfb-5962-4792-b858-31b4177ad46f" />

Prueba Dickey-Fuller
<img width="773" height="416" alt="image" src="https://github.com/user-attachments/assets/57beccad-f7fa-4c46-913f-320f3d5b1332" />

Comparación Arima con AIC
<img width="774" height="416" alt="image" src="https://github.com/user-attachments/assets/7847fecb-569f-49f9-8fa0-3d50b321f9e2" />


Ajuste de modelo ARIMA(3,1,3)
<img width="577" height="432" alt="image" src="https://github.com/user-attachments/assets/ceee7e15-2e75-45d9-95cd-8f23de909f11" />

Graficamos con IC = 95%

<img width="540" height="432" alt="image" src="https://github.com/user-attachments/assets/f0d82d71-01d4-4de4-825a-63e0c43827a3" />

Predicciones

<img width="601" height="432" alt="image" src="https://github.com/user-attachments/assets/0af29a1f-2403-4632-abf2-ff48d84e8d34" />

Métricas de Error

<img width="774" height="255" alt="image" src="https://github.com/user-attachments/assets/21ad3ece-293e-4c65-9115-acd198543cff" />


Como podemos observar, el MAPE = 8.06%, lo que indica un buen desempeño en el modelo para la confiabilidad de sus predicciones, respecto a la gráfica, podemos observar que la mayoría de nuestra base de prueba está dentro del intervalo de confianza, si acaso hubo un pico entre mayo y julio, que pudo haberse debido a algún factor externo como pudiera ser algún pedido grande o alguna demanda anormal en el mercado. Sin embargo, en media general se encuentra bien el modelo y es bastante confiable.













