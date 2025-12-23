# Diccionario Tecnico de Datos: emu-b-cuentas.sql

## RESUMEN DE LA BASE DE DATOS
- Archivo Origen: emu-b-cuentas.sql
- Cantidad de Tablas: 3

---

## TABLA: b_news

### INFO CONTEXTUAL
- Registros totales: 6

### ESTRUCTURA TECNICA
| Columna   | Tipo         | Clave Primaria   |
|:----------|:-------------|:-----------------|
| id        | int          | SI               |
| title     | varchar(200) | NO               |
| author    | varchar(200) | NO               |
| content   | text         | NO               |
| img       | tinyint      | NO               |
| date      | datetime     | NO               |

### MUESTRA DE DATOS
*Datos presentes en formato complejo.*

---
## TABLA: banip

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna   | Tipo        | Clave Primaria   |
|:----------|:------------|:-----------------|
| ip        | varchar(15) | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: cuentas

### INFO CONTEXTUAL
- Registros totales: 20
- Relaciones sugeridas: Relacionada con Cuentas.

### ESTRUCTURA TECNICA
| Columna       | Tipo         | Clave Primaria   |
|:--------------|:-------------|:-----------------|
| id            | int          | SI               |
| cuenta        | varchar(30)  | NO               |
| pass          | varchar(50)  | NO               |
| rango         | tinyint      | NO               |
| nombre        | varchar(255) | NO               |
| apellido      | varchar(255) | NO               |
| pais          | varchar(255) | NO               |
| idioma        | varchar(255) | NO               |
| ipRegistro    | varchar(15)  | NO               |
| cumpleaños    | varchar(255) | NO               |
| email         | varchar(100) | NO               |
| ultimaIP      | varchar(15)  | NO               |
| pregunta      | varchar(100) | NO               |
| respuesta     | varchar(100) | NO               |
| apodo         | varchar(30)  | NO               |
| baneado       | bigint       | NO               |
| logeado       | tinyint(1)   | NO               |
| creditos      | int          | NO               |
| ogrinas       | int          | NO               |
| votos         | int          | NO               |
| actualizar    | tinyint(1)   | NO               |
| ultimoVoto    | varchar(255) | NO               |
| abono         | bigint       | NO               |
| fechaCreacion | bigint       | NO               |
| ticket        | text         | NO               |

### MUESTRA DE DATOS
|   id | cuenta       | pass             |   rango | nombre    | apellido   | pais        | idioma   | ipRegistro    | cumpleaños   | email                    | ultimaIP       | pregunta          | respuesta   | apodo     |   baneado |   logeado |   creditos |   ogrinas |   votos |   actualizar |   ultimoVoto |         abono |   fechaCreacion | ticket   |
|-----:|:-------------|:-----------------|--------:|:----------|:-----------|:------------|:---------|:--------------|:-------------|:-------------------------|:---------------|:------------------|:------------|:----------|----------:|----------:|-----------:|----------:|--------:|-------------:|-------------:|--------------:|----------------:|:---------|
|    1 | admin        | contraseñaSegura |       5 | aa        | aaa        | ES          | ES       |               | 1~1~2011     | yacosama@hotmail.com     | 181.78.6.106   | aa                | aaa         | beta1     |         0 |         0 |        166 |     86335 |     163 |            1 |   1526149045 | 1797398400000 |   1445382095692 |          |
|    2 | yaco         | contraseñaSegura |       5 | yaco      | dofus      | ES          | ES       |               | 1~1~2011     | maestro-yaco@hotmail.com | 181.78.6.106   | aa                | aaa         | beta2     |         0 |         0 |        166 |     85985 |     163 |            1 |   1526149045 | 1797398400000 |   1445382095692 |          |
|   21 | tester2      | contraseñaSegura |       0 | tester2   | tester2    | Desconocido | Es       | 172.71.6.160  | 2025-11-19   | yacosama@hotmail.com     | 172.71.6.160   | dofus             | dofus       | tester2   |         0 |         0 |          0 |         0 |       0 |            1 |            0 | 1797398400000 |      1763559710 |          |
|   22 | fumador      | contraseñaSegura |       0 | lokillo   | lokillo    | Desconocido | Es       | 172.71.6.161  | 2025-11-20   | yacosama@hotmail.com     | 179.6.15.67    | juego             | uno1        | lokillo   |         0 |         0 |          0 |         0 |       0 |            1 |            0 | 1797398400000 |      1763650602 |          |
|   23 | nascar123456 | contraseñaSegura |       5 | KillerTNT | KillerTNT  | Desconocido | Es       | 172.70.255.37 | 2025-11-20   | maestro-yaco@hotmail.com | 161.10.126.125 | nombre de mascota | ponki       | KillerTNT |         0 |         0 |          0 |         0 |       0 |            1 |            0 | 1797398400000 |      1763658830 |          |

---
