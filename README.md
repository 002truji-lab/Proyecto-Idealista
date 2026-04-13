### Proyecto Colaborativo: Análisis Exploratorio y Modelado Estadístico
### Dataset: Idealista 2018

### Contexto del Dataset

El dataset contiene anuncios de viviendas en venta publicados en Idealista 
durante el año 2018 en tres ciudades españolas: Madrid, Barcelona y 
Valencia. 

Los datos provienen de dos archivos CSV que combinados suman casi **200.000** aproximadamente

Tras el proceso de limpieza el dataset final cuenta con **189.923** viviendas 
limpias y sin duplicados. Dejando las siguientes columnas en un nuevo CSV 
limpio df_idealista_limpio.csv para trabajar en las Fase2, las columnas 
finales serian las siguientes:
- - -
`ASSETID, PERIOD, PRICE, UNITPRICE, CONSTRUCTEDAREA, ROOMNUMBER, BATHNUMBER, HASTERRACE, HASLIFT,
HASAIRCONDITIONING, HASPARKINGSPACE, ISPARKINGSPACEINCLUDEDINPRICE, PARKINGSPACEPRICE, HASNORTHORIENTATION,
HASSOUTHORIENTATION, HASEASTORIENTATION, HASWESTORIENTATION, HASBOXROOM, HASWARDROBE, HASSWIMMINGPOOL,
HASDOORMAN, HASGARDEN, ISDUPLEX, ISSTUDIO, ISINTOPFLOOR, CONSTRUCTIONYEAR, FLOORCLEAN, FLATLOCATIONID,
CADCONSTRUCTIONYEAR, CADMAXBUILDINGFLOOR, CADDWELLINGCOUNT, CADASTRALQUALITYID, BUILTTYPEID_1, BUILTTYPEID_2,
BUILTTYPEID_3, DISTANCE_TO_CITY_CENTER, DISTANCE_TO_METRO, DISTANCE_TO_STREET, LONGITUDE, LATITUDE,
CITYNAME, PRECIO_POR_METRO, LOG_PRICE, LOG_CONSTRUCTEDAREA, LOG_DISTANCE_TO_CITY_CENTER, LOG_DISTANCE_TO_METRO,
LOG_PRECIO_POR_METRO, bin_tipo_acabado, bin_floorclean, bin_habitaciones, bin_baños, bin_tipo_edificio,
bin_categoria_edificio, Z_LOG_PRICE, Z_LOG_CONSTRUCTEDAREA, Z_LOG_DISTANCE_TO_CITY_CENTER, Z_LOG_DISTANCE_TO_METRO`
- - -

### Preguntas de Investigación
---
Las preguntas que ha realizado el grupo de proyecto.
---
- 1 - Pisos con mas habitaciones tiene precios mas altos ?
- 2 - Los pisos construidos en el años 1998 en Barcelona cuestan lo mismo, que los pisos construidos en el mismo año en Madrid ?
- 3 - Los pisos de Madrid y Barcelona son iguales en metros cuadrados ?
- 4 - Los pisos de Madrid cercanos al centro de la ciudad ( 2 km ),tienen precios mas altos, que los de Barcelona ?


### Conclusiones de las respuestas

- - -
### 1 - Pisos con mas habitaciones tiene precios mas altos ❓
- - -
👉 Valores estadisticos del test de ( Mann-Whitney U )
- - -
Estadístico  : 3027488.5  ( valor {u} )  
p-value      : 0.0 ( p_value {p_value} )
- - -
⚠️ Conclusión del test de Mann-Whitney U
- - -
α = 0.05
p-value = 0.0

Rechazamos H0 → Los pisos con mas de 4 habitaciones tienen precios diferentes a los pisos con 4 o menos habitaciones
- - -
⚠️ Conclusion de las graficas
- - -
Podemos concluir que rechazamos la hipotesis nula H0, ya que las probabilidades de que un piso con 4 habitaciones o menos, tenga el mismo precio, que un piso con mas de 4 habitaciones es muy pequeña , casi nula, con la siguiente grafica apoyamos nuestra hipotesis
- - -



### 2 - Los pisos construidos en el años 1998 en Barcelona cuestan lo mismo, que los pisos construidos en el mismo año en Madrid ❓
- - -
👉 Valores estadisticos del test de ( Mann-Whitney U )
- - -
Estadístico  : 20214.5  ( valor {u} )  
p-value      : 0.029719035456255788 ( p_value {p_value} )
- - -
⚠️ Conclusión del test de Mann-Whitney U
- - -
α = 0.05
p-value = 0.029719035456255788

Rechazamos H0 → Los pisos construidos en el año 1998 tienen precios diferentes en Barcelona y Madrid
- - -
⚠️ Conclusion de las graficas
- - -
Podemos concluir que rechazamos la hipotesis nula H0, como vimos con los test y en la grafica, los precios de los pisos de Madrid contruidos en el año 1998, son diferentes a los de Barcelona, en la grafica se ve claramente que los de Madrid cosntruidos en el año 1998, son mas caros que los de Barcelona.
- - -




### 3 - Los pisos de Madrid y Barcelona son iguales en metros cuadrados ❓
- - -
👉 Valores estadisticos del test de ( Mann-Whitney U )
- - -
Estadístico  : 12583715.0  ( valor {u} )  
p-value      : 0.5618907578865159 ( p_value {p_value} )
- - -
⚠️ Conclusión del test de Mann-Whitney U
- - -
α = 0.05
p-value = 0.5618907578865159

No podemos rechazar H0  → Las superficies de los pisos en Madrid y Barcelona son iguales
- - -
⚠️ Conclusion de las graficas
- - -
Podemos concluir que rechazamos la hipotesis nula H0, como vimos con los test y en la grafica, los precios de los pisos de Madrid contruidos en el año 1998, de los pisos de Madrid y Barcelona en cuanto a superficie son iguales, en la grafica vemos tambien, la similitud entre estas distribuciones
- - -



### 4 - Los pisos de Madrid cercanos al centro de la ciudad ( 2 km ),tienen precios mas altos, que los de Barcelona ❓
- - -
👉 Valores estadisticos del test de ( Mann-Whitney U )
- - -
Estadístico  : 10417082.5  ( valor {u} )  
p-value      : 3.3420885178604915e-47 ( p_value {p_value} )
- - -
⚠️ Conclusión del test de Mann-Whitney U
- - -
α = 0.05
p-value = 3.3420885178604915e-47

Rechazamos H0 → Los precios de los pisos en Madrid y Barcelona son diferentes para los pisos cercanos al centro de la ciudad
- - -
⚠️ Conclusion de las graficas
- - -
Podemos concluir que rechazamos la hipotesis nula H0, como vimos con los test, las distribuciones de los precios de los pisos con una distancia de ( 2 km ) al centro de la ciudad, son diferentes en Madrid y Barcelona, en la grafica se ve claramente que los precios de los pisos cercanos al centro de Madrid  son mas altos que los de Barcelona
- - -



### Estructura del Repositorio
proyecto-01-datos/
├── .git/
├── Fase1_Proyecto_Colaborativo_Idealista.ipynb
├── Fase2_Proyecto_Colaborativo_Idealista.ipynb
├── Proyecto Colaborativo.ipynb
├── Idealista/
    ├── idealista18_1.csv
    ├── idealista18_2.csv
    └── Xlsx/

- - -

### Tecnologías Utilizadas

- Python 3.14
- Pandas, NumPy
- Matplotlib, Seaborn
- Scipy (tests estadísticos)
- Scikit-learn (regresión lineal)

---

### Equipo

Proyecto desarrollado como trabajo colaborativo del bootcamp de Ciencia de Datos e IA 2026
