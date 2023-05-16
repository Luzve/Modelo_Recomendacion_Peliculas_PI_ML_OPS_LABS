<h1 align="center"><strong>MODELO DE RECOMENDACIÓN DE PELÍCULAS</strong></h1>

<p align="center">
<img src="src\movies.jpg"  height=300>
</p>

<h2><strong>DESCRIPCIÓN: </strong></h2>

_En este modelo de ML, se resuelve un problema creando un sistema de recomendación de películas a una star-up, que provee servicios de agregación de plataformas de streaming._

_El modelo recomienda películas a los usuarios basándose en películas similares, por lo que se debe encontrar la similitud de puntuación entre esa película y el resto de películas._

_También ordena según el score de similaridad y devuelve una lista con valores, cada uno siendo el nombre de las películas con mayor puntaje._

<h2><strong>INSTALACIÓN: </strong></h2>

1. _Clonar proyecto._
2. _Ir a Visual Code y abrir carpeta a usar._
3. _Crear tu entorno virtual y activarlo._
4. _Instalar requirements.txt._
5. _Correr el ambiente local._

<h2><strong>COMPILACIÓN: </strong></h2>

1. **[ETL](https://github.com/Luzve/PI_ML_OPS_LABS/blob/main/etl.ipynb)** 

* _belongs_to_collection, production_companies y otros, deberán desanidarlos para poder acceder a los datos y unirlos al dataset para luego hacer una consulta en la API._

* _Los valores nulos de los campos revenue, budget deben ser rellenados por el número 0._

* _Usar este formato AAAA-mm-dd, y crear la columna release_year donde extraerán el año de la fecha de estreno._

* _Crear la columna return con los campos revenue y budget, dividiendo estas dos últimas revenue / budget, cuando no hay datos disponibles para calcularlo, deberá tomar el valor 0._

* _Eliminar columnas video,imdb_id,adult,original_title,vote_count,poster_path y homepage._


2. **[API](http://127.0.0.1:8000/docs)**

* Uso de framework FastAPI.

* Render para el deploy del proyecto.

* **[Endpoints.](https://github.com/Luzve/PI_ML_OPS_LABS/blob/main/main.py)**
Crear 6 funciones que se consumirán en la API.

* _def peliculas_mes(mes): '''Se ingresa el mes y la funcion retorna la cantidad de peliculas que se estrenaron ese mes (nombre del mes, en str, ejemplo 'enero') historicamente''' return {'mes':mes, 'cantidad':respuesta}_

* _def peliculas_dia(dia): '''Se ingresa el dia y la funcion retorna la cantidad de peliculas que se estrenaron ese dia (de la semana, en str, ejemplo 'lunes') historicamente''' return {'dia':dia, 'cantidad':respuesta}_

* _def franquicia(franquicia): '''Se ingresa la franquicia, retornando la cantidad de peliculas, ganancia total y promedio''' return {'franquicia':franquicia, 'cantidad':respuesta, 'ganancia_total':respuesta, 'ganancia_promedio':respuesta}_

* _def peliculas_pais(pais): '''Ingresas el pais, retornando la cantidad de peliculas producidas en el mismo''' return {'pais':pais, 'cantidad':respuesta}_

* _def productoras(productora): '''Ingresas la productora, retornando la ganancia total y la cantidad de peliculas que produjeron''' return {'productora':productora, 'ganancia_total':respuesta, 'cantidad':respuesta}_

* _def retorno(pelicula): '''Ingresas la pelicula, retornando la inversion, la ganancia, el retorno y el año en el que se lanzo''' return {'pelicula':pelicula, 'inversion':respuesta, 'ganacia':respuesta,'retorno':respuesta, 'anio':respuesta}_

3. **[DEPLOYMENT](https://deploy-movies.onrender.com/docs)**

* Para el deployment se realizo en Render.


4. **[EDA](https://github.com/Luzve/PI_ML_OPS_LABS/blob/main/eda.ipynb)**

* Se utilizó Pandas Profile Report para efectuar un análisis más profundo del archivo.
  Se realizó un histograma con Matplotlib y Seaborn para obtener una visión general de distribución de los datos del dataframe.


**[LINK VIDEO](https://drive.google.com/file/d/1p557WVVqSGGmW6qq9qzMBXncg2Gtx_6k/view?usp=sharing)**
