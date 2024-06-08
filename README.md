# Instrucciones para llevar acabo la practica.

1. Descargar el archivo de `Registros de Urgencias 2022 (194 Mb)` que se encuentra en la [pagina](http://www.dgis.salud.gob.mx/contenidos/basesdedatos/da_urgencias_gobmx.html) de la secretaria de salud.
2. Ejecutar el archivo SQL de `URGENCIAS_CDMX.sql`.

NOTA: Tener en cuenta que en la linea

`LOAD DATA INFILE 'C:/ProgramData/MySQL/MySQL Server 8.4/Uploads/URGENCIAS.txt'`

Ya que aqui se necesita especificar el direccion del txt descargado desde la pagina de los datos abiertos de abiertos de la secretaria de salud de Mexico

---

# **ANALISIS DE DATOS UTILIZANDO PANDAS**
### Para este analisis se utilizaron los [datos abiertos](http://www.dgis.salud.gob.mx/contenidos/basesdedatos/Datos_Abiertos_gobmx.html) de la **Secretaria de Salud de Mexico**. Se utilizaron los [registros de urgencias de 2022](http://www.dgis.salud.gob.mx/contenidos/basesdedatos/da_urgencias_gobmx.html).
![imagen_2024-06-07_223856835.png](data:image/png;base64,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)
---
Para este conjunto de datos se desea encontrar la relacion entre la hora de ingreso de la urgencia y el motivo de urgencia que es en el estado de Ciudad de Mexico, los motivos de urgencias que existen en este conjunto de datos son:
1. ACCIDENTES, ENVENENAMIENTO Y VIOLENCIA: Se refiere cuando la o las afecciones tratadas fueron resultado de un accidente, envenenamiento y
violencia.                                     
2. MÉDICA:Se refiere cuando la o las afecciones tratadas fueron resultado de una enfermedad.

3. GINECO-OBSTÉTRICA: Se refiere cuando la o las afecciones tratadas fueron resultado del embarazo, parto o puerperio.

4. PEDIÁTRICA: Se refiere cuando la o las afecciones tratadas fueron dirigidas a un paciente pediátrico menor de 18 años.

5. NO ESPECIFICADO

De los cuales se omitira el no especificado, por motivo de querer estudiar la relacion del motivo especifico de urgencia con la hora, este dato no arrojaria informacion significativa.

*   **Hipotesis principal**: El motivo de urgencia esta relacionado con la hora de ingreso de la urgencia.

*   **Hipotesis secundaria**: El caso de ACCIDENTES, ENVENENAMIENTO Y VIOLENCIA sera mas comun entre las 20:00 y las 6:00.

---
* Pagina donde se extrajeron los datos y catalogo de los datos: http://www.dgis.salud.gob.mx/contenidos/basesdedatos/da_urgencias_gobmx.html

* INSTRUCTIVO DE LLENADO DE LA HOJA DIARIA DEL SERVICIO DE URGENCIAS (SINBA-SEUL-16-P DGIS) MODELO 2024: http://www.dgis.salud.gob.mx/descargas/urgencias/pdf/Instructivo_Urgencias_2024.pdf
---


## *Eduardo Alonso Martinez Chenoweth*
