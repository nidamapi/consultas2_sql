# consultas2_sql

## Modelo físico BD

![modelo_fisico](modelo_fisico.png "modelo_fisico")

## Estructura BD

![estructura_bd](estructura_bd.png "estructura_bd")

## consultas SQL

1. Obtener la lista de los apellidos de todos los empleados.

`SELECT apellidos_empleado FROM Empleado;`

![consulta1](consulta1.png "consulta1")

2. Obtener los apellidos de todos los empleados sin repeticiones.

`SELECT DISTINCT apellidos_empleado FROM Empleado;`

![consulta2](consulta2.png "consulta2")

3. Obtener todos los datos de los empleados que se apellidan 'Gomez'.

`SELECT AVG(apellidos_empleado) AS Gomez_apellido FROM Empleado WHERE apellidos_empleado = "Gomez";`

![consulta3](consulta3.png "consulta3")
