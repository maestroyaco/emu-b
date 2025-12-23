# Diccionario Tecnico de Datos: emu-b-dinamicos.sql

## RESUMEN DE LA BASE DE DATOS
- Archivo Origen: emu-b-dinamicos.sql
- Cantidad de Tablas: 27

---

## TABLA: casas

### INFO CONTEXTUAL
- Registros totales: 1052

### ESTRUCTURA TECNICA
| Columna        | Tipo       | Clave Primaria   |
|:---------------|:-----------|:-----------------|
| id             | int        | SI               |
| dueño          | int        | NO               |
| precio         | int        | NO               |
| bloqueado      | tinyint    | NO               |
| clave          | varchar(8) | NO               |
| derechosGremio | int        | NO               |

### MUESTRA DE DATOS
|   id |   dueño |   precio |   bloqueado | clave   |   derechosGremio |
|-----:|--------:|---------:|------------:|:--------|-----------------:|
|   66 |       0 |  1000000 |           0 | -       |                0 |
|   67 |       0 |  1000000 |           0 | -       |                0 |
|   68 |       0 |  1000000 |           0 | -       |                0 |
|   69 |       0 |  1000000 |           0 | -       |                0 |
|   70 |       0 |  1000000 |           0 | -       |                0 |

---
## TABLA: cementerio

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| nombre    | text   | NO               |
| nivel     | int    | NO               |
| sexo      | int    | NO               |
| clase     | int    | NO               |
| asesino   | text   | NO               |
| subArea   | int    | NO               |
| fecha     | bigint | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: cercados

### INFO CONTEXTUAL
- Registros totales: 388
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna          | Tipo   | Clave Primaria   |
|:-----------------|:-------|:-----------------|
| mapa             | int    | SI               |
| propietario      | int    | NO               |
| gremio           | int    | NO               |
| precio           | int    | NO               |
| criando          | text   | NO               |
| objetosColocados | text   | NO               |

### MUESTRA DE DATOS
|   mapa |   propietario |   gremio |   precio | criando   | objetosColocados   |
|-------:|--------------:|---------:|---------:|:----------|:-------------------|
|   2209 |             0 |       -1 |        0 |           |                    |
|   2210 |             0 |       -1 |        0 |           |                    |
|   2215 |             0 |       -1 |        0 |           |                    |
|   2216 |             0 |       -1 |        0 |           |                    |
|   2218 |             0 |       -1 |        0 |           |                    |

---
## TABLA: cofres

### INFO CONTEXTUAL
- Registros totales: 171

### ESTRUCTURA TECNICA
| Columna   | Tipo       | Clave Primaria   |
|:----------|:-----------|:-----------------|
| id        | int        | SI               |
| objetos   | text       | NO               |
| kamas     | bigint     | NO               |
| clave     | varchar(8) | NO               |
| dueño     | int        | NO               |

### MUESTRA DE DATOS
|   id | objetos   |   kamas | clave   |   dueño |
|-----:|:----------|--------:|:--------|--------:|
|    0 |           |       0 | -       |      -1 |
|    1 |           |       0 | -       |      -1 |
|    2 |           |       0 | -       |      -1 |
|    3 |           |       0 | -       |      -1 |
|    4 |           |       0 | -       |      -1 |

---
## TABLA: comandos

### INFO CONTEXTUAL
- Registros totales: 188

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| nombre    | gm     | NO               |
| comando   | text   | NO               |
| date      | text   | NO               |

### MUESTRA DE DATOS
|    id | nombre   | comando     | date                   |
|------:|:---------|:------------|:-----------------------|
| 10043 | Faurtes  | quienes     | 20/12/2023 05:42:35 AM |
| 10044 | Faurte   | quienes     | 20/12/2023 05:48:40 AM |
| 10045 | Faurte   | panel_admin | 20/12/2023 05:57:44 AM |
| 10046 | Faurte   | quienes     | 20/12/2023 06:09:07 AM |
| 10047 | Faurte   | quienes     | 20/12/2023 06:16:26 AM |

---
## TABLA: cuentas_servidor

### INFO CONTEXTUAL
- Registros totales: 20
- Relaciones sugeridas: Relacionada con Cuentas.

### ESTRUCTURA TECNICA
| Columna        | Tipo        | Clave Primaria   |
|:---------------|:------------|:-----------------|
| id             | int         | SI               |
| cuenta         | varchar(40) | NO               |
| kamas          | bigint      | NO               |
| objetos        | text        | NO               |
| establo        | text        | NO               |
| amigos         | text        | NO               |
| enemigos       | text        | NO               |
| reportes       | text        | NO               |
| primeraVez     | tinyint(1)  | NO               |
| regalo         | text        | NO               |
| ultimaConexion | text        | NO               |
| ultimaIP       | text        | NO               |
| mensajes       | text        | NO               |

### MUESTRA DE DATOS
|   id | cuenta   |   kamas | objetos   | establo   | amigos   | enemigos   | reportes   |   primeraVez | regalo   | ultimaConexion      | ultimaIP   | mensajes   |
|-----:|:---------|--------:|:----------|:----------|:---------|:-----------|:-----------|-------------:|:---------|:--------------------|:-----------|:-----------|
|    3 | beta3    |       0 |           |           |          |            |            |            0 |          | 2023~12~10~16~22~53 | 127.0.0.1  |            |
|    4 | beta4    |       0 |           |           |          |            |            |            0 |          | 2023~12~10~16~1~37  | 127.0.0.1  |            |
|    6 | beta5    |       0 |           |           |          |            |            |            0 |          | 2023~12~10~16~1~51  | 127.0.0.1  |            |
|    7 | beta6    |       0 |           |           |          |            |            |            0 |          | 2016~5~29~17~15~16  | 127.0.0.1  |            |
|    8 | beta7    |       0 |           |           |          |            |            |            0 |          | 2018~5~21~14~32~28  | 127.0.0.1  |            |

---
## TABLA: denuncias

### INFO CONTEXTUAL
- Registros totales: 0
- Relaciones sugeridas: Relacionada con Personajes.

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| perso     | text   | NO               |
| asunto    | text   | NO               |
| detalle   | text   | NO               |
| fecha     | text   | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: gremios

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna      | Tipo         | Clave Primaria   |
|:-------------|:-------------|:-----------------|
| id           | int          | SI               |
| nombre       | varchar(50)  | NO               |
| emblema      | varchar(20)  | NO               |
| nivel        | int          | NO               |
| xp           | bigint       | NO               |
| capital      | int          | NO               |
| recaudadores | int          | NO               |
| hechizos     | varchar(255) | NO               |
| stats        | varchar(255) | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: intercambios

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna     | Tipo   | Clave Primaria   |
|:------------|:-------|:-----------------|
| id          | int    | SI               |
| intercambio | text   | NO               |
| fecha       | text   | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: live_action

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna      | Tipo   | Clave Primaria   |
|:-------------|:-------|:-----------------|
| id           | int    | SI               |
| idModelo     | int    | NO               |
| cantidad     | int    | NO               |
| stats        | text   | NO               |
| idPersonaje  | int    | NO               |
| nombreObjeto | text   | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: logs_aggro

### INFO CONTEXTUAL
- Registros totales: 16

### ESTRUCTURA TECNICA
| Columna         | Tipo   | Clave Primaria   |
|:----------------|:-------|:-----------------|
| gagnant_account | text   | NO               |
| gagnant_perso   | text   | NO               |
| gagnant_ip      | text   | NO               |
| gagnant_ph      | text   | NO               |
| perdant_account | text   | NO               |
| perdant_perso   | text   | NO               |
| perdant_ip      | text   | NO               |
| perdant_ph      | text   | NO               |
| duree           | text   | NO               |
| aggroBy         | text   | NO               |
| aggroTo         | text   | NO               |
| idMap           | text   | NO               |
| timestamp       | text   | NO               |
| id              | int    | SI               |

### MUESTRA DE DATOS
|   gagnant_account |   gagnant_perso | gagnant_ip   |   gagnant_ph |   perdant_account |   perdant_perso | perdant_ip   |   perdant_ph |   duree |   aggroBy |   aggroTo |   idMap |     timestamp |   id |
|------------------:|----------------:|:-------------|-------------:|------------------:|----------------:|:-------------|-------------:|--------:|----------:|----------:|--------:|--------------:|-----:|
|                 1 |              17 | 127.0.0.1    |            0 |                 2 |              15 | 127.0.0.1    |            0 |      52 |        17 |        15 |    8608 | 1421083299589 |    1 |
|                 1 |              17 | 127.0.0.1    |            0 |                 2 |              15 | 127.0.0.1    |            0 |      45 |        17 |        15 |    8608 | 1421084003279 |    2 |
|                 1 |              17 | 127.0.0.1    |            0 |                 2 |              15 | 127.0.0.1    |            0 |     101 |        15 |        17 |    7772 | 1429567915697 |    3 |
|                 1 |              33 | 127.0.0.1    |            0 |                 2 |              32 | 127.0.0.1    |         -750 |      20 |        32 |        33 |    7609 | 1487090968073 |    4 |
|                 1 |              33 | 127.0.0.1    |           25 |                 2 |              32 | 127.0.0.1    |        -1000 |       8 |        32 |        33 |    7609 | 1487091300996 |    5 |

---
## TABLA: mapas_estrellas

### INFO CONTEXTUAL
- Registros totales: 0
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| mapa      | int    | SI               |
| estrellas | text   | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: mapas_heroico

### INFO CONTEXTUAL
- Registros totales: 0
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| mapa      | int    | SI               |
| mobs      | text   | NO               |
| objetos   | text   | NO               |
| kamas     | text   | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: mercadillo_objetos

### INFO CONTEXTUAL
- Registros totales: 1

### ESTRUCTURA TECNICA
| Columna    | Tipo   | Clave Primaria   |
|:-----------|:-------|:-----------------|
| objeto     | int    | SI               |
| mercadillo | int    | NO               |
| cantidad   | int    | NO               |
| dueño      | int    | NO               |
| precio     | bigint | NO               |

### MUESTRA DE DATOS
|   objeto |   mercadillo |   cantidad |   dueño |   precio |
|---------:|-------------:|-----------:|--------:|---------:|
|     5766 |            1 |          3 |       1 |    43434 |

---
## TABLA: miembros_gremio

### INFO CONTEXTUAL
- Registros totales: 0

### ESTRUCTURA TECNICA
| Columna   | Tipo    | Clave Primaria   |
|:----------|:--------|:-----------------|
| id        | int     | SI               |
| gremio    | int     | NO               |
| rango     | int     | NO               |
| xpDonada  | bigint  | NO               |
| porcXp    | tinyint | NO               |
| derechos  | int     | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: monturas

### INFO CONTEXTUAL
- Registros totales: 21
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna        | Tipo        | Clave Primaria   |
|:---------------|:------------|:-----------------|
| id             | int         | SI               |
| color          | int         | NO               |
| sexo           | int         | NO               |
| nombre         | varchar(30) | NO               |
| xp             | bigint      | NO               |
| nivel          | int         | NO               |
| talla          | int         | NO               |
| resistencia    | int         | NO               |
| amor           | int         | NO               |
| madurez        | int         | NO               |
| serenidad      | int         | NO               |
| reproducciones | int         | NO               |
| fatiga         | int         | NO               |
| energia        | int         | NO               |
| objetos        | text        | NO               |
| ancestros      | varchar(50) | NO               |
| habilidad      | varchar(50) | NO               |
| orientacion    | int         | NO               |
| celda          | int         | NO               |
| mapa           | int         | NO               |
| dueño          | int         | NO               |
| fecundable     | bigint      | NO               |
| pareja         | int         | NO               |
| salvaje        | tinyint(1)  | NO               |

### MUESTRA DE DATOS
|   id |   color |   sexo | nombre     |    xp |   nivel |   talla |   resistencia |   amor |   madurez |   serenidad |   reproducciones |   fatiga |   energia | objetos   | ancestros                   | habilidad   |   orientacion |   celda |   mapa |   dueño |   fecundable |   pareja |   salvaje |
|-----:|--------:|-------:|:-----------|------:|--------:|--------:|--------------:|-------:|----------:|------------:|-----------------:|---------:|----------:|:----------|:----------------------------|:------------|--------------:|--------:|-------:|--------:|-------------:|---------:|----------:|
| -164 |      35 |      0 | Sin Nombre |  4000 |       5 |     100 |             0 |      0 |         0 |           0 |               -1 |        0 |         0 |           | ?,?,?,?,?,?,?,?,?,?,?,?,?,? |             |             1 |      -1 |     -1 |      42 |            0 |       -1 |         0 |
| -161 |      88 |      1 | Sin Nombre | 26820 |      14 |     100 |             0 |      0 |         0 |           0 |               -1 |        0 |         0 |           | ?,?,?,?,?,?,?,?,?,?,?,?,?,? |             |             1 |      -1 |     -1 |      42 |            0 |       -1 |         0 |
| -158 |      35 |      1 | Sin Nombre |  4000 |       5 |     100 |             0 |      0 |         0 |           0 |                0 |        0 |         0 |           | ?,?,?,?,?,?,?,?,?,?,?,?,?,? |             |             1 |      -1 |     -1 |      42 |            0 |       -1 |         0 |
| -155 |      88 |      1 | Sin Nombre |  4000 |       5 |     100 |             0 |      0 |         0 |           0 |                0 |        0 |         0 |           | ?,?,?,?,?,?,?,?,?,?,?,?,?,? |             |             1 |      -1 |     -1 |      42 |            0 |       -1 |         0 |
| -152 |      88 |      0 | Sin Nombre |  4000 |       5 |     100 |             0 |      0 |         0 |           0 |                0 |        0 |         0 |           | ?,?,?,?,?,?,?,?,?,?,?,?,?,? |             |             1 |      -1 |     -1 |      41 |            0 |       -1 |         0 |

---
## TABLA: objetos

### INFO CONTEXTUAL
- Registros totales: 5446

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | NO               |
| modelo    | int    | NO               |
| cantidad  | int    | NO               |
| posicion  | int    | NO               |
| stats     | text   | NO               |
| objevivo  | int    | NO               |
| precio    | int    | NO               |

### MUESTRA DE DATOS
|   id |   modelo |   cantidad |   posicion | stats                                                                            |   objevivo |   precio |
|-----:|---------:|-----------:|-----------:|:---------------------------------------------------------------------------------|-----------:|---------:|
|   14 |     2428 |          1 |         -1 | 9e#39#0#0#0d0+57                                                                 |          0 |        0 |
|   15 |     2074 |          1 |         -1 | 320#0#0#7,326#0#0#7,328#7dd#3f0#5a6                                              |          0 |        0 |
|   16 |     2409 |          1 |         -1 | 7c#6#0#0#0d0+6,7e#c#0#0#0d0+12,d5#5#0#0#0d0+5                                    |          0 |        0 |
|   17 |     2412 |          1 |         -1 | 7e#e#0#0#0d0+14,ae#19#0#0#0d0+25,b6#1#0#0#0d0+1,d5#4#0#0#0d0+4                   |          0 |        0 |
|   18 |     2415 |          1 |         -1 | 63#10#19#0#1d10+15,73#3#0#0#0d0+3,7d#c#0#0#0d0+12,7e#d#0#0#0d0+13,b0#1#0#0#0d0+1 |          0 |        0 |

---
## TABLA: personajes

### INFO CONTEXTUAL
- Registros totales: 0
- Relaciones sugeridas: Relacionada con Mapas., Relacionada con Cuentas.

### ESTRUCTURA TECNICA
| Columna           | Tipo         | Clave Primaria   |
|:------------------|:-------------|:-----------------|
| id                | int          | SI               |
| nombre            | varchar(30)  | NO               |
| sexo              | tinyint      | NO               |
| clase             | smallint     | NO               |
| color1            | int          | NO               |
| color2            | int          | NO               |
| color3            | int          | NO               |
| kamas             | bigint       | NO               |
| puntosHechizo     | int          | NO               |
| capital           | int          | NO               |
| energia           | int          | NO               |
| nivel             | int          | NO               |
| xp                | bigint       | NO               |
| talla             | int          | NO               |
| gfx               | int          | NO               |
| alineacion        | int          | NO               |
| honor             | int          | NO               |
| deshonor          | int          | NO               |
| nivelAlin         | int          | NO               |
| cuenta            | int          | NO               |
| vitalidad         | int          | NO               |
| fuerza            | int          | NO               |
| sabiduria         | int          | NO               |
| inteligencia      | int          | NO               |
| suerte            | int          | NO               |
| agilidad          | int          | NO               |
| mostrarAmigos     | tinyint      | NO               |
| mostrarAlineacion | int          | NO               |
| canal             | varchar(15)  | NO               |
| mapa              | int          | NO               |
| celda             | int          | NO               |
| porcVida          | int          | NO               |
| hechizos          | text         | NO               |
| objetos           | text         | NO               |
| posSalvada        | varchar(20)  | NO               |
| zaaps             | varchar(250) | NO               |
| oficios           | varchar(300) | NO               |
| xpMontura         | tinyint      | NO               |
| montura           | int          | NO               |
| esposo            | int          | NO               |
| tienda            | text         | NO               |
| mercante          | int          | NO               |
| sFuerza           | int          | NO               |
| sInteligencia     | int          | NO               |
| sAgilidad         | int          | NO               |
| sSuerte           | int          | NO               |
| sVitalidad        | int          | NO               |
| sSabiduria        | int          | NO               |
| restriccionesA    | int          | NO               |
| restriccionesB    | int          | NO               |
| encarnacion       | int          | NO               |
| emotes            | int          | NO               |
| titulos           | text         | NO               |
| tituloVIP         | text         | NO               |
| ornamentos        | text         | NO               |
| misiones          | text         | NO               |
| coleccion         | text         | NO               |
| resets            | smallint     | NO               |
| almanax           | text         | NO               |
| ultimoNivel       | int          | NO               |
| setsRapidos       | text         | NO               |
| colorNombre       | int          | NO               |
| orden             | text         | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: prismas

### INFO CONTEXTUAL
- Registros totales: 0
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna          | Tipo   | Clave Primaria   |
|:-----------------|:-------|:-----------------|
| id               | int    | SI               |
| alineacion       | int    | NO               |
| nivel            | int    | NO               |
| mapa             | int    | NO               |
| celda            | int    | NO               |
| honor            | int    | NO               |
| subArea          | int    | NO               |
| area             | int    | NO               |
| tiempoProteccion | bigint | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: problema_ogrinas

### INFO CONTEXTUAL
- Registros totales: 1
- Relaciones sugeridas: Relacionada con Personajes.

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| perso     | text   | NO               |
| asunto    | text   | NO               |
| detalle   | text   | NO               |
| fecha     | text   | NO               |

### MUESTRA DE DATOS
|   id | perso   | asunto                | detalle              | fecha                  |
|-----:|:--------|:----------------------|:---------------------|:-----------------------|
|    1 | Elbusta | TU ASUNTO TU PROBLEME | HOLA :D     SALUT :D | 09/11/2013 02:50:54 AM |

---
## TABLA: ranking_koliseo

### INFO CONTEXTUAL
- Registros totales: 2

### ESTRUCTURA TECNICA
| Columna   | Tipo         | Clave Primaria   |
|:----------|:-------------|:-----------------|
| id        | int          | SI               |
| nombre    | varchar(255) | NO               |
| victorias | int          | NO               |
| derrotas  | int          | NO               |

### MUESTRA DE DATOS
|   id | nombre       |   victorias |   derrotas |
|-----:|:-------------|------------:|-----------:|
|   21 | Faurte       |           0 |          0 |
|   22 | Maestro-Yaco |           0 |          0 |

---
## TABLA: ranking_pvp

### INFO CONTEXTUAL
- Registros totales: 2

### ESTRUCTURA TECNICA
| Columna         | Tipo         | Clave Primaria   |
|:----------------|:-------------|:-----------------|
| id              | int          | SI               |
| nombre          | varchar(255) | NO               |
| victorias       | int          | NO               |
| derrotas        | int          | NO               |
| nivelAlineacion | int          | NO               |

### MUESTRA DE DATOS
|   id | nombre       |   victorias |   derrotas |   nivelAlineacion |
|-----:|:-------------|------------:|-----------:|------------------:|
|   31 | Maestro-Yaco |           0 |          1 |                 1 |
|   33 | Khay         |           1 |          0 |                 2 |

---
## TABLA: recaudadores

### INFO CONTEXTUAL
- Registros totales: 0
- Relaciones sugeridas: Relacionada con Mapas.

### ESTRUCTURA TECNICA
| Columna          | Tipo        | Clave Primaria   |
|:-----------------|:------------|:-----------------|
| id               | int         | SI               |
| mapa             | int         | NO               |
| celda            | int         | NO               |
| orientacion      | int         | NO               |
| gremio           | int         | NO               |
| nombre1          | varchar(11) | NO               |
| nombre2          | varchar(11) | NO               |
| objetos          | text        | NO               |
| kamas            | int         | NO               |
| xp               | bigint      | NO               |
| tiempoProteccion | bigint      | NO               |
| dueño            | int         | NO               |
| tiempoCreacion   | bigint      | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: reporte_bugs

### INFO CONTEXTUAL
- Registros totales: 0
- Relaciones sugeridas: Relacionada con Personajes.

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| perso     | text   | NO               |
| asunto    | text   | NO               |
| detalle   | text   | NO               |
| fecha     | text   | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: sugerencias

### INFO CONTEXTUAL
- Registros totales: 0
- Relaciones sugeridas: Relacionada con Personajes.

### ESTRUCTURA TECNICA
| Columna   | Tipo   | Clave Primaria   |
|:----------|:-------|:-----------------|
| id        | int    | SI               |
| perso     | text   | NO               |
| asunto    | text   | NO               |
| detalle   | text   | NO               |
| fecha     | text   | NO               |

### MUESTRA DE DATOS
*Sin registros.*

---
## TABLA: tiendacategoria

### INFO CONTEXTUAL
- Registros totales: 3

### ESTRUCTURA TECNICA
| Columna   | Tipo         | Clave Primaria   |
|:----------|:-------------|:-----------------|
| id        | int          | SI               |
| icono     | int          | NO               |
| nombre    | varchar(255) | NO               |

### MUESTRA DE DATOS
|   id |   icono | nombre      |
|-----:|--------:|:------------|
|  113 |   12847 | Apariencias |
|   97 |    7807 | Monturas    |
|   12 |   10484 | Pócimas     |

---
## TABLA: tiendaobjetos

### INFO CONTEXTUAL
- Registros totales: 5

### ESTRUCTURA TECNICA
| Columna       | Tipo         | Clave Primaria   |
|:--------------|:-------------|:-----------------|
| id            | int          | SI               |
| idObjeto      | int          | NO               |
| tipo          | int          | NO               |
| ogrinas       | int          | NO               |
| contenidoCaja | varchar(255) | NO               |

### MUESTRA DE DATOS
|   id |   idObjeto |   tipo |   ogrinas |   contenidoCaja |
|-----:|-----------:|-------:|----------:|----------------:|
|    1 |       9234 |    113 |       650 |              -1 |
|    2 |       9233 |    113 |       600 |              -1 |
|    3 |      10457 |     12 |        50 |              -1 |
|    4 |       9582 |     97 |      1500 |              -1 |
|    5 |       7143 |    113 |      1500 |              -1 |

---
