# Diccionario Tecnico de Datos: emu-b-estaticos.sql

## RESUMEN DE LA BASE DE DATOS
- Archivo Origen: emu-b-estaticos.sql
- Cantidad de Tablas: 57

---

## TABLA: accion_pelea

### INFO CONTEXTUAL
- Registros totales: 420
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna     | Tipo         | Clave Primaria   |
|:------------|:-------------|:-----------------|
| mapa        | int          | SI               |
| tipoPelea   | tinyint      | SI               |
| accion      | tinyint      | SI               |
| args        | varchar(100) | NO               |
| condicion   | varchar(100) | SI               |
| descripcion | text         | NO               |

### MUESTRA DE DATOS
|   mapa |   tipoPelea |   accion | args     | condicion   | descripcion     |
|-------:|------------:|---------:|:---------|:------------|:----------------|
|    325 |           4 |        0 | 7411,340 |             | dark vlad       |
|   1443 |           4 |        0 | 1443,104 |             |                 |
|   1687 |           4 |        0 | 1443,286 |             |                 |
|   1765 |           4 |        0 | 1792,120 |             | 1ere salle moon |
|   1767 |           4 |        0 | 1768,409 |             |                 |

---
## TABLA: almanax

### INFO CONTEXTUAL
- Registros totales: 365

### ESTRUCTURA TECNICA
| Columna     | Tipo   | Clave Primaria   |
|:------------|:-------|:-----------------|
| id          | int    | SI               |
| dia         | int    | NO               |
| mes         | text   | NO               |
| ofrenda     | text   | NO               |
| tipo        | int    | NO               |
| bonus       | int    | NO               |
| descripcion | text   | NO               |

### MUESTRA DE DATOS
|   id |   dia | mes   | ofrenda   |   tipo |   bonus | descripcion                |
|-----:|------:|:------|:----------|-------:|--------:|:---------------------------|
|    1 |     1 | Enero | 312,15    |      1 |      15 | X% XP PJ                   |
|    2 |     2 | Enero | 312,15    |      2 |      35 | X% KAMAS PELEA             |
|    3 |     3 | Enero | 312,15    |      3 |      50 | X% DROP PELEA              |
|    4 |     4 | Enero | 312,15    |      4 |      15 | X% XP OFICIO RECETAS       |
|    5 |     5 | Enero | 312,15    |      5 |      20 | X% XP OFICIO AL RECOLECTAR |

---
## TABLA: animaciones

### INFO CONTEXTUAL
- Registros totales: 459

### ESTRUCTURA TECNICA
| Columna          | Tipo   | Clave Primaria   |
|:-----------------|:-------|:-----------------|
| id               | int    | SI               |
| hechizoAnimacion | int    | NO               |
| nombre           | text   | NO               |
| tipoDisplay      | int    | NO               |
| spriteAnimacion  | int    | NO               |
| level            | int    | NO               |
| duracion         | int    | NO               |
| talla            | int    | NO               |

### MUESTRA DE DATOS
|   id |   hechizoAnimacion | nombre             |   tipoDisplay |   spriteAnimacion |   level |   duracion |   talla |
|-----:|-------------------:|:-------------------|--------------:|------------------:|--------:|-----------:|--------:|
|    1 |                101 | Reenvio de Hechizo |            10 |                 1 |       6 |          0 |     100 |
|    2 |                101 | Tregua             |            10 |                 1 |       6 |          0 |     100 |
|    3 |                101 | Ciencia del Palo   |            10 |                 1 |       6 |          0 |     100 |
|    4 |                102 | Ceguera            |            11 |                 1 |       6 |          0 |     100 |
|    5 |                102 | Burla              |            11 |                 1 |       6 |          0 |     100 |

---
## TABLA: areas

### INFO CONTEXTUAL
- Registros totales: 47

### ESTRUCTURA TECNICA
| Columna   | Tipo         | Clave Primaria   |
|:----------|:-------------|:-----------------|
| id        | int          | SI               |
| nombre    | varchar(100) | NO               |
| superarea | int          | NO               |

### MUESTRA DE DATOS
|   id | nombre                 |   superarea |
|-----:|:-----------------------|------------:|
|    0 | Amakna                 |           0 |
|    1 | La Isla de los Wabbits |           0 |
|    2 | La Isla de Moon        |           0 |
|    3 | Prisión                |           0 |
|    4 | Tainela                |           0 |

---
## TABLA: battle_mapas

### INFO CONTEXTUAL
- Registros totales: 12

### ESTRUCTURA TECNICA
| Columna    | Tipo   | Clave Primaria   |
|:-----------|:-------|:-----------------|
| prioridad  | int    | SI               |
| superAreas | text   | NO               |
| areas      | text   | NO               |
| subAreas   | text   | NO               |
| mapas      | text   | NO               |

### MUESTRA DE DATOS
|   prioridad | superAreas   | areas   | subAreas                                        | mapas   |
|------------:|:-------------|:--------|:------------------------------------------------|:--------|
|          -1 |              |         | 447,501,492,491,339,78,77,314,39,536,91,316,181 |         |
|           0 | 2            |         |                                                 |         |
|           1 |              | 0       |                                                 |         |
|           2 |              |         |                                                 |         |
|           3 |              |         |                                                 |         |

---
## TABLA: battle_mobs

### INFO CONTEXTUAL
- Registros totales: 22

### ESTRUCTURA TECNICA
| Columna   | Tipo    | Clave Primaria   |
|:----------|:--------|:-----------------|
| id        | int     | SI               |
| nombreMob | text    | NO               |
| exps      | text    | NO               |
| pdvs      | text    | NO               |
| drops     | text    | NO               |
| gradoMin  | tinyint | NO               |
| gradoMax  | tinyint | NO               |
| totalMobs | int     | NO               |
| rareza    | tinyint | NO               |

### MUESTRA DE DATOS
|   id | nombreMob                | exps                  | pdvs                | drops   |   gradoMin |   gradoMax |   totalMobs |   rareza |
|-----:|:-------------------------|:----------------------|:--------------------|:--------|-----------:|-----------:|------------:|---------:|
|   48 | Girasol Salvaje          | 92|136|189|250|300    | 80|95|110|125|140   |         |          1 |          5 |          50 |        1 |
|   55 | Gelatina Azul            | 11|23|37|55|76        | 15|26|37|48|59      |         |          1 |          5 |          30 |        1 |
|   56 | Gelatina de Menta        | 52|92|143|206|280     | 60|80|100|120|140   |         |          1 |          5 |          20 |        3 |
|   57 | Gelatina de Fresa        | 618|780|960|1119|1286 | 180|210|240|270|300 |         |          1 |          5 |          10 |        5 |
|   79 | Diente de León Diabólico | 8|15|24|56|74         | 25|33|41|49|57      |         |          1 |          5 |          50 |        1 |

---
## TABLA: battle_objetos

### INFO CONTEXTUAL
- Registros totales: 1585

### ESTRUCTURA TECNICA
| Columna       | Tipo       | Clave Primaria   |
|:--------------|:-----------|:-----------------|
| id            | int        | SI               |
| nombreObjeto  | text       | NO               |
| stats         | text       | NO               |
| pods          | smallint   | NO               |
| hechizoID     | smallint   | NO               |
| hechizoNivel  | tinyint    | NO               |
| nombreHechizo | text       | NO               |
| delay         | int        | NO               |
| accionID      | text       | NO               |
| params        | text       | NO               |
| dropMin       | smallint   | NO               |
| dropMax       | smallint   | NO               |
| dropTotal     | smallint   | NO               |
| rareza        | tinyint    | NO               |
| esDropAereo   | varchar(5) | NO               |

### MUESTRA DE DATOS
|   id | nombreObjeto                | stats          |   pods |   hechizoID |   hechizoNivel | nombreHechizo    |   delay | accionID   | params   |   dropMin |   dropMax |   dropTotal |   rareza | esDropAereo   |
|-----:|:----------------------------|:---------------|-------:|------------:|---------------:|:-----------------|--------:|:-----------|:---------|----------:|----------:|------------:|---------:|:--------------|
|   39 | Pequeño Amuleto del Búho    | 7e#2#0#0#0d0+2 |      4 |         446 |              1 | Castigo          |      -1 |            |          |         1 |         1 |           1 |        1 | false         |
|   40 | Espadita de Maderucha       | 64#1#7#0#1d7+0 |     20 |          61 |              1 | Engaño           |      -1 |            |          |         1 |         1 |           1 |        1 | false         |
|   42 | Espada de Maderucha         | 64#2#8#0#1d7+1 |     20 |           7 |              1 | Escudo Feca      |      -1 |            |          |         1 |         1 |           1 |        1 | false         |
|   43 | Gran Espada de Maderucha    | 64#3#9#0#1d7+2 |     20 |         108 |              1 | Espíritu Felino  |      -1 |            |          |         1 |         1 |           1 |        1 | false         |
|   44 | Potente Espada de Maderucha | 64#4#a#0#1d7+3 |     20 |         174 |              1 | Flecha Azotadora |      -1 |            |          |         1 |         1 |           1 |        1 | false         |

---
## TABLA: casas_modelo

### INFO CONTEXTUAL
- Registros totales: 368

### ESTRUCTURA TECNICA
| Columna         | Tipo   | Clave Primaria   |
|:----------------|:-------|:-----------------|
| id              | int    | SI               |
| mapaFuera       | int    | NO               |
| celdaFuera      | int    | NO               |
| mapaDentro      | int    | NO               |
| celdaDentro     | int    | NO               |
| mapasContenidos | text   | NO               |
| precio          | bigint | NO               |
| descripcion     | text   | NO               |

### MUESTRA DE DATOS
|   id |   mapaFuera |   celdaFuera |   mapaDentro |   celdaDentro |   mapasContenidos |   precio | descripcion                  |
|-----:|------------:|-------------:|-------------:|--------------:|------------------:|---------:|:-----------------------------|
|   68 |          30 |          309 |         1524 |           356 |              1524 |  2000000 | Casa pequeña                 |
|   81 |          50 |          161 |          516 |           223 |               516 |  2000000 | Casa cerca del templo Xelor  |
|   88 |         540 |          181 |         1582 |           386 |              1582 |  1000000 | Casa cerca de la tienda ocra |
|   90 |         761 |          285 |         1583 |           246 |              1583 |   525000 | Chabola del Marinero         |
|   91 |         761 |          119 |         1584 |           233 |              1584 |   525000 | Cabaña del pescador          |

---
## TABLA: category_shop

### INFO CONTEXTUAL
- Registros totales: 9

### ESTRUCTURA TECNICA
| Columna   | Tipo         | Clave Primaria   |
|:----------|:-------------|:-----------------|
| id        | int          | SI               |
| nombre    | varchar(255) | NO               |
| icon      | int          | NO               |

### MUESTRA DE DATOS
|   id | nombre               |   icon |
|-----:|:---------------------|-------:|
|    1 | Objeto Viviente      |      5 |
|    2 | Mimobiontes Capas    |      1 |
|    3 | Mimobiontes Hats     |      1 |
|    4 | Lupas For Full       |      1 |
|    5 | Potions Boss/Invasão |      1 |

---
## TABLA: celdas_accion

### INFO CONTEXTUAL
- Registros totales: 20222
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| mapa      | int    | SI               |
| celda     | int    | SI               |
| accion    | int    | SI               |
| args      | text   | NO               |
| condicion | text   | NO               |

### MUESTRA DE DATOS
|   mapa |   celda |   accion | args     | condicion   |
|-------:|--------:|---------:|:---------|:------------|
|      4 |     436 |        0 | 2147,169 |             |
|      5 |     422 |        0 | 2142,265 |             |
|      6 |      33 |        0 | 7,439    |             |
|      6 |     173 |        0 | 54,175   |             |
|      6 |     392 |        0 | 49,419   |             |

---
## TABLA: cercados_modelo

### INFO CONTEXTUAL
- Registros totales: 0
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna        | Tipo     | Clave Primaria   |
|:---------------|:---------|:-----------------|
| mapa           | smallint | SI               |
| capacidad      | tinyint  | NO               |
| objetos        | tinyint  | NO               |
| precioOriginal | bigint   | NO               |
| celdaPJ        | smallint | NO               |
| celdaPuerta    | smallint | NO               |
| celdaMontura   | smallint | NO               |
| celdasObjetos  | text     | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: clases

### INFO CONTEXTUAL
- Registros totales: 12

### ESTRUCTURA TECNICA
| Columna           | Tipo   | Clave Primaria   |
|:------------------|:-------|:-----------------|
| id                | int    | SI               |
| nombre            | text   | NO               |
| gfxs              | text   | NO               |
| tallas            | text   | NO               |
| mapaInicio        | int    | NO               |
| celdaInicio       | int    | NO               |
| PDV               | int    | NO               |
| boostVitalidad    | text   | NO               |
| boostSabiduria    | text   | NO               |
| boostFuerza       | text   | NO               |
| boostInteligencia | text   | NO               |
| boostAgilidad     | text   | NO               |
| boostSuerte       | text   | NO               |
| statsInicio       | text   | NO               |
| hechizos          | text   | NO               |

### MUESTRA DE DATOS
|   id | nombre   | gfxs     | tallas      |   mapaInicio |   celdaInicio |   PDV | boostVitalidad   | boostSabiduria   | boostFuerza                 | boostInteligencia           | boostAgilidad               | boostSuerte                 | statsInicio                        | hechizos                                                                            |
|-----:|:---------|:---------|:------------|-------------:|--------------:|------:|:-----------------|:-----------------|:----------------------------|:----------------------------|:----------------------------|:----------------------------|:-----------------------------------|:------------------------------------------------------------------------------------|
|    1 | feca     | 10,11,12 | 100,100,100 |           33 |           368 |    50 | 0,1              | 0,3              | 0,2|50,3|150,4|250,5        | 0,1|100,2|200,3|300,4|400,5 | 0,1|20,2|40,3|60,4|80,5     | 0,1|20,2|40,3|60,4|80,5     | 111,6|128,3|182,1|176,100|158,1000 | 1,3|1,17|1,6|3,4|6,2|9,1|13,9|17,18|21,20|26,14|31,19|36,5|42,16|48,8|54,12|60,1... |
|    2 | osamodas | 20,21,22 | 100,100,100 |           33 |           368 |    50 | 0,1              | 0,3              | 0,2|50,3|150,4|250,5        | 0,1|100,2|200,3|300,4|400,5 | 0,1|20,2|40,3|60,4|80,5     | 0,1|100,2|200,3|300,4|400,5 | 111,6|128,3|182,1|176,100|158,1000 | 1,23|1,34|1,21|3,26|6,22|9,35|13,28|17,37|21,30|26,27|31,24|36,33|42,25|48,38|54... |
|    3 | anutrof  | 30,31,32 | 100,100,100 |           33 |           368 |    50 | 0,1              | 0,3              | 0,1|50,2|150,3|250,4|350,5  | 0,1|20,2|60,3|100,4|140,5   | 0,1|20,2|40,3|60,4|80,5     | 0,1|100,2|150,3|230,4|330,5 | 111,6|128,3|182,1|176,120|158,1000 | 1,51|1,41|1,43|3,49|6,42|9,47|13,48|17,45|21,53|26,46|31,52|36,44|42,50|48,54|54... |
|    4 | sram     | 40,41,42 | 100,100,100 |           33 |           368 |    50 | 0,1              | 0,3              | 0,1|100,2|200,3|300,4|400,5 | 0,2|50,3|150,4|250,5        | 0,1|100,2|200,3|300,4|400,5 | 0,1|20,2|40,3|60,4|80,5     | 111,6|128,3|182,1|176,100|158,1000 | 1,72|1,61|1,65|3,66|6,68|9,63|13,74|17,64|21,79|26,78|31,71|36,62|42,69|48,77|54... |
|    5 | xelor    | 50,51,52 | 100,100,100 |           33 |           368 |    50 | 0,1              | 0,3              | 0,2|50,3|150,4|250,5        | 0,1|100,2|200,3|300,4|400,5 | 0,1|20,2|40,3|60,4|80,5     | 0,1|20,2|40,3|60,4|80,5     | 111,6|128,3|182,1|176,100|158,1000 | 1,81|1,83|1,82|3,84|6,100|9,92|13,88|17,93|21,85|26,96|31,98|36,86|42,89|48,90|5... |

---
## TABLA: clases_copy1

### INFO CONTEXTUAL
- Registros totales: 12

### ESTRUCTURA TECNICA
| Columna           | Tipo   | Clave Primaria   |
|:------------------|:-------|:-----------------|
| id                | int    | SI               |
| nombre            | text   | NO               |
| gfxs              | text   | NO               |
| tallas            | text   | NO               |
| mapaInicio        | int    | NO               |
| celdaInicio       | int    | NO               |
| PDV               | int    | NO               |
| boostVitalidad    | text   | NO               |
| boostSabiduria    | text   | NO               |
| boostFuerza       | text   | NO               |
| boostInteligencia | text   | NO               |
| boostAgilidad     | text   | NO               |
| boostSuerte       | text   | NO               |
| statsInicio       | text   | NO               |
| hechizos          | text   | NO               |

### MUESTRA DE DATOS
|   id | nombre   | gfxs     | tallas      |   mapaInicio |   celdaInicio |   PDV | boostVitalidad   | boostSabiduria   | boostFuerza                 | boostInteligencia           | boostAgilidad               | boostSuerte                 | statsInicio                        | hechizos                                                                            |
|-----:|:---------|:---------|:------------|-------------:|--------------:|------:|:-----------------|:-----------------|:----------------------------|:----------------------------|:----------------------------|:----------------------------|:-----------------------------------|:------------------------------------------------------------------------------------|
|    1 | feca     | 10,11,12 | 100,100,100 |        10300 |           337 |    50 | 0,1              | 0,3              | 0,2|50,3|150,4|250,5        | 0,1|100,2|200,3|300,4|400,5 | 0,1|20,2|40,3|60,4|80,5     | 0,1|20,2|40,3|60,4|80,5     | 111,6|128,3|182,1|176,100|158,1000 | 1,3|1,17|1,6|3,4|6,2|9,1|13,9|17,18|21,20|26,14|31,19|36,5|42,16|48,8|54,12|60,1... |
|    2 | osamodas | 20,21,22 | 100,100,100 |        10284 |           386 |    50 | 0,1              | 0,3              | 0,2|50,3|150,4|250,5        | 0,1|100,2|200,3|300,4|400,5 | 0,1|20,2|40,3|60,4|80,5     | 0,1|100,2|200,3|300,4|400,5 | 111,6|128,3|182,1|176,100|158,1000 | 1,23|1,34|1,21|3,26|6,22|9,35|13,28|17,37|21,30|26,27|31,24|36,33|42,25|48,38|54... |
|    3 | anutrof  | 30,31,32 | 100,100,100 |        10299 |           300 |    50 | 0,1              | 0,3              | 0,1|50,2|150,3|250,4|350,5  | 0,1|20,2|60,3|100,4|140,5   | 0,1|20,2|40,3|60,4|80,5     | 0,1|100,2|150,3|230,4|330,5 | 111,6|128,3|182,1|176,120|158,1000 | 1,51|1,41|1,43|3,49|6,42|9,47|13,48|17,45|21,53|26,46|31,52|36,44|42,50|48,54|54... |
|    4 | sram     | 40,41,42 | 100,100,100 |        10285 |           263 |    50 | 0,1              | 0,3              | 0,1|100,2|200,3|300,4|400,5 | 0,2|50,3|150,4|250,5        | 0,1|100,2|200,3|300,4|400,5 | 0,1|20,2|40,3|60,4|80,5     | 111,6|128,3|182,1|176,100|158,1000 | 1,72|1,61|1,65|3,66|6,68|9,63|13,74|17,64|21,79|26,78|31,71|36,62|42,69|48,77|54... |
|    5 | xelor    | 50,51,52 | 100,100,100 |        10298 |           315 |    50 | 0,1              | 0,3              | 0,2|50,3|150,4|250,5        | 0,1|100,2|200,3|300,4|400,5 | 0,1|20,2|40,3|60,4|80,5     | 0,1|20,2|40,3|60,4|80,5     | 111,6|128,3|182,1|176,100|158,1000 | 1,81|1,83|1,82|3,84|6,100|9,92|13,88|17,93|21,85|26,96|31,98|36,86|42,89|48,90|5... |

---
## TABLA: cofres_modelo

### INFO CONTEXTUAL
- Registros totales: 170
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| casa      | int    | NO               |
| mapa      | int    | NO               |
| celda     | int    | NO               |

### MUESTRA DE DATOS
|   id |   casa |   mapa |   celda |
|-----:|-------:|-------:|--------:|
|    1 |    515 |   6199 |     200 |
|    2 |    516 |   6201 |     121 |
|    3 |    525 |   6225 |     121 |
|    4 |    526 |   6226 |     121 |
|    5 |    527 |   6227 |     121 |

---
## TABLA: comandos_modelo

### INFO CONTEXTUAL
- Registros totales: 651

### ESTRUCTURA TECNICA
| Columna     | Tipo   | Clave Primaria   |
|:------------|:-------|:-----------------|
| comando     | text   | NO               |
| rango       | int    | NO               |
| descripcion | text   | NO               |

### MUESTRA DE DATOS
| comando         |   rango | descripcion   |
|:----------------|--------:|:--------------|
| !GETITEM        |       4 |               |
| A               |       3 |               |
| ABONO_DAYS      |       5 |               |
| ABONO_DIAS      |       5 |               |
| ACCESSORIES_NPC |       3 |               |

---
## TABLA: crear_objetos_modelos

### INFO CONTEXTUAL
- Registros totales: 1

### ESTRUCTURA TECNICA
| Columna       | Tipo   | Clave Primaria   |
|:--------------|:-------|:-----------------|
| id            | int    | SI               |
| nombre        | text   | NO               |
| statsMaximos  | text   | NO               |
| limiteOgrinas | text   | NO               |
| precioBase    | int    | NO               |

### MUESTRA DE DATOS
|    id | nombre          | statsMaximos   |   limiteOgrinas |   precioBase |
|------:|:----------------|:---------------|----------------:|-------------:|
| 99999 | crea tu amuleto | 111,9|123,4    |            1000 |           20 |

---
## TABLA: crear_objetos_stats

### INFO CONTEXTUAL
- Registros totales: 49

### ESTRUCTURA TECNICA
| Columna   | Tipo     | Clave Primaria   |
|:----------|:---------|:-----------------|
| id        | int      | SI               |
| stat      | text     | NO               |
| ogrinas   | float(11 | NO               |

### MUESTRA DE DATOS
|   id | stat                                                             |   ogrinas |
|-----:|:-----------------------------------------------------------------|----------:|
|   78 | Añade +#1{~1~2 à }#2 PM\", c: 0, o: \"+\", j: true               |         1 |
|  111 | +#1{~1~2 a }#2 PA\", c: 1, o: \"+\", j: true                     |         1 |
|  112 | +#1{~1~2 a }#2 a los daños\", c: 16, o: \"+\", j: true           |         1 |
|  115 | +#1{~1~2 a }#2 a los golpes críticos\", c: 18, o: \"+\", j: true |         1 |
|  117 | +#1{~1~2 a }#2 al alcance\", c: 19, o: \"+\", j: true            |         1 |

---
## TABLA: dones

### INFO CONTEXTUAL
- Registros totales: 22

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| nombre    | text   | NO               |
| stat      | int    | NO               |

### MUESTRA DE DATOS
|   id | nombre                  |   stat |
|-----:|:------------------------|-------:|
|    1 | Eficacia                |    115 |
|    2 | Iniciativa              |    174 |
|    3 | Resistencia a la tierra |    240 |
|    4 | Resistencia al fuego    |    243 |
|    5 | Resistencia al agua     |    241 |

---
## TABLA: drops

### INFO CONTEXTUAL
- Registros totales: 3835

### ESTRUCTURA TECNICA
| Columna       | Tipo         | Clave Primaria   |
|:--------------|:-------------|:-----------------|
| mob           | int          | SI               |
| objeto        | int          | SI               |
| prospeccion   | int          | NO               |
| porcentaje    | double       | NO               |
| max           | int          | NO               |
| nombre_mob    | varchar(100) | NO               |
| nombre_objeto | varchar(100) | NO               |
| condicion     | text         | NO               |

### MUESTRA DE DATOS
|   mob |   objeto |   prospeccion |   porcentaje |   max | nombre_mob   | nombre_objeto           | condicion   |
|------:|---------:|--------------:|-------------:|------:|:-------------|:------------------------|:------------|
|    31 |      362 |           100 |       27.75  |     4 | Larva Azul   | Piel de larva azul      |             |
|    31 |     2272 |           100 |        0.2   |     1 | Larva Azul   | Larva dorada            |             |
|    31 |     2474 |           300 |        2.978 |     1 | Larva Azul   | Sombrero del Aventurero |             |
|    31 |     8143 |           100 |        0.997 |     4 | Larva Azul   | Llave de los Campos     |             |
|    34 |      364 |           100 |       22.56  |     4 | Larva Verde  | Piel de larva verde     |             |

---
## TABLA: drops_fijos

### INFO CONTEXTUAL
- Registros totales: 3516

### ESTRUCTURA TECNICA
| Columna       | Tipo         | Clave Primaria   |
|:--------------|:-------------|:-----------------|
| objeto        | int          | SI               |
| porcentaje    | double       | NO               |
| nivelMin      | int          | NO               |
| nivelMax      | int          | NO               |
| nombre_objeto | varchar(100) | NO               |

### MUESTRA DE DATOS
|   objeto |   porcentaje |   nivelMin |   nivelMax | nombre_objeto                |
|---------:|-------------:|-----------:|-----------:|:-----------------------------|
|      678 |         0.01 |          1 |        200 | pergamino de marfil          |
|      679 |         0.01 |          1 |        200 | pergamino blanco             |
|      680 |         0.01 |          1 |        200 | pergamino dorado             |
|      724 |         0.01 |          1 |        200 | Hechizo Dominio del Bastón   |
|      725 |         0.01 |          1 |        200 | Hechizo Dominio de la Espada |

---
## TABLA: encarnaciones_modelo

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna       | Tipo   | Clave Primaria   |
|:--------------|:-------|:-----------------|
| gfx           | int    | SI               |
| statsFijos    | text   | NO               |
| statsPorNivel | text   | NO               |
| hechizos      | text   | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: especialidades

### INFO CONTEXTUAL
- Registros totales: 39

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| nombre    | text   | NO               |
| orden     | int    | NO               |
| nivel     | int    | NO               |
| dones     | text   | NO               |

### MUESTRA DE DATOS
|   id | nombre                    |   orden |   nivel | dones         |
|-----:|:--------------------------|--------:|--------:|:--------------|
|    0 | Neutra                    |       0 |       0 |               |
|    1 | Neófito                   |       1 |       0 |               |
|    2 | Discípulo de Menalt       |       2 |      20 | 22,1,200|21,1 |
|    3 | Escudero                  |       2 |      40 | 22,2,400|21,2 |
|    4 | Caballero de la Esperanza |       2 |      60 | 21,3|22,3,600 |

---
## TABLA: experiencia

### INFO CONTEXTUAL
- Registros totales: 501
- Relaciones sugeridas: Relacionada con Personajes.

### ESTRUCTURA TECNICA
| Columna     | Tipo   | Clave Primaria   |
|:------------|:-------|:-----------------|
| nivel       | int    | SI               |
| personaje   | bigint | NO               |
| oficio      | int    | NO               |
| dragopavo   | int    | NO               |
| gremio      | bigint | NO               |
| pvp         | int    | NO               |
| encarnacion | int    | NO               |

### MUESTRA DE DATOS
|   nivel |   personaje |   oficio |   dragopavo |   gremio |   pvp |   encarnacion |
|--------:|------------:|---------:|------------:|---------:|------:|--------------:|
|       1 |           0 |        0 |           0 |        0 |     0 |             0 |
|       2 |         110 |       50 |         600 |     1100 |   500 |          1750 |
|       3 |         650 |      140 |        1750 |     6500 |  1500 |          4000 |
|       4 |        1500 |      271 |        2750 |    15000 |  3000 |          7250 |
|       5 |        2800 |      441 |        4000 |    28000 |  5000 |         11500 |

---
## TABLA: hechizos

### INFO CONTEXTUAL
- Registros totales: 1917

### ESTRUCTURA TECNICA
| Columna     | Tipo         | Clave Primaria   |
|:------------|:-------------|:-----------------|
| id          | int          | SI               |
| nombre      | varchar(100) | NO               |
| sprite      | int          | NO               |
| spriteInfos | varchar(20)  | NO               |
| nivel1      | text         | NO               |
| nivel2      | text         | NO               |
| nivel3      | text         | NO               |
| nivel4      | text         | NO               |
| nivel5      | text         | NO               |
| nivel6      | text         | NO               |
| afectados   | text         | NO               |
| condiciones | text         | NO               |
| valorIA     | int          | NO               |
| descripcion | text         | NO               |

### MUESTRA DE DATOS
|   id | nombre                 |   sprite | spriteInfos   | nivel1                                                                              | nivel2                                                                              | nivel3                                                                              | nivel4                                                                              | nivel5                                                                              | nivel6                                                                              | afectados   | condiciones   |   valorIA | descripcion                                                                         |
|-----:|:-----------------------|---------:|:--------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------|:--------------|----------:|:------------------------------------------------------------------------------------|
|    0 | Cuerpo a Cuerpo        |       -1 | 0,0,0         | [[[100, 2, 6, null, 0, 0, 1d5+1]], [[100, 5, 9, null, 0, 0, 1d5+4]], 4, 1, 1, 20... | [[[100, 2, 6, null, 0, 0, 1d5+1]], [[100, 5, 9, null, 0, 0, 1d5+4]], 4, 1, 1, 20... | [[[100, 2, 6, null, 0, 0, 1d5+1]], [[100, 5, 9, null, 0, 0, 1d5+4]], 4, 1, 1, 20... | [[[100, 2, 6, null, 0, 0, 1d5+1]], [[100, 5, 9, null, 0, 0, 1d5+4]], 4, 1, 1, 20... | [[[100, 2, 6, null, 0, 0, 1d5+1]], [[100, 5, 9, null, 0, 0, 1d5+4]], 4, 1, 1, 20... | [[[100, 2, 6, null, 0, 0, 1d5+1]], [[100, 5, 9, null, 0, 0, 1d5+4]], 4, 1, 1, 20... |             |               |         0 | Ataque de cuerpo a cuerpo que ocasiona pocos daños a tu adversario. Para que sea... |
|    1 | Armadura Incandescente |      108 | 10,1,1        | [[[265, 7, null, null, 4, 0, 0d0+7]], [[265, 8, null, null, 4, 0, 0d0+8]], 2, 0,... | [[[265, 8, null, null, 4, 0, 0d0+8]], [[265, 9, null, null, 4, 0, 0d0+9]], 2, 0,... | [[[265, 9, null, null, 4, 0, 0d0+9]], [[265, 10, null, null, 4, 0, 0d0+10]], 2, ... | [[[265, 10, null, null, 4, 0, 0d0+10]], [[265, 11, null, null, 4, 0, 0d0+11]], 2... | [[[265, 11, null, null, 4, 0, 0d0+11]], [[265, 12, null, null, 4, 0, 0d0+12]], 2... | [[[265, 14, null, null, 4, 0, 0d0+14]], [[265, 15, null, null, 4, 0, 0d0+15]], 2... | 4|4         |               |         0 | Esta armadura protege contra los daños de fuego.                                    |
|    2 | Ceguera                |      102 | 11,1,1        | [[[101, 1, 2, null, 1, 0, 1d2+0], [100, 1, null, null, 0, 0, 0d0+1]], [[101, 2, ... | [[[100, 2, 3, null, 1, 0, 1d2+1], [101, 1, 2, null, 1, 0, 1d2+0]], [[101, 2, nul... | [[[101, 1, 2, null, 1, 0, 1d2+0], [100, 2, 4, null, 0, 0, 1d3+1]], [[101, 2, nul... | [[[101, 1, 2, null, 1, 0, 1d2+0], [100, 2, 5, null, 0, 0, 1d4+1]], [[101, 2, nul... | [[[101, 2, null, null, 1, 0, 0d0+2], [100, 3, 7, null, 0, 0, 1d5+2]], [[101, 2, ... | [[[101, 2, 3, null, 1, 0, 1d2+1], [100, 6, 15, null, 0, 0, 1d10+5]], [[101, 3, n... |             |               |         0 | Ceguera ocasiona daños neutros y hace que el enemigo pierda PA.                     |
|    3 | Ataque Natural         |      103 | 30,1,1        | [[[99, 2, 6, null, 0, 0, 1d5+1]], [[99, 8, null, null, 0, 0, 0d0+8]], 5, 1, 6, 5... | [[[99, 3, 7, null, 0, 0, 1d5+2]], [[99, 9, null, null, 0, 0, 0d0+9]], 5, 1, 6, 5... | [[[99, 4, 8, null, 0, 0, 1d5+3]], [[99, 10, null, null, 0, 0, 0d0+10]], 4, 1, 6,... | [[[99, 5, 9, null, 0, 0, 1d5+4]], [[99, 11, null, null, 0, 0, 0d0+11]], 4, 1, 6,... | [[[99, 7, 11, null, 0, 0, 1d5+6]], [[99, 13, null, null, 0, 0, 0d0+13]], 4, 1, 7... | [[[99, 9, 13, null, 0, 0, 1d5+8]], [[99, 15, null, null, 0, 0, 0d0+15]], 3, 1, 8... |             |               |         0 | Ataque Natural causa daños de fuego.                                                |
|    4 | Reenvío de Hechizo     |      101 | 10,1,1        | [[[106, null, 1, 100, 1, 0]], null, 3, 0, 1, 0, 100, false, false, false, true, ... | [[[106, null, 2, 100, 1, 0]], null, 3, 0, 2, 0, 100, false, false, false, true, ... | [[[106, null, 3, 100, 1, 0]], null, 3, 0, 3, 0, 100, false, false, false, true, ... | [[[106, null, 4, 100, 1, 0]], null, 3, 0, 4, 0, 100, false, false, false, true, ... | [[[106, null, 5, 100, 1, 0]], null, 3, 0, 5, 0, 100, false, false, false, true, ... | [[[106, null, 6, 100, 1, 0]], null, 3, 0, 6, 0, 100, false, false, false, true, ... |             |               |         0 | Reenvío de Hechizo permite reenviar un hechizo que provoca una pérdida de PDV o ... |

---
## TABLA: items_shop

### INFO CONTEXTUAL
- Registros totales: 1

### ESTRUCTURA TECNICA
| Columna     | Tipo         | Clave Primaria   |
|:------------|:-------------|:-----------------|
| iditem      | int          | NO               |
| value       | int          | NO               |
| nuevo       | int          | NO               |
| promo       | int          | NO               |
| categoria   | int          | NO               |
| descripcion | varchar(255) | NO               |

### MUESTRA DE DATOS
|   iditem |   value |   nuevo |   promo |   categoria | descripcion           |
|---------:|--------:|--------:|--------:|------------:|:----------------------|
|     9234 |    1000 |       0 |       0 |           0 | Item de tipo especial |

---
## TABLA: mapas

### INFO CONTEXTUAL
- Registros totales: 16676

### ESTRUCTURA TECNICA
| Columna          | Tipo       | Clave Primaria   |
|:-----------------|:-----------|:-----------------|
| id               | bigint     | SI               |
| fecha            | text       | NO               |
| ancho            | int        | NO               |
| alto             | int        | NO               |
| bgID             | int        | NO               |
| musicID          | int        | NO               |
| ambienteID       | int        | NO               |
| outDoor          | tinyint(1) | NO               |
| capabilities     | int        | NO               |
| posPelea         | text       | NO               |
| mapData          | text       | NO               |
| mobs             | text       | NO               |
| X                | int        | NO               |
| Y                | int        | NO               |
| subArea          | int        | NO               |
| maxGrupoMobs     | int        | NO               |
| maxMobsPorGrupo  | int        | NO               |
| minNivelGrupoMob | int        | NO               |
| maxNivelGrupoMob | int        | NO               |
| maxMercantes     | int        | NO               |
| maxPeleas        | tinyint    | NO               |

### MUESTRA DE DATOS
*Datos presentes en formato complejo.*

---
## TABLA: mapas_buta7base

### INFO CONTEXTUAL
- Registros totales: 8338

### ESTRUCTURA TECNICA
| Columna          | Tipo       | Clave Primaria   |
|:-----------------|:-----------|:-----------------|
| id               | bigint     | SI               |
| fecha            | text       | NO               |
| ancho            | int        | NO               |
| alto             | int        | NO               |
| bgID             | int        | NO               |
| musicID          | int        | NO               |
| ambienteID       | int        | NO               |
| outDoor          | tinyint(1) | NO               |
| capabilities     | int        | NO               |
| posPelea         | text       | NO               |
| mapData          | text       | NO               |
| mobs             | text       | NO               |
| X                | int        | NO               |
| Y                | int        | NO               |
| subArea          | int        | NO               |
| maxGrupoMobs     | int        | NO               |
| maxMobsPorGrupo  | int        | NO               |
| minNivelGrupoMob | int        | NO               |
| maxNivelGrupoMob | int        | NO               |
| maxMercantes     | int        | NO               |
| maxPeleas        | tinyint    | NO               |

### MUESTRA DE DATOS
*Datos presentes en formato complejo.*

---
## TABLA: mascotas_modelo

### INFO CONTEXTUAL
- Registros totales: 24

### ESTRUCTURA TECNICA
| Columna        | Tipo         | Clave Primaria   |
|:---------------|:-------------|:-----------------|
| mascota        | int          | SI               |
| nombre         | text         | NO               |
| comidas        | text         | NO               |
| devorador      | tinyint(1)   | NO               |
| statsPorEfecto | varchar(255) | NO               |
| maximoComidas  | int          | NO               |
| fantasma       | int          | NO               |

### MUESTRA DE DATOS
|   mascota | nombre                                 | comidas   |   devorador | statsPorEfecto   |   maximoComidas |   fantasma |
|----------:|:---------------------------------------|:----------|------------:|:-----------------|----------------:|-----------:|
|      1711 | Wauwau                                 |           |           0 |                  |               0 |       7536 |
|      6604 | Kuakuá                                 |           |           0 |                  |               0 |       7543 |
|      6717 | Wauwau negro                           |           |           0 |                  |               0 |      10955 |
|      6718 | Miaumiau Blanco                        |           |           0 |                  |               0 |      10956 |
|      6894 | Superpoderoso Miaumiau de Combate (MJ) |           |           0 |                  |               0 |      10957 |

---
## TABLA: mercadillos

### INFO CONTEXTUAL
- Registros totales: 23
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna     | Tipo         | Clave Primaria   |
|:------------|:-------------|:-----------------|
| id          | int          | SI               |
| mapa        | varchar(250) | NO               |
| categorias  | varchar(250) | NO               |
| porcVenta   | double       | NO               |
| nivelMax    | int          | NO               |
| cantidad    | int          | NO               |
| tiempoVenta | int          | NO               |

### MUESTRA DE DATOS
|   id | mapa           | categorias                    |   porcVenta |   nivelMax |   cantidad |   tiempoVenta |
|-----:|:---------------|:------------------------------|------------:|-----------:|-----------:|--------------:|
|    1 | 4216,4622,7514 | 1,9                           |           1 |       1000 |         20 |           320 |
|    3 | 4271,4607,7516 | 12,14,26,43,44,45,66,70,71,86 |           1 |       1000 |         20 |           320 |
|    4 | 8759,8753      | 18,72,77,90,97,113,116        |           1 |       1000 |         20 |           320 |
|    5 | 4287,4595,7515 | 63,64,69                      |           1 |       1000 |         20 |           320 |
|    6 | 2221,4630,7510 | 33,42                         |           1 |       1000 |         20 |           320 |

---
## TABLA: mision_etapas

### INFO CONTEXTUAL
- Registros totales: 962

### ESTRUCTURA TECNICA
| Columna     | Tipo         | Clave Primaria   |
|:------------|:-------------|:-----------------|
| id          | int          | SI               |
| nombre      | text         | NO               |
| descripcion | text         | NO               |
| recompensas | varchar(255) | NO               |
| objetivos   | varchar(255) | NO               |

### MUESTRA DE DATOS
|   id | nombre                   | descripcion                                                                         | recompensas                    | objetivos   |
|-----:|:-------------------------|:------------------------------------------------------------------------------------|:-------------------------------|:------------|
|    2 | El regador renegado      | Erty Trapchet se olvidó de regar  sus plantas, tienes que ir a su casa para rega... | 3000|null|null|null|null|null  |             |
|    3 | La specia necia          | Erty Trapchet quiere estudiar las semillas del Diente de León para compararlas c... | 6000|null|null|null|null|null  |             |
|    4 | No pisar el césped...    | Para sus investigaciones, Trapchet necesita estudiar la repartición geográfica d... | 6500|500|null|null|null|null   |             |
|    5 | La flora puede matar...  | Tres-Flores, un amigo de Trapchet vive en Amakna y conoce perfectamente la flora... | 12500|null|null|null|null|null |             |
|    6 | Leleche para un Miaumiau | Traer leche para el pobre miaumiau.                                                 | 1220|null|null|null|null|null  |             |

---
## TABLA: mision_objetivos

### INFO CONTEXTUAL
- Registros totales: 3299

### ESTRUCTURA TECNICA
| Columna   | Tipo         | Clave Primaria   |
|:----------|:-------------|:-----------------|
| id        | int          | SI               |
| tipo      | tinyint      | NO               |
| args      | varchar(255) | NO               |
| detalle   | varchar(255) | NO               |

### MUESTRA DE DATOS
|   id |   tipo | args           | detalle                              |
|-----:|-------:|:---------------|:-------------------------------------|
|    2 |      4 |                | [\"Casa de Trapchet.\"]              |
|    3 |      3 | [449, 306, 1]  | [449, 306, 1]                        |
|   26 |      1 | [488]          | [488]                                |
|   32 |      0 |                | [\"Riega las plantas de Trapchet.\"] |
|   34 |      3 | [457, 6765, 1] | [457, 6765, 1]                       |

---
## TABLA: misiones

### INFO CONTEXTUAL
- Registros totales: 461

### ESTRUCTURA TECNICA
| Columna           | Tipo       | Clave Primaria   |
|:------------------|:-----------|:-----------------|
| id                | int        | SI               |
| nombre            | text       | NO               |
| etapas            | text       | NO               |
| pregDarMision     | text       | NO               |
| pregMisCompletada | text       | NO               |
| pregMisIncompleta | text       | NO               |
| puedeRepetirse    | varchar(5) | NO               |

### MUESTRA DE DATOS
|   id | nombre                         | etapas   | pregDarMision   | pregMisCompletada   | pregMisIncompleta   | puedeRepetirse   |
|-----:|:-------------------------------|:---------|:----------------|:--------------------|:--------------------|:-----------------|
|    3 | La discordia vegetal           |          |                 |                     |                     | false            |
|    4 | El llanto del miaumiau         |          |                 |                     |                     | false            |
|    5 | De la dificultad de ser Joyero |          |                 |                     |                     | false            |
|    6 | En busca del Golpe Divino      |          |                 |                     |                     | false            |
|    7 | La dura labor del Sram         |          |                 |                     |                     | false            |

---
## TABLA: mobs_evento

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna     | Tipo    | Clave Primaria   |
|:------------|:--------|:-----------------|
| mobOriginal | int     | SI               |
| mobEvento   | int     | NO               |
| evento      | tinyint | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: mobs_fix

### INFO CONTEXTUAL
- Registros totales: 29
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna         | Tipo         | Clave Primaria   |
|:----------------|:-------------|:-----------------|
| mapa            | varchar(100) | SI               |
| celda           | int          | SI               |
| mobs            | text         | NO               |
| tipo            | int          | NO               |
| condicion       | text         | NO               |
| segundosRespawn | int          | NO               |
| descripcion     | text         | NO               |

### MUESTRA DE DATOS
|   mapa |   celda | mobs    |   tipo | condicion   |   segundosRespawn | descripcion   |
|-------:|--------:|:--------|-------:|:------------|------------------:|:--------------|
|  10305 |     266 | 999,1,1 |     -1 |             |                 0 |               |
|  10322 |     337 | 999,1,1 |     -1 |             |                 0 |               |
|  10324 |     252 | 999,1,1 |     -1 |             |                 0 |               |
|  10326 |     266 | 999,1,1 |     -1 |             |                 0 |               |
|  10327 |     266 | 999,1,1 |     -1 |             |                 0 |               |

---
## TABLA: mobs_modelo

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna    | Tipo         | Clave Primaria   |
|:-----------|:-------------|:-----------------|
| id         | int          | SI               |
| nombre     | varchar(100) | NO               |
| gfxID      | int          | NO               |
| tipo       | tinyint      | NO               |
| alineacion | int          | NO               |
| kickeable  | varchar(5)   | NO               |
| grados     | text         | NO               |
| agresion   | tinyint      | NO               |
| colores    | varchar(30)  | NO               |
| stats      | text         | NO               |
| hechizos   | text         | NO               |
| pdvs       | varchar(200) | NO               |
| puntos     | varchar(200) | NO               |
| iniciativa | varchar(200) | NO               |
| minKamas   | int          | NO               |
| maxKamas   | int          | NO               |
| exps       | varchar(200) | NO               |
| tipoIA     | int          | NO               |
| capturable | int          | NO               |
| talla      | int          | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: mobs_raros

### INFO CONTEXTUAL
- Registros totales: 315

### ESTRUCTURA TECNICA
| Columna      | Tipo         | Clave Primaria   |
|:-------------|:-------------|:-----------------|
| idMobRaro    | int          | SI               |
| idMobNormal  | int          | NO               |
| nombre       | text         | NO               |
| subAreas     | varchar(150) | NO               |
| probabilidad | int          | NO               |

### MUESTRA DE DATOS
|   idMobRaro |   idMobNormal | nombre                       | subAreas                |   probabilidad |
|------------:|--------------:|:-----------------------------|:------------------------|---------------:|
|         422 |            -1 | Dopeul Dark Vlad             | 74                      |              2 |
|         446 |            -1 | Aermyne \Braco\' Scalptaras' | 105,171,107,108,106,109 |              1 |
|         459 |            -1 | Padgref Demo                 | 69                      |              1 |
|         460 |            -1 | Frakacia Leukocytine         | 97                      |              1 |
|         462 |            -1 | Ogivol Scalarcin             | 53                      |              1 |

---
## TABLA: monturas_modelo

### INFO CONTEXTUAL
- Registros totales: 5

### ESTRUCTURA TECNICA
| Columna     | Tipo         | Clave Primaria   |
|:------------|:-------------|:-----------------|
| id          | int          | SI               |
| nombre      | text         | NO               |
| stats       | varchar(255) | NO               |
| color       | varchar(100) | NO               |
| certificado | int          | NO               |
| generacion  | tinyint      | NO               |

### MUESTRA DE DATOS
|   id | nombre                        | stats   | color                      |   certificado |   generacion |
|-----:|:------------------------------|:--------|:---------------------------|--------------:|-------------:|
|    1 | Dragopavo almendrado salvaje  |         | 16772045,-1,16772045       |          7807 |            1 |
|    6 | Dragopavo pelirrojo y salvaje |         | 16747520,-1,16747520       |          7809 |            1 |
|   10 | Dragopavo pelirrojo           | 125,100 | 16747520,-1,16747520       |          7811 |            1 |
|   74 | Dragopavo dorado salvaje      |         | 16766720,16766720,16766720 |          7864 |            1 |
|   75 | Dragopavo esqueleto           |         | -1,-1,-1                   |          7865 |            1 |

---
## TABLA: npc_preguntas

### INFO CONTEXTUAL
- Registros totales: 477

### ESTRUCTURA TECNICA
| Columna    | Tipo         | Clave Primaria   |
|:-----------|:-------------|:-----------------|
| id         | int          | SI               |
| respuestas | varchar(100) | NO               |
| params     | varchar(100) | NO               |
| alternos   | text         | NO               |

### MUESTRA DE DATOS
|   id | respuestas   | params   | alternos   |
|-----:|:-------------|:---------|:-----------|
|    1 |              | [gremio] |            |
|   33 | 279          |          |            |
|   82 | 7            |          |            |
|  127 | 65           |          |            |
|  131 | 14           |          |            |

---
## TABLA: npc_respuestas

### INFO CONTEXTUAL
- Registros totales: 1188

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| accion    | int    | SI               |
| args      | text   | NO               |
| condicion | text   | NO               |

### MUESTRA DE DATOS
|   id |   accion |   args | condicion   |
|-----:|---------:|-------:|:------------|
|   78 |        1 |     82 |             |
|   79 |        1 |     83 |             |
|   80 |        1 |     84 |             |
|  109 |        1 |    127 |             |
|  110 |        1 |    128 |             |

---
## TABLA: npcs_modelo

### INFO CONTEXTUAL
- Registros totales: 1038

### ESTRUCTURA TECNICA
| Columna   | Tipo       | Clave Primaria   |
|:----------|:-----------|:-----------------|
| id        | int        | SI               |
| gfxID     | int        | NO               |
| nombre    | text       | NO               |
| ventas    | text       | NO               |
| scaleX    | int        | NO               |
| scaleY    | int        | NO               |
| sexo      | tinyint(1) | NO               |
| color1    | int        | NO               |
| color2    | int        | NO               |
| color3    | int        | NO               |
| arma      | int        | NO               |
| sombrero  | int        | NO               |
| capa      | int        | NO               |
| mascota   | int        | NO               |
| escudo    | int        | NO               |
| foto      | int        | NO               |
| pregunta  | int        | NO               |

### MUESTRA DE DATOS
|   id |   gfxID | nombre        | ventas   |   scaleX |   scaleY |   sexo |   color1 |   color2 |   color3 |   arma |   sombrero |   capa |   mascota |   escudo |   foto |   pregunta |
|-----:|--------:|:--------------|:---------|---------:|---------:|-------:|---------:|---------:|---------:|-------:|-----------:|-------:|----------:|---------:|-------:|-----------:|
|    1 |    1211 | Guía Bustofus |          |      100 |      100 |      1 |       -1 |       -1 |       -1 |      0 |          0 |      0 |         0 |        0 |      0 |       8000 |
|   23 |    9013 | Carlota       |          |      100 |      100 |      1 |  8017470 | 12288585 | 16770534 |      0 |          0 |      0 |         0 |        0 |      0 |          0 |
|   26 |    9013 | Celín         |          |      100 |      100 |      1 |  5197647 |       -1 | 13336370 |      0 |          0 |      0 |         0 |        0 |      0 |          0 |
|   35 |    9012 | Laura Soho    |          |      100 |      100 |      1 |  1252453 | 15264239 |  3349067 |      0 |          0 |      0 |         0 |        0 |      0 |          0 |
|   37 |    9024 | Amino         |          |      100 |      100 |      0 |       -1 |       -1 |       -1 |      0 |          0 |      0 |         0 |        0 |      0 |         81 |

---
## TABLA: npcs_ubicacion

### INFO CONTEXTUAL
- Registros totales: 469
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna     | Tipo         | Clave Primaria   |
|:------------|:-------------|:-----------------|
| mapa        | smallint     | SI               |
| celda       | smallint     | NO               |
| npc         | int          | SI               |
| orientacion | tinyint(1)   | NO               |
| nombre      | varchar(255) | NO               |

### MUESTRA DE DATOS
|   mapa |   celda |   npc |   orientacion | nombre                |
|-------:|--------:|------:|--------------:|:----------------------|
|     32 |     313 |    78 |             1 | Guardián del Kanojedo |
|     33 |     177 |  2001 |             3 | Vendedor De Mascotas  |
|     33 |     211 |  2002 |             1 | Vendedor De Capas     |
|     33 |     239 |  2003 |             1 | Vendedor DeSombreros  |
|     33 |     126 |  2005 |             3 | Vendedor De botas     |

---
## TABLA: objetos_accion

### INFO CONTEXTUAL
- Registros totales: 715

### ESTRUCTURA TECNICA
| Columna      | Tipo         | Clave Primaria   |
|:-------------|:-------------|:-----------------|
| objetoModelo | int          | SI               |
| accion       | int          | SI               |
| args         | text         | NO               |
| nombre       | varchar(255) | NO               |

### MUESTRA DE DATOS
|   objetoModelo |   accion | args   | nombre                        |
|---------------:|---------:|:-------|:------------------------------|
|            282 |       10 | 51,100 | Frasco de cuidados superiores |
|            283 |       10 | 31,60  | Frasco de cuidados            |
|            468 |       10 | 10,10  | Pan de Amakna                 |
|            520 |       10 | 51,100 | Pan con granos de adormidera  |
|            521 |       10 | 30,30  | Pan con semillas de sésamo    |

---
## TABLA: objetos_interactivos

### INFO CONTEXTUAL
- Registros totales: 92

### ESTRUCTURA TECNICA
| Columna   | Tipo         | Clave Primaria   |
|:----------|:-------------|:-----------------|
| id        | int          | SI               |
| nombre    | text         | NO               |
| gfx       | varchar(350) | NO               |
| tipo      | tinyint      | NO               |
| accionPJ  | tinyint      | NO               |
| recarga   | int          | NO               |
| duracion  | int          | NO               |
| caminable | tinyint      | NO               |
| skill     | varchar(350) | NO               |

### MUESTRA DE DATOS
|   id | nombre             | gfx            |   tipo |   accionPJ |   recarga |   duracion |   caminable | skill   |
|-----:|:-------------------|:---------------|-------:|-----------:|----------:|-----------:|------------:|:--------|
|    1 | Fresno             | 7500           |      1 |          4 |    180000 |         -1 |           0 | 6       |
|    2 | Sierra             | 7003           |      2 |          4 |        -1 |       1500 |           0 | 101     |
|    8 | Roble              | 7503           |      1 |          4 |    180000 |         -1 |           0 | 10      |
|   11 | Mesa de confección | 7011           |      2 |          4 |        -1 |       1500 |           0 | 13,14   |
|   12 | Taller             | 7010,7009,7008 |      2 |          4 |        -1 |       1500 |           0 | 11,12   |

---
## TABLA: objetos_modelo

### INFO CONTEXTUAL
- Registros totales: 9518

### ESTRUCTURA TECNICA
| Columna         | Tipo       | Clave Primaria   |
|:----------------|:-----------|:-----------------|
| id              | int        | SI               |
| tipo            | int        | NO               |
| nombre          | text       | NO               |
| gfx             | smallint   | NO               |
| nivelCore       | varchar(5) | NO               |
| nivel           | int        | NO               |
| statsModelo     | text       | NO               |
| pods            | int        | NO               |
| kamas           | int        | NO               |
| ogrinas         | int        | NO               |
| diasIntercambio | int        | NO               |
| magueable       | varchar(5) | NO               |
| etereo          | varchar(5) | NO               |
| infosArma       | text       | NO               |
| condicion       | text       | NO               |
| vendidos        | int        | NO               |
| precioMedio     | int        | NO               |
| panelOgrinas    | int        | NO               |
| panelKamas      | int        | NO               |
| itemPago        | text       | NO               |

### MUESTRA DE DATOS
|   id |   tipo | nombre                      |   gfx | nivelCore   |   nivel | statsModelo    |   pods |   kamas |   ogrinas |   diasIntercambio | magueable   | etereo   | infosArma                       | condicion   |   vendidos |   precioMedio |   panelOgrinas |   panelKamas | itemPago   |
|-----:|-------:|:----------------------------|------:|:------------|--------:|:---------------|-------:|--------:|----------:|------------------:|:------------|:---------|:--------------------------------|:------------|-----------:|--------------:|---------------:|-------------:|:-----------|
|   39 |      1 | Pequeño Amuleto del Búho    |     0 | false       |       1 | 7e#2#0#0#0d0+2 |      4 |     100 |         0 |                 7 | true        | false    |                                 |             |          0 |             0 |             50 |            0 |            |
|   40 |      6 | Espadita de Maderucha       |     0 | false       |       2 | 64#1#7#0#1d7+0 |     20 |     200 |         0 |                 0 | true        | false    | 5,4,1,1,50,30,false,false,false | CS>4        |          0 |             0 |             50 |            0 |            |
|   42 |      6 | Espada de Maderucha         |     0 | false       |       3 | 64#2#8#0#1d7+1 |     20 |     250 |         0 |                 0 | true        | false    | 5,4,1,1,50,30,false,false,false | CS>6        |          0 |             0 |             50 |            0 |            |
|   43 |      6 | Gran Espada de Maderucha    |     0 | false       |       6 | 64#3#9#0#1d7+2 |     20 |     300 |         0 |                 0 | true        | false    | 5,4,1,1,50,30,false,false,false | CS>12       |          0 |             0 |             50 |            0 |            |
|   44 |      6 | Potente Espada de Maderucha |     0 | false       |       7 | 64#4#a#0#1d7+3 |     20 |     350 |         0 |                 0 | true        | false    | 5,4,1,1,50,30,false,false,false | CS>14       |          0 |             0 |             50 |            0 |            |

---
## TABLA: objetos_set

### INFO CONTEXTUAL
- Registros totales: 359

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| nombre    | text   | NO               |
| 2_objetos | text   | NO               |
| 3_objetos | text   | NO               |
| 4_objetos | text   | NO               |
| 5_objetos | text   | NO               |
| 6_objetos | text   | NO               |
| 7_objetos | text   | NO               |
| 8_objetos | text   | NO               |
| objetos   | text   | NO               |

### MUESTRA DE DATOS
|   id | nombre                 | 2_objetos                                                                           | 3_objetos                                                                           | 4_objetos                                                                           | 5_objetos                                                                           | 6_objetos                                                                           | 7_objetos                                                                           | 8_objetos                                                                           | objetos                                 |
|-----:|:-----------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|:----------------------------------------|
|    1 | Set de jalató          | 76#5#0#0#0d0+5,7e#5#0#0#0d0+5                                                       | 76#a#0#0#0d0+10,7e#a#0#0#0d0+10                                                     | 76#a#0#0#0d0+10,7e#a#0#0#0d0+10,70#2#0#0#0d0+2                                      | 76#1e#0#0#0d0+30,7e#1e#0#0#0d0+30,70#4#0#0#0d0+4                                    | 76#28#0#0#0d0+40,7e#28#0#0#0d0+40,70#4#0#0#0d0+4                                    | 7d#1e#0#0#0d0+30,7c#14#0#0#0d0+20,76#32#0#0#0d0+50,7e#32#0#0#0d0+50,6f#1#0#0#0d0... |                                                                                     | 2411,2414,2416,2419,2422,2425,2428      |
|    2 | Set del kwak de llamas | 7d#f#0#0#0d0+15,7e#f#0#0#0d0+15                                                     | 7d#14#0#0#0d0+20,7e#14#0#0#0d0+20,77#a#0#0#0d0+10                                   | 7d#19#0#0#0d0+25,7c#5#0#0#0d0+5,7e#19#0#0#0d0+25,77#f#0#0#0d0+15                    | 7d#1e#0#0#0d0+30,7c#a#0#0#0d0+10,7e#1e#0#0#0d0+30,77#14#0#0#0d0+20,75#1#0#0#0d0+... | 7d#23#0#0#0d0+35,7c#f#0#0#0d0+15,7e#23#0#0#0d0+35,77#19#0#0#0d0+25,80#1#0#0#0d0+... | 7d#2d#0#0#0d0+45,7c#14#0#0#0d0+20,7e#2d#0#0#0d0+45,77#1e#0#0#0d0+30,6f#1#0#0#0d0... | 7d#37#0#0#0d0+55,7c#19#0#0#0d0+25,7e#37#0#0#0d0+55,77#23#0#0#0d0+35,6f#1#0#0#0d0... | 2074,2409,2412,2415,2418,2421,2424,2427 |
|    3 | Set de abráknido       | 76#a#0#0#0d0+10                                                                     | 7d#a#0#0#0d0+10,76#a#0#0#0d0+10                                                     | 7d#14#0#0#0d0+20,76#14#0#0#0d0+20,fe#a#0#0#0d0+10                                   | 7d#1e#0#0#0d0+30,76#1e#0#0#0d0+30,fa#f#0#0#0d0+15,fe#f#0#0#0d0+15                   | 7d#28#0#0#0d0+40,76#28#0#0#0d0+40,fa#14#0#0#0d0+20,fe#14#0#0#0d0+20,d9#14#0#0#0d... | 7d#32#0#0#0d0+50,76#32#0#0#0d0+50,6f#1#0#0#0d0+1,70#4#0#0#0d0+4,fa#14#0#0#0d0+20... |                                                                                     | 2410,2413,2417,2420,2423,2426,2429      |
|    4 | Set de Jalató Real     | 7d#14#0#0#0d0+20                                                                    | 7d#1e#0#0#0d0+30,70#2#0#0#0d0+2                                                     | 7d#28#0#0#0d0+40,76#28#0#0#0d0+40,70#3#0#0#0d0+3                                    | 7d#32#0#0#0d0+50,76#32#0#0#0d0+50,70#4#0#0#0d0+4                                    | 7d#3c#0#0#0d0+60,76#3c#0#0#0d0+60,7e#3c#0#0#0d0+60,70#5#0#0#0d0+5                   | 7d#46#0#0#0d0+70,76#46#0#0#0d0+70,7e#46#0#0#0d0+70,6f#1#0#0#0d0+1,70#6#0#0#0d0+6    |                                                                                     | 2438,2440,2441,2442,2443,2444,2445      |
|    5 | Set de aventurero      | 7d#a#0#0#0d0+10,7c#a#0#0#0d0+10,76#a#0#0#0d0+10,7e#a#0#0#0d0+10,7b#a#0#0#0d0+10,... | 7d#f#0#0#0d0+15,7c#f#0#0#0d0+15,76#f#0#0#0d0+15,7e#f#0#0#0d0+15,7b#f#0#0#0d0+15,... | 7d#14#0#0#0d0+20,7c#14#0#0#0d0+20,76#14#0#0#0d0+20,7e#14#0#0#0d0+20,7b#14#0#0#0d... | 7d#19#0#0#0d0+25,7c#19#0#0#0d0+25,76#19#0#0#0d0+25,7e#19#0#0#0d0+25,7b#19#0#0#0d... | 7d#28#0#0#0d0+40,7c#28#0#0#0d0+40,76#28#0#0#0d0+40,7e#28#0#0#0d0+40,7b#28#0#0#0d... |                                                                                     |                                                                                     | 2473,2474,2475,2476,2477,2478           |

---
## TABLA: objetos_trueque

### INFO CONTEXTUAL
- Registros totales: 91

### ESTRUCTURA TECNICA
| Columna       | Tipo         | Clave Primaria   |
|:--------------|:-------------|:-----------------|
| idObjeto      | int          | SI               |
| necesita      | varchar(100) | SI               |
| prioridad     | tinyint      | NO               |
| npc_ids       | text         | NO               |
| nombre_objeto | text         | NO               |

### MUESTRA DE DATOS
|   idObjeto | necesita   |   prioridad | npc_ids   | nombre_objeto            |
|-----------:|:-----------|------------:|:----------|:-------------------------|
|         81 | 290,4      |           1 | 93        | Pequeño Amuleto del Lobo |
|        395 | 2336,1     |           0 | 92        | Trébol de 5 hojas        |
|        420 | 303,1      |           0 | 122       | Hilo de lino             |
|        468 | 289,4      |           1 | 93        | Pan de Amakna            |
|        678 | 307,10     |           1 |           | Pergamino de Marfil      |

---
## TABLA: oficios

### INFO CONTEXTUAL
- Registros totales: 11

### ESTRUCTURA TECNICA
| Columna      | Tipo         | Clave Primaria   |
|:-------------|:-------------|:-----------------|
| id           | tinyint      | NO               |
| herramientas | varchar(300) | NO               |
| recetas      | text         | NO               |
| nombre       | varchar(50)  | NO               |

### MUESTRA DE DATOS
|   id |   herramientas | recetas   | nombre   |
|-----:|---------------:|:----------|:---------|
|   43 |           1520 |           |          |
|   44 |           1539 |           |          |
|   45 |           1561 |           |          |
|   46 |           1560 |           |          |
|   47 |           1562 |           |          |

---
## TABLA: ornamentos

### INFO CONTEXTUAL
- Registros totales: 124

### ESTRUCTURA TECNICA
| Columna   | Tipo       | Clave Primaria   |
|:----------|:-----------|:-----------------|
| id        | int        | SI               |
| nombre    | text       | NO               |
| creditos  | int        | NO               |
| ogrinas   | int        | NO               |
| kamas     | int        | NO               |
| vender    | varchar(5) | NO               |
| valido    | varchar(5) | NO               |

### MUESTRA DE DATOS
|   id | nombre   |   creditos |   ogrinas |   kamas | vender   | valido   |
|-----:|:---------|-----------:|----------:|--------:|:---------|:---------|
|    1 |          |          0 |       100 |       0 | true     | true     |
|    2 |          |          0 |       100 |       0 | true     | true     |
|    3 |          |          0 |       100 |       0 | true     | true     |
|    4 |          |          0 |       100 |       0 | true     | true     |
|    5 |          |          0 |       100 |       0 | true     | true     |

---
## TABLA: otros_interactivos

### INFO CONTEXTUAL
- Registros totales: 10

### ESTRUCTURA TECNICA
| Columna       | Tipo         | Clave Primaria   |
|:--------------|:-------------|:-----------------|
| gfx           | int          | NO               |
| mapaID        | int          | NO               |
| celdaID       | int          | NO               |
| accion        | int          | NO               |
| args          | varchar(255) | NO               |
| condicion     | text         | NO               |
| tiempoRecarga | int          | NO               |
| descripcion   | text         | NO               |

### MUESTRA DE DATOS
|   gfx |   mapaID |   celdaID |   accion | args   | condicion   |   tiempoRecarga | descripcion             |
|------:|---------:|----------:|---------:|:-------|:------------|----------------:|:------------------------|
|    -1 |     2196 |       253 |       -2 |        | PO=1575,1   |               0 | punto para crear gremio |
|   542 |       -1 |        -1 |       57 |        |             |               0 |                         |
|    -1 |     2047 |       282 |       65 | 5      |             |               0 |                         |
|    -1 |     8539 |       282 |       65 | 14     |             |               0 |                         |
|    -1 |     2025 |       282 |       65 | 3      |             |               0 |                         |

---
## TABLA: recetas

### INFO CONTEXTUAL
- Registros totales: 134

### ESTRUCTURA TECNICA
| Columna   | Tipo         | Clave Primaria   |
|:----------|:-------------|:-----------------|
| id        | int          | NO               |
| receta    | varchar(255) | NO               |
| nombre    | varchar(255) | NO               |
| tipo      | int          | NO               |
| nivel     | int          | NO               |

### MUESTRA DE DATOS
|   id | receta   | nombre                    |   tipo |   nivel |
|-----:|:---------|:--------------------------|-------:|--------:|
|  285 | 289,2    | Harina de trigo           |     52 |       1 |
|  389 | 288,10   | Aceite de Girasol Salvaje |     60 |      12 |
|  396 | 398,8    | Aceite de Palma           |     60 |      32 |
|  399 | 287,10   | Aceite de SÃ©samo         |     60 |       1 |
|  420 | 423,10   | Hilo de lino              |     15 |       1 |

---
## TABLA: retos

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna   | Tipo        | Clave Primaria   |
|:----------|:------------|:-----------------|
| id        | int         | SI               |
| bonus     | varchar(50) | NO               |
| reto      | text        | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: servicios

### INFO CONTEXTUAL
- Registros totales: 28

### ESTRUCTURA TECNICA
| Columna     | Tipo        | Clave Primaria   |
|:------------|:------------|:-----------------|
| id          | int         | SI               |
| descripcion | text        | NO               |
| creditos    | int         | NO               |
| ogrinas     | int         | NO               |
| activado    | varchar(11) | NO               |
| creditosVIP | int         | NO               |
| ogrinasVIP  | int         | NO               |

### MUESTRA DE DATOS
|   id | descripcion          |   creditos |   ogrinas | activado   |   creditosVIP |   ogrinasVIP |
|-----:|:---------------------|-----------:|----------:|:-----------|--------------:|-------------:|
|    1 | cambiar nombre       |          0 |       500 | true       |             0 |            0 |
|    2 | cambiar color        |          0 |       500 | true       |             0 |            0 |
|    3 | cambiar sexo         |          0 |       500 | true       |             0 |            0 |
|    4 | revivir              |          0 |       500 | true       |             0 |            0 |
|    5 | titulo personalizado |          0 |       500 | true       |             0 |            0 |

---
## TABLA: subareas

### INFO CONTEXTUAL
- Registros totales: 375

### ESTRUCTURA TECNICA
| Columna          | Tipo         | Clave Primaria   |
|:-----------------|:-------------|:-----------------|
| id               | int          | SI               |
| area             | int          | NO               |
| nombre           | varchar(200) | NO               |
| conquistable     | tinyint(1)   | NO               |
| minNivelGrupoMob | int          | NO               |
| maxNivelGrupoMob | int          | NO               |
| cementerio       | text         | NO               |

### MUESTRA DE DATOS
|   id |   area | nombre                       |   conquistable |   minNivelGrupoMob |   maxNivelGrupoMob | cementerio   |
|-----:|-------:|:-----------------------------|---------------:|-------------------:|-------------------:|:-------------|
|    0 |      0 | //Amakna                     |              1 |                  0 |                  0 | 1188,297     |
|    1 |      0 | Puerto de Madrestam          |              1 |                  0 |                  0 | 1188,297     |
|    2 |      0 | La montaña de los crujidores |              1 |                  0 |                  0 | 1188,297     |
|    3 |      0 | El campo de los Ingals       |              1 |                  0 |                  0 | 1188,297     |
|    4 |      0 | El bosque de Amakna          |              1 |                  0 |                  0 | 1188,297     |

---
## TABLA: titulos

### INFO CONTEXTUAL
- Registros totales: 124

### ESTRUCTURA TECNICA
| Columna   | Tipo       | Clave Primaria   |
|:----------|:-----------|:-----------------|
| id        | int        | SI               |
| nombre    | text       | NO               |
| creditos  | int        | NO               |
| ogrinas   | int        | NO               |
| kamas     | int        | NO               |
| vender    | varchar(5) | NO               |
| valido    | varchar(5) | NO               |

### MUESTRA DE DATOS
|   id | nombre   |   creditos |   ogrinas |   kamas | vender   | valido   |
|-----:|:---------|-----------:|----------:|--------:|:---------|:---------|
|    1 |          |          0 |        50 |       0 | true     | true     |
|    2 |          |          0 |        50 |       0 | true     | true     |
|    3 |          |          0 |        50 |       0 | true     | true     |
|    4 |          |          0 |        50 |       0 | true     | true     |
|    5 |          |          0 |        50 |       0 | true     | true     |

---
## TABLA: tutoriales

### INFO CONTEXTUAL
- Registros totales: 9

### ESTRUCTURA TECNICA
| Columna     | Tipo         | Clave Primaria   |
|:------------|:-------------|:-----------------|
| id          | int          | SI               |
| inicio      | varchar(255) | NO               |
| recompensa1 | varchar(255) | NO               |
| recompensa2 | varchar(255) | NO               |
| recompensa3 | varchar(255) | NO               |
| recompensa4 | varchar(255) | NO               |
| final       | varchar(255) | NO               |
| nombre      | text         | NO               |

### MUESTRA DE DATOS
|   id | inicio     | recompensa1   | recompensa2   | recompensa3   | recompensa4   | final      | nombre        |
|-----:|:-----------|:--------------|:--------------|:--------------|:--------------|:-----------|:--------------|
|   21 | 0@6864,169 |               |               | 5@1749,10     |               | 0@3297,410 | tofu smash    |
|   22 |            |               |               | 5@1749,10     |               |            | duelo trool   |
|   23 | 0@6867,284 |               |               | 5@1749,20     |               | 0@3334,216 | duelo blop    |
|   24 | 0@6876,284 |               |               | 5@1749,10     |               | 0@3334,216 | memoria blop  |
|   25 |            | 5@1749,20     |               |               |               |            | carrera larva |

---
## TABLA: zaaps

### INFO CONTEXTUAL
- Registros totales: 32
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| mapa      | int    | SI               |
| celda     | int    | NO               |

### MUESTRA DE DATOS
|   mapa |   celda |
|-------:|--------:|
|    164 |     193 |
|    528 |     156 |
|    844 |     212 |
|    935 |     295 |
|    951 |     126 |

---
## TABLA: zonas

### INFO CONTEXTUAL
- Registros totales: 12
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna   | Tipo         | Clave Primaria   |
|:----------|:-------------|:-----------------|
| nombre    | varchar(255) | NO               |
| mapa      | int          | SI               |
| celda     | int          | NO               |

### MUESTRA DE DATOS
| nombre   |   mapa |   celda |
|:---------|-------:|--------:|
| PVM 5    |   1711 |     197 |
| PVM 4    |   1714 |     282 |
| PVM 11   |   4193 |     210 |
| PVM 9    |   4685 |     384 |
| PVM 12   |   4776 |     225 |

---
