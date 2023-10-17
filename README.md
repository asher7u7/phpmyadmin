## DB Zapateria

![Database](DB_Zapateria.png "Foto Base de Datos")
## Tabla Articulo
![Tabla Articulos](Articulos.png "tabla de articulos")
## Tabla Fabricantes
![Tabla Fabricantes](Fabricantes.png "Tabla de Fabricantes")

## Relaciones Tablas
![Relacion Tablas](relacion_tablas.png "Relación de tablas")

## Obtener los nombres de los productos de la Zapateria
SELECT nombre FROM Articulo;
![Nombres_productos](1.png "primera consulta")

## Obtener los nombres y los precios de los productos de la Zapatería.
SELECT Nombre,precio FROM Articulo;
![Nombres y Precio](2.png "Segunda consulta")

## Obtener el nombre de los productos cuyo precio sea menor o igual a 50000
SELECT nombre,precio FROM Articulo WHERE precio <= 50000;
![Nombre de menores a 50k](3.png "Tercera consulta")

## Obtener todos los datos de los artículos cuyo precio esté entre 5000 y 40000 (ambas canditades incluidas)
SELECT * FROM Articulo WHERE precio BETWEEN 5000 AND 40000;
![Precio entre 5k y 40k](4.png "Cuarta Consulta")

## Obtener el nombre y el precio de cada artículo, en dolares.
SELECT nombre, precio / 4231 AS precio_en_dolares FROM Articulo;
![Precio en dolar](5.png "Quinta Consulta")

## Obtener el precio promedio de todos los artículos
SELECT AVG(precio) as precio_promedio FROM Articulo;
![Precio Promedio](6.png "Sexta consulta")

## Obtener el precio medio de los artículos cuyo codigo de fabricante sea 2.
SELECT AVG(precio) as precio_medio FROM Articulo WHERE Codigo_fab = 2;
![Promedio codigo Fabricante](7.png "Septima consulta")

## Obtener el número de artículos cuyo precio sea mayor o igual a 50000
SELECT COUNT(*) as cantidad_articulos FROM Articulo WHERE precio >= 50000;
![Cantidad articulos](8.png "Octava consulta")

## Obtener el nombre y precio de los artículos cuyo precio sea mayor o igual a 50000 y ordenarlos descendentemente por precio, y luego ascendentemente por nombre.
SELECT Nombre,precio FROM Articulo WHERE precio >=50000 ORDER BY precio DESC, Nombre ASC;
![Ordenar](9.png "Novena consulta")

## Obtener un listado completo de artículos, incluyendo por cada articulo los datos del artículo y de su fabricante.