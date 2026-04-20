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

4. Obtener todos los datos de los empleados que se apellidan "Diaz" y los que se apellidan "Rodriguez".  Usar OR o IN

`SELECT * FROM Empleado WHERE apellidos_empleado = 'Diaz' OR apellidos_empleado = 'Rodriguez';`

![consulta4or](consulta4or.png "consulta4or")

![consulta4in](consulta4in.png "consulta4in")

5. Obtener los nombres de los empleados que trabajan en el departamento 11

`SELECT nombre_empleado FROM Empleado WHERE id_departamento = '11'; `

![consulta5](consulta5.png "consulta5")

6. Obtener todos los datos de los empleados cuyo apellido empiece por 'P'

`SELECT * FROM Empleado WHERE apellidos_empleado LIKE 'P%'; `

![consulta6](consulta6.png "consulta6")

7. Obtener el presupuesto total de todos los departamentos.

`SELECT SUM(presupuesto_departamento) AS total_presupuesto FROM Departamento; `

![consulta7](consulta7.png "consulta7")

8. Obtener el número de empleados de cada departamento.

`SELECT id_departamento, COUNT(*) AS total_empleados FROM Empleado GROUP BY id_departamento; `

![consulta8](consulta8.png "consulta8")

9. Obtener un listado completo de empleados, incluyendo por cada empleado los datos del empleado y de su departamento.

`SELECT * FROM Empleado e JOIN Departamento d ON e.id_departamento = d.id_departamento;`

![consulta9](consulta9.png "consulta9")

10. Obtener un listado completo de empleados, incluyendo el nombre y apellidos del empleado junto al nombre y presupuesto de su departamento.

`SELECT e.nombre_empleado AS nombre_empleado, e.apellidos_empleado AS apellidos_empleado, d.nombre_departamento AS nombre_departamanto, d.presupuesto_departamento AS presupuesto_departamento FROM Empleado e INNER JOIN Departamento d ON e.id_departamento = d.id_departamento; `

![consulta10](consulta10.png "consulta10")

11. Obtener los nombres y apellidos de los empleados que trabajen en departamentos cuyo presupuesto sea mayor a 100000000

`SELECT e.nombre_empleado, e.apellidos_empleado FROM Empleado e JOIN Departamento d ON e.id_departamento = d.id_departamento WHERE d.presupuesto_departamento > 100000000; `

![consulta11](consulta11.png "consulta11")