![IronHack Logo](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_d5c5793015fec3be28a63c4fa3dd4d55.png)

# Project: API and Web Data Scraping

## Nombre Sofia Bonilla

## Technical Requirements

The technical requirements for this project are as follows:

* You must obtain data from an API using Python.
* You must scrape and clean HTML from a web page using Python.
* The results should be two files - one containing the tabular results of your API request and the other containing the results of your web page scrape.
* Your code should be saved in a Jupyter Notebook and your results should be saved in a folder named output.
* You should include a README.md file that describes the steps you took and your thought process for obtaining data from the API and web page.

## Explicacion del Codigo

Se selecciono el siguiente url(https://www.ultimatetennisstatistics.com/), que contiene estadisticas de los jugadores de tenis en el rankin mundial.
para ello se utilizo selenium commo metodo de extracion de los datos. a continuacion se describen los pasos a seguir para realizar el web scraping:

* se importaron las librerias.
* Se inspecciono la pagina a scrapear, como el url era igual para cada pagina, se utlizo el metodo de click para extraer la informacion.
* Se definieron funciones que extrajeran la informacion y otras que la limpiaran y colocaran en el mismo formato, para poder armar el data frame.
* Se hizo un merge para unir la informacion, utilizando los nombres de los jugadores como llave  para el cruce.
* finalmente se llamaron a las funciones para comenzar el scraping de las paginas, obteniendo asi n > 100 filas y 14 columnas.

## Dificultades:

* la pagina tiene anuncios que no dejan visualizar al codigo los botones a clickear, esto se resolvio con scroll del mouse.
* los nombres de los jugadores no tienen la misma longitud, para poder armar el df , se redujo el nombre del jugador a len=2, para asi tener la misma longitud del full name.
